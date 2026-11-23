<script lang="ts">
  import { reveal } from '#lib/actions/reveal.ts';

</script>

<section id="contato" class="contact-section" use:reveal>
  <div class="container">
    <div class="section-header">
      <span class="section-number">04 / CONTATO</span>
      <span class="section-label">VAMOS CONVERSAR</span>
    </div>

    <div class="contact-content">
      <div class="contact-main">
        <h2>
          Vamos construir algo <span>juntos?</span>
        </h2>

        <p>
          Estou aberto a oportunidades, conexões profissionais e projetos
          que envolvam tecnologia e desenvolvimento de software.
        </p>

        <a href="mailto:henriqueribeiro88bb@gmail.com" class="contact-email">
          <span>Entre em contato</span>
          <span class="arrow">↗</span>
        </a>
      </div>

      <div class="contact-links">
        <a href="https://github.com/Henrique088" target="_blank" rel="noreferrer">
          <span>GitHub</span>
          <span>↗</span>
        </a>

        <a href="https://www.linkedin.com/in/henrique-ribeiro-dev/" target="_blank" rel="noreferrer">
          <span>LinkedIn</span>
          <span>↗</span>
        </a>

        <a href="mailto:henriqueribeiro88bb@gmail.com">
          <span>E-mail</span>
          <span>↗</span>
        </a>
      </div>
    </div>

    <div class="contact-footer">
      <span>DISPONÍVEL PARA NOVAS OPORTUNIDADES</span>
      <span>VAMOS CRIAR ALGO RELEVANTE.</span>
    </div>
  </div>
</section>

<style>
  .contact-section {
    padding: 120px 0 40px;
    border-top: 1px solid var(--color-border);
  }

  .section-header {
    display: flex;
    justify-content: space-between;
    align-items: center;
    margin-bottom: 75px;
  }

  .section-number,
  .section-label {
    font-size: 0.72rem;
    letter-spacing: 0.12em;
    color: var(--color-muted);
  }

  .contact-content {
    display: grid;
    grid-template-columns: 1.5fr 0.7fr;
    gap: 100px;
    align-items: end;
  }

  .contact-main h2 {
    max-width: 700px;
    font-family: var(--font-heading);
    font-size: clamp(2.8rem, 6vw, 5.5rem);
    line-height: 1.08;
    letter-spacing: -0.055em;
  }

  .contact-main h2 span {
    color: var(--color-primary);
  }

  .contact-main p {
    max-width: 500px;
    margin-top: 28px;
    color: var(--color-muted);
    font-size: 1rem;
    line-height: 1.8;
  }

  .contact-email {
    display: inline-flex;
    align-items: center;
    gap: 30px;
    margin-top: 40px;
    padding: 15px 20px;
    background: var(--color-primary);
    color: #101114;
    font-weight: 700;
    border-radius: 4px;
    transition: transform 0.25s ease, background 0.25s ease;
  }

  .contact-email:hover {
    transform: translateY(-4px);
    background: #c9f58c;
  }

  .contact-email .arrow {
    font-size: 1.2rem;
  }

  .contact-links {
    display: flex;
    flex-direction: column;
    border-top: 1px solid var(--color-border);
  }

  .contact-links a {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 20px 0;
    border-bottom: 1px solid var(--color-border);
    color: var(--color-muted);
    transition: color 0.2s ease;
  }

  .contact-links a:hover {
    color: var(--color-primary);
  }

  .contact-links a span:last-child {
    font-size: 1.1rem;
  }

  .contact-footer {
    display: flex;
    justify-content: space-between;
    gap: 20px;
    margin-top: 120px;
    padding-top: 25px;
    border-top: 1px solid var(--color-border);
    color: var(--color-muted);
    font-size: 0.65rem;
    letter-spacing: 0.1em;
  }

  @media (max-width: 768px) {
    .contact-section {
      padding-top: 85px;
    }

    .section-header {
      margin-bottom: 55px;
    }

    .contact-content {
      grid-template-columns: 1fr;
      gap: 60px;
    }

    .contact-main h2 {
      font-size: clamp(2.7rem, 11vw, 4rem);
    }

    .contact-footer {
      flex-direction: column;
      margin-top: 80px;
    }
  }
</style>