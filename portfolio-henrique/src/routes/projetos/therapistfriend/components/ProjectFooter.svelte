<script lang="ts">
  import { reveal } from '#lib/actions/reveal.ts';

</script>

<footer class="project-footer" use:reveal>
  <div class="footer-container">
    <div class="footer-content">
      <span class="footer-label">FIM DO PROJETO</span>

      <h2>
        Vamos construir
        <span>algo interessante?</span>
      </h2>

      <p>
        O TherapistFriend representa a integração entre desenvolvimento
        web, arquitetura de software e inteligência artificial em uma
        plataforma voltada à conexão entre pessoas.
      </p>

      <div class="footer-actions">
        <a href="/#contato" class="contact-link">
          Vamos conversar
          <span>↗</span>
        </a>

        <a href="/#projetos" class="projects-link">
          Conhecer outros projetos
          <span>→</span>
        </a>
      </div>
    </div>

    <div class="footer-bottom">
      <a href="/" class="footer-brand" aria-label="Voltar ao portfólio">
        H<span>.</span>
      </a>

      <span>Desenvolvido por Henrique</span>

      <a href="#visao-geral" class="back-to-top">
        Voltar ao início ↑
      </a>
    </div>
  </div>
</footer>

<style>
  .project-footer {
    padding: 100px 0 30px;
    background: #f7faf6;
  }

  .footer-container {
    width: min(1180px, calc(100% - 64px));
    margin: 0 auto;
  }

  .footer-content {
    padding: 70px;
    border-radius: 20px;
    background: #e0ffe0;
  }

  .footer-label {
    color: #0abf48;
    font-size: 10px;
    font-weight: 700;
    letter-spacing: 2px;
  }

  .footer-content h2 {
    max-width: 650px;
    margin-top: 22px;
    color: #17251e;
    font-family: 'Space Grotesk', sans-serif;
    font-size: clamp(38px, 5vw, 60px);
    line-height: 1.1;
    letter-spacing: -2px;
  }

  .footer-content h2 span {
    display: block;
    color: #0abf48;
  }

  .footer-content p {
    max-width: 570px;
    margin-top: 22px;
    color: #66766c;
    font-size: 14px;
    line-height: 1.9;
  }

  .footer-actions {
    display: flex;
    flex-wrap: wrap;
    align-items: center;
    gap: 28px;
    margin-top: 34px;
  }

  .contact-link {
    display: inline-flex;
    align-items: center;
    gap: 18px;
    padding: 15px 20px;
    border-radius: 8px;
    background: #17251e;
    color: #f7faf6;
    font-size: 13px;
    font-weight: 700;
    transition:
      background 0.2s ease,
      transform 0.2s ease;
  }

  .contact-link:hover {
    transform: translateY(-2px);
    background: #263d2e;
  }

  .contact-link span {
    color: #0fd850;
    font-size: 17px;
  }

  .projects-link {
    display: inline-flex;
    align-items: center;
    gap: 10px;
    color: #526257;
    font-size: 13px;
    font-weight: 700;
    transition: color 0.2s ease;
  }

  .projects-link:hover {
    color: #0abf48;
  }

  .projects-link span {
    font-size: 17px;
  }

  .footer-bottom {
    display: flex;
    align-items: center;
    justify-content: space-between;
    gap: 20px;
    padding-top: 28px;
  }

  .footer-brand {
    color: #17251e;
    font-family: 'Space Grotesk', sans-serif;
    font-size: 25px;
    font-weight: 700;
  }

  .footer-brand span {
    color: #0abf48;
  }

  .footer-bottom > span,
  .back-to-top {
    color: #849389;
    font-size: 11px;
    font-weight: 500;
  }

  .back-to-top {
    transition: color 0.2s ease;
  }

  .back-to-top:hover {
    color: #0abf48;
  }

  @media (max-width: 600px) {
    .project-footer {
      padding: 70px 0 24px;
    }

    .footer-container {
      width: calc(100% - 40px);
    }

    .footer-content {
      padding: 35px 25px;
      border-radius: 14px;
    }

    .footer-content h2 {
      letter-spacing: -1.5px;
    }

    .footer-actions {
      align-items: flex-start;
      flex-direction: column;
      gap: 22px;
    }

    .footer-bottom {
      flex-wrap: wrap;
    }

    .footer-bottom > span {
      order: 3;
      width: 100%;
    }
  }
</style>