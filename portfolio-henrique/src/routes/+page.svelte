
<script lang="ts">
  import Navbar from '#lib/components/Navbar.svelte';
  import Hero from '#lib/components/Hero.svelte';
  import About from '#lib/components/About.svelte';
  import Projects  from '#lib/components/Projects.svelte';
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

  <section id="contato" class="placeholder">
    <div class="container">
      <span>04 / CONTATO</span>
      <h2>Vamos construir algo juntos?</h2>
    </div>
  </section>
</main>

<style>
  .placeholder {
    padding-block: 110px;
    border-top: 1px solid var(--color-border);
  }

  .placeholder span {
    color: var(--color-primary);
    font-size: 11px;
    letter-spacing: 1.5px;
  }

  .placeholder h2 {
    margin-top: 25px;
    font-family: var(--font-heading);
    font-size: clamp(30px, 5vw, 48px);
  }

  .placeholder p {
    margin-top: 15px;
    color: var(--color-muted);
  }
</style>
