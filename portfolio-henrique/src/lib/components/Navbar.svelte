
<script lang="ts">
  let menuOpen = $state(false);

  const closeMenu = () => {
    menuOpen = false;
  };

  import { reveal } from '#lib/actions/reveal.ts';
</script>

<header class="navbar" use:reveal>
  <div class="container navbar-content">
    <a href="#inicio" class="logo" onclick={closeMenu}>
      HENRIQUE<span>.</span>
    </a>

    <button
      class="menu-toggle"
      aria-label={menuOpen ? 'Fechar menu' : 'Abrir menu'}
      aria-expanded={menuOpen}
      onclick={() => (menuOpen = !menuOpen)}
    >
      {menuOpen ? '✕' : '☰'}
    </button>

    <nav class:open={menuOpen}>
      <a href="#inicio" onclick={closeMenu}>Início</a>
      <a href="#sobre" onclick={closeMenu}>Sobre</a>
      <a href="/sobre">Sobre mim</a>
      <a href="#projetos" onclick={closeMenu}>Projetos</a>
      <a href="#contato" class="contact-link" onclick={closeMenu}>
        Vamos conversar <span>↗</span>
      </a>
    </nav>
  </div>
</header>

<style>
  .navbar {
    position: relative;
    z-index: 10;
    border-bottom: 1px solid var(--color-border);
  }

  .navbar-content {
    height: 84px;
    display: flex;
    align-items: center;
    justify-content: space-between;
  }

  .logo {
    font-family: var(--font-heading);
    font-size: 21px;
    font-weight: 700;
    letter-spacing: -1px;
  }

  .logo span {
    color: var(--color-primary);
  }

  nav {
    display: flex;
    align-items: center;
    gap: 36px;
  }

  nav a {
    color: var(--color-muted);
    font-size: 14px;
    transition: color 0.2s ease;
  }

  nav a:hover {
    color: var(--color-primary);
  }

  nav .contact-link {
    color: var(--color-text);
    border: 1px solid var(--color-border);
    padding: 12px 18px;
    border-radius: 6px;
  }

  .contact-link span {
    color: var(--color-primary);
    margin-left: 8px;
  }

  .menu-toggle {
    display: none;
    border: 0;
    background: transparent;
    color: var(--color-text);
    font-size: 25px;
  }

  @media (max-width: 700px) {
    .navbar-content {
      height: 72px;
    }

    .menu-toggle {
      display: block;
    }

    nav {
      display: none;
      position: absolute;
      top: 72px;
      left: 0;
      width: 100%;
      padding: 24px;
      background: var(--color-background);
      border-bottom: 1px solid var(--color-border);
      flex-direction: column;
      align-items: stretch;
      gap: 22px;
    }

    nav.open {
      display: flex;
    }

    nav .contact-link {
      text-align: center;
    }
  }
</style>
