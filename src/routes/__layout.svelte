<script>
  import NavTop from "../components/NavTop.svelte";
  import Footer from "../components/Footer.svelte";
  import { page } from "$app/stores";
</script>

<div class="nav">
  {#if $page.url.pathname != "/"}
  <NavTop />

  <nav>
    <div class="options">
      <ul>
        <a class:selected={$page.url.pathname === "/"} href="/">
          <li>
            <i class="fas fa-home" /> Home
          </li>
        </a>

        <a
          class:selected={$page.url.pathname === "/resturant"}
          href="/resturant"
        >
          <li>
            <i class="fas fa-utensils" /> Resturant
          </li>
        </a>

        <a
          class:selected={$page.url.pathname === "/grocery"}
          href="/grocery"
        >
          <li>
            <i class="fas fa-shopping-cart" /> Grocery
          </li>
        </a>

        <a
          class:selected={$page.url.pathname === "/healthcare"}
          href="/healthcare"
        >
          <li>
            <i class="fas fa-clinic-medical" /> Healthcare
          </li>
        </a>

        <a class:selected={$page.url.pathname === "/services"} href="/services">
          <li>
            <i class="fas fa-cog" /> Others
          </li>
        </a>
      </ul>
    </div>
  </nav>
  {/if}
  

  
</div>

<slot />


<Footer />

<style lang="scss">
  :global(body) {
    min-width: 1300px;
    background-color: rgb(255, 255, 255);
    padding: 0;
    margin: 0;
    box-sizing: border-box;
    min-height: 80vh;
  }

  :global(h1, h2, h3, h4, h5, h6) {
    font-family: "Roboto";
    padding: 0;
    margin: 0;
  }

  :global(p) {
    font-family: "Roboto";
    padding: 0;
    margin: 0;
  }
  :global(a) {
    font-family: "Roboto";
    padding: 0;
    margin: 0;
  }

  :global(main) {
    width: 80%;
    margin: auto;
  }

  nav {
   padding-top: 3vh;
    width: 100%;
    background-color: #2e108e;

    .options {
      width: 100%;

      ul {
        width: 90%;
        display: grid;
        grid-template-columns: repeat(5, 1fr);
        list-style: none;
        margin: auto;

        * {
          color: #ffffff;
          transition: color 0.3s;
        }

        a {
          text-decoration: none;
        }

        .active,
        .selected {
          li {
            border-top: 5px #ff4f04 solid;
            color: #ff4f04;
            cursor: pointer;

            i {
              color: #ff4f04;
              
            }
          }
        }

  
        li {
          width: 80%;
          text-align: center;
          padding: 15px 0;
          border-top: 5px solid #fff;
          font-family: "Roboto", sans-serif;
          font-weight: bolder;

      
            font-size: 24px;
          

          &:hover {
            border-top: 5px #ff4f04 solid;
            color: #ff4f04;
            cursor: pointer;

            i {
              color: #ff4f04;
              
            }
          }
        }
      }
    }
  }
</style>
