<section class="hero">

  <div
    class="hero-bg"
    style="background-image: url('/images/gita_banner.png');"
    aria-hidden="true"
  >
    <div class="overlay-top"></div>
    <div class="overlay-gray"></div>
  </div>

 
  <div class="hero-overlay">
    <h1>BHAGAVAD GITA</h1>
  </div>


  <div class="hero-book">
    <img src="/images/gita_open.png" alt="Bhagavad Gita book" />
  </div>
</section>

<style>
  .hero {
    position: relative;
    /* overflow: hidden; */
  }


  .hero-bg {
    position: relative;       
    height: 500px;
    background-size: cover;
    background-position: center top;
    transform: scale(1.03);
  }


  .overlay-gray {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;                 
    height: 140px;               
    background: rgba(255, 255, 255, 0.658);  
    z-index: 1;
  }


  .hero-overlay {
    position: absolute;
    inset: 0;
    display: flex;
    justify-content: center;
    align-items: flex-start;
    padding-top: 20px;
    z-index: 2;   
                 
  }
  .overlay-top{
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;                 
    height: 60px;              
    background: rgba(226, 226, 226, 0.925);  
    z-index: 1;
  }

  .hero-overlay h1 {
    margin: 0;
    margin-top: -20px;
    font-family: edensor, "Noto Sans Devanagari";
    font-size: 100px ; 
    font-weight: 100;
    color: #3c4f3a;
    text-shadow:
      0 4px 7px rgba(0, 0, 0, 0.55),
      0 0 3px rgba(0, 0, 0, 0.35);
  }

.hero-book {
  position: absolute;
  left: 50%;
  bottom: -104px;
  transform: translateX(-50%);
  width: 220px;
  z-index: 5;   
}


  .hero-book img {
   width: 100%;
  height: auto;
  display: block;
  }

  @media (max-width: 900px) {
    .hero-bg {
      height: 260px;
    }

    .overlay-gray {
      height: 90px;
    }

    .hero-overlay {
      padding-top: 48px;
    }

    .hero-overlay h1 {
      font-size: 10px;
      letter-spacing: 0.24em;
    }

    .hero-book {
      width: 135px;
      bottom: -50px;
    }
  }

  @media (max-width: 600px) {
    .hero-bg {
      height: 230px;
    }

    .overlay-gray {
      height: 75px;
    }

    .hero-overlay {
      padding-top: 40px;
    }

    .hero-overlay h1 {
      font-size: 2.1rem;
      letter-spacing: 0.2em;
    }

    .hero-book {
      width: 120px;
      bottom: -44px;
    }
  }
</style>
