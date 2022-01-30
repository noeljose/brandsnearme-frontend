
<script>
  import HeroBanner from '../pageComponents/HeroBanner.svelte';
  import Card from "../pageComponents/card.svelte";

  let data = [
    {
      name: "Burger Bay",
      description:
        "Lorem ipsum dolor sit amet consectetur, adipisicing elit. Necessitatibus similique fugiat, esse temporibus laudantium molestiae minus ex consectetur delectus debitis possimus iure, quasi vero dolores sunt aliquid dolorem! Quae, soluta!",
      location: "Madmbakkam",
      image:
        "https://scontent.fmaa2-1.fna.fbcdn.net/v/t39.30808-1/p148x148/259855312_2095122263968632_7979243900832395632_n.png?_nc_cat=107&ccb=1-5&_nc_sid=1eb0c7&_nc_ohc=VSWgfG8t28cAX_xSF16&_nc_ht=scontent.fmaa2-1.fna&oh=00_AT-RO9LWYBcJVJkGZrfl_Q58uFElZWJchAyl2Yn-2sAaUg&oe=61FA73F2",

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
        "https://i.ytimg.com/vi/pyg8JIIIlFI/maxresdefault.jpg",
        phone: "1234567899",

      email: "test@123.com"
    },
    {
      name: "Italia Pizza",
      description:
        "Lorem ipsum dolor sit amet consectetur, adipisicing elit. Necessitatibus similique fugiat, esse temporibus laudantium molestiae minus ex consectetur delectus debitis possimus iure, quasi vero dolores sunt aliquid dolorem! Quae, soluta!",
      location: "Madambakkam",
      image:
        "data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAARMAAAC3CAMAAAAGjUrGAAAAFVBMVEX///8AkkbOKzcAjz56uI/ehIjNHy1xf0V9AAAA/klEQVR4nO3QSQ0AIAADsHH6l4yKPUhaCc2oWTs9586aOHHixIkTJ06cOHHixIkTJ06cOHHixIkTJ06cOHHixIkTJ06cOHHixIkTJ06cOHHixIkTJ06cOHHixIkTJ06cOHHixIkTJ06cOHHixIkTJ06cOHHixIkTJ06cOHHixIkTJ06cOHHixIkTJ06cOHHixIkTJ06cOHHixIkTJ06cOHHixIkTJ06cOHHixIkTJ06cOHHixIkTJ06cOHHixIkTJ06cOHHixIkTJ06cOHHixIkTJ06cOHHixIkTJ06cOHHixIkTJ06cOHHixIkTJ06cOHHixIkTJ06cOHHy4ckD5KrN4eD2boIAAAAASUVORK5CYII=",
        phone: "1234567899",

      email: "test@123.com"
    },
    {
      name: "FD Chicken",
      description:
        "Lorem ipsum dolor sit amet consectetur, adipisicing elit. Necessitatibus similique fugiat, esse temporibus laudantium molestiae minus ex consectetur delectus debitis possimus iure, quasi vero dolores sunt aliquid dolorem! Quae, soluta!",
      location: "Pallikarani",
      image:
        "https://thumbs.dreamstime.com/z/chicken-mascot-design-premium-logo-chicken-mascot-design-premium-logo-label-product-badge-business-stamps-shop-more-220379649.jpg",
        phone: "1234567899",

      email: "test@123.com"
    },
    {
      name: "SS Chicken",
      description:
        "Lorem ipsum dolor sit amet consectetur, adipisicing elit. Necessitatibus similique fugiat, esse temporibus laudantium molestiae minus ex consectetur delectus debitis possimus iure, quasi vero dolores sunt aliquid dolorem! Quae, soluta!",
      location: "Medavakkam",
      image:
        "https://image.shutterstock.com/image-vector/chicken-mascot-restaurant-logo-vector-260nw-765560698.jpg",
        phone: "1234567899",

      email: "test@123.com"
    },
  ];

</script>


<svelte:head>
    <title>Home</title>
</svelte:head>


<HeroBanner/>

<main class="cardsM">
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


  .cardsM {
    transform: translateY(-25%);
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
  }
</style>

