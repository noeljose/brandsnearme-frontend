<script>
</script>

<main>
  <div class="banner">
    <img src="https://via.placeholder.com/1920x720" alt="" />
  </div>

  <div class="newEvents">
    <div class="card">
      <img src="https://via.placeholder.com/200x200" alt="" />
      <h3>Lorem, ipsum dolor.</h3>
      <p>
        Lorem ipsum, dolor sit amet consectetur adipisicing elit. Facilis,
        sapiente?
      </p>
    </div>
    <div class="card">
      <img src="https://via.placeholder.com/200x200" alt="" />
      <h3>Lorem, ipsum dolor.</h3>
      <p>
        Lorem ipsum, dolor sit amet consectetur adipisicing elit. Facilis,
        sapiente?
      </p>
    </div>
    <div class="card">
      <img src="https://via.placeholder.com/200x200" alt="" />
      <h3>Lorem, ipsum dolor.</h3>
      <p>
        Lorem ipsum, dolor sit amet consectetur adipisicing elit. Facilis,
        sapiente?
      </p>
    </div>
    <div class="card">
      <img src="https://via.placeholder.com/200x200" alt="" />
      <h3>Lorem, ipsum dolor.</h3>
      <p>
        Lorem ipsum, dolor sit amet consectetur adipisicing elit. Facilis,
        sapiente?
      </p>
    </div>
  </div>
</main>

<style lang="scss">
  .banner {
    width: 80%;
    margin: 5vh auto;

    img {
      width: 100%;
      border-radius: 30px;
    }
  }

  .newEvents {
    width: 80%;
    margin: auto;
    display: flex;
    justify-content: center;
    align-items: center;
    flex-wrap: warp;
    font-family: "Roboto", sans-serif;

    .card {
      display: flex;
      justify-content: center;
      align-items: center;
      flex-direction: column;
      width: 25%;
      text-align: center;

      img {
        width: 80%;
        border-radius: 30px;
      }

      h3 {
        color: #ff4f04;
        font-size: 25px;
        padding: 0;
        margin: 20px 0 0 0;
      }

      p {
        color: #766f6f;
      }
    }
  }
</style>
