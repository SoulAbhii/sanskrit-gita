<script>
  const scrollTop = () => {
    window.scrollTo({ top: 0, behavior: "smooth" });
  };
</script>

<button class="scroll-top" on:click={scrollTop} aria-label="Scroll to top">
  <span class="arrow">⌃</span>
</button>

<style>
  .scroll-top {
    position: fixed;
    right: 1.5rem;
    bottom: 1.5rem;
    width: 48px;
    height: 48px;
    border-radius: 12px;
    background: #111;
    color: #fff;
    font-size: 1.4rem;

    display: flex;
    align-items: center;
    justify-content: center;

    cursor: pointer;
    z-index: 50;

    transition: background 0.25s ease, transform 0.25s ease;
  }


  .arrow {
    display: inline-block;
    transition: transform 0.25s ease;
  }


  .scroll-top:hover {
    background: #222;
  }

 
  .scroll-top:hover .arrow {
    transform: translateY(-6px);   }  
</style>
