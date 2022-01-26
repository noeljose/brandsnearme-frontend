<script>
  import { each } from "svelte/internal";
  import Card from "../pageComponents/card.svelte";

  let data = [
    {
      name: "name resturant",
      description:
        "Lorem ipsum dolor sit amet consectetur, adipisicing elit. Necessitatibus similique fugiat, esse temporibus laudantium molestiae minus ex consectetur delectus debitis possimus iure, quasi vero dolores sunt aliquid dolorem! Quae, soluta!",
      location: "lorem colony",
      image:
        "https://external-content.duckduckgo.com/iu/?u=https%3A%2F%2Fwagoodfoodguide.com%2Fwp-content%2Fuploads%2F2020%2F12%2Fburger3.jpg&f=1&nofb=1",
    },
    {
      name: "name resturant",
      description:
        "Lorem ipsum dolor sit amet consectetur, adipisicing elit. Necessitatibus similique fugiat, esse temporibus laudantium molestiae minus ex consectetur delectus debitis possimus iure, quasi vero dolores sunt aliquid dolorem! Quae, soluta!",
      location: "lorem colony",
      image:
        "https://external-content.duckduckgo.com/iu/?u=https%3A%2F%2Fwagoodfoodguide.com%2Fwp-content%2Fuploads%2F2020%2F12%2Fburger3.jpg&f=1&nofb=1",
    },
    {
      name: "name resturant",
      description:
        "Lorem ipsum dolor sit amet consectetur, adipisicing elit. Necessitatibus similique fugiat, esse temporibus laudantium molestiae minus ex consectetur delectus debitis possimus iure, quasi vero dolores sunt aliquid dolorem! Quae, soluta!",
      location: "lorem colony",
      image:
        "https://external-content.duckduckgo.com/iu/?u=https%3A%2F%2Fwagoodfoodguide.com%2Fwp-content%2Fuploads%2F2020%2F12%2Fburger3.jpg&f=1&nofb=1",
    },
    {
      name: "name resturant",
      description:
        "Lorem ipsum dolor sit amet consectetur, adipisicing elit. Necessitatibus similique fugiat, esse temporibus laudantium molestiae minus ex consectetur delectus debitis possimus iure, quasi vero dolores sunt aliquid dolorem! Quae, soluta!",
      location: "lorem colony",
      image:
        "https://external-content.duckduckgo.com/iu/?u=https%3A%2F%2Fwagoodfoodguide.com%2Fwp-content%2Fuploads%2F2020%2F12%2Fburger3.jpg&f=1&nofb=1",
    },
    {
      name: "name resturant",
      description:
        "Lorem ipsum dolor sit amet consectetur, adipisicing elit. Necessitatibus similique fugiat, esse temporibus laudantium molestiae minus ex consectetur delectus debitis possimus iure, quasi vero dolores sunt aliquid dolorem! Quae, soluta!",
      location: "lorem colony",
      image:
        "https://external-content.duckduckgo.com/iu/?u=https%3A%2F%2Fwagoodfoodguide.com%2Fwp-content%2Fuploads%2F2020%2F12%2Fburger3.jpg&f=1&nofb=1",
    },
  ];
</script>

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
