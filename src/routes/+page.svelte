<script lang="ts">
	import Navbar from '$lib/sections/navbar.svelte';
	import Profile from '$lib/sections/profile.svelte';
	import About from '$lib/sections/about.svelte';
	import Skills from '$lib/sections/skills.svelte';
	import EduExp from '$lib/sections/edu_exp.svelte';
	import Projects from '$lib/sections/projects.svelte';
	import Footer from '$lib/sections/footer.svelte';
</script>

<main>
	<Navbar />
	<Profile />
	<About />
	<div class="mb-40 sm:mb-20"></div>
	<Skills />
	<div class="mb-40 sm:mb-20"></div>
	<EduExp />
	<div class="mb-40 sm:mb-20"></div>
	<Projects />
	<Footer />
</main>
