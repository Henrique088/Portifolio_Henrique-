
<header class="project-nav">
  <a href="/" class="brand" aria-label="Voltar ao início">
    H<span>.</span>
  </a>

  <nav aria-label="Navegação do projeto">
    <a href="#visao-geral">Visão geral</a>
    <a href="#funcionalidades">Funcionalidades</a>
    <a href="#arquitetura">Arquitetura</a>
  </nav>

  <a href="/#projetos" class="back-link">
    <span>←</span>
    Portfólio
  </a>
</header>

<style>
  .project-nav {
    height: 82px;
    display: flex;
    align-items: center;
    justify-content: space-between;
    padding: 0 max(calc((100% - 1180px) / 2), 32px);
    border-bottom: 1px solid #e5ece5;
  }

  .brand {
    font-family: 'Space Grotesk', sans-serif;
    font-size: 27px;
    font-weight: 700;
  }

  .brand span {
    color: #0abf48;
  }

  nav {
    display: flex;
    gap: 32px;
  }

  nav a,
  .back-link {
    color: #66766c;
    font-size: 12px;
    font-weight: 600;
    transition: color 0.2s;
  }

  nav a:hover,
  .back-link:hover {
    color: #0abf48;
  }

  .back-link {
    display: flex;
    align-items: center;
    gap: 8px;
  }

  .back-link span {
    font-size: 18px;
  }

  @media (max-width: 800px) {
    .project-nav {
      padding-inline: 22px;
    }

    nav {
      display: none;
    }
  }
</style>
