<script>
    let menuOpen = false;  // Initialize as false to hide the menu initially
    function toggleMenu() {
      menuOpen = !menuOpen;  // Toggle menu open/close
    }
  </script>
  
  <style>
    .imageIcon {
      align-self: stretch;
      position: relative;
      max-width: 100%;
      overflow: hidden;
      height: 28px;
      flex-shrink: 0;
      object-fit: cover;
    }
  
    .homeParent {
      display: flex;
      flex-direction: row;
      justify-content: space-between;
      align-items: flex-start;
      gap: 48px;
      font-size: 16px;
      color: #003459;
    }
  
    .homeParent a {
      text-decoration: none;
      color: #003459;
      font-size: 16px;
      font-family: Poppins;
      text-align: left;
    }
  
    .menuicon {
      display: none;  /* Hidden on larger screens */
    }
  
  
    .menuicon {
      height: 32px;
      aspect-ratio: 1;
      border: 2px solid var(--light);
      background-color: transparent;
      border-radius: 5px;
      display: flex;
      align-items: center;
      justify-content: center;
      cursor: pointer;
    }
  
    .menuicon > div {
      height: 2px;
      border-radius: 1px;
      width: 14px;
      background-color: #003459;
      position: absolute;
    }
  
    .bar-1 {
      transform: translateY(-5px);
    }
  
    .bar-3 {
      transform: translateY(5px);
    }
  
    /* Hide the menu by default on smaller screens */
    .homeParent {
      display: none;
    }
  
    /* Show menu when open */
    nav.open .homeParent {
      display: flex;
      flex-direction: column;
      position: absolute;
      top: 60px;
      left: 0;
      width: 100%;
      background-color: #fff;
      padding: 10px 0;
      gap: 10px;
    }
  
    @media (max-width: 768px) {
      .menuicon {
        display: flex;
      }
    }
  </style>
  
  <div class="headerDesktop">
    <button class="menuicon" on:click={toggleMenu}>
      <div class="bar-1"></div>
      <div class="bar-2"></div>
      <div class="bar-3"></div>
    </button>
  
    <div class="frame">
      <img class="imageIcon" src="/Logo.png" alt="Logo" />
      <div class="group">
        <div class="shopForBest">Shop for Best</div>
      </div>
    </div>
  
    <nav class={menuOpen ? 'open' : ''}>
      <div class="homeParent">
        <a href="/">Home</a>
        <a href="/category">Category</a>
        <a href="/about">About</a>
        <a href="/contact">Contact</a>
      </div>
    </nav>
  
    <div class="frameGroup">
      <div class="usearchParent">
        <input class="search" placeholder="Search something here!" />
        <img src="/icons/u-search.svg" alt="Search" />
      </div>
      <div class="buttonL">
        <b>Join</b>
      </div>
      <div class="frameContainer">
        <div class="frameDiv">
          <img class="frameChild" alt="" src="images/frame.svg" />
          <div class="vnd">VND</div>
        </div>
        <img class="arrowCaretDownSm" alt="" src="icons/arrow-caret-down-sm.svg" />
      </div>
    </div>
  </div>
  