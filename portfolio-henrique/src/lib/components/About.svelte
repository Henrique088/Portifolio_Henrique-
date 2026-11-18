
<section id="sobre" class="about-section">
  <div class="container">
    <div class="section-header">
      <span class="eyebrow">01 / SOBRE MIM</span>
      <h2>Mais do que código.<br />
        <span>Construção de soluções.</span>
      </h2>
    </div>

    <div class="about-content">
      <div class="about-intro">
        <span class="about-symbol">H.</span>
        <p class="intro-text">
          Sou desenvolvedor de software e gosto de transformar ideias
          em aplicações funcionais, bem estruturadas e pensadas para
          resolver problemas reais.
        </p>
      </div>

      <div class="about-details">
        <p>
          Tenho interesse especial em arquitetura de software,
          desenvolvimento backend e integração de tecnologias.
          Ao longo dos meus projetos, busco unir organização,
          qualidade de código e uma boa experiência para quem utiliza
          o produto.
        </p>

        <p>
          Também exploro aplicações de inteligência artificial e
          tecnologias em tempo real, sempre procurando entender
          como diferentes ferramentas podem trabalhar juntas para
          construir soluções completas.
        </p>

        <div class="about-focus">
          <span>ÁREAS DE INTERESSE</span>
          <div class="focus-list">
            <span>Arquitetura de software</span>
            <span>Backend</span>
            <span>Inteligência artificial</span>
            <span>Aplicações web</span>
            <span>Tecnologias em tempo real</span>
          </div>
        </div>
      </div>
    </div>
  </div>
</section>

<style>
  .about-section {
    padding: 130px 0;
    border-top: 1px solid var(--color-border);
  }

  .section-header {
    margin-bottom: 75px;
  }

  .eyebrow {
    display: block;
    margin-bottom: 24px;
    color: var(--color-primary);
    font-size: 12px;
    font-weight: 700;
    letter-spacing: 2px;
  }

  .section-header h2 {
    font-family: var(--font-heading);
    font-size: clamp(38px, 5vw, 64px);
    line-height: 1.12;
    letter-spacing: -2.5px;
  }

  .section-header h2 span {
    color: var(--color-muted);
  }

  .about-content {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 100px;
  }

  .about-intro {
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    gap: 35px;
  }

  .about-symbol {
    display: grid;
    place-items: center;
    width: 76px;
    height: 76px;
    border: 1px solid var(--color-primary);
    border-radius: 18px;
    color: var(--color-primary);
    font-family: var(--font-heading);
    font-size: 32px;
    font-weight: 700;
  }

  .intro-text {
    max-width: 490px;
    font-family: var(--font-heading);
    font-size: clamp(22px, 2.5vw, 30px);
    font-weight: 500;
    line-height: 1.5;
  }

  .about-details {
    display: flex;
    flex-direction: column;
    gap: 24px;
    color: var(--color-muted);
    font-size: 15px;
    line-height: 1.9;
  }

  .about-focus {
    margin-top: 15px;
    padding-top: 25px;
    border-top: 1px solid var(--color-border);
  }

  .about-focus > span {
    display: block;
    margin-bottom: 18px;
    color: var(--color-text);
    font-size: 11px;
    font-weight: 700;
    letter-spacing: 1.5px;
  }

  .focus-list {
    display: flex;
    flex-wrap: wrap;
    gap: 10px;
  }

  .focus-list span {
    padding: 9px 13px;
    border: 1px solid var(--color-border);
    border-radius: 6px;
    color: var(--color-muted);
    font-size: 12px;
  }

  @media (max-width: 750px) {
    .about-section {
      padding: 90px 0;
    }

    .section-header {
      margin-bottom: 45px;
    }

    .about-content {
      grid-template-columns: 1fr;
      gap: 45px;
    }

    .about-intro {
      gap: 25px;
    }
  }
</style>
