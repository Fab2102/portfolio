<script>
	import Footer from '$lib/sections/footer.svelte';
</script>

<div class="mx-auto max-w-3xl space-y-8 px-6 py-12">
	<h1 class="text-4xl font-bold text-gray-800">Imprint</h1>

	<div class="space-y-4 text-gray-700">
		<p>This website is operated by:</p>

		<address class="not-italic">
			<p class="font-semibold">Example Company GmbH</p>
			<p>Example Street 12<br />1010 Vienna<br />Austria</p>
			<p>
				Phone: <a href="tel:+43123456789" class="text-blue-600 hover:underline">+43 123 456 789</a
				><br />
				Email:
				<a href="mailto:info@example.com" class="text-blue-600 hover:underline">info@example.com</a>
			</p>
			<p>
				VAT ID: ATU12345678<br />
				Commercial Register: FN 123456a, Commercial Court Vienna
			</p>
		</address>
	</div>

	<section class="space-y-4 text-gray-700">
		<h2 class="text-2xl font-semibold text-gray-800">Disclaimer</h2>
		<p>
			The contents of this website were created with great care. However, we cannot guarantee the
			accuracy, completeness, or timeliness of the content.
		</p>
	</section>

	<section class="space-y-4 text-gray-700">
		<h2 class="text-2xl font-semibold text-gray-800">Liability for Links</h2>
		<p>
			Our site contains links to external websites. We have no influence on the content of those
			websites and assume no liability for them.
		</p>
	</section>
</div>

<Footer />
