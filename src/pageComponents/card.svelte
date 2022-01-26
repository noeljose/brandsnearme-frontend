<script>
    export let data;

    let modalVisibility = false;
</script>

{#if modalVisibility}
    <div class="modal">
        <div class="data">
            <div class="close">
                <i class="fas fa-times-circle"
                    on:click={() => { modalVisibility = !modalVisibility;}}
                />
            </div>

            <div class="content">
                <div class="visual">
                    <h3>{data.name}</h3>
                    <img src={data.image} alt="">
                    <p>{data.description}</p>
                </div>
                <div class="social">
                    <a target="_blank" href="https://facebook.com"><i class="fas fa-times-circle"></i> Facebook</a>
                </div>
            </div>

          
        </div>
        <div class="black"
            on:click={() => {modalVisibility = !modalVisibility;}}
            />
    </div>
{/if}

<main
    on:click={() => {
        modalVisibility = !modalVisibility;
    }}
>
    <div class="img" style={`background-image: url(${data.image}`} />
    <h2>{data.name}</h2>
    <p>{data.location}</p>
</main>

<style lang="scss">
    .modal {
        .data {
            width: 80vw;
            min-height: 80vh;
            background-color: #fff;
            position: absolute;
            top: 10vh;
            left: 10vw;
            z-index: 1;

            .close {
                width: 100%;

                display: flex;
                justify-content: right;

                .fas {
                    padding: 10px;
                    margin: 10px;
                    font-size: 32px;
                    color: red;
                }
            }

            .content {
                width: 80%;
                height: 100%;
                margin: auto;
                display: grid;    
                grid-template-columns: 2fr 1fr;

                .visual{
                    h3 {
                        text-transform: capitalize;
                        font-weight: bold;
                        font-size: 200%;
                    }
                    img {
                        width: 50%;
                        border-radius: 10px;
                        border: #f12711 10px solid;
                    }
                }

            }


        }

        .black {
            position: fixed;
            top: 0;
            left: 0;
            height: 100vh;
            width: 100vw;
            background-color: rgba(0, 0, 0, 0.609);
        }
    }
    main {
        display: inline-flex;
        flex-direction: column;
        width: 80%;
        margin: 10%;
        padding: 0;

        .img {
            width: 100%;
            height: 200px;
            background-size: cover;
            background-position: center;
            border-radius: 10%;
            border: 5px solid;
            border-color: #f12711;
            box-shadow: 0px 0px 1px #000;
            transition: box-shadow 0.3s ease-in-out;

            &:hover {
                box-shadow: 0px 0px 20px #f12711;
            }
        }
    }
</style>
