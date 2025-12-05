<script>
  import Navbar from './components/Navbar.svelte';
  import Hero from './components/Hero.svelte';
  import ChaptersGrid from './components/ChaptersGrid.svelte';
  import Footer from './components/Footer.svelte';
  import ScrollTopButton from './components/ScrollTopButton.svelte';

  const handleChapterSelect = (chapter) => {
    
    console.log('Go to chapter', chapter);
  };
</script>

<div class="page">
  <Navbar logoSrc="/images/logo.png" />

  <main>
    <Hero
      backgroundSrc="/images/gita-hero.jpg"
      bookSrc="/images/book.png"
    />

    <ChaptersGrid
      chapterImage="/images/chapter-card.jpg"
      onSelect={handleChapterSelect}
    />
  </main>

  <Footer logoSrc="/images/logo.png" />
  <ScrollTopButton />
</div>

<style>
  .page {
    min-height: 100vh;
  }

  main {
    /* margin-top: 40px; space under hero book overlap */
  }

  @media (max-width: 768px) {
    main {
      margin-top: 30px;
    }
  }
</style>
