
<script lang="ts">
  import { reveal } from '#lib/actions/reveal.ts';

  const interests = [
    {
      number: '01',
      symbol: '↗',
      title: 'Caminhar',
      description:
        'Gosto de caminhar e aproveitar momentos para desacelerar, observar e renovar as ideias.',
      category: 'BEM-ESTAR'
    },
    {
      number: '02',
      symbol: '♪',
      title: 'Cantar',
      description:
        'A música é uma das formas que encontro para me expressar e aproveitar o tempo livre.',
      category: 'MÚSICA'
    },
    {
      number: '03',
      symbol: '⌘',
      title: 'Jogar',
      description:
        'Gosto de jogos como forma de entretenimento, desafios e experiências diferentes.',
      category: 'ENTRETENIMENTO'
    },
    {
      number: '04',
      symbol: '▶',
      title: 'Filmes, séries e desenhos',
      description:
        'Gosto de explorar diferentes histórias, universos e estilos de animação.',
      category: 'CULTURA'
    }
  ];
</script>

<section class="interests-section" id="alem-do-codigo" use:reveal>
  <div class="interests-container">
    <div class="interests-heading">
      <div class="heading-intro">
        <span class="section-number">03 / ALÉM DO CÓDIGO</span>

        <h2>
          Outras formas
          de <em>explorar o mundo.</em>
        </h2>
      </div>

      <p>
        Nem tudo acontece diante de uma tela de código. Também gosto de
        atividades que permitem relaxar, conhecer novas histórias e
        experimentar diferentes formas de expressão.
      </p>
    </div>

    <div class="interests-grid">
      {#each interests as interest}
        <article class="interest-card" use:reveal>
          <div class="card-top">
            <span>{interest.number}</span>
            <span>{interest.category}</span>
          </div>

          <div class="interest-symbol">
            {interest.symbol}
          </div>

          <div class="card-content">
            <h3>{interest.title}</h3>
            <p>{interest.description}</p>
          </div>

          <div class="card-bottom">
            <span>INTERESSE PESSOAL</span>
            <span class="bottom-decoration">✳</span>
          </div>
        </article>
      {/each}
    </div>

    <div class="interests-footer">
      <span class="footer-decoration">✳</span>

      <p>
        Também gosto de consumir conteúdos variados, desde vídeos
        informativos até produções de entretenimento. A curiosidade
        não fica restrita à tecnologia.
      </p>

      <span class="footer-label">CURIOSIDADE SEMPRE</span>
    </div>
  </div>
</section>

<style>
  .interests-section {
    padding: 125px 0;
    background: #f5f2eb;
    color: #292820;
  }

  .interests-container {
    width: min(1080px, calc(100% - 64px));
    margin-inline: auto;
  }

  .interests-heading {
    display: grid;
    grid-template-columns: 1fr 0.75fr;
    align-items: end;
    gap: 70px;
    margin-bottom: 65px;
  }

  .section-number {
    color: #8b9875;
    font-size: 10px;
    font-weight: 700;
    letter-spacing: 1.8px;
  }

  .heading-intro h2 {
    max-width: 550px;
    margin-top: 25px;
    font-family: var(--font-heading);
    font-size: clamp(38px, 4.5vw, 55px);
    font-weight: 500;
    line-height: 1.1;
    letter-spacing: -2.3px;
  }

  .heading-intro h2 em {
    display: block;
    color: #8b9875;
    font-family: Georgia, serif;
    font-weight: 400;
  }

  .interests-heading > p {
    max-width: 410px;
    padding-bottom: 5px;
    color: #77705f;
    font-size: 14px;
    line-height: 1.9;
  }

  .interests-grid {
    display: grid;
    grid-template-columns: repeat(4, minmax(0, 1fr));
    gap: 13px;
  }

  .interest-card {
    display: flex;
    min-height: 310px;
    flex-direction: column;
    padding: 20px;
    border: 1px solid #ded7c9;
    background: #eae6dd;
    transition:
      transform 0.3s ease,
      border-color 0.3s ease,
      background 0.3s ease;
  }

  .interest-card:hover {
    transform: translateY(-5px);
    border-color: #a6ad91;
    background: #efede4;
  }

  .card-top,
  .card-bottom {
    display: flex;
    align-items: center;
    justify-content: space-between;
    gap: 8px;
  }

  .card-top {
    color: #8b9875;
    font-size: 9px;
    font-weight: 700;
    letter-spacing: 1px;
  }

  .card-top span:last-child {
    color: #77705f;
    font-size: 8px;
    letter-spacing: 0.8px;
  }

  .interest-symbol {
    display: grid;
    width: 55px;
    height: 55px;
    margin: 35px 0 25px;
    place-items: center;
    border: 1px solid #c8bca6;
    border-radius: 50%;
    color: #8b9875;
    font-family: Georgia, serif;
    font-size: 27px;
    transition:
      background 0.3s ease,
      transform 0.3s ease;
  }

  .interest-card:hover .interest-symbol {
    transform: rotate(-8deg);
    background: #f5f2eb;
  }

  .card-content h3 {
    font-family: var(--font-heading);
    font-size: 18px;
    font-weight: 600;
    letter-spacing: -0.5px;
  }

  .card-content p {
    margin-top: 11px;
    color: #77705f;
    font-size: 12px;
    line-height: 1.8;
  }

  .card-bottom {
    margin-top: auto;
    padding-top: 25px;
    color: #9a947f;
    font-size: 8px;
    font-weight: 700;
    letter-spacing: 1px;
  }

  .bottom-decoration {
    color: #8b9875;
    font-size: 15px;
  }

  .interests-footer {
    display: grid;
    grid-template-columns: auto 1fr auto;
    align-items: center;
    gap: 20px;
    margin-top: 45px;
    padding-top: 25px;
    border-top: 1px solid #ded7c9;
  }

  .footer-decoration {
    color: #8b9875;
    font-size: 23px;
  }

  .interests-footer p {
    max-width: 560px;
    color: #77705f;
    font-family: Georgia, serif;
    font-size: 15px;
    font-style: italic;
    line-height: 1.8;
  }

  .footer-label {
    color: #8b9875;
    font-size: 9px;
    font-weight: 700;
    letter-spacing: 1.3px;
    text-align: right;
  }

  @media (max-width: 900px) {
    .interests-grid {
      grid-template-columns: repeat(2, minmax(0, 1fr));
    }

    .interest-card {
      min-height: 270px;
    }

    .interests-heading {
      gap: 35px;
    }
  }

  @media (max-width: 650px) {
    .interests-section {
      padding: 85px 0 95px;
    }

    .interests-container {
      width: calc(100% - 40px);
    }

    .interests-heading {
      grid-template-columns: 1fr;
      gap: 20px;
      margin-bottom: 40px;
    }

    .heading-intro h2 {
      font-size: 42px;
      letter-spacing: -1.8px;
    }

    .interests-heading > p {
      font-size: 13px;
    }

    .interests-grid {
      gap: 10px;
    }

    .interest-card {
      min-height: 260px;
      padding: 16px;
    }

    .interest-symbol {
      width: 45px;
      height: 45px;
      margin: 25px 0 20px;
      font-size: 23px;
    }

    .card-content h3 {
      font-size: 16px;
    }

    .card-content p {
      font-size: 11px;
    }

    .card-top span:last-child {
      font-size: 7px;
    }

    .interests-footer {
      grid-template-columns: auto 1fr;
      gap: 12px;
    }

    .footer-label {
      grid-column: 2;
      text-align: left;
    }
  }

  @media (max-width: 380px) {
    .interests-grid {
      grid-template-columns: 1fr;
    }

    .interest-card {
      min-height: 230px;
    }
  }

  @media (prefers-reduced-motion: reduce) {
    .interest-card,
    .interest-symbol {
      transition: none;
    }

    .interest-card:hover,
    .interest-card:hover .interest-symbol {
      transform: none;
    }
  }
</style>
