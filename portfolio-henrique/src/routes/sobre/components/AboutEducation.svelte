
<script lang="ts">
  import { reveal } from '#lib/actions/reveal.ts';
</script>

<section class="education-section" use:reveal>
  <div class="education-container">
    <div class="section-heading">
      <span class="section-number">01 / FORMAÇÃO</span>

      <div class="heading-content">
        <h2>
          Onde minha
          <em>trajetória começou.</em>
        </h2>

        <p>
          Minha formação acadêmica foi uma etapa importante para desenvolver
          o raciocínio lógico, explorar diferentes áreas da computação e
          construir uma base para minha trajetória profissional.
        </p>
      </div>
    </div>

    <div class="education-content">
      <div class="timeline">
        <div class="timeline-line"></div>

        <div class="timeline-marker">
          <span></span>
        </div>

        <div class="timeline-year">
          <span>CONCLUSÃO</span>
          <strong>2026</strong>
        </div>
      </div>

      <article class="education-card">
        <div class="card-top">
          <span>FORMAÇÃO ACADÊMICA</span>
          <span class="completion-status">
            <span class="status-dot"></span>
            CONCLUÍDO
          </span>
        </div>

        <div class="card-main">
          <div class="institution-symbol">
            <span>IF</span>
            <span>MG</span>
          </div>

          <div class="degree-info">
            <h3>Bacharelado em Ciência da Computação</h3>
            <p>Instituto Federal de Minas Gerais</p>
            <span class="campus">Campus Formiga · Minas Gerais</span>
          </div>
        </div>

        <div class="card-footer">
          <span>ENSINO SUPERIOR</span>
          <span>2026 · CONCLUÍDO</span>
        </div>
      </article>
    </div>

    <div class="education-note">
      <span class="note-symbol">“</span>
      <p>
        A computação me proporcionou uma forma estruturada de compreender
        problemas, explorar possibilidades e transformar ideias em soluções.
      </p>
    </div>
  </div>
</section>

<style>
  .education-section {
    padding: 115px 0 125px;
    background: #f5f2eb;
    color: #292820;
  }

  .education-container {
    width: min(1080px, calc(100% - 64px));
    margin-inline: auto;
  }

  .section-heading {
    display: grid;
    grid-template-columns: 0.7fr 1.3fr;
    gap: 50px;
    margin-bottom: 75px;
  }

  .section-number {
    padding-top: 9px;
    color: #8b9875;
    font-size: 10px;
    font-weight: 700;
    letter-spacing: 2px;
  }

  .heading-content h2 {
    font-family: var(--font-heading);
    font-size: clamp(35px, 4.5vw, 55px);
    font-weight: 500;
    line-height: 1.12;
    letter-spacing: -2px;
  }

  .heading-content h2 em {
    display: block;
    color: #8b9875;
    font-family: Georgia, serif;
    font-weight: 400;
  }

  .heading-content p {
    max-width: 550px;
    margin-top: 22px;
    color: #77705f;
    font-size: 14px;
    line-height: 1.9;
  }

  .education-content {
    display: grid;
    grid-template-columns: 130px 1fr;
    gap: 35px;
    align-items: stretch;
  }

  .timeline {
    position: relative;
    display: flex;
    flex-direction: column;
    align-items: center;
  }

  .timeline-line {
    position: absolute;
    top: 12px;
    bottom: 0;
    left: 50%;
    width: 1px;
    background: #c8bca6;
    transform: translateX(-50%);
  }

  .timeline-marker {
    position: relative;
    z-index: 1;
    display: grid;
    width: 25px;
    height: 25px;
    place-items: center;
    border: 1px solid #8b9875;
    border-radius: 50%;
    background: #f5f2eb;
  }

  .timeline-marker span {
    width: 7px;
    height: 7px;
    border-radius: 50%;
    background: #8b9875;
  }

  .timeline-year {
    position: relative;
    z-index: 1;
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 6px;
    margin-top: 18px;
    padding: 10px 12px;
    background: #f5f2eb;
  }

  .timeline-year > span {
    color: #77705f;
    font-size: 8px;
    font-weight: 700;
    letter-spacing: 1.5px;
  }

  .timeline-year strong {
    color: #8b9875;
    font-family: var(--font-heading);
    font-size: 25px;
    font-weight: 500;
  }

  .education-card {
    padding: 30px;
    border: 1px solid #ded7c9;
    background: #eae6dd;
    transition: border-color 0.3s ease, transform 0.3s ease;
  }

  .education-card:hover {
    transform: translateY(-3px);
    border-color: #a6ad91;
  }

  .card-top,
  .card-footer {
    display: flex;
    justify-content: space-between;
    align-items: center;
    gap: 15px;
    color: #77705f;
    font-size: 9px;
    font-weight: 700;
    letter-spacing: 1.5px;
  }

  .completion-status {
    display: flex;
    align-items: center;
    gap: 7px;
    color: #71805e;
  }

  .status-dot {
    width: 6px;
    height: 6px;
    border-radius: 50%;
    background: #8b9875;
  }

  .card-main {
    display: flex;
    align-items: center;
    gap: 25px;
    padding: 45px 0;
  }

  .institution-symbol {
    display: flex;
    width: 72px;
    height: 72px;
    flex-shrink: 0;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    border: 1px solid #b9b19f;
    color: #71805e;
    font-family: var(--font-heading);
    font-size: 21px;
    font-weight: 600;
    line-height: 1;
  }

  .institution-symbol span:last-child {
    margin-top: 4px;
    font-size: 11px;
    letter-spacing: 3px;
  }

  .degree-info h3 {
    font-family: var(--font-heading);
    font-size: clamp(20px, 2.5vw, 27px);
    font-weight: 500;
    letter-spacing: -0.8px;
  }

  .degree-info p {
    margin-top: 10px;
    color: #555248;
    font-size: 14px;
  }

  .campus {
    display: block;
    margin-top: 5px;
    color: #77705f;
    font-size: 12px;
  }

  .card-footer {
    padding-top: 18px;
    border-top: 1px solid #c8bca6;
  }

  .education-note {
    display: flex;
    align-items: flex-start;
    gap: 20px;
    max-width: 660px;
    margin: 65px 0 0 auto;
  }

  .note-symbol {
    color: #8b9875;
    font-family: Georgia, serif;
    font-size: 55px;
    line-height: 0.8;
  }

  .education-note p {
    color: #77705f;
    font-family: Georgia, serif;
    font-size: 17px;
    font-style: italic;
    line-height: 1.8;
  }

  @media (max-width: 700px) {
    .education-section {
      padding: 85px 0 95px;
    }

    .education-container {
      width: calc(100% - 40px);
    }

    .section-heading {
      grid-template-columns: 1fr;
      gap: 20px;
      margin-bottom: 50px;
    }

    .heading-content h2 {
      font-size: 40px;
    }

    .education-content {
      grid-template-columns: 45px 1fr;
      gap: 12px;
    }

    .education-card {
      padding: 22px 18px;
    }

    .card-top,
    .card-footer {
      font-size: 8px;
      letter-spacing: 1px;
    }

    .card-main {
      align-items: flex-start;
      gap: 15px;
      padding: 35px 0;
    }

    .institution-symbol {
      width: 53px;
      height: 53px;
      font-size: 16px;
    }

    .degree-info h3 {
      font-size: 20px;
    }

    .degree-info p {
      font-size: 12px;
      line-height: 1.6;
    }

    .campus {
      font-size: 11px;
    }

    .education-note {
      margin-top: 45px;
    }

    .education-note p {
      font-size: 15px;
    }
  }

  @media (max-width: 420px) {
    .completion-status {
      font-size: 7px;
    }

    .card-top > span:first-child {
      font-size: 7px;
    }

    .card-footer {
      flex-wrap: wrap;
    }
  }

  @media (prefers-reduced-motion: reduce) {
    .education-card {
      transition: none;
    }

    .education-card:hover {
      transform: none;
    }
  }
</style>
