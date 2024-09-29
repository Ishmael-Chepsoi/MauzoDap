<script>
    let menuOpen = true;
    function toggleMenu() {
        menuOpen = !menuOpen;
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
    .shopForBest {
        position: absolute;
        height: 100%;
        width: 100%;
        top: 0%;
        left: 0%;
        line-height: 16px;
        font-weight: 500;
        display: inline-block;
    }
    .group {
        width: 68.3px;
        position: relative;
        height: 17.6px;
    }
    .frame {
        width: 119px;
        overflow: hidden;
        flex-shrink: 0;
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: flex-start;
    }
    .homeParent {
        display: flex;
        flex-direction: row;
        justify-content: space-between;
        align-items: flex-start;
        align-items: center;
        gap: 48px;
        font-size: 16px;
        color: #003459;
    }
    .homeParent a {
        text-decoration: none;
        color: #003459;
        position: relative;
        line-height: 24px; 
        position: relative;
        font-size: 16px;
        font-family: Poppins;
        color: #003459;
        text-align: left; 
    }
    .menuicon {
      display: none;  /* Hidden on larger screens */
    }
  

    .usearchParent {
        width: auto;
        border-radius: 46px;
        background-color: #fdfdfd;
        display: flex;
        flex-direction: row;
        align-items: center;
        justify-content: flex-start;
        padding: 12px 20px 12px 16px;
        box-sizing: border-box;
        gap: 12px;
        font-size: 14px;
    }

    .search {
        border-radius: none;
        border: none;
        cursor: auto;
        outline: none; 
    }

    .buttonL {
        border-radius: 57px;
        background-color: #003459;
        height: 44px;
        display: flex;
        flex-direction: row;
        align-items: center;
        justify-content: center;
        padding: 14px 28px 10px;
        box-sizing: border-box;
        color: #fdfdfd;
    }
    .frameChild {
        width: 21px;
        position: relative;
        height: 21px;
        overflow: hidden;
        flex-shrink: 0;
    }
    .vnd {
        position: relative;
        line-height: 23px;
        font-weight: 500;
    }
    .frameDiv {
        display: flex;
        flex-direction: row;
        align-items: center;
        justify-content: flex-start;
        gap: 6px;
    }
    .arrowCaretDownSm {
        width: 24px;
        position: relative;
        height: 24px;
        overflow: hidden;
        flex-shrink: 0;
    }
    .frameContainer {
        align-self: stretch;
        display: flex;
        flex-direction: row;
        align-items: center;
        justify-content: flex-end;
        padding: 10px 8px 8px;
        gap: 4px;
        color: #002a48;
    }
    .frameGroup {
        display: flex;
        flex-direction: row;
        align-items: flex-start;
        justify-content: flex-start;
        gap: 14px;
        font-size: 16px;
        color: #99a2a5;
    }
    .headerDesktop {
        width: 100%;
        position: absolute; /* Overlay the header on top of the banner */
        top: 0; /* Position the header at the top of the page */
        left: 0;
        /* position: relative; */
        display: flex;
        flex-direction: row;
        align-items: center;
        justify-content: space-between;
        padding: 28px 113px;
        box-sizing: border-box;
        text-align: left;
        font-size: 10px;
        color: #103559;
        font-family: Poppins;
        z-index: 10; /* Ensure the header appears above the banner */
        background-color: transparent; /* Make the header background transparent */
    }

    nav:open {
        display: block;
        position: absolute;
        top: 100%;
        left: 0;
        width: 100%;
    }
    .menuicon {
        display: none;
    }
    
    @media (max-width: 768px) {
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
    }


    </style>

    <div class="headerDesktop">
        <button class="menuicon" on:click={toggleMenu}>
            <!-- lan horizontal line -->
                <div class="bar-1" />
                <div class="bar-2" />
                <div class="bar-3" />
        </button>
        <div class="frame">
            <img class="imageIcon " src="/Logo.png" alt="Logo" />
            <div class="group">
                <div class="shopForBest">Shop for Best</div>
            </div>
    </div>
        <nav class:open={menuOpen}>
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
        <b>Join </b>
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
    