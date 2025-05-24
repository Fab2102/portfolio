<script lang="ts">
	import Button from '$lib/components/ui/button/button.svelte';
	import { Skeleton } from '$lib/components/ui/skeleton';
	import { ArrowDownToLine, Github, Linkedin } from '@lucide/svelte';

	let imageLoaded = false;

	function handleImageLoad() {
		imageLoaded = true;
	}
</script>

<section
	id="hero"
	class="
 flex min-h-[90vh]
 items-start justify-center px-4 pt-20 sm:px-8 sm:pt-24
 md:px-16 md:pt-40 lg:px-24 lg:pt-40 xl:px-32 xl:pt-40
 "
>
	<div
		class="flex flex-col items-center space-y-10 sm:space-y-12 md:flex-row md:space-x-16 md:space-y-0"
	>
		<!-- Profile Image with Skeleton -->
		<div class="flex-shrink-0 rounded-full">
			{#if imageLoaded}
				<img
					src="/profile_pic.png"
					alt="Profilbild"
					class="h-[25vh] w-[25vh] rounded-full object-cover object-center
    transition-opacity duration-300
    sm:h-[30vh] sm:w-[30vh]
    md:h-[35vh] md:w-[35vh]
    lg:h-[40vh] lg:w-[40vh] xl:h-[45vh] xl:w-[45vh]"
					onload={handleImageLoad}
				/>
			{:else}
				<Skeleton
					class="h-[25vh] w-[25vh] rounded-full
    sm:h-[30vh] sm:w-[30vh]
    md:h-[35vh] md:w-[35vh]
    lg:h-[40vh] lg:w-[40vh]
    xl:h-[45vh] xl:w-[45vh]"
				/>
				<!-- Hidden image to trigger loading -->
				<img src="/profile_pic.png" alt="Profilbild" class="hidden" onload={handleImageLoad} />
			{/if}
		</div>

		<!-- Text Block -->
		<div
			class="flex max-w-md flex-col justify-center space-y-2 whitespace-nowrap
 text-center sm:space-y-3 md:space-y-4"
		>
			<p class="text-sm font-semibold text-gray-500 sm:text-base md:text-lg">Hello, I'm</p>
			<h1 class="text-3xl font-bold sm:text-4xl md:text-4xl lg:text-5xl">Fabian Bauer</h1>
			<h2 class="text-2xl font-semibold text-gray-600 sm:text-3xl md:text-3xl lg:text-4xl">
				Student & Developer
			</h2>

			<!-- Buttons -->
			<div class="!mt-6 flex items-center justify-center gap-x-3 sm:gap-x-4">
				<Button
					variant="outline"
					size="sm"
					class="w-24 overflow-hidden transition-all duration-100 active:scale-[0.97] sm:w-24 md:w-28 lg:w-32"
				>
					<ArrowDownToLine class="mr-1 h-3 w-3 sm:mr-2 sm:h-5 sm:w-5" />
					CV
				</Button>
				<Button
					size="sm"
					class="w-24 overflow-hidden transition-all duration-100 active:scale-[0.97] sm:w-24 md:w-28 lg:w-32"
				>
					Contact Info
				</Button>
			</div>

			<!-- Social Icons -->
			<div class="!mt-6 flex items-center justify-center space-x-6">
				<a href="https://github.com/Fab2102" aria-label="GitHub">
					<Github
						class="h-6 w-6 overflow-hidden text-[#2463EB] transition-all duration-100 hover:opacity-80 active:scale-[0.97]"
					/>
				</a>
				<a href="https://linkedin.com/in/fabian-bauer-21d" aria-label="LinkedIn">
					<Linkedin
						class="h-6 w-6 overflow-hidden text-[#2463EB] transition-all duration-100 hover:opacity-80 active:scale-[0.97]"
					/>
				</a>
			</div>
		</div>
	</div>
</section>
