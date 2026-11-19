<script lang="ts">
  import { reveal } from '#lib/actions/reveal.ts';

</script>

<section class="project-hero" id="visao-geral" use:reveal>
  <div class="hero-content">
    <span class="eyebrow">
      PROJETO EM DESTAQUE
    </span>

    <h1>
      Tecnologia que aproxima.
      <span>Cuidado que conecta.</span>
    </h1>

    <p class="hero-description">
      O TherapistFriend é uma plataforma web desenvolvida para aproximar
      pacientes e profissionais da saúde mental, criando um ambiente
      digital de acolhimento, comunicação e acompanhamento.
    </p>

    <div class="hero-tags">
      <span>Full Stack</span>
      <span>Inteligência Artificial</span>
      <span>Saúde e Tecnologia</span>
    </div>
  </div>

  <!-- Mantenha aqui a composição visual do Hero que já existe na página,
       caso ela tenha sido construída com elementos HTML e CSS. -->
</section>

<style>
  .project-hero {
    width: min(1180px, calc(100% - 64px));
    min-height: 490px;
    margin: 0 auto;
    padding: 100px 0;
    display: flex;
    align-items: center;
  }

  .hero-content {
    max-width: 780px;
  }

  .eyebrow {
    display: inline-block;
    margin-bottom: 24px;
    color: #0abf48;
    font-size: 11px;
    font-weight: 700;
    letter-spacing: 2px;
  }

  h1 {
    max-width: 760px;
    font-family: 'Space Grotesk', sans-serif;
    font-size: clamp(42px, 6vw, 72px);
    line-height: 1.08;
    letter-spacing: -3px;
  }

  h1 span {
    display: block;
    color: #0abf48;
  }

  .hero-description {
    max-width: 620px;
    margin-top: 28px;
    color: #66766c;
    font-size: 16px;
    line-height: 1.8;
  }

  .hero-tags {
    display: flex;
    flex-wrap: wrap;
    gap: 10px;
    margin-top: 32px;
  }

  .hero-tags span {
    padding: 9px 14px;
    border: 1px solid #dce8dc;
    border-radius: 30px;
    color: #526257;
    font-size: 12px;
    font-weight: 600;
  }

  @media (max-width: 600px) {
    .project-hero {
      width: calc(100% - 40px);
      min-height: auto;
      padding: 80px 0;
    }

    h1 {
      letter-spacing: -2px;
    }

    .hero-description {
      font-size: 14px;
    }
  }
</style>