<script context="module" lang="ts">
	export interface TimelineItem {
		date: string;
		title: string;
		description: string;
		imageUrl?: string;
	}
</script>

<script lang="ts">
	export let items: TimelineItem[] = [];
</script>

<div class="relative">
	<div class="absolute left-4 top-0 h-full border-l-2 border-gray-200"></div>

	<ul class="ml-8 space-y-20">
		{#each items as { date, title, description, imageUrl }}
			<li class="relative">
				<!-- timeline dot -->
				<span class="absolute -left-5 top-1.5 h-3 w-3 rounded-full bg-[#2463EB]"></span>

				<!-- main content -->
				<div class="ml-6">
					<time class="text-sm font-medium text-[#2463EB]">{date}</time>

					<div class="mt-2 flex items-start space-x-4">
						{#if imageUrl}
							<div class="h-11 w-11 flex-shrink-0">
								<img src={imageUrl} alt="{title} image" class="w-full rounded object-cover" />
							</div>
						{/if}

						<div>
							<h3 class="text-lg font-bold text-gray-900">{title}</h3>
							<p class="mt-1 text-gray-600">{description}</p>
						</div>
					</div>
				</div>
			</li>
		{/each}
	</ul>
</div>
