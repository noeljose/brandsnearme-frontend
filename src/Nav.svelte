
<script lang="ts">

let current = 'home'

</script>

<nav>
    <div class="{`options active`}">
       <ul>
        <a 	
            class:selected="{current === 'home'}"
            on:click="{() => current = 'home'}"
            href="/">
            <li>   
                <i class="fas fa-home"></i> Home
            </li>
        </a>
        



        <a 
        class:selected="{current === 'grocery'}"
            on:click="{() => current = 'grocery'}"
        href="/grocery">
            <li>
                <i class="fas fa-shopping-cart"></i> Grocery
            </li>
        </a>

        <a
        class:selected="{current === 'store'}"
        on:click="{() => current = 'store'}"
        href="/store">
            <li>
                <i class="fas fa-store"></i> Store
            </li>
        </a>

        <a 
        class:selected="{current === 'real'}"
            on:click="{() => current = 'real'}"
        href="/realestate">
            <li>
                <i class="fas fa-building"></i> Real Estate
            </li>
        </a>

        <a
        class:selected="{current === 'rest'}"
            on:click="{() => current = 'rest'}"
        href="/resturant">
            <li>
                <i class="fas fa-utensils"></i> Resturant
            </li>
    
        </a>

        <a
        class:selected="{current === 'service'}"
            on:click="{() => current = 'service'}"
        href="/services">
            <li>
                <i class="fas fa-cog"></i> Services
            </li>
        </a>

        
        <a
        class:selected="{current === 'events'}"
            on:click="{() => current = 'events'}"
        href="/events">
            <li>
            <i class="far fa-calendar-check"></i> Events
            </li>
        </a>
        
        <a
        class:selected="{current === 'mb'}"
            on:click="{() => current = 'mb'}"
        href="/marketboard">
            <li><i class="fas fa-shopping-basket"></i> Marketboard</li>
        </a>

        

       </ul>
    </div>
</nav>


<style lang="scss">
    nav {
        width: 100%;
        
        .options {
            width: 100%;

            ul {
                width: 90%;
                display: grid;
                grid-template-columns: repeat(8, 1.5fr);
                list-style: none;
                margin: auto;

                * {
                    color: #766f6f;
                    transition: color 0.3s;
                    
                }

                a {
                    text-decoration: none;

                }

                .active, .selected {

                    li {
                        border-top: 5px #ff4f04 solid;
                        color: #ff4f04;
                        cursor: pointer;

                        i {
                            color: #ff4f04;
                            
                        }

                        
                    }
                }

                li {
                    width: 80%;
                    text-align: center;
                    padding: 15px 0;
                    border-top: 5px solid #fff;
                    font-family: 'Roboto', sans-serif;
                    font-weight: bolder;

                    &:hover {
                        border-top: 5px #ff4f04 solid;
                        color: #ff4f04;
                        cursor: pointer;
                        
                        
                        i {
                            color: #ff4f04;
                            
                        }

                    }
                }
                
            }
        }
    }
</style>

