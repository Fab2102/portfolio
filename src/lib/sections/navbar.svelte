<script>
	import { fade } from 'svelte/transition';

	let searchTerm = $state('');

	const anchors = [
		{ name: 'About Me', href: '#about' },
		{ name: 'Skills', href: '#skills' },
		{ name: 'Experience', href: '#experience' },
		{ name: 'Projects', href: '#projects' }
	];

	let mobileOpen = $state(false);

	function toggleMobile() {
		mobileOpen = !mobileOpen;
	}
</script>

<nav class="relative border-b border-gray-300 bg-white">
	<div class="ml-3 max-w-7xl px-4 sm:px-6 lg:px-8">
		<div class="flex h-20 justify-between">
			<div class="flex">
				<div class="mr-10 flex flex-shrink-0 items-center">
					<a href="/" class="flex items-center space-x-2 rounded-lg bg-slate-100 px-1 py-1">
						<div class="flex h-8 w-8 items-center justify-center rounded-lg">
							<span class="text-sm font-bold text-[#2463EB]">FB</span>
						</div>
					</a>
				</div>
				<!-- Links container: uses space-x-8 for equal spacing -->
				<div class="hidden lg:ml-6 lg:flex lg:space-x-8">
					{#each anchors as item}
						<a
							href={item.href}
							class="text-md inline-flex items-center border-b-2 border-transparent px-1 pt-1 font-medium
                     text-gray-700 transition-colors duration-150 ease-in-out
                     hover:border-primary/80 hover:text-primary
                     active:border-primary active:text-primary"
						>
							{item.name}
						</a>
					{/each}
				</div>
			</div>

			<div class="absolute inset-y-0 right-16 hidden items-center lg:flex">
				<div class="relative">
					<input
						type="text"
						bind:value={searchTerm}
						placeholder="Search..."
						class="block w-full max-w-xs rounded-md border border-gray-300 bg-white py-2 pl-10 pr-3 leading-5 placeholder-gray-500 focus:border-blue-500 focus:outline-none focus:ring-1 focus:ring-blue-500 sm:text-sm"
					/>
					<div class="pointer-events-none absolute inset-y-0 left-0 flex items-center pl-3">
						<svg
							xmlns="http://www.w3.org/2000/svg"
							fill="none"
							viewBox="0 0 24 24"
							stroke="currentColor"
							stroke-width="1.5"
							class="h-5 w-5 text-gray-400"
						>
							<path
								stroke-linecap="round"
								stroke-linejoin="round"
								d="M21 21l-5.197-5.197m0 0A7.5 7.5 0 1 0 5.196 5.196a7.5 7.5 0 0 0 10.607 10.607Z"
							/>
						</svg>
					</div>
				</div>
			</div>

			<div class="absolute right-4 top-0 flex h-20 items-center lg:hidden">
				<button
					type="button"
					onclick={toggleMobile}
					aria-expanded={mobileOpen}
					class="inline-flex items-center justify-center rounded-md p-2 text-gray-500 transition-colors duration-150 ease-in-out focus:outline-none focus-visible:rounded-md focus-visible:bg-primary/10 active:rounded-md active:bg-primary/20"
				>
					<span class="sr-only">Open main menu</span>
					<svg
						xmlns="http://www.w3.org/2000/svg"
						class="icon h-7 w-7 {mobileOpen ? 'open' : ''}"
						viewBox="0 0 24 24"
						fill="none"
						stroke="currentColor"
						stroke-width="1.5"
					>
						<path
							class="hamburger"
							stroke-linecap="round"
							stroke-linejoin="round"
							d="M3.75 6.75h16.5M3.75 12h16.5m-16.5 5.25h16.5"
						/>
						<path
							class="close"
							stroke-linecap="round"
							stroke-linejoin="round"
							d="M6 18L18 6M6 6l12 12"
						/>
					</svg>
				</button>
			</div>
		</div>
	</div>

	<!-- Mobile menu -->
	{#if mobileOpen}
		<div
			class="absolute inset-x-0 top-full z-50 border-t border-gray-200 bg-white lg:hidden"
			transition:fade={{ duration: 100 }}
		>
			<div class="my-2 space-y-3 pb-3 pl-2 pt-2">
				{#each anchors as item}
					<a
						href={item.href}
						class="block rounded-l-md border-l-2 border-transparent py-1.5 pl-8 pr-4 text-sm font-medium text-gray-500 transition-colors duration-150 ease-in-out hover:border-primary/80 hover:bg-primary/10 hover:text-primary active:border-primary active:bg-primary/20 active:text-primary"
					>
						{item.name}
					</a>
				{/each}
			</div>
		</div>
	{/if}
</nav>

<style>
	.icon path {
		transition:
			transform 0.3s ease,
			opacity 0.3s ease;
		transform-origin: center;
	}

	.hamburger {
		opacity: 1;
		transform: rotate(0deg) scale(1);
	}
	.close {
		opacity: 0;
		transform: rotate(90deg) scale(0.8);
	}

	.open .hamburger {
		opacity: 0;
		transform: rotate(-90deg) scale(0.8);
	}

	.open .close {
		opacity: 1;
		transform: rotate(0deg) scale(1);
	}
</style>
