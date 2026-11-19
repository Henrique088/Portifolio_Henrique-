<script lang="ts">
  import { reveal } from '#lib/actions/reveal.ts';

</script>

<section class="content-section problem-section" id="contexto" use:reveal>
  <div class="section-heading">
    <span class="section-label">01 — CONTEXTO</span>
    <h2>
      O cuidado começa antes
      <span>da primeira consulta.</span>
    </h2>
  </div>

  <div class="section-content">
    <div class="context-description">
      <p>
        A busca por apoio psicológico envolve confiança, acolhimento e
        comunicação. Por isso, o primeiro contato entre pacientes e
        profissionais também merece um ambiente que facilite essa aproximação.
      </p>

      <p>
        A partir dessa perspectiva, surgiu a proposta do TherapistFriend:
        utilizar a tecnologia para criar um espaço digital onde pacientes
        possam compartilhar suas experiências e encontrar profissionais
        preparados para oferecer acompanhamento.
      </p>
    </div>

    <div class="context-highlights">
      <article class="context-card">
        <span class="card-number">01</span>
        <div>
          <h3>Acolhimento</h3>
          <p>
            Um ambiente para que pacientes possam expressar seus sentimentos
            e experiências.
          </p>
        </div>
      </article>

      <article class="context-card">
        <span class="card-number">02</span>
        <div>
          <h3>Privacidade</h3>
          <p>
            Possibilidade de compartilhar relatos anonimamente e estabelecer
            conversas privadas.
          </p>
        </div>
      </article>

      <article class="context-card">
        <span class="card-number">03</span>
        <div>
          <h3>Conexão</h3>
          <p>
            Aproximar pacientes e profissionais por meio de recursos digitais
            de comunicação e acompanhamento.
          </p>
        </div>
      </article>
    </div>
  </div>
</section>

<style>
  .problem-section {
    width: min(1180px, calc(100% - 64px));
    margin: 0 auto;
    padding: 120px 0;
  }

  .section-label {
    color: #0abf48;
    font-size: 11px;
    font-weight: 700;
    letter-spacing: 1.8px;
  }

  .section-heading h2 {
    max-width: 720px;
    margin-top: 20px;
    color: #17251e;
    font-family: 'Space Grotesk', sans-serif;
    font-size: clamp(36px, 5vw, 56px);
    line-height: 1.12;
    letter-spacing: -2px;
  }

  .section-heading h2 span {
    color: #0abf48;
  }

  .section-content {
    display: grid;
    grid-template-columns: 1fr 0.9fr;
    gap: 80px;
    margin-top: 58px;
    align-items: start;
  }

  .context-description {
    display: flex;
    flex-direction: column;
    gap: 22px;
  }

  .context-description p {
    color: #66766c;
    font-size: 15px;
    line-height: 1.9;
  }

  .context-highlights {
    display: flex;
    flex-direction: column;
  }

  .context-card {
    display: flex;
    gap: 22px;
    padding: 24px 0;
    border-bottom: 1px solid #e1eae1;
  }

  .context-card:first-child {
    padding-top: 0;
  }

  .card-number {
    color: #0abf48;
    font-family: 'Space Grotesk', sans-serif;
    font-size: 14px;
    font-weight: 700;
  }

  .context-card h3 {
    margin-bottom: 8px;
    color: #17251e;
    font-family: 'Space Grotesk', sans-serif;
    font-size: 18px;
  }

  .context-card p {
    color: #66766c;
    font-size: 13px;
    line-height: 1.7;
  }

  @media (max-width: 800px) {
    .section-content {
      grid-template-columns: 1fr;
      gap: 42px;
    }
  }

  @media (max-width: 600px) {
    .problem-section {
      width: calc(100% - 40px);
      padding: 80px 0;
    }

    .section-heading h2 {
      letter-spacing: -1.5px;
    }
  }
</style>