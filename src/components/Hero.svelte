<div class="topBar">
  <div class="logo">
    <img src="logo.png" alt="" />
  </div>

  <div class="search">
    <input type="text" placeholder="Search For services, Category etc" />
    <button><i class="fas fa-search" /></button>
  </div>


</div>

<style lang="scss">
  .topBar {
    width: 100%;
    height: 50vh;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;



    .logo {
      display: flex;
      justify-content: center;
      align-items: center;
      margin-bottom: 10px;

      img {
        height: 100px;
      }
    }

    .search {
      display: flex;
      justify-content: center;
      align-items: center;


      input {
        all: unset;
        color: rgb(0, 0, 0);
        width: 50vw;
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

  
  }
</style>
