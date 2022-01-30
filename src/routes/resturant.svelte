<script>
  import { each } from "svelte/internal";
  import Card from "../pageComponents/card.svelte";
import AdBannner from "../pageComponents/AdBannner.svelte";

  let data = [
    {
      name: "Burger Bay",
      description:
        "Lorem ipsum dolor sit amet consectetur, adipisicing elit. Necessitatibus similique fugiat, esse temporibus laudantium molestiae minus ex consectetur delectus debitis possimus iure, quasi vero dolores sunt aliquid dolorem! Quae, soluta!",
      location: "Madmbakkam",
      image:
        "https://external-content.duckduckgo.com/iu/?u=https%3A%2F%2Fwagoodfoodguide.com%2Fwp-content%2Fuploads%2F2020%2F12%2Fburger3.jpg&f=1&nofb=1",

      phone: "1234567899",

      email: "test@123.com",
      website: "https://d3box.com",

      social : [
        [
          {company : "vimeo",
          url: "http://d3box.in",
          icon: "fab fa-vimeo-v",
          color: "#2bb3e7"
        },

          {company : "facebook",
          url: "http://d3box.in",
          icon: "fab fa-facebook",
          color: "#4267B2"
        },

          {company : "instagram",
          url: "http://d3box.in",
          icon: "fab fa-instagram",
          color: "#e3224a"
        },

          {company : "twitter",
          url: "http://d3box.in",
          icon: "fab fa-twitter",
          color: "#00a6e5"
        }
      ]
      ],

      offers: [[
        {
          offer : "10% off on biriyanis",
          code: "biryani10off"
  
        }
      ]]
    },
    {
      name: "Bay Burger",
      description:
        "Lorem ipsum dolor sit amet consectetur, adipisicing elit. Necessitatibus similique fugiat, esse temporibus laudantium molestiae minus ex consectetur delectus debitis possimus iure, quasi vero dolores sunt aliquid dolorem! Quae, soluta!",
      location: "Tambaram",
      image:
        "https://media-cldnry.s-nbcnews.com/image/upload/newscms/2019_21/2870431/190524-classic-american-cheeseburger-ew-207p.jpg",
        phone: "1234567899",

      email: "test@123.com"
    },
    {
      name: "Italia Pizza",
      description:
        "Lorem ipsum dolor sit amet consectetur, adipisicing elit. Necessitatibus similique fugiat, esse temporibus laudantium molestiae minus ex consectetur delectus debitis possimus iure, quasi vero dolores sunt aliquid dolorem! Quae, soluta!",
      location: "Madambakkam",
      image:
        "https://img.onmanorama.com/content/dam/mm/en/food/features/images/2021/10/17/pizza.jpg",
        phone: "1234567899",

      email: "test@123.com"
    },
    {
      name: "FD Chicken",
      description:
        "Lorem ipsum dolor sit amet consectetur, adipisicing elit. Necessitatibus similique fugiat, esse temporibus laudantium molestiae minus ex consectetur delectus debitis possimus iure, quasi vero dolores sunt aliquid dolorem! Quae, soluta!",
      location: "Pallikarani",
      image:
        "data:image/jpeg;base64,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",
        phone: "1234567899",

      email: "test@123.com"
    },
    {
      name: "SS Chicken",
      description:
        "Lorem ipsum dolor sit amet consectetur, adipisicing elit. Necessitatibus similique fugiat, esse temporibus laudantium molestiae minus ex consectetur delectus debitis possimus iure, quasi vero dolores sunt aliquid dolorem! Quae, soluta!",
      location: "Medavakkam",
      image:
        "https://nationaltoday.com/wp-content/uploads/2019/07/national-fried-chicken-day.jpg",
        phone: "1234567899",

      email: "test@123.com"
    },
  ];




</script>

<svelte:head>
    <title>Resturant</title>
</svelte:head>

<AdBannner/>

<main>
  <h2>Our Top Picks For You</h2>
  <div class="picks">
    {#each data as datum}
      <div class="cards">
        <Card data={datum} />
      </div>
    {/each}
  </div>
</main>

<style lang="scss">

  main {
    margin: 5vh auto;
  }
  h2 {
    font-size: 200%;
  }

  .picks {
    width: 100%;
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    align-items: center;

    .cards {
      display: inline-flex;
      width: 20%;
    }
  }
</style>
