<script lang="ts">
	import * as Card from '$lib/components/ui/card';
	import { Separator } from '$lib/components/ui/separator';
	import { Badge } from '$lib/components/ui/badge';

	interface CardItem {
		logo: string;
		date: string;
		position: string;
		company: string;
		description: string;
		skills: string[];
	}

	const workItems: CardItem[] = [
		{
			logo: '/HBLA_logo.jpg',
			date: '2017 – 2022',
			position: 'High school diploma',
			company: 'Federal College for Viticulture and Pomology Klosterneuburg',
			description:
				'Earned a high school diploma (Matura) from a five-year technical college specializing in viticulture and pomology, with a strong foundation in natural sciences and agricultural practices.',
			skills: ['Viticulture', 'Chemistry', 'Biology']
		},
		{
			logo: '/WU_logo.jpg',
			date: '2023 – 2026',
			position: 'B.Sc. Business Informatics',
			company: 'WU (Vienna University of Economics and Business)',
			description:
				'Bachelor’s degree program combining business administration and computer science. Focus on data analysis, database systems and software development in business contexts.',
			skills: ['Python', 'SQL', 'R', 'SPARQL', 'Machine Learning']
		},
		{
			logo: '/RBI_logo.jpg',
			date: 'Jul 2024 – Sep 2024',
			position: 'Intern',
			company: 'Raiffeisen Bank International',
			description:
				'Assisted the Custody department with administrative support, including handling securities-related processes and preparing Due Diligence documentation for institutional clients.',
			skills: ['Python', 'JIRA']
		},
		{
			logo: '/RBI_logo.jpg',
			date: 'Nov 2024 – Present',
			position: 'Student Support',
			company: 'Raiffeisen Bank International',
			description:
				'Contributed to software development projects with Python aimed at automating internal processes. Focused on scripting, task automation, and supporting agile project workflows.',
			skills: ['Python', 'Github', 'Git', 'Software Architecture']
		}
	];
</script>

<section
	id="experience"
	class="mx-auto max-w-7xl px-5 py-8 sm:px-4 sm:py-12 md:px-6 md:py-16 lg:px-8 lg:py-24"
>
	<h2 class="mb-12 px-5 text-3xl font-bold text-gray-900 sm:text-4xl">Education & Experience</h2>

	<!-- Education Section -->
	<div class="mb-8">
		<div class="grid gap-6 md:grid-cols-2 lg:gap-8">
			{#each workItems.slice(0, 2) as item}
				<Card.Root
					class="mx-4 rounded-2xl border border-gray-200 p-1 transition-colors hover:border-gray-300 sm:mx-0 sm:px-2"
				>
					<Card.Header class="px-5 pb-3 pt-6 sm:px-6 sm:pb-4 sm:pt-8">
						<div class="flex items-start space-x-6">
							<img
								src={item.logo}
								alt={`${item.company} logo`}
								class="h-12 w-12 rounded object-contain"
							/>
							<div class="space-y-1">
								<Card.Title class="text-lg font-medium text-gray-800 sm:text-xl">
									{item.position}
								</Card.Title>
								<Card.Description class="text-sm text-gray-500 sm:text-base">
									{item.company}
								</Card.Description>
								<p class="text-sm text-gray-500">{item.date}</p>
							</div>
						</div>
					</Card.Header>
					<Card.Content
						class="px-5 pb-4 text-sm leading-relaxed text-gray-700 sm:px-8 sm:pb-6 sm:text-base"
					>
						<p class="mb-6">{item.description}</p>
						<div class="flex flex-wrap gap-2">
							{#each item.skills as skill}
								<Badge variant="secondary" class="text-xs">
									{skill}
								</Badge>
							{/each}
						</div>
					</Card.Content>
				</Card.Root>
			{/each}
		</div>
	</div>

	<!-- Separator -->
	<div class="mx-20 my-16 sm:mx-40">
		<Separator class="bg-gray-200" />
	</div>

	<!-- Work Experience Section -->
	<div>
		<div class="grid gap-6 md:grid-cols-2 lg:gap-8">
			{#each workItems.slice(2) as item}
				<Card.Root
					class="mx-4 rounded-2xl border border-gray-200 p-1 transition-colors hover:border-gray-300 sm:mx-0 sm:px-2"
				>
					<Card.Header class="px-5 pb-3 pt-6 sm:px-6 sm:pb-4 sm:pt-8">
						<div class="flex items-start space-x-6">
							<img
								src={item.logo}
								alt={`${item.company} logo`}
								class="h-12 w-12 rounded object-contain"
							/>
							<div class="space-y-1">
								<Card.Title class="text-lg font-medium text-gray-800 sm:text-xl">
									{item.position}
								</Card.Title>
								<Card.Description class="text-sm text-gray-500 sm:text-base">
									{item.company}
								</Card.Description>
								<p class="text-sm text-gray-500">{item.date}</p>
							</div>
						</div>
					</Card.Header>
					<Card.Content
						class="px-5 pb-4 text-sm leading-relaxed text-gray-700 sm:px-8 sm:pb-6 sm:text-base"
					>
						<p class="mb-6">{item.description}</p>
						<div class="flex flex-wrap gap-2">
							{#each item.skills as skill}
								<Badge variant="secondary" class="text-xs">
									{skill}
								</Badge>
							{/each}
						</div>
					</Card.Content>
				</Card.Root>
			{/each}
		</div>
	</div>
</section>
