<!-- Projects.svelte -->
<script>
	import { onMount } from 'svelte';
	import { Github, ExternalLink, Package, Calculator, Globe, ChevronRight } from '@lucide/svelte';

	let mounted = false;

	onMount(() => {
		mounted = true;
	});

	const projects = [
		{
			id: 1,
			title: 'PyDataFlow',
			description:
				'A powerful Python package for streamlined data processing and analysis workflows. Features include pipeline management, data validation, and comprehensive error handling.',
			type: 'Python Package',
			tech: ['Python', 'PyPI', 'NumPy', 'Pandas'],
			icon: Package,
			gradient: 'from-blue-500 to-cyan-500',
			bgGradient: 'from-blue-50 to-cyan-50',
			darkBgGradient: 'from-blue-950/20 to-cyan-950/20',
			github: 'https://github.com/yourusername/pydataflow',
			live: 'https://pypi.org/project/pydataflow/',
			featured: true
		},
		{
			id: 2,
			title: 'Compound Calculator',
			description:
				'An interactive compound interest calculator built with Next.js. Visualize your investments growth with beautiful charts and detailed breakdowns.',
			type: 'Web Application',
			tech: ['Next.js', 'React', 'Chart.js', 'Tailwind CSS'],
			icon: Calculator,
			gradient: 'from-emerald-500 to-teal-500',
			bgGradient: 'from-emerald-50 to-teal-50',
			darkBgGradient: 'from-emerald-950/20 to-teal-950/20',
			github: 'https://github.com/yourusername/compound-calculator',
			live: 'https://compound-calculator.vercel.app',
			featured: false
		},
		{
			id: 3,
			title: 'Portfolio Tracker',
			description:
				'A comprehensive portfolio tracking application with real-time market data, performance analytics, and personalized investment insights.',
			type: 'Web Application',
			tech: ['Next.js', 'TypeScript', 'Prisma', 'PostgreSQL'],
			icon: Globe,
			gradient: 'from-purple-500 to-pink-500',
			bgGradient: 'from-purple-50 to-pink-50',
			darkBgGradient: 'from-purple-950/20 to-pink-950/20',
			github: 'https://github.com/yourusername/portfolio-tracker',
			live: 'https://portfolio-tracker.vercel.app',
			featured: false
		}
	];
</script>

<section class="mx-auto max-w-7xl px-4 py-24 sm:px-6 lg:px-8" id="projects">
	<div class="mb-16 text-center">
		<h2
			class="mb-4 bg-gradient-to-r from-gray-900 to-gray-600 bg-clip-text text-4xl font-bold text-transparent dark:from-gray-100 dark:to-gray-400 sm:text-5xl"
		>
			Featured Projects
		</h2>
		<p class="mx-auto max-w-2xl text-xl text-gray-600 dark:text-gray-400">
			A collection of projects showcasing my expertise in Python development, web applications, and
			modern frontend technologies.
		</p>
	</div>

	<div class="grid gap-8 lg:gap-12">
		<!-- Featured Project -->
		{#each projects.filter((p) => p.featured) as project (project.id)}
			<div
				class="group relative overflow-hidden rounded-2xl border border-gray-200 bg-white shadow-xl transition-all duration-500 hover:shadow-2xl dark:border-gray-800 dark:bg-gray-900"
				class:opacity-0={!mounted}
				class:translate-y-8={!mounted}
				class:opacity-100={mounted}
				class:translate-y-0={mounted}
				style="transition-delay: {project.id * 100}ms"
			>
				<div
					class="absolute inset-0 bg-gradient-to-br {project.bgGradient} dark:{project.darkBgGradient} opacity-50"
				></div>
				<div class="relative p-8 lg:p-12">
					<div class="flex flex-col gap-8 lg:flex-row lg:items-center">
						<div class="flex-1">
							<div class="mb-4 flex items-center gap-3">
								<div class="rounded-xl bg-gradient-to-r p-3 {project.gradient} shadow-lg">
									<svelte:component this={project.icon} class="h-6 w-6 text-white" />
								</div>
								<span
									class="rounded-full border border-gray-200 bg-white/80 px-3 py-1 text-sm font-medium text-gray-700 backdrop-blur-sm dark:border-gray-700 dark:bg-gray-800/80 dark:text-gray-300"
								>
									{project.type}
								</span>
							</div>

							<h3 class="mb-4 text-3xl font-bold text-gray-900 dark:text-gray-100">
								{project.title}
							</h3>

							<p class="mb-6 text-lg leading-relaxed text-gray-600 dark:text-gray-400">
								{project.description}
							</p>

							<div class="mb-8 flex flex-wrap gap-2">
								{#each project.tech as tech}
									<span
										class="rounded-lg border border-gray-200 bg-gray-100 px-3 py-1 text-sm font-medium text-gray-700 dark:border-gray-700 dark:bg-gray-800 dark:text-gray-300"
									>
										{tech}
									</span>
								{/each}
							</div>

							<div class="flex gap-4">
								<a
									href={project.github}
									target="_blank"
									rel="noopener noreferrer"
									class="inline-flex items-center gap-2 rounded-xl bg-gray-900 px-6 py-3 font-semibold text-white shadow-lg transition-colors duration-200 hover:bg-gray-800 hover:shadow-xl dark:bg-gray-100 dark:text-gray-900 dark:hover:bg-gray-200"
								>
									<Github class="h-5 w-5" />
									View Code
								</a>
								<a
									href={project.live}
									target="_blank"
									rel="noopener noreferrer"
									class="inline-flex items-center gap-2 rounded-xl border-2 border-gray-200 bg-white px-6 py-3 font-semibold text-gray-900 shadow-lg transition-colors duration-200 hover:border-gray-300 hover:shadow-xl dark:border-gray-700 dark:bg-gray-800 dark:text-gray-100 dark:hover:border-gray-600"
								>
									<ExternalLink class="h-5 w-5" />
									Live Demo
								</a>
							</div>
						</div>
					</div>
				</div>
			</div>
		{/each}

		<!-- Other Projects Grid -->
		<div class="grid gap-8 md:grid-cols-2">
			{#each projects.filter((p) => !p.featured) as project, index (project.id)}
				<div
					class="group relative overflow-hidden rounded-2xl border border-gray-200 bg-white shadow-lg transition-all duration-500 hover:border-gray-300 hover:shadow-xl dark:border-gray-800 dark:bg-gray-900 dark:hover:border-gray-700"
					class:opacity-0={!mounted}
					class:translate-y-8={!mounted}
					class:opacity-100={mounted}
					class:translate-y-0={mounted}
					style="transition-delay: {(index + 2) * 150}ms"
				>
					<div
						class="absolute inset-0 bg-gradient-to-br {project.bgGradient} dark:{project.darkBgGradient} opacity-30"
					></div>
					<div class="relative p-8">
						<div class="mb-4 flex items-center gap-3">
							<div class="rounded-lg bg-gradient-to-r p-2.5 {project.gradient} shadow-md">
								<svelte:component this={project.icon} class="h-5 w-5 text-white" />
							</div>
							<span
								class="rounded-full border border-gray-200 bg-white/70 px-2.5 py-1 text-xs font-medium text-gray-700 backdrop-blur-sm dark:border-gray-700 dark:bg-gray-800/70 dark:text-gray-300"
							>
								{project.type}
							</span>
						</div>

						<h3 class="mb-3 text-2xl font-bold text-gray-900 dark:text-gray-100">
							{project.title}
						</h3>

						<p class="mb-4 leading-relaxed text-gray-600 dark:text-gray-400">
							{project.description}
						</p>

						<div class="mb-6 flex flex-wrap gap-2">
							{#each project.tech as tech}
								<span
									class="rounded-md border border-gray-200 bg-gray-100 px-2.5 py-1 text-xs font-medium text-gray-700 dark:border-gray-700 dark:bg-gray-800 dark:text-gray-300"
								>
									{tech}
								</span>
							{/each}
						</div>

						<div class="flex gap-3">
							<a
								href={project.github}
								target="_blank"
								rel="noopener noreferrer"
								class="inline-flex items-center gap-2 rounded-lg bg-gray-900 px-4 py-2 text-sm font-medium text-white transition-colors duration-200 hover:bg-gray-800 dark:bg-gray-100 dark:text-gray-900 dark:hover:bg-gray-200"
							>
								<Github class="h-4 w-4" />
								Code
							</a>
							<a
								href={project.live}
								target="_blank"
								rel="noopener noreferrer"
								class="group inline-flex items-center gap-2 rounded-lg border border-gray-200 bg-white px-4 py-2 text-sm font-medium text-gray-900 transition-colors duration-200 hover:border-gray-300 dark:border-gray-700 dark:bg-gray-800 dark:text-gray-100 dark:hover:border-gray-600"
							>
								<ExternalLink class="h-4 w-4" />
								Demo
								<ChevronRight
									class="h-3 w-3 opacity-0 transition-opacity duration-200 group-hover:opacity-100"
								/>
							</a>
						</div>
					</div>
				</div>
			{/each}
		</div>
	</div>
</section>

<style>
	.group:hover .group-hover\:opacity-100 {
		opacity: 1;
	}
</style>
