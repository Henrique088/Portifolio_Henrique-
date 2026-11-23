<script lang="ts">
	import AboutHero from './components/AboutHero.svelte';
	import AboutEducation from './components/AboutEducation.svelte';
	import AboutProfile from './components/AboutProfile.svelte';
    import AboutInterests from './components/AboutInterests.svelte';
    import AboutClosing from './components/AboutClosing.svelte';
</script>

<svelte:head>
	<title>Sobre mim | Henrique Ribeiro</title>
	<meta
		name="description"
		content="Conheça Henrique Ribeiro, sua trajetória, formação e interesses."
	/>
</svelte:head>

<main>
	<AboutHero />
	<AboutEducation />
	<AboutProfile />
	<AboutInterests />
    <AboutClosing />
	<!-- Próxima seção: perfil pessoal e profissional -->
</main>
