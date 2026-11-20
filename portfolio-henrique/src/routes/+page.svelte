
<script lang="ts">
  import Navbar from '#lib/components/Navbar.svelte';
  import Hero from '#lib/components/Hero.svelte';
  import About from '#lib/components/About.svelte';
  import Projects  from '#lib/components/Projects.svelte';
  import Contact from '#lib/components/Contact.svelte';
  import OtherProjects from '#lib/components/OtherProjects.svelte';
</script>

<svelte:head>
  <title>Henrique | Desenvolvedor de Software</title>
  <meta
    name="description"
    content="Conheça Henrique, sua trajetória, projetos e soluções em desenvolvimento de software."
  />
  <meta name="theme-color" content="#101114" />
</svelte:head>

<Navbar />

<main>
  <Hero />

  <About />

  <Projects />
  
  <OtherProjects />
  
  <Contact />


</main>

<style>
  
</style>
