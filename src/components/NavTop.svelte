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
    background-color: #2e108e;

    .logo {
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
        color: rgb(0, 0, 0);
        width: 80%;
        height: 50px;
        border: 5px #909090 solid;
        border-right: 0;
        padding-left: 5px;
        font-family: "Roboto", sans-serif;
        border-radius:25px 0 0 25px ;
        background-color: #fff ;
        
      }

      button {
        display: flex;
        all: unset;
        width: 10%;
        height: 50px;
        border: 5px #909090 solid;
        border-radius:0 25px 25px 0 ;
        text-align: center;
        border-left: 0;
        transition: all 0.3s cubic-bezier(0.75, 0.25, 0.25, 0.75);
        background-color: #fff ;



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
        color: #ffffff;

        &:hover {
          color: #ff4f04;
        }
      }
    }
  }
</style>
