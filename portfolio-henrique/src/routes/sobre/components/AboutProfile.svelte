
<script lang="ts">
  import { reveal } from '#lib/actions/reveal.ts';

  const characteristics = [
    {
      number: '01',
      title: 'Aprendizado contínuo',
      description:
        'Sou movido pela curiosidade e pela vontade de aprender. Gosto de explorar novas ideias, tecnologias e perspectivas.'
    },
    {
      number: '02',
      title: 'Pensamento analítico',
      description:
        'Tenho interesse em compreender como as coisas funcionam, investigar problemas e encontrar soluções com lógica e atenção aos detalhes.'
    },
    {
      number: '03',
      title: 'Determinação',
      description:
        'Valorizo a dedicação e o compromisso com aquilo que me proponho a fazer, buscando qualidade em cada etapa do trabalho.'
    },
    {
      number: '04',
      title: 'Colaboração',
      description:
        'Acredito que diferentes perspectivas enriquecem as ideias e que o trabalho em equipe permite alcançar resultados melhores.'
    }
  ];
</script>

<section class="profile-section" id="perfil" use:reveal>
  <div class="profile-container">
    <div class="profile-intro">
      <span class="section-number">02 / COMO PENSO E TRABALHO</span>

      <h2>
        Aprender,
        questionar e
        <em>construir.</em>
      </h2>

      <p class="intro-description">
        Acredito que o desenvolvimento pessoal e profissional é um processo
        contínuo. Gosto de compreender problemas, explorar possibilidades
        e transformar conhecimento em algo significativo.
      </p>

      <div class="profile-quote">
        <span class="quote-mark">“</span>
        <p>
          Mais do que encontrar respostas, gosto de entender as perguntas
          e descobrir os caminhos que levam até elas.
        </p>
      </div>
    </div>

    <div class="characteristics">
      {#each characteristics as item}
        <article class="characteristic-card">
          <div class="card-number">{item.number}</div>

          <div class="card-content">
            <h3>{item.title}</h3>
            <p>{item.description}</p>
          </div>

          <span class="card-decoration">↗</span>
        </article>
      {/each}
    </div>

    <div class="profile-note">
      <span class="note-indicator"></span>
      <p>
        Também sou uma pessoa autista. Essa característica faz parte da minha
        identidade e da minha forma de perceber o mundo.
      </p>
    </div>
  </div>
</section>

<style>
  .profile-section {
    padding: 125px 0;
    background: #e3e5d9;
    color: #292820;
  }

  .profile-container {
    display: grid;
    width: min(1080px, calc(100% - 64px));
    grid-template-columns: 0.85fr 1.15fr;
    column-gap: 85px;
    margin-inline: auto;
  }

  .profile-intro {
    align-self: start;
  }

  .section-number {
    color: #71805e;
    font-size: 10px;
    font-weight: 700;
    letter-spacing: 1.8px;
  }

  .profile-intro h2 {
    margin-top: 35px;
    font-family: var(--font-heading);
    font-size: clamp(40px, 4.5vw, 56px);
    font-weight: 500;
    line-height: 1.1;
    letter-spacing: -2.5px;
  }

  .profile-intro h2 em {
    display: block;
    color: #71805e;
    font-family: Georgia, serif;
    font-weight: 400;
  }

  .intro-description {
    max-width: 390px;
    margin-top: 25px;
    color: #686a5d;
    font-size: 14px;
    line-height: 1.9;
  }

  .profile-quote {
    display: flex;
    gap: 13px;
    margin-top: 55px;
    padding-top: 22px;
    border-top: 1px solid #c4c8b7;
  }

  .quote-mark {
    color: #879473;
    font-family: Georgia, serif;
    font-size: 43px;
    line-height: 0.8;
  }

  .profile-quote p {
    max-width: 300px;
    color: #77705f;
    font-family: Georgia, serif;
    font-size: 15px;
    font-style: italic;
    line-height: 1.8;
  }

  .characteristics {
    display: grid;
    grid-template-columns: repeat(2, minmax(0, 1fr));
    gap: 14px;
  }

  .characteristic-card {
    position: relative;
    display: flex;
    min-height: 225px;
    flex-direction: column;
    justify-content: space-between;
    padding: 25px;
    border: 1px solid #cbd0be;
    background: #eef0e7;
    transition:
      transform 0.3s ease,
      background 0.3s ease,
      border-color 0.3s ease;
  }

  .characteristic-card:hover {
    transform: translateY(-4px);
    border-color: #879473;
    background: #f5f5ed;
  }

  .card-number {
    color: #879473;
    font-family: var(--font-heading);
    font-size: 12px;
    font-weight: 600;
  }

  .card-content {
    padding-top: 35px;
  }

  .card-content h3 {
    font-family: var(--font-heading);
    font-size: 19px;
    font-weight: 600;
    letter-spacing: -0.5px;
  }

  .card-content p {
    margin-top: 10px;
    color: #777568;
    font-size: 12px;
    line-height: 1.8;
  }

  .card-decoration {
    position: absolute;
    top: 20px;
    right: 20px;
    color: #a4ad91;
    font-size: 15px;
    opacity: 0;
    transform: translate(-3px, 3px);
    transition:
      opacity 0.3s ease,
      transform 0.3s ease;
  }

  .characteristic-card:hover .card-decoration {
    opacity: 1;
    transform: translate(0, 0);
  }

  .profile-note {
    display: flex;
    grid-column: 2;
    align-items: center;
    gap: 12px;
    margin-top: 25px;
    padding-top: 20px;
    border-top: 1px solid #c4c8b7;
  }

  .note-indicator {
    width: 6px;
    height: 6px;
    flex-shrink: 0;
    border-radius: 50%;
    background: #879473;
  }

  .profile-note p {
    color: #777568;
    font-size: 11px;
    line-height: 1.8;
  }

  @media (max-width: 850px) {
    .profile-container {
      grid-template-columns: 1fr;
      gap: 50px;
    }

    .profile-intro h2 {
      max-width: 500px;
    }

    .intro-description {
      max-width: 550px;
    }

    .profile-quote {
      max-width: 500px;
    }

    .profile-note {
      grid-column: 1;
    }
  }

  @media (max-width: 600px) {
    .profile-section {
      padding: 85px 0 95px;
    }

    .profile-container {
      width: calc(100% - 40px);
      gap: 38px;
    }

    .profile-intro h2 {
      margin-top: 25px;
      font-size: 43px;
      letter-spacing: -2px;
    }

    .intro-description {
      font-size: 13px;
    }

    .profile-quote {
      margin-top: 35px;
    }

    .characteristics {
      grid-template-columns: 1fr;
      gap: 11px;
    }

    .characteristic-card {
      min-height: 175px;
      padding: 22px;
    }

    .card-content {
      padding-top: 25px;
    }

    .card-content h3 {
      font-size: 18px;
    }

    .card-content p {
      max-width: 400px;
    }
  }

  @media (prefers-reduced-motion: reduce) {
    .characteristic-card,
    .card-decoration {
      transition: none;
    }

    .characteristic-card:hover {
      transform: none;
    }
  }
</style>
