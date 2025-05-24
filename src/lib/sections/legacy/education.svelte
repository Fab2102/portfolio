<script lang="ts">
	import Timeline from '$lib/components/ui/timeline.svelte';
	import type { TimelineItem } from '$lib/components/ui/timeline.svelte';

	const educationItems: TimelineItem[] = [
		{
			date: '2017 – 2022',
			title: 'High school diploma (Matura)',
			description: 'Federal College and Institute for Viticulture and Pomology in Klosterneuburg',
			imageUrl: '/HBLA_logo.jpg'
		},
		{
			date: '2023 – 2026',
			title: 'B.Sc. in Business Informatics',
			description: 'WU (Vienna University of Economics and Business)',
			imageUrl: '/WU_logo.jpg'
		}
	];
</script>

<section id="education">
	<div class="mx-auto flex max-w-7xl px-10 py-12 sm:px-6 lg:px-8">
		<div>
			<h2 class="text-3xl font-bold text-gray-900">Education</h2>
			<div class="mt-10">
				<Timeline items={educationItems} />
			</div>
		</div>
	</div>
</section>
