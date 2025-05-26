<script lang="ts">
	import { onMount } from 'svelte';
	import { Badge } from '$lib/components/ui/badge';
	import * as Card from '$lib/components/ui/card';
	import { Separator } from '$lib/components/ui/separator';
	import { Progress } from '$lib/components/ui/progress/index.js';

	const programmingLanguages = [
		{ name: 'JavaScript', level: 75 },
		{ name: 'TypeScript', level: 70 },
		{ name: 'Python', level: 90 },
		{ name: 'SQL', level: 70 },
		{ name: 'R', level: 65 },
		{ name: 'Swift', level: 60 }
	];

	const frameworks = [
		{ name: 'React', level: 70 },
		{ name: 'Angular', level: 50 },
		{ name: 'Vue', level: 60 },
		{ name: 'Svelte', level: 75 },
		{ name: 'Next.js', level: 70 },
		{ name: 'FastAPI', level: 70 }
	];

	let langProgress = programmingLanguages.map(() => 0);
	let frameworkProgress = frameworks.map(() => 0);
	let skillsSection: HTMLElement;
	let hasAnimated = false;

	onMount(() => {
		const observer = new IntersectionObserver(
			(entries) => {
				entries.forEach((entry) => {
					if (entry.isIntersecting && !hasAnimated) {
						hasAnimated = true;

						// Animate programming languages progress bars
						programmingLanguages.forEach((lang, index) => {
							setTimeout(
								() => {
									langProgress[index] = lang.level;
								},
								100 + index * 150
							); // Stagger the animations
						});

						// Animate frameworks progress bars
						frameworks.forEach((framework, index) => {
							setTimeout(
								() => {
									frameworkProgress[index] = framework.level;
								},
								100 + index * 150
							);
						});
					}
				});
			},
			{
				threshold: 0.3,
				rootMargin: '0px 0px -50px 0px'
			}
		);

		if (skillsSection) {
			observer.observe(skillsSection);
		}

		return () => {
			observer.disconnect();
		};
	});
</script>

<section
	bind:this={skillsSection}
	class="mx-auto mb-20 max-w-7xl px-5 py-8 sm:px-4 sm:py-12 md:mb-0 md:-scroll-mt-16 md:px-6 md:py-16 lg:px-8 lg:py-24"
	id="skills"
>
	<div class="mb-12">
		<h2 class="mb-3 px-5 text-3xl font-bold text-gray-900 sm:text-4xl">Skills</h2>
		<p class="px-5 text-lg text-gray-600 sm:text-xl">
			My technical expertise across various programming languages and frameworks.
		</p>
	</div>

	<div class="grid gap-8 px-4 md:grid-cols-2">
		<!-- Programming Languages -->
		<Card.Root class="p-6">
			<Card.Header class="pb-4">
				<Card.Title class="text-xl font-semibold text-gray-900">Languages & Technologies</Card.Title
				>
			</Card.Header>
			<Separator class="ml-6 w-auto" />
			<Card.Content class="mt-2 space-y-6">
				{#each programmingLanguages as lang, index}
					<div class="space-y-4">
						<div class="flex items-center justify-between">
							<Badge variant="secondary">{lang.name}</Badge>
							<span class="text-sm text-gray-500">{lang.level}%</span>
						</div>
						<Progress value={langProgress[index]} class="h-2" />
					</div>
				{/each}
			</Card.Content>
		</Card.Root>

		<!-- Frameworks & Tools -->
		<Card.Root class="p-6">
			<Card.Header class="pb-4">
				<Card.Title class="text-xl font-semibold text-gray-900">Frameworks</Card.Title>
			</Card.Header>
			<Separator class="ml-6 w-auto" />
			<Card.Content class="mt-2 space-y-6">
				{#each frameworks as framework, index}
					<div class="space-y-4">
						<div class="flex items-center justify-between">
							<Badge variant="secondary">{framework.name}</Badge>
							<span class="text-sm text-gray-500">{framework.level}%</span>
						</div>
						<Progress value={frameworkProgress[index]} class="h-2" />
					</div>
				{/each}
			</Card.Content>
		</Card.Root>
	</div>
</section>
