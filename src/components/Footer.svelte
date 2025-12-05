<script>
  
  const logoSrc = "/images/android-chrome-192x192.png";
  const footerBg = "/images/footerimg.png";

  const socials = [
    {
      name: "facebook",
      href: "#",
      svg: `
        <svg width="16" height="16" fill="currentColor" viewBox="0 0 320 512">
          <path d="M279.14 288l14.22-92.66h-88.91V129.33c0-25.35 
          12.42-50.06 52.24-50.06H295V6.26S259.61 0 
          225.36 0C141.09 0 89.09 54.42 
          89.09 154.33V195.3H0v92.66h89.09V512h107.82V288z"/>
        </svg>
      `
    },
    {
      name: "twitter",
      href: "#",
      svg: `
        <svg width="16" height="16" fill="currentColor" viewBox="0 0 512 512">
          <path d="M459.37 151.716c.325 
          4.548.325 9.097.325 13.645 0 
          138.72-105.583 298.558-298.558 
          298.558-59.452 0-114.68-17.219-161.137-47.106 
          8.447.974 16.568 1.299 25.34 1.299 
          49.055 0 94.213-16.568 130.274-44.832 
          -46.132-.975-84.792-31.188-98.112-72.772 
          6.498.974 12.995 1.624 19.818 1.624 
          9.421 0 18.843-1.3 27.614-3.573 
          -48.081-9.747-84.143-51.98-84.143-103.001 
          0-.486 0-.972.162-1.458 
          14.182 7.83 30.355 12.67 47.431 13.319 
          -28.264-18.843-46.781-51.005-46.781-87.391 
          0-19.492 5.197-37.36 14.507-52.954 
          52.954 64.3 132.3 106.496 221.153 111.103 
          -1.624-7.83-2.599-15.984-2.599-24.138 
          0-57.828 46.782-104.934 104.934-104.934 
          30.355 0 57.502 12.67 76.67 33.137 
          24.138-4.548 46.456-13.645 66.599-25.66 
          -7.83 24.461-24.461 44.833-46.132 57.827 
          21.411-2.273 41.783-8.122 60.665-16.243 
          -14.182 21.084-32.161 39.763-52.628 54.89z"/>
        </svg>
      `
    },
    {
      name: "youtube",
      href: "#",
      svg: `
        <svg width="16" height="16" fill="currentColor" viewBox="0 0 576 512">
          <path d="M549.655 124.083c-6.281-23.65-24.787-42.276-48.284-48.597C458.781 
          64 288 64 288 64S117.22 64 74.629 75.486c-23.497 
          6.321-42.003 24.947-48.284 
          48.597C15.999 167.539 16 256.002 16 256.002s0 
          88.465 10.345 131.919c6.281 23.65 24.787 42.276 
          48.284 48.597C117.22 448 288 448 288 
          448s170.78 0 213.371-11.486c23.497-6.321 
          42.003-24.947 48.284-48.597C560 344.468 560 
          256.002 560 256.002s.001-88.463-10.345-131.919zM232 
          336V176l142.857 80L232 336z"/>
        </svg>
      `
    },
    {
      name: "website",
      href: "#",
      svg: `
        <svg width="16" height="16" fill="currentColor" viewBox="0 0 512 512">
          <path d="M256 48C141.13 48 48 141.13 48 
          256s93.13 208 208 208 208-93.13 
          208-208S370.87 48 256 48zm0 
          64c25.9 0 70.6 38.7 89.6 
          96H166.4c19-57.3 63.7-96 89.6-96zm-128 
          144c0-11 .7-21.7 2-32h156v64H130c-1.3-10.3-2-21-2-32zm128 
          160c-25.9 0-70.6-38.7-89.6-96h179.2c-19 
          57.3-63.7 96-89.6 96zm106-128h-106v-64h106c1.3 
          10.3 2 21 2 32s-.7 21.7-2 32z"/>
        </svg>
      `
    }
  ];
</script>

<footer class="site-footer">
  <div class="footer-inner">
    <div class="connect-row">
      <div class="connect-text">Connect</div>

      <div class="socials">
        {#each socials as s}
          <a class="social-btn" href={s.href} aria-label={s.name}>
            {@html s.svg}
          </a>
        {/each}
      </div>
    </div>

    <div class="logo-wrap">
      <img src={logoSrc} alt="Well Being Svasti logo" class="footer-logo" />
    </div>

    <h3 class="brand-name">WELLBEING~SVASTI</h3>

    <div class="copyright-row">
      <div>© 2025 Rutger Kortenhorst. All Rights Reserved | Design and Developed by</div>
      <a class="credit-link" href="#" target="_blank">Burning Desire Inclusive</a>
    </div>
  </div>
</footer>

<style>

.site-footer {
  background-image: url("/images/footerimg.png");
  background-size: cover;
  background-position: center;
  padding: 48px 16px 56px;
  color: #dfe8de;
  text-align: center;
}

.footer-inner {
  max-width: 1180px;
  margin: 0 auto;
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 14px;
}


.connect-row {
  display: flex;
  justify-content: center;
  align-items: center;
  gap: 14px;
  flex-wrap: wrap; 
  width: 100%;
}

.connect-text {
  font-family: "Cinzel", serif;
  letter-spacing: 0.2em;
  font-size: 18px;
  color: #e6e0c8;
}


.socials {
  display: flex;
  gap: 10px;
  flex-wrap: wrap; 
}

.social-btn {
  display: flex;
  justify-content: center;
  align-items: center;
  width: 34px;
  height: 34px;
  border-radius: 50%;
  background: rgba(255,255,255,0.07);
  border: 1px solid rgba(255,255,255,0.15);
  color: #ffffff;
  transition: 0.25s ease;
}

.social-btn:hover {
  background: rgba(100, 240, 7, 0.945);
}


.logo-wrap {
  width: 100%;
  display: flex;
  justify-content: center;
}

.footer-logo {
  width: 90px;
  height: 90px;
  margin: 10px auto;
  display: block;
  filter: drop-shadow(0px 2px 4px rgba(0,0,0,0.4));
}


.brand-name {
  font-family: "Cinzel", serif;
  font-size: 32px;
  letter-spacing: 0.15em;
  color: #b8ad86;
  margin-top: 4px;
}

.credit-link {
  color: #90c7b6;
  text-decoration: none;
}

.credit-link:hover {
  text-decoration: underline;
}



@media (max-width: 768px) {
  .brand-name {
    font-size: 26px;
    letter-spacing: 0.12em;
  }

  .footer-logo {
    width: 75px;
    height: 75px;
  }

  .connect-text {
    font-size: 16px;
    letter-spacing: 0.18em;
  }
}

@media (max-width: 520px) {
  .connect-row {
    flex-direction: column; 
    gap: 10px;
  }

  .socials {
    justify-content: center;
  }

  .footer-logo {
    width: 68px;
    height: 68px;
  }

  .brand-name {
    font-size: 22px;
  }

  .credit-link {
    font-size: 13px;
    display: block;
    margin-top: 4px;
  }
}

@media (max-width: 380px) {
  .brand-name {
    font-size: 20px;
  }

  .footer-logo {
    width: 60px;
    height: 60px;
  }
}


</style>
