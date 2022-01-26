<div class="topBar">
  <div class="logo">
    <img src="logo.png" alt="" />
  </div>

  <div class="search">
    <input type="text" placeholder="Search For services, Category etc" />
    <button><i class="fas fa-search" /></button>
  </div>

  <div class="option">
    <i class="far fa-user-circle" />
    <i class="fas fa-comment-dots" />
    <i class="fas fa-sign-in-alt" />
  </div>
</div>

<style lang="scss">
  .topBar {
    width: 100%;
    height: 10vh;
    display: grid;
    grid-template-columns: 1.5fr 2fr 1fr;

    .logo {
      background-color: #fff;
      display: flex;
      justify-content: center;
      align-items: center;

      img {
        height: 50px;
      }
    }

    .search {
      display: flex;
      justify-content: center;
      align-items: center;
      overflow: hidden;

      input {
        all: unset;
        width: 80%;
        height: 50px;
        border: 5px #766f6f solid;
        border-right: 0;
        padding-left: 5px;
        font-family: "Roboto", sans-serif;
        border-image: linear-gradient(
            to right,
            #4285f4 25%,
            #db4437 25%,
            #db4437 50%,
            #f4b400 50%,
            #f4b400 75%,
            #0f9d58 75%
          )
          5;
      }

      button {
        display: flex;
        all: unset;
        width: 10%;
        height: 50px;
        border: 5px #766f6f solid;
        text-align: center;
        border-left: 0;
        transition: all 0.3s cubic-bezier(0.75, 0.25, 0.25, 0.75);

        border-image: linear-gradient(
            to right,
            #0f9d58 75%,
            #f4b400 75%,
            #f4b400 75%,
            #4285f4 25%
          )
          5;

        i {
          text-shadow: 0 0 5px #fff;
          transition: text-shadow 0.3s cubic-bezier(0.75, 0.25, 0.25, 0.75);
        }

        &:hover {
          background-color: #ff4f04;

          i {
            color: #fff;
            text-shadow: 0 5px 5px rgba(0, 0, 0, 0.541);
            transition: text-shadow 0.3s;
          }
        }
      }
    }

    .option {
      display: flex;
      justify-content: center;
      align-items: center;

      i {
        font-size: 30px;
        margin: 10px;
        color: #766f6f;

        &:hover {
          color: #ff4f04;
        }
      }
    }
  }
</style>
