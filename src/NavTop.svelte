<script lang="ts">

</script>
<div class="topBar">

    <div class="logo">
        <img src="logo.png" alt="">
    </div>

    <div class="search">
        <input type="text" placeholder="Search For services, Category etc">
        <button><i class="fas fa-search"></i></button>
    </div> 

    <div class="option">
        <i class="far fa-user-circle"></i>
        <i class="fas fa-comment-dots"></i>
        <i class="fas fa-sign-in-alt"></i>
    </div>
</div>


<style lang="scss">
    .topBar{
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
                width: 80%;
            }

            
        }

        .search {

            display: flex;
            justify-content: center;
            align-items: center;


            input {
                all: unset;
                width: 80%;
                height: 50px;
                border: 0.5px #766f6f solid;
                border-right: 0;
                padding-left: 5px;
                font-family: 'Roboto', sans-serif;

            }

            button {
                display: flex;
                all: unset;
                width: 10%;
                height: 50px;
                border: 0.5px #766f6f solid;
                text-align: center;
                border-left: 0;
                transition: all 0.3s cubic-bezier(0.75, 0.25, 0.25, 0.75);

                i {
                    text-shadow:0 0 5px #fff ;
                    transition: text-shadow 0.3s cubic-bezier(0.75, 0.25, 0.25, 0.75);
                }

                &:hover {

                    background-color: #ff4f04;

                    i {
                        color: #fff;
                        text-shadow:0 5px 5px rgba(0, 0, 0, 0.541) ;
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
                margin:10px;
                color: #766f6f;
              
                &:hover {
                    color: #ff4f04;
                }
                
            }
        }

    }
</style>