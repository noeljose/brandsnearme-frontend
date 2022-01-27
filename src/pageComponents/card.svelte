<script>
    import { fade} from 'svelte/transition';


    export let data;
    let modalVisibility = false;


</script>

{#if modalVisibility}
    <div transition:fade class="modal">
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
                    <br>
                    {#if data?.website}
                    <a class="websiteButton" target="_blank" href={data.website}><i class="fab fa-internet-explorer"></i>&nbsp;Visit website</a>
                    <br>
                    {/if}
                    <p>Phone: <b> {data.phone}</b> </p>
                    <p>Email: <b>{data.email}</b></p>
                </div>
                <div class="social">
                    <h3 class="title">Our Social Media Pages</h3>
                   {#if data?.social}
                        {#each data.social[0] as media}
                        <a style={`background-color: ${media.color}`} target="_blank" href={media.url}><i class={media.icon}></i> {media.company}</a>
                        {/each}
                   {:else}
                        <p style={`background-color: white`}>No Social media connected</p>
                   {/if}
                </div>

                <div class="offers">
                    <h3 class="title">Our Offers</h3>
                   {#if data?.offers}
                        {#each data.offers[0] as offer}
                        <p style={`background-color: white`}> 
                            {offer.offer} <br/> <br>

                            Code: <span>{offer.code}</span>
                        
                        </p>
                        {/each}
                   {:else}
                        <p style={`background-color: white`}>No Offers Yet</p>
                   {/if}
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
    <div class="img" style={`background-image: url(${data.image}`}>
        {#if data?.offers}
        <p>Offers Avaliable</p>
        {/if}
    </div>
    <h2>{data.name}</h2>
    <p>{data.location}</p>
</main>

<style lang="scss">

    .title {
        margin-bottom: 10px;
    }
    .modal {
    

        .data {
            width: 80vw;
            min-height: 80vh;
            background-color: #fff;
            position: absolute;
            top: 10vh;
            left: 10vw;
            z-index: 1;
            border: 10px #766f6f solid;
            border-image: linear-gradient(
                            to right,
                            #4285f4 25%,
                            #db4437 25%,
                            #db4437 50%,
                            #f4b400 50%,
                            #f4b400 75%,
                            #0f9d58 75% )5;

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
                grid-template-columns: 3fr 3fr 2fr;
                

                .visual{
                    h3 {
                        text-transform: capitalize;
                        font-weight: bold;
                        font-size: 200%;
                    }
                    img {
                        width: 90%;
                        border-radius: 10px;
                        border: #f12711 10px solid;
                    }
                    p {
                        width: 90%;
                        text-align: justify;
                    }

                    .websiteButton{
                        display: inline-flex;
                        background-color: red;
                        font-size: 200%;
                        padding: 20px;
                        margin-bottom: 10px;
                        text-decoration: none;
                        color: #fff;
                        border-radius: 5px;
                        box-shadow: 0px 0px 5px #000;
                        transition: 0.3s ease-in-out;
                        &:hover {
                            box-shadow: -3px 3px 10px rgba(0, 0, 0, 0.733);
                        }
                    }
                }

                .social {
                    width: 90%;

                    a {
                        display: block;
                        font-size: 150%;
                        padding: 20px;
                        margin-bottom: 10px;
                        text-decoration: none;
                        color: #fff;
                        border-radius: 5px;
                        box-shadow: 0px 0px 5px #000;
                        transition: 0.3s ease-in-out;
                        &:hover {
                            box-shadow: -3px 3px 10px rgba(0, 0, 0, 0.733);
                        }
                    }

                    p {
                        display: block;
                            font-size: 20px;
                            padding: 20px;
                            margin-bottom: 10px;
                            color: rgb(0, 0, 0);
                            font-weight: bolder;
                            border-radius: 5px;
                            border:5px solid #f12711;
                            box-shadow: 0px 0px 5px #000;
                            transition: 0.3s ease-in-out;
                    }

                }

                .offers {
                    width: 100%;

                        p {
                            display: block;
                            font-size: 20px;
                            padding: 20px;
                            margin-bottom: 10px;
                            color: rgb(0, 0, 0);
                            font-weight: bolder;
                            border-radius: 5px;
                            border:5px solid #f12711;
                            box-shadow: 0px 0px 5px #000;
                            transition: 0.3s ease-in-out;

                            span {
                                background-color: #f12711;
                                color: #fff;
                                padding: 5px;
                                margin: 5px;
                            }

                            &:hover {
                                box-shadow: -3px 3px 10px rgba(0, 0, 0, 0.733);
                            }
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
            display: flex;
            justify-content: end;
            align-items: flex-end;
            overflow: hidden;

            p{
                padding: 5px;
                background-color: red;
                border-radius: 10px 0 0 0;
                color: #fff;
                font-weight: bold;
                padding-left: 10px;
            }


            &:hover {
                box-shadow: 0px 0px 20px #f12711;
            }
        }
    }
</style>
