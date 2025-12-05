<script>
  export let logoSrc = '/images/logo.png';

  let mobileOpen = false;
  const toggleMobile = () => {
    mobileOpen = !mobileOpen;
    document.documentElement.style.overflow = mobileOpen ? 'hidden' : '';
  };

  const closeMobile = () => {
    mobileOpen = false;
    document.documentElement.style.overflow = '';
  };


  const onKey = (e) => {
    if (e.key === 'Escape' && mobileOpen) closeMobile();
  };


  import { onMount, onDestroy } from 'svelte';
  onMount(() => window.addEventListener('keydown', onKey));
  onDestroy(() => window.removeEventListener('keydown', onKey));
</script>

<header class="nav-wrapper" role="banner">
  <div class="nav-inner">
    
    <div class="nav-left">
      <a href="/" class="logo-link" aria-label="Homepage">
        <img src={logoSrc} alt="Wellbeing-Svasti logo" class="logo" />
      </a>
    </div>

    
    <div class="nav-right">
    
      <button class="search-btn" aria-label="Search" title="Search">
        <span class="search-icon" aria-hidden="true"></span>
      </button>

      
      <nav class="nav-links" aria-label="Primary">
        <a href="#">ĀYURVEDA <img src="/images/nav-arrow.png" class="caret-icon" alt="" /></a>
        <a href="#">YOGASŪTRAS <img src="/images/nav-arrow.png" class="caret-icon" alt="" /></a>
        <a href="#" class="active">BHAGAVAD GĪTĀ</a>
        <a href="#">UPANIṢADS <img src="/images/nav-arrow.png" class="caret-icon" alt="" /></a>
        <a href="#">SANSKRIT <img src="/images/nav-arrow.png" class="caret-icon" alt="" /></a>
        <a href="#">CONTACT US</a>
      </nav>

      
      <button
        class="burger-btn"
        aria-label={mobileOpen ? "Close menu" : "Open menu"}
        aria-expanded={mobileOpen}
        on:click={toggleMobile}
      >
        <span class="burger" aria-hidden="true"></span>
      </button>
    </div>
  </div>

  {#if mobileOpen}
    <div class="mobile-overlay" role="dialog" aria-modal="true" aria-label="Mobile menu">
      <div class="mobile-panel">
        <button class="mobile-close" aria-label="Close menu" on:click={closeMobile}>✕</button>

        <nav class="mobile-nav" aria-label="Mobile primary">
          <a href="#" on:click={closeMobile}>ĀYURVEDA</a>
          <a href="#" on:click={closeMobile}>YOGASŪTRAS</a>
          <a href="#" class="active" on:click={closeMobile}>BHAGAVAD GĪTĀ</a>
          <a href="#" on:click={closeMobile}>UPANIṢADS</a>
          <a href="#" on:click={closeMobile}>SANSKRIT</a>
          <a href="#" on:click={closeMobile}>CONTACT US</a>
        </nav>
      </div>
    </div>
  {/if}
</header>

<style>
  :root {
    --container-w: 1180px;
    --accent: #7a9a69;
  }

  .nav-wrapper {
    background: #fff;
    position: sticky;
    top: 0;
    z-index: 100;
    box-shadow: 0 1px 0 rgba(0,0,0,0.06);
  
  }

  .nav-inner {
    width: 100%;
    max-width: var(--container-w);
    margin: 0 auto;
    display: flex;
    align-items: center;
    justify-content: space-between; 
    padding: 18px 20px;
    box-sizing: border-box;
    gap: 12px;
  }

  .logo {
    height: 56px;
    width: auto;
    object-fit: contain;
    display: block;
  }

  .nav-right {
    display: flex;
    align-items: center;
    gap: 18px;
    margin-left: auto;
  }


  .search-btn {
    border: none;
    background: none;
    padding: 6px;
    display: inline-flex;
    align-items: center;
    justify-content: center;
    cursor: pointer;
  }
  .search-icon {
    width: 18px;
    height: 18px;
    border: 2px solid #111;
    border-radius: 50%;
    position: relative;
    box-sizing: border-box;
    display: inline-block;
  }
  .search-icon::after {
    content: "";
    position: absolute;
    width: 8px;
    height: 2px;
    background: #111;
    right: -7px;
    bottom: -1px;
    transform: rotate(45deg);
    border-radius: 2px;
  }

  
  .nav-links {
    display: flex;
    align-items: center;

    gap: 26px;
    font-family: "Cinzel", serif;
    font-size: 14px;
    letter-spacing: 0.22em;
    text-transform: uppercase;
    font-weight: 500;
  }
  .nav-links a {
    color: #000;
    text-decoration: none;
    display: inline-flex;
    align-items: center;
    gap: 6px;
    white-space: nowrap;
  }
  .nav-links a.active {
    color: var(--accent);
  }
  .nav-links a:hover { color: #b51f3b; }
  .caret-icon { width: 10px; height: auto; opacity: .85; transform: translateY(1px); }

  
  .burger-btn {
    display: none;
    border: none;
    background: none;
    padding: 6px;
    cursor: pointer;
  }
  .burger {
    width: 22px;
    height: 2px;
    background: #111;
    position: relative;
    display: block;
  }
  .burger::before, .burger::after {
    content: "";
    position: absolute;
    left: 0;
    right: 0;
    height: 2px;
    background: #111;
  }
  .burger::before { top: -6px; }
  .burger::after { top: 6px; }


  @media (max-width: 1024px) {
    .nav-links { display: none; }
    .search-btn { display: none; }
    .burger-btn { display: inline-flex; margin-left: 12px; }
    .logo { height: 48px; }
    .nav-inner { padding: 12px 14px; }
  }

  .mobile-overlay {
    position: fixed;
    inset: 0;
    background: rgba(0,0,0,0.35);
    z-index: 110;
    display: flex;
    justify-content: flex-end;
  }
  .mobile-panel {
    width: min(320px, 90vw);
    background: #fff;
    padding: 18px;
    box-shadow: -8px 0 30px rgba(0,0,0,0.2);
    display: flex;
    flex-direction: column;
    gap: 12px;
    position: relative;
  }
  .mobile-close {
    background: none;
    border: none;
    font-size: 20px;
    align-self: flex-end;
    cursor: pointer;
  }
  .mobile-nav {
    display: flex;
    flex-direction: column;
    gap: 8px;
    margin-top: 4px;
  }
  .mobile-nav a {
    text-decoration: none;
    color: #222;
    font-size: 18px;
    padding: 8px 6px;
  }
  .mobile-nav a.active { color: var(--accent); font-weight: 600; }

  
  .search-btn:focus, .burger-btn:focus, .nav-links a:focus, .mobile-nav a:focus {
    outline: 3px solid rgba(122,154,105,0.12);
    outline-offset: 2px;
  }
</style>
