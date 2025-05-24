<script>
	import { Github, Twitter, Linkedin, Mail, MapPin, Code } from '@lucide/svelte';
	const currentYear = new Date().getFullYear();
	const quickLinks = [
		{ name: 'Privacy Policy', href: '/privacy' },
		{ name: 'Imprint', href: '/imprint' }
	];
	const socialLinks = [
		{ name: 'GitHub', href: 'https://github.com/Fab2102', icon: Github },
		{ name: 'LinkedIn', href: 'https://linkedin.com/in/fabian-bauer-21d', icon: Linkedin }
	];
	const skills = [
		'Python',
		'R',
		'JavaScript',
		'TypeScript',
		'Swift',
		'React',
		'Angular',
		'Vue',
		'Svelte',
		'Next.js',
		'Bootstrap',
		'Tailwind CSS',
		'Git',
		'Github'
	];
</script>

<footer class="bg-[#2463EB] text-white">
	<div class="mx-auto max-w-7xl px-9 sm:px-10 lg:px-8">
		<!-- Main Footer Content -->
		<div class="py-12 lg:py-16">
			<div class="grid grid-cols-1 gap-8 md:grid-cols-3 md:gap-12">
				<!-- Personal Info -->
				<div class="md:col-span-1">
					<div class="mb-4 flex items-center space-x-2">
						<div class="flex h-8 w-8 items-center justify-center rounded-lg bg-white">
							<span class="text-sm font-bold text-[#2463EB]">FB</span>
						</div>
						<span class="text-xl font-bold">Fabian Bauer</span>
					</div>
					<p class="mb-6 max-w-md text-sm text-blue-100 sm:text-base">
						Junior developer passionate about creating innovative digital solutions and bringing
						ideas to life through code.
					</p>
					<!-- Contact 
					<div class="space-y-2">
						<div class="flex items-center space-x-3 text-blue-100">
							<Mail class="h-4 w-4" />
							<span class="text-xs sm:text-sm">fab.bauer@outlook.com</span>
						</div>
						<div class="flex items-center space-x-3 text-blue-100">
							<MapPin class="h-4 w-4" />
							<span class="text-sm">Vienna, Austria</span>
						</div>
					</div>
					-->
				</div>
				<!-- Quick Links -->
				<div class="md:pl-14 lg:pl-20 xl:pl-24">
					<h3 class="mb-4 text-base font-semibold sm:text-lg">Quick Links</h3>
					<ul class="space-y-3">
						{#each quickLinks as item}
							<li>
								<a
									href={item.href}
									class="inline-block text-sm text-blue-100 transition-all duration-200 hover:text-white active:scale-95 active:text-blue-200 sm:text-base"
								>
									{item.name}
								</a>
							</li>
						{/each}
					</ul>
				</div>
				<!-- Skills & Expertise -->
				<div>
					<h3 class="mb-4 flex items-center space-x-2 text-base font-semibold sm:text-lg">
						<Code class="h-5 w-5" />
						<span>Tech Stack</span>
					</h3>
					<div class="flex flex-wrap gap-2">
						{#each skills as skill}
							<span
								class="rounded-full bg-white/10 px-3 py-1 text-xs font-medium text-blue-100 backdrop-blur-sm"
							>
								{skill}
							</span>
						{/each}
					</div>
				</div>
			</div>
		</div>
		<!-- Bottom Bar -->
		<div class="border-t border-white/20 py-6">
			<div class="flex flex-col md:flex-row md:items-center md:justify-between">
				<div class="mb-4 text-xs text-blue-100 sm:text-sm md:mb-0">
					&copy; {currentYear} FB. All rights reserved.
				</div>
				<!-- Social Links -->
				<div class="flex items-center space-x-4">
					{#each socialLinks as social}
						<a
							href={social.href}
							class="rounded-lg p-2 text-blue-200 transition-all duration-100 hover:bg-white/10 hover:text-white active:scale-[0.97]"
							aria-label={social.name}
						>
							<svelte:component this={social.icon} class="h-5 w-5" />
						</a>
					{/each}
				</div>
			</div>
		</div>
	</div>
</footer>
