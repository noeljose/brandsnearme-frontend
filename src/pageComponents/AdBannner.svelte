<script>
	import {fade} from 'svelte/transition'
	
	const carouselPhotos = [
		'1.png',
		'2.png',
		'3.png'
	]
	
	let index = 0
	
	const next = () => {
    
		index = index + 1
    index == carouselPhotos.length? index=0:null 
	}
	const back = () => {
		index = index - 1
    index < 0? index=0:null 
	}

  setInterval(()=>{next()}, 5000)
</script>
 
<main>
   
 <div class="imgs">
  {#each [carouselPhotos[index]] as src (index)}
  <img {src} alt="" />	
  {/each}
 </div>

 <!-- <div class="buttons">
  <div class="button">
    <button on:click={back}><i class="fas fa-arrow-circle-left"></i></button>
  </div>
  <div class="space"></div>
  <div class="button">
    <button on:click={next}><i class="fas fa-arrow-circle-right"></i></button>
  </div>
 </div> -->


</main>



  <style lang="scss">
 	main{
     width: 100%;
     height: 16vw;

      .imgs {
        z-index: -1;
        img {
          position: absolute;
          width: 100%;
        }
      }

      // .buttons {
      //   width: 100%;
      //   position: absolute;
      //   display: grid;
      //   grid-template-columns: 0.5fr 9fr 0.5fr;
      //   height: 16vw;

      //   .button{
      //     display: flex;
      //     justify-content: center;
      //     align-items: center;

      //     button {
      //       all: unset;
      //       font-size: 32px;
      //       background-color: blue;
      //       padding: 10px;
      //       border-radius: 50%;
      //       height: 40px;
      //       width: 40px;
      //       display: flex;
      //       justify-content: center;
      //       align-items: center;
      //       i{
      //         color: white;
      //       }

      //     }
      //   }
      // }

   }
  </style>