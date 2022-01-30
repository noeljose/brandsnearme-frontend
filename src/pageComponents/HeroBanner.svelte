
<script>
    import Hero from "../components/Hero.svelte"
</script>
<main>
    <div class="banner">
    <Hero/>
    </div>
    <div class="options">
        
        <a href="resturant">
            <div class="option">
                <img src="main/fast-food.png" alt="">
                <h2>Food</h2>
            </div>
        </a>

        <a href="resturant">
            <div class="option">
                <img src="main/healthcare.png" alt="">
                <h2>Healthcare</h2>
            </div>
        </a>

        <a href="resturant">
            <div class="option">
                <img src="main/cart.png" alt="">
                <h2>Grocery</h2>
            </div>
        </a>

        <a href="resturant">
            <div class="option">
                <img src="main/service.png" alt="">
                <h2>Service</h2>
            </div>
        </a>

    </div>
</main>

<style lang="scss">

    main{
        width: 100%;
        

        .banner {
            min-height: 50vh;
            background-image: url("skyline.svg");
            background-color: #2e108e;

            
        }

        .options {
            transform: translateY(-40%);
                width: 100%;
                display: flex;
                justify-content: center;
                align-items: center;
                height: 25vh;
                padding-top: 20px;
                padding-bottom: 20px;
               
                a {

                    color: rgb(32, 32, 32);
                    text-decoration: none;
                   
                    h2 {
                        padding-top: 10px;
                    }

                    .option{
                    width: 15vh;
                    height: 15vh;
                    display: flex;
                    justify-content: center;
                    align-items: center;
                    flex-direction: column;
                    background-color: #fff;
                    border-radius: 50%;
                    padding: 5vh;
                    margin : auto 5vh;
                    box-shadow: 0px 10px 24px rgba(0, 0, 0, 0.123);

                    img {
                        width: 70%;
                    }
                }
                }


            }
    }

</style>