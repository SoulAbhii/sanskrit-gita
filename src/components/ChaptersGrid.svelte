<script>
  const chapters = Array.from({ length: 18 }, (_, i) => i + 1);
</script>

<section class="chapter_main">
  <div class="chapter_head">
    <p>GITA CHAPTERS</p>
  </div>

  <div class="chapter_container">
    {#each chapters as n}
      <a class="chapter" href="#" aria-label={`Open chapter ${n}`}>
        <div class="chapter_img">
          <img src="/images/gita_book.jpg" alt="Chapter Background" />
        </div>
        <div class="chapter_num">
          <span>{n}</span>
        </div>
      </a>
    {/each}
  </div>
</section>
<style>

.chapter_main {
  padding: 5.5rem 1.5rem 4.5rem;
}

.chapter_head {
  text-align: center;
  margin-bottom: 3rem;
}

.chapter_head p {
  margin: 0 0 0.6rem;
  font-family: "Cinzel", serif;
  font-size: 14px;
  letter-spacing: 0.28em;
  text-transform: uppercase;
  color: #6b362f;
  position: relative;
}

.chapter_head p::after {
  content: "";
  display: block;
  width: 140px;
  height: 2px;
  background: #c2253b;
  margin: 0.4rem auto 0;
}

.chapter_container {
  width: 100%;
  max-width: 1180px;
  margin-left: 150px ;
  display: grid;
  grid-template-columns: repeat(7, 1fr);
  justify-items:flex-start;
  row-gap: 4.5rem;
  column-gap: 4.5rem;
}


.chapter {
  position: relative;
  width: 140px;
  height: 140px;
  transform: rotate(45deg);
  border-radius: 18px;
  overflow: hidden;
  border: 1px solid #666;
  box-shadow: 0 14px 22px rgba(0, 0, 0, 0.25);
  background: #d7d0c0;
  text-decoration: none;
}

.chapter_img,
.chapter_num {
  position: absolute;
  inset: 0;
  transform: rotate(-45deg);
}


.chapter_img img {
  width: 170%;
  height: 170%;
  object-fit: cover;
  position: absolute;
  top: -15%;
  left: -5%;
}

.chapter_num {
  display: flex;
  align-items: center;
  justify-content: center;
}

.chapter_num::before {
  content: "";
  position: absolute;
  left: -40%;
  right: -40%;
  top: 50%;
  transform: translateY(-50%);
  height: 40%;
  background: rgba(0, 0, 0, 0.45);
}

.chapter_num span {
  position: relative;
  color: #ffffff;
  font-size: 26px;
  font-weight: 600;
}


@media (max-width: 1200px) {
  .chapter_container {
    grid-template-columns: repeat(6, 1fr);
    row-gap: 6rem;

  }
}

@media (max-width: 992px) {
  .chapter_container {
    grid-template-columns: repeat(4, 1fr);
    row-gap: 4.5rem;
    column-gap: 2rem;
  }

  .chapter {
    width: 135px;
    height: 135px;
  }

  .chapter_num span {
    font-size: 22px;
  }
}

@media (max-width: 768px) {
  .chapter_container {
    grid-template-columns: repeat(3, 1fr);
    row-gap: 3.5rem;
    column-gap: 1.8rem;
    margin: 0 auto;
  }

  .chapter {
    width: 118px;
    height: 118px;
  }
}

@media (max-width: 520px) {
  .chapter_container {
    grid-template-columns: repeat(2, 1fr);
    row-gap: 3rem;
    column-gap: 1.4rem;
    margin: 0 auto;
   
  }

  .chapter {
    width: 110px;
    height: 110px;
  }

  .chapter_num span {
    font-size: 20px;
  }
}

@media (max-width: 380px) {
  .chapter {
    width: 98px;
    height: 98px;
  }

  .chapter_num span {
    font-size: 18px;
  }
}

</style>