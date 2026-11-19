<script lang="ts">
  import { reveal } from '#lib/actions/reveal.ts';

</script>

<section class="project-facts" use:reveal>
  <div class="fact">
    <span class="fact-label">CATEGORIA</span>
    <strong>Saúde e Tecnologia</strong>
  </div>

  <div class="fact">
    <span class="fact-label">TIPO DE PROJETO</span>
    <strong>Projeto acadêmico</strong>
  </div>

  <div class="fact">
    <span class="fact-label">DESENVOLVIMENTO</span>
    <strong>Full Stack</strong>
  </div>

  <div class="fact">
    <span class="fact-label">PLATAFORMA</span>
    <strong>Gratuita e web</strong>
  </div>
</section>

<style>
  .project-facts {
    width: min(1180px, calc(100% - 64px));
    margin: 0 auto;
    padding: 30px 0;
    display: grid;
    grid-template-columns: repeat(4, 1fr);
    border-top: 1px solid #e1eae1;
    border-bottom: 1px solid #e1eae1;
  }

  .fact {
    display: flex;
    flex-direction: column;
    gap: 10px;
    padding: 8px 24px;
    border-right: 1px solid #e1eae1;
  }

  .fact:first-child {
    padding-left: 0;
  }

  .fact:last-child {
    border-right: none;
  }

  .fact-label {
    color: #8a998e;
    font-size: 10px;
    font-weight: 700;
    letter-spacing: 1.5px;
  }

  .fact strong {
    color: #17251e;
    font-family: 'Space Grotesk', sans-serif;
    font-size: 15px;
    font-weight: 600;
  }

  @media (max-width: 700px) {
    .project-facts {
      width: calc(100% - 40px);
      grid-template-columns: repeat(2, 1fr);
      row-gap: 24px;
    }

    .fact:nth-child(2) {
      border-right: none;
    }

    .fact:nth-child(3) {
      padding-left: 0;
    }
  }
</style>