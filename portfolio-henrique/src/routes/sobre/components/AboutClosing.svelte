
<script lang="ts">
  import { reveal } from '#lib/actions/reveal.ts';
</script>

<section class="closing-section" id="proposito" use:reveal>
  <div class="closing-container">
    <div class="closing-topline">
      <span>04 / PROPÓSITO</span>
      <span>O QUE VEM PELA FRENTE</span>
    </div>

    <div class="closing-content">
      <div class="closing-heading">
        <span class="closing-eyebrow">
          IDEIAS QUE GANHAM FORMA
          <span class="eyebrow-line"></span>
        </span>

        <h2>
          O próximo passo
          é <em>construir.</em>
        </h2>
      </div>

      <div class="closing-description">
        <p>
          Quero continuar aprendendo, aprofundando meus conhecimentos e
          participando da construção de soluções que tenham utilidade
          e impacto na vida das pessoas.
        </p>

        <p>
          Vejo a tecnologia como um meio para transformar ideias em
          possibilidades reais. É nessa direção que pretendo desenvolver
          minha trajetória.
        </p>
      </div>
    </div>

    <div class="closing-actions">
      <a href="/#projetos" class="primary-link">
        CONHEÇA MEUS PROJETOS
        <span>↗</span>
      </a>

      <a href="/#contato" class="secondary-link">
        VAMOS CONVERSAR
        <span>→</span>
      </a>
    </div>

    <footer class="closing-footer">
      <a href="/" class="footer-logo">
        HENRIQUE<span>.</span>
      </a>

      <span>DESENVOLVIMENTO · TECNOLOGIA · POSSIBILIDADES</span>

      <a href="#top" class="back-top">
        VOLTAR AO TOPO ↑
      </a>
    </footer>
  </div>
</section>

<style>
  .closing-section {
    position: relative;
    overflow: hidden;
    padding: 35px 0 25px;
    background: #101114;
    color: #f5f5f5;
  }

  .closing-container {
    position: relative;
    z-index: 1;
    width: min(1180px, calc(100% - 64px));
    margin-inline: auto;
  }

  .closing-topline {
    display: flex;
    justify-content: space-between;
    gap: 20px;
    padding-bottom: 22px;
    border-bottom: 1px solid #30323a;
    color: #9699a3;
    font-size: 9px;
    font-weight: 600;
    letter-spacing: 1.8px;
  }

  .closing-content {
    display: grid;
    grid-template-columns: 1.1fr 0.9fr;
    align-items: center;
    gap: 90px;
    padding: 105px 0 75px;
  }

  .closing-eyebrow {
    display: flex;
    align-items: center;
    gap: 13px;
    color: #9699a3;
    font-size: 9px;
    font-weight: 700;
    letter-spacing: 1.7px;
  }

  .eyebrow-line {
    width: 35px;
    height: 1px;
    background: #b8ef6b;
  }

  .closing-heading h2 {
    margin-top: 28px;
    font-family: var(--font-heading);
    font-size: clamp(45px, 5.5vw, 72px);
    font-weight: 500;
    line-height: 1.08;
    letter-spacing: -3.5px;
  }

  .closing-heading h2 em {
    display: block;
    color: #b8ef6b;
    font-family: Georgia, serif;
    font-weight: 400;
  }

  .closing-description {
    max-width: 440px;
  }

  .closing-description p {
    color: #9699a3;
    font-size: 14px;
    line-height: 1.95;
  }

  .closing-description p + p {
    margin-top: 20px;
  }

  .closing-actions {
    display: flex;
    flex-wrap: wrap;
    align-items: center;
    gap: 30px;
    padding-bottom: 95px;
  }

  .primary-link,
  .secondary-link {
    display: inline-flex;
    align-items: center;
    gap: 20px;
    font-size: 10px;
    font-weight: 700;
    letter-spacing: 1.2px;
    transition: color 0.25s ease;
  }

  .primary-link {
    padding: 17px 21px;
    background: #b8ef6b;
    color: #101114;
  }

  .primary-link span {
    font-size: 16px;
    transition: transform 0.25s ease;
  }

  .primary-link:hover {
    background: #c8f58a;
  }

  .primary-link:hover span {
    transform: translate(3px, -3px);
  }

  .secondary-link {
    color: #f5f5f5;
  }

  .secondary-link span {
    color: #b8ef6b;
    font-size: 17px;
    transition: transform 0.25s ease;
  }

  .secondary-link:hover {
    color: #b8ef6b;
  }

  .secondary-link:hover span {
    transform: translateX(4px);
  }

  .closing-footer {
    display: flex;
    align-items: center;
    justify-content: space-between;
    gap: 20px;
    padding-top: 22px;
    border-top: 1px solid #30323a;
    color: #777b85;
    font-size: 8px;
    font-weight: 600;
    letter-spacing: 1.4px;
  }

  .footer-logo {
    color: #f5f5f5;
    font-family: var(--font-heading);
    font-size: 16px;
    font-weight: 700;
    letter-spacing: -0.5px;
  }

  .footer-logo span {
    color: #b8ef6b;
  }

  .back-top {
    transition: color 0.25s ease;
  }

  .back-top:hover {
    color: #b8ef6b;
  }

  .primary-link:focus-visible,
  .secondary-link:focus-visible,
  .footer-logo:focus-visible,
  .back-top:focus-visible {
    outline: 2px solid #b8ef6b;
    outline-offset: 5px;
  }

  @media (max-width: 800px) {
    .closing-content {
      grid-template-columns: 1fr;
      gap: 35px;
      padding: 75px 0 50px;
    }

    .closing-description {
      max-width: 600px;
    }

    .closing-actions {
      padding-bottom: 70px;
    }
  }

  @media (max-width: 600px) {
    .closing-section {
      padding-top: 25px;
    }

    .closing-container {
      width: calc(100% - 40px);
    }

    .closing-topline {
      font-size: 8px;
      letter-spacing: 1px;
    }

    .closing-content {
      padding: 65px 0 40px;
    }

    .closing-heading h2 {
      font-size: 48px;
      letter-spacing: -2px;
    }

    .closing-description p {
      font-size: 13px;
    }

    .closing-actions {
      align-items: flex-start;
      flex-direction: column;
      gap: 25px;
      padding-bottom: 65px;
    }

    .closing-footer {
      align-items: flex-start;
      flex-direction: column;
      gap: 16px;
    }
  }

  @media (prefers-reduced-motion: reduce) {
    .primary-link,
    .secondary-link,
    .primary-link span,
    .secondary-link span,
    .back-top {
      transition: none;
    }

    .primary-link:hover span,
    .secondary-link:hover span {
      transform: none;
    }
  }
</style>
