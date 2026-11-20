
<script lang="ts">
  import { reveal } from '#lib/actions/reveal.ts';

  const mobileProjects = [
    {
      number: '01',
      title: 'Leitor NFC',
      category: 'APLICAÇÃO MOBILE',
      description:
        'Aplicativo desenvolvido em React Native para leitura de cartões NFC/RFID de 13,56 MHz, com interface inicial e suporte a temas claro e escuro.',
      technologies: ['React Native', 'NFC', 'RFID'],
      link: 'https://github.com/Henrique088/Leitor-NFC',
      linkLabel: 'Ver repositório'
    },
    {
      number: '02',
      title: 'Leitor de QR Code',
      category: 'APLICAÇÃO MOBILE',
      description:
        'Aplicativo para captura e armazenamento de imagens no dispositivo, leitura de QR Codes e reconhecimento de texto utilizando a câmera.',
      technologies: [
        'React Native',
        'Vision Camera',
        'Text Recognition'
      ],
      link: 'https://github.com/Henrique088/frame_qrcode',
      linkLabel: 'Ver repositório'
    }
  ];

  const experiments = [
    {
      title: 'Agendador com Crontab',
      description: 'Automação e agendamento de tarefas utilizando Crontab.',
      technology: 'Linux · Automação',
      link: 'https://github.com/Henrique088/Crontab'
    },
    {
      title: 'Jogos em Python',
      description: 'Implementação de jogos de adivinhação e forca executados no terminal.',
      technology: 'Python · Lógica',
      link: 'https://github.com/Henrique088/Jogos-em-python'
    },
    {
      title: 'Máquina de Turing',
      description: 'Implementação de uma simulação de Máquina de Turing em Python.',
      technology: 'Python · Computação teórica',
      link: 'https://github.com/Henrique088/Maquina-Turing'
    },
    {
      title: 'Consultas com Prolog',
      description: 'Leitura de planilhas Excel e elaboração de consultas sobre os dados utilizando Prolog.',
      technology: 'Prolog · Processamento de dados',
      link: 'https://github.com/Henrique088/trabalho-prolog'
    }
  ];
</script>

<section class="other-projects-section" id="outros-projetos" use:reveal>
  <div class="other-projects-container">
    <div class="section-heading">
      <div>
        <span class="section-label">PROJETOS COMPLEMENTARES</span>
        <h2>
          Explorando diferentes
          <span>possibilidades.</span>
        </h2>
      </div>

      <p class="section-description">
        Outros projetos e experimentos que fizeram parte da minha trajetória,
        explorando diferentes tecnologias, conceitos e formas de resolver problemas.
      </p>
    </div>

    <div class="category-heading">
      <span>01</span>
      <div>
        <h3>Aplicações e integrações</h3>
        <p>Projetos com interfaces, aplicações mobile e integração de tecnologias.</p>
      </div>
    </div>

    <article class="carvoaria-card" use:reveal>
      <div class="carvoaria-visual">
        <div class="visual-top">
          <span>PROTÓTIPO DE SOLUÇÃO</span>
          <span>01 / 03</span>
        </div>

        <div class="carvoaria-symbol">
          <div class="symbol-ring"></div>
          <div class="symbol-center">C.</div>
        </div>

        <div class="visual-bottom">
          <span>CARVOARIA</span>
          <span>APP + WEB</span>
        </div>
      </div>

      <div class="carvoaria-info">
        <span class="project-category">APLICAÇÃO MOBILE + DASHBOARD WEB</span>
        <h3>Solução para carvoaria</h3>
        <p>
          Conjunto de protótipos composto por um aplicativo mobile em React Native
          e uma aplicação web em Flask. O projeto web apresenta dados simulados
          em um painel visual e permite gerar relatórios dinâmicos em HTML.
        </p>

        <div class="project-technologies">
          <span>React Native</span>
          <span>Python</span>
          <span>Flask</span>
          <span>HTML</span>
        </div>

        <div class="project-links">
          <a href="https://github.com/Henrique088/app_carvoaria" target="_blank" rel="noreferrer">
            Aplicativo mobile <span>↗</span>
          </a>
          <a href="https://github.com/Henrique088/carvao_web" target="_blank" rel="noreferrer">
            Aplicação web <span>↗</span>
          </a>
        </div>
      </div>
    </article>

    <div class="mobile-projects">
      {#each mobileProjects as project}
        <article class="mobile-card" use:reveal>
          <div class="mobile-card-top">
            <span>{project.category}</span>
            <span>{project.number} / 02</span>
          </div>

          <div class="mobile-card-content">
            <h3>{project.title}</h3>
            <p>{project.description}</p>
          </div>

          <div class="mobile-card-bottom">
            <div class="project-technologies">
              {#each project.technologies as technology}
                <span>{technology}</span>
              {/each}
            </div>

            <a href={project.link} target="_blank" rel="noreferrer">
              {project.linkLabel} <span>↗</span>
            </a>
          </div>
        </article>
      {/each}
    </div>

    <div class="category-heading experiments-heading">
      <span>02</span>
      <div>
        <h3>Fundamentos e experimentos</h3>
        <p>Exercícios práticos de lógica, automação e fundamentos da computação.</p>
      </div>
    </div>

    <div class="experiments-grid">
      {#each experiments as project, index}
        <article class="experiment-card" use:reveal>
          <div class="experiment-top">
            <span>0{index + 1}</span>
            <span class="experiment-arrow">↗</span>
          </div>

          <h4>{project.title}</h4>
          <p>{project.description}</p>

          <div class="experiment-bottom">
            <span>{project.technology}</span>
            <a href={project.link} target="_blank" rel="noreferrer" aria-label={`Ver repositório de ${project.title}`}>
              GitHub
            </a>
          </div>
        </article>
      {/each}
    </div>
  </div>
</section>

<style>
  .other-projects-section {
    padding: 110px 0 130px;
    background: var(--color-background);
  }

  .other-projects-container {
    width: min(1180px, calc(100% - 64px));
    margin-inline: auto;
  }

  .section-heading {
    display: grid;
    grid-template-columns: 1fr 0.65fr;
    align-items: end;
    gap: 60px;
    margin-bottom: 76px;
  }

  .section-label,
  .project-category {
    color: var(--color-primary);
    font-size: 11px;
    font-weight: 700;
    letter-spacing: 2px;
  }

  .section-heading h2 {
    margin-top: 18px;
    font-family: var(--font-heading);
    font-size: clamp(36px, 4.5vw, 58px);
    line-height: 1.08;
    letter-spacing: -2.5px;
  }

  .section-heading h2 span {
    display: block;
    color: var(--color-primary);
  }

  .section-description {
    max-width: 410px;
    color: var(--color-muted);
    font-size: 15px;
    line-height: 1.8;
  }

  .category-heading {
    display: flex;
    align-items: flex-start;
    gap: 18px;
    margin-bottom: 24px;
  }

  .category-heading > span {
    padding-top: 3px;
    color: var(--color-primary);
    font-family: var(--font-heading);
    font-size: 13px;
  }

  .category-heading h3 {
    font-family: var(--font-heading);
    font-size: 21px;
    font-weight: 600;
  }

  .category-heading p {
    margin-top: 6px;
    color: var(--color-muted);
    font-size: 13px;
    line-height: 1.6;
  }

  .carvoaria-card {
    display: grid;
    grid-template-columns: 0.9fr 1.1fr;
    overflow: hidden;
    border: 1px solid var(--color-border);
    border-radius: 18px;
    background: var(--color-surface);
    transition: border-color 0.3s ease, transform 0.3s ease;
  }

  .carvoaria-card:hover {
    transform: translateY(-4px);
    border-color: #77705c;
  }

  .carvoaria-visual {
    position: relative;
    display: flex;
    min-height: 340px;
    flex-direction: column;
    justify-content: space-between;
    overflow: hidden;
    padding: 25px;
    background:
      radial-gradient(circle at 50% 48%, #77664b 0, #423a30 30%, transparent 65%),
      #29251f;
    color: #e9dfc9;
  }

  .visual-top,
  .visual-bottom {
    display: flex;
    justify-content: space-between;
    gap: 12px;
    font-size: 9px;
    font-weight: 600;
    letter-spacing: 1.7px;
  }

  .visual-top span:last-child,
  .visual-bottom span:last-child {
    color: #b6a88c;
  }

  .carvoaria-symbol {
    position: relative;
    display: grid;
    width: 160px;
    height: 160px;
    place-items: center;
    align-self: center;
  }

  .symbol-ring {
    position: absolute;
    width: 150px;
    height: 150px;
    border: 1px solid #b6a88c70;
    border-radius: 50%;
    box-shadow: 0 0 0 15px #b6a88c10, 0 0 0 30px #b6a88c08;
  }

  .symbol-center {
    display: grid;
    width: 86px;
    height: 86px;
    place-items: center;
    border: 1px solid #d4c5a2;
    border-radius: 50%;
    color: #f0e5ce;
    font-family: var(--font-heading);
    font-size: 35px;
  }

  .carvoaria-info {
    display: flex;
    flex-direction: column;
    justify-content: center;
    padding: 42px;
  }

  .carvoaria-info h3 {
    margin-top: 15px;
    font-family: var(--font-heading);
    font-size: clamp(25px, 3vw, 34px);
    letter-spacing: -1px;
  }

  .carvoaria-info > p {
    margin-top: 15px;
    color: var(--color-muted);
    font-size: 14px;
    line-height: 1.8;
  }

  .project-technologies {
    display: flex;
    flex-wrap: wrap;
    gap: 8px;
  }

  .project-technologies span {
    padding: 7px 10px;
    border: 1px solid var(--color-border);
    border-radius: 5px;
    color: #c4c6cd;
    font-size: 10px;
  }

  .carvoaria-info > .project-technologies {
    margin-top: 22px;
  }

  .project-links {
    display: flex;
    flex-wrap: wrap;
    gap: 22px;
    margin-top: 28px;
  }

  .project-links a,
  .mobile-card-bottom > a {
    color: var(--color-primary);
    font-size: 12px;
    font-weight: 600;
    transition: opacity 0.2s ease;
  }

  .project-links a:hover,
  .mobile-card-bottom > a:hover {
    opacity: 0.7;
  }

  .project-links a span,
  .mobile-card-bottom > a span {
    margin-left: 4px;
  }

  .mobile-projects {
    display: grid;
    grid-template-columns: repeat(2, minmax(0, 1fr));
    gap: 18px;
    margin-top: 18px;
  }

  .mobile-card {
    display: flex;
    min-height: 280px;
    flex-direction: column;
    justify-content: space-between;
    padding: 25px;
    border: 1px solid var(--color-border);
    border-radius: 14px;
    background: var(--color-surface);
    transition: border-color 0.3s ease, transform 0.3s ease;
  }

  .mobile-card:hover,
  .experiment-card:hover {
    transform: translateY(-4px);
    border-color: #65734f;
  }

  .mobile-card-top,
  .experiment-top {
    display: flex;
    justify-content: space-between;
    color: var(--color-muted);
    font-size: 10px;
    font-weight: 600;
    letter-spacing: 1.3px;
  }

  .mobile-card-content {
    margin: 30px 0;
  }

  .mobile-card-content h3 {
    font-family: var(--font-heading);
    font-size: 24px;
    letter-spacing: -0.7px;
  }

  .mobile-card-content p {
    max-width: 440px;
    margin-top: 12px;
    color: var(--color-muted);
    font-size: 13px;
    line-height: 1.75;
  }

  .mobile-card-bottom {
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    gap: 20px;
  }

  .experiments-heading {
    margin-top: 78px;
  }

  .experiments-grid {
    display: grid;
    grid-template-columns: repeat(2, minmax(0, 1fr));
    gap: 14px;
  }

  .experiment-card {
    display: flex;
    min-height: 190px;
    flex-direction: column;
    padding: 22px;
    border: 1px solid var(--color-border);
    border-radius: 12px;
    background: #15171b;
    transition: border-color 0.3s ease, transform 0.3s ease;
  }

  .experiment-top > span:first-child {
    color: var(--color-primary);
  }

  .experiment-arrow {
    color: var(--color-muted);
    font-size: 15px;
  }

  .experiment-card h4 {
    margin-top: 20px;
    font-family: var(--font-heading);
    font-size: 17px;
    font-weight: 600;
  }

  .experiment-card > p {
    margin-top: 8px;
    color: var(--color-muted);
    font-size: 12px;
    line-height: 1.7;
  }

  .experiment-bottom {
    display: flex;
    justify-content: space-between;
    align-items: center;
    gap: 12px;
    margin-top: auto;
    padding-top: 22px;
  }

  .experiment-bottom > span {
    color: #858995;
    font-size: 10px;
  }

  .experiment-bottom a {
    color: var(--color-primary);
    font-size: 11px;
    font-weight: 600;
  }

  .experiment-bottom a:hover {
    opacity: 0.7;
  }

  a:focus-visible {
    outline: 2px solid var(--color-primary);
    outline-offset: 4px;
    border-radius: 3px;
  }

  @media (max-width: 850px) {
    .section-heading {
      grid-template-columns: 1fr;
      gap: 22px;
    }

    .section-description {
      max-width: 600px;
    }

    .carvoaria-card {
      grid-template-columns: 1fr;
    }

    .carvoaria-visual {
      min-height: 280px;
    }

    .carvoaria-info {
      padding: 30px;
    }
  }

  @media (max-width: 600px) {
    .other-projects-section {
      padding: 85px 0 95px;
    }

    .other-projects-container {
      width: calc(100% - 40px);
    }

    .section-heading {
      margin-bottom: 55px;
    }

    .section-heading h2 {
      letter-spacing: -1.8px;
    }

    .category-heading h3 {
      font-size: 18px;
    }

    .carvoaria-visual {
      min-height: 240px;
      padding: 20px;
    }

    .carvoaria-info {
      padding: 25px 22px;
    }

    .project-links {
      flex-direction: column;
      gap: 14px;
    }

    .mobile-projects,
    .experiments-grid {
      grid-template-columns: 1fr;
    }

    .mobile-card {
      min-height: 250px;
      padding: 22px;
    }

    .experiments-heading {
      margin-top: 60px;
    }

    .experiment-card {
      min-height: 175px;
    }
  }

  @media (prefers-reduced-motion: reduce) {
    .carvoaria-card,
    .mobile-card,
    .experiment-card {
      transition: none;
    }

    .carvoaria-card:hover,
    .mobile-card:hover,
    .experiment-card:hover {
      transform: none;
    }
  }
</style>
