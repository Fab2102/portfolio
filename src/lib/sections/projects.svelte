<script lang="ts">
	import { Button } from '$lib/components/ui/button';
	import { Badge } from '$lib/components/ui/badge';
	import * as Card from '$lib/components/ui/card';
	import { toast } from 'svelte-sonner';
	import { Separator } from '$lib/components/ui/separator';
	import {
		Github,
		ExternalLink,
		ChevronRight,
		Package,
		Calculator,
		Globe,
		Grape,
		Moon,
		Landmark,
		ScanHeart,
		FileChartColumnIncreasing,
		DatabaseZap,
		CalendarCog,
		Plane,
		PlaneTakeoff,
		Image,
		CloudUpload,
		TreePine,
		Trees,
		Sprout,
		Tractor,
		Bitcoin
	} from '@lucide/svelte';
</script>

<!-- Section 1 -->
<section
	class="mx-auto mb-10 max-w-7xl -scroll-mt-16 px-5 py-8 sm:px-4 sm:py-12 md:mb-0 md:px-6 md:py-16 lg:px-8 lg:py-24"
	id="projects"
>
	<h2 class="mb-4 px-5 text-3xl font-bold text-gray-900 sm:text-4xl">Projects</h2>
	<Separator class="mb-12 ml-4 w-5/6" />
	<div class="flex flex-col items-center gap-4 sm:gap-6 md:gap-8 lg:gap-12 xl:flex-row">
		<div class="w-full max-w-md xl:w-2/5 xl:max-w-lg">
			<Card.Root
				class="mx-4 h-full border border-gray-200 p-1 transition-colors hover:border-gray-300 sm:mx-0 sm:p-2"
			>
				<Card.Header class="px-5 sm:px-6 sm:pb-2">
					<div class="mb-4 flex flex-row items-center gap-3 sm:mb-6 sm:gap-4">
						<div class="rounded-lg bg-gradient-to-br from-[#2463EB] to-[#3b82f6] p-2 sm:p-2.5">
							<Package class="h-4 w-4 text-white sm:h-5 sm:w-5" />
						</div>
						<Badge variant="outline" class="py-1 text-xs font-semibold sm:text-sm"
							>Python Package</Badge
						>
					</div>
					<Card.Title class="mb-2 text-2xl font-bold sm:text-3xl">PyCIClib</Card.Title>
					<Card.Description>Compound Interest Calculation Package</Card.Description>
				</Card.Header>
				<Card.Content class="mb-6 flex-grow px-5 text-gray-700 sm:px-6">
					<p class="mb-4 text-sm leading-relaxed sm:text-base">
						PyCIClib is a lightweight Python package for modeling compound interest with flexible
						rates, compounding frequencies, and contribution schedules.
					</p>
					<div class="mt-8 space-y-3 text-sm text-gray-600">
						<div class="flex items-center gap-2">
							<Calculator class="h-4 w-4 text-blue-500" />
							<span>Flexible calculations</span>
						</div>
						<div class="flex items-center gap-2">
							<Package class="h-4 w-4 text-blue-500" />
							<span>Export to CSV / Excel</span>
						</div>
						<div class="flex items-center gap-2">
							<Globe class="h-4 w-4 text-blue-500" />
							<span>Available on PyPI</span>
						</div>
					</div>
				</Card.Content>
				<Card.Footer class="mt-auto flex flex-col items-start gap-4 px-5 pt-4 sm:gap-6 sm:px-6">
					<div class="flex flex-wrap gap-2">
						<Badge variant="secondary" class="py-1 text-xs">Python</Badge>
						<Badge variant="secondary" class="py-1 text-xs">PyPI</Badge>
						<Badge variant="secondary" class="py-1 text-xs">Pandas</Badge>
						<Badge variant="secondary" class="py-1 text-xs">Numpy</Badge>
					</div>
					<div class="flex items-center gap-3 sm:gap-4">
						<Button
							size="sm"
							variant="default"
							class="group flex items-center justify-center overflow-hidden px-4 py-2 transition-all duration-100 active:scale-[0.97]"
							href="https://github.com/Fab2102/pyciclib"
						>
							<Github class="mr-2 h-4 w-4" />Code
						</Button>
						<Button
							size="sm"
							variant="outline"
							class="group flex items-center justify-center overflow-hidden px-4 py-2 transition-all duration-100 active:scale-[0.97]"
							href="https://pypi.org/project/pyciclib/"
						>
							<ExternalLink class="mr-2 h-4 w-4" />
							Demo
							<span
								class="ml-2 flex max-w-0 items-center opacity-0 transition-all duration-300 group-hover:max-w-[1rem] group-hover:opacity-100 group-active:max-w-[1rem] group-active:opacity-100"
							>
								<ChevronRight class="h-3 w-3" />
							</span>
						</Button>
					</div>
				</Card.Footer>
			</Card.Root>
		</div>
		<div class="hidden flex-shrink-0 xl:block">
			<Separator orientation="vertical" class="h-64 sm:h-80 md:h-96" />
		</div>
		<div class="mx-auto block w-full max-w-md xl:hidden">
			<Separator orientation="horizontal" class="mx-auto my-4 w-60" />
		</div>
		<div class="flex w-full items-center justify-center xl:w-3/5">
			<div
				class="mx-4 w-full overflow-hidden rounded-lg bg-white sm:mx-0 sm:w-3/4 md:w-2/3 lg:w-1/2 xl:w-full"
			>
				<img src="/code_snippet.png" alt="code snippet" class="h-auto w-auto" />
			</div>
		</div>
	</div>
</section>

<!-- Section 2 -->
<section
	class="mx-auto mb-10 max-w-7xl px-5 py-8 sm:px-4 sm:py-12 md:mb-0 md:px-6 md:py-16 lg:px-8 lg:py-24"
>
	<div class="flex flex-col-reverse items-center gap-4 sm:gap-6 md:gap-8 lg:gap-12 xl:flex-row">
		<div class="flex w-full items-center justify-center xl:w-3/5">
			<div
				class="mx-4 w-full overflow-hidden rounded-lg bg-white sm:mx-0 sm:w-3/4 md:w-2/3 lg:w-1/2 xl:w-full"
			>
				<img src="/dashboard_compoundify.png" alt="code snippet" class="h-auto w-auto" />
			</div>
		</div>

		<div class="mx-auto block w-full max-w-md xl:hidden">
			<Separator orientation="horizontal" class="mx-auto my-4 w-60" />
		</div>
		<div class="hidden flex-shrink-0 xl:block">
			<Separator orientation="vertical" class="h-64 sm:h-80 md:h-96" />
		</div>

		<div class="w-full max-w-md xl:w-2/5 xl:max-w-lg">
			<Card.Root
				class="mx-4 h-full border border-gray-200 p-1 transition-colors hover:border-gray-300 sm:mx-0 sm:p-2"
			>
				<Card.Header class="px-5 sm:px-6 sm:pb-2">
					<div class="mb-4 flex flex-row items-center gap-3 sm:mb-6 sm:gap-4">
						<div class="rounded-lg bg-gradient-to-br from-[#2463EB] to-[#3b82f6] p-2 sm:p-2.5">
							<Calculator class="h-4 w-4 text-white sm:h-5 sm:w-5" />
						</div>
						<Badge variant="outline" class="py-1 text-xs font-semibold sm:text-sm"
							>React WebApp</Badge
						>
					</div>
					<Card.Title class="mb-2 text-2xl font-bold sm:text-3xl">Compoundify</Card.Title>
					<Card.Description>Compound Interest Calculation WebApp</Card.Description>
				</Card.Header>
				<Card.Content class="mb-6 flex-grow px-5 text-gray-700 sm:px-6">
					<p class="mb-4 text-sm leading-relaxed sm:text-base">
						This WebApp lets you model compound interest with customizable deposits, compounding
						intervals, and growth projections powered by a Python FastAPI backend. It uses <strong
							>PyCIClib</strong
						>.
					</p>
					<div class="mt-8 space-y-3 text-sm text-gray-600">
						<div class="flex items-center gap-2">
							<CalendarCog class="h-4 w-4 text-blue-500" />
							<span>Customizable schedules</span>
						</div>
						<div class="flex items-center gap-2">
							<FileChartColumnIncreasing class="h-4 w-4 text-blue-500" />
							<span>Interactive dashboard</span>
						</div>
						<div class="flex items-center gap-2">
							<DatabaseZap class="h-4 w-4 text-blue-500" />
							<span>FastAPI backend</span>
						</div>
					</div>
				</Card.Content>
				<Card.Footer class="mt-auto flex flex-col items-start gap-4 px-5 pt-4 sm:gap-6 sm:px-6">
					<div class="flex flex-wrap gap-2">
						<Badge variant="secondary" class="py-1 text-xs">React</Badge>
						<Badge variant="secondary" class="py-1 text-xs">Vite</Badge>
						<Badge variant="secondary" class="py-1 text-xs">Tailwind</Badge>
						<Badge variant="secondary" class="py-1 text-xs">FastAPI</Badge>
					</div>
					<div class="flex items-center gap-3 sm:gap-4">
						<Button
							size="sm"
							variant="default"
							class="group flex items-center justify-center overflow-hidden px-4 py-2 transition-all duration-100 active:scale-[0.97]"
							href="https://github.com/Fab2102/compoundify"
						>
							<Github class="mr-2 h-4 w-4" />Code
						</Button>
						<Button
							size="sm"
							variant="outline"
							class="group flex items-center justify-center overflow-hidden px-4 py-2 transition-all duration-100 active:scale-[0.97]"
							href="https://compoundify.vercel.app/"
						>
							<ExternalLink class="mr-2 h-4 w-4" />
							Demo
							<span
								class="ml-2 flex max-w-0 items-center opacity-0 transition-all duration-300 group-hover:max-w-[1rem] group-hover:opacity-100 group-active:max-w-[1rem] group-active:opacity-100"
							>
								<ChevronRight class="h-3 w-3" />
							</span>
						</Button>
					</div>
				</Card.Footer>
			</Card.Root>
		</div>
	</div>
</section>

<!-- Section 3 -->
<section
	class="mx-auto mb-10 max-w-7xl px-5 py-8 sm:px-4 sm:py-12 md:px-6 md:py-16 lg:px-8 lg:py-24"
>
	<div class="flex flex-col items-center gap-4 sm:gap-6 md:gap-8 lg:gap-12 xl:flex-row">
		<div class="w-full max-w-md xl:w-2/5 xl:max-w-lg">
			<Card.Root
				class="mx-4 h-full border border-gray-200 p-1 transition-colors hover:border-gray-300 sm:mx-0 sm:p-2"
			>
				<Card.Header class="px-5 sm:px-6 sm:pb-2">
					<div class="mb-4 flex flex-row items-center gap-3 sm:mb-6 sm:gap-4">
						<div class="rounded-lg bg-gradient-to-br from-[#2463EB] to-[#3b82f6] p-2 sm:p-2.5">
							<Grape class="h-4 w-4 text-white sm:h-5 sm:w-5" />
						</div>
						<Badge variant="outline" class="py-1 text-xs font-semibold sm:text-sm"
							>NextJS WebApp</Badge
						>
					</div>
					<Card.Title class="mb-2 text-2xl font-bold sm:text-3xl">Nutrient Tables</Card.Title>
					<Card.Description>Nutrient tables for wines</Card.Description>
				</Card.Header>
				<Card.Content class="mb-6 flex-grow px-5 text-gray-700 sm:px-6">
					<p class="mb-4 text-sm leading-relaxed sm:text-base">
						This Next.js web application displays the nutrient tables for various wines. It was
						developed in response to a new EU policy that mandates the inclusion of nutrient
						information on wine labels.
					</p>
					<div class="mt-8 space-y-3 text-sm text-gray-600">
						<div class="flex items-center gap-2">
							<ScanHeart class="h-4 w-4 text-blue-500" />
							<span>Instant nutrient lookup</span>
						</div>
						<div class="flex items-center gap-2">
							<Landmark class="h-4 w-4 text-blue-500" />
							<span>EU label compliance</span>
						</div>
						<div class="flex items-center gap-2">
							<Moon class="h-4 w-4 text-blue-500" />
							<span>Dark mode support</span>
						</div>
					</div>
				</Card.Content>
				<Card.Footer class="mt-auto flex flex-col items-start gap-4 px-5 pt-4 sm:gap-6 sm:px-6">
					<div class="flex flex-wrap gap-2">
						<Badge variant="secondary" class="py-1 text-xs">NextJS</Badge>
						<Badge variant="secondary" class="py-1 text-xs">React</Badge>
						<Badge variant="secondary" class="py-1 text-xs">TypeScript</Badge>
						<Badge variant="secondary" class="py-1 text-xs">shadcn/ui</Badge>
					</div>
					<div class="flex items-center gap-3 sm:gap-4">
						<Button
							size="sm"
							variant="default"
							class="group flex items-center justify-center overflow-hidden px-4 py-2 transition-all duration-100 active:scale-[0.97]"
							href="https://github.com/Fab2102/next-WebApp"
						>
							<Github class="mr-2 h-4 w-4" />Code
						</Button>
						<Button
							size="sm"
							variant="outline"
							class="group flex items-center justify-center overflow-hidden px-4 py-2 transition-all duration-100 active:scale-[0.97]"
							href="https://nutritional-info.vercel.app/"
						>
							<ExternalLink class="mr-2 h-4 w-4" />
							Demo
							<span
								class="ml-2 flex max-w-0 items-center opacity-0 transition-all duration-300 group-hover:max-w-[1rem] group-hover:opacity-100 group-active:max-w-[1rem] group-active:opacity-100"
							>
								<ChevronRight class="h-3 w-3" />
							</span>
						</Button>
					</div>
				</Card.Footer>
			</Card.Root>
		</div>
		<div class="hidden flex-shrink-0 xl:block">
			<Separator orientation="vertical" class="h-64 sm:h-80 md:h-96" />
		</div>
		<div class="mx-auto block w-full max-w-md xl:hidden">
			<Separator orientation="horizontal" class="mx-auto my-4 w-60" />
		</div>
		<div class="flex w-full items-center justify-center xl:w-3/5">
			<div
				class="mx-4 w-full overflow-hidden rounded-lg bg-white sm:mx-0 sm:w-3/4 md:w-2/3 lg:w-1/2 xl:w-full"
			>
				<img src="/nutrient_webapp.png" alt="code snippet" class="h-auto w-auto" />
			</div>
		</div>
	</div>
</section>

<!-- Section 4 -->
<section
	class="mx-auto mb-10 max-w-7xl px-5 py-8 sm:px-4 sm:py-12 md:mb-0 md:px-6 md:py-16 lg:px-8 lg:py-24"
>
	<div class="flex flex-col-reverse items-center gap-4 sm:gap-6 md:gap-8 lg:gap-12 xl:flex-row">
		<div class="flex w-full items-center justify-center xl:w-3/5">
			<div
				class="mx-4 w-full overflow-hidden rounded-lg bg-white sm:mx-0 sm:w-3/4 md:w-2/3 lg:w-1/2 xl:w-full"
			>
				<img src="/iOS_pic.png" alt="code snippet" class="h-auto w-auto" />
			</div>
		</div>

		<div class="mx-auto block w-full max-w-md xl:hidden">
			<Separator orientation="horizontal" class="mx-auto my-4 w-60" />
		</div>
		<div class="hidden flex-shrink-0 xl:block">
			<Separator orientation="vertical" class="h-64 sm:h-80 md:h-96" />
		</div>

		<div class="w-full max-w-md xl:w-2/5 xl:max-w-lg">
			<Card.Root
				class="mx-4 h-full border border-gray-200 p-1 transition-colors hover:border-gray-300 sm:mx-0 sm:p-2"
			>
				<Card.Header class="px-5 sm:px-6 sm:pb-2">
					<div class="mb-4 flex flex-row items-center gap-3 sm:mb-6 sm:gap-4">
						<div class="rounded-lg bg-gradient-to-br from-[#2463EB] to-[#3b82f6] p-2 sm:p-2.5">
							<Plane class="h-4 w-4 text-white sm:h-5 sm:w-5" />
						</div>
						<Badge variant="outline" class="py-1 text-xs font-semibold sm:text-sm">iOS App</Badge>
					</div>
					<Card.Title class="mb-2 text-2xl font-bold sm:text-3xl">Tripify</Card.Title>
					<Card.Description>Trip Diary App</Card.Description>
				</Card.Header>
				<Card.Content class="mb-6 flex-grow px-5 text-gray-700 sm:px-6">
					<p class="mb-4 text-sm leading-relaxed sm:text-base">
						This iOS app lets users create and manage personal travel diaries, with text, images,
						and locations. It supports offline entry creation, local storage, and publishing to a
						backend, making trip documentation easy and flexible.
					</p>
					<div class="mt-8 space-y-3 text-sm text-gray-600">
						<div class="flex items-center gap-2">
							<PlaneTakeoff class="h-4 w-4 text-blue-500" />
							<span>Create and manage trips</span>
						</div>
						<div class="flex items-center gap-2">
							<Image class="h-4 w-4 text-blue-500" />
							<span>Entries with text, images, and location</span>
						</div>
						<div class="flex items-center gap-2">
							<CloudUpload class="h-4 w-4 text-blue-500" />
							<span>Offline and online sync</span>
						</div>
					</div>
				</Card.Content>
				<Card.Footer class="mt-auto flex flex-col items-start gap-4 px-5 pt-4 sm:gap-6 sm:px-6">
					<div class="flex flex-wrap gap-2">
						<Badge variant="secondary" class="py-1 text-xs">Swift</Badge>
						<Badge variant="secondary" class="py-1 text-xs">SwiftUI</Badge>
						<Badge variant="secondary" class="py-1 text-xs">SwiftData</Badge>
						<Badge variant="secondary" class="py-1 text-xs">XCode</Badge>
					</div>
					<div class="flex items-center gap-3 sm:gap-4">
						<Button
							size="sm"
							variant="default"
							class="group flex items-center justify-center overflow-hidden px-4 py-2 transition-all duration-100 active:scale-[0.97]"
							href="https://github.com/Fab2102/iOS_TravelDiaryApp"
						>
							<Github class="mr-2 h-4 w-4" />Code
						</Button>
						<Button
							size="sm"
							variant="outline"
							class="group flex items-center justify-center overflow-hidden px-4 py-2 transition-all duration-100 active:scale-[0.97]"
							onclick={() => {
								const now = new Date()
									.toLocaleString('de-DE', {
										day: '2-digit',
										month: '2-digit',
										year: 'numeric',
										hour: '2-digit',
										minute: '2-digit',
										hour12: false
									})
									.replace(',', '');
								toast.error('No demo available', {
									description: now,
									action: {
										label: 'Remove',
										onClick: () => console.info('Undo')
									}
								});
							}}
						>
							<ExternalLink class="mr-2 h-4 w-4" />
							Demo
							<span
								class="ml-2 flex max-w-0 items-center opacity-0 transition-all duration-300 group-hover:max-w-[1rem] group-hover:opacity-100 group-active:max-w-[1rem] group-active:opacity-100"
							>
								<ChevronRight class="h-3 w-3" />
							</span>
						</Button>
					</div>
				</Card.Footer>
			</Card.Root>
		</div>
	</div>
</section>

<!-- Section 5 -->
<section
	class="mx-auto mb-40 max-w-7xl px-5 py-8 sm:px-4 sm:py-12 md:px-6 md:py-16 lg:px-8 lg:py-24"
>
	<div class="flex flex-col items-center gap-4 sm:gap-6 md:gap-8 lg:gap-12 xl:flex-row">
		<div class="w-full max-w-md xl:w-2/5 xl:max-w-lg">
			<Card.Root
				class="mx-4 h-full border border-gray-200 p-1 transition-colors hover:border-gray-300 sm:mx-0 sm:p-2"
			>
				<Card.Header class="px-5 sm:px-6 sm:pb-2">
					<div class="mb-4 flex flex-row items-center gap-3 sm:mb-6 sm:gap-4">
						<div class="rounded-lg bg-gradient-to-br from-[#2463EB] to-[#3b82f6] p-2 sm:p-2.5">
							<Trees class="h-4 w-4 text-white sm:h-5 sm:w-5" />
						</div>
						<Badge variant="outline" class="py-1 text-xs font-semibold sm:text-sm"
							>Business Website</Badge
						>
					</div>
					<Card.Title class="mb-2 text-2xl font-bold sm:text-3xl">Investree</Card.Title>
					<Card.Description>Sustainable investments via Blockchain</Card.Description>
				</Card.Header>
				<Card.Content class="mb-6 flex-grow px-5 text-gray-700 sm:px-6">
					<p class="mb-4 text-sm leading-relaxed sm:text-base">
						Investree is a conceptual forest investment platform developed as a university project.
						It demonstrates how blockchain can enable transparent, accessible, and sustainable
						forest ownership — but it was created solely for academic purposes.
					</p>
					<div class="mt-8 space-y-3 text-sm text-gray-600">
						<div class="flex items-center gap-2">
							<Sprout class="h-4 w-4 text-blue-500" />
							<span>Connects people to forest projects</span>
						</div>
						<div class="flex items-center gap-2">
							<Bitcoin class="h-4 w-4 text-blue-500" />
							<span>Revenue sharing via smart contracts</span>
						</div>
						<div class="flex items-center gap-2">
							<Globe class="h-4 w-4 text-blue-500" />
							<span>Global access to green investing</span>
						</div>
					</div>
				</Card.Content>
				<Card.Footer class="mt-auto flex flex-col items-start gap-4 px-5 pt-4 sm:gap-6 sm:px-6">
					<div class="flex flex-wrap gap-2">
						<Badge variant="secondary" class="py-1 text-xs">HTML</Badge>
						<Badge variant="secondary" class="py-1 text-xs">CSS</Badge>
						<Badge variant="secondary" class="py-1 text-xs">JavaScript</Badge>
						<Badge variant="secondary" class="py-1 text-xs">Bootstrap</Badge>
					</div>
					<div class="flex items-center gap-3 sm:gap-4">
						<Button
							size="sm"
							variant="default"
							class="group flex items-center justify-center overflow-hidden px-4 py-2 transition-all duration-100 active:scale-[0.97]"
							href="https://github.com/Fab2102/project_corp_IT1"
						>
							<Github class="mr-2 h-4 w-4" />Code
						</Button>
						<Button
							size="sm"
							variant="outline"
							class="group flex items-center justify-center overflow-hidden px-4 py-2 transition-all duration-100 active:scale-[0.97]"
							href="https://project-corp-it-1.vercel.app/"
						>
							<ExternalLink class="mr-2 h-4 w-4" />
							Demo
							<span
								class="ml-2 flex max-w-0 items-center opacity-0 transition-all duration-300 group-hover:max-w-[1rem] group-hover:opacity-100 group-active:max-w-[1rem] group-active:opacity-100"
							>
								<ChevronRight class="h-3 w-3" />
							</span>
						</Button>
					</div>
				</Card.Footer>
			</Card.Root>
		</div>
		<div class="hidden flex-shrink-0 xl:block">
			<Separator orientation="vertical" class="h-64 sm:h-80 md:h-96" />
		</div>
		<div class="mx-auto block w-full max-w-md xl:hidden">
			<Separator orientation="horizontal" class="mx-auto my-4 w-60" />
		</div>
		<div class="flex w-full items-center justify-center xl:w-3/5">
			<div
				class="mx-4 w-full overflow-hidden rounded-lg bg-white sm:mx-0 sm:w-3/4 md:w-2/3 lg:w-1/2 xl:w-full"
			>
				<img src="/investree.png" alt="code snippet" class="h-auto w-auto" />
			</div>
		</div>
	</div>
</section>

<style>
	:global([data-sonner-toast]) {
		display: flex !important;
		align-items: center !important;
	}

	:global([data-sonner-toast] [data-content]) {
		flex: 1 !important;
	}

	:global([data-sonner-toast] [data-button]) {
		margin-left: auto !important;
		flex-shrink: 0 !important;
	}
</style>
