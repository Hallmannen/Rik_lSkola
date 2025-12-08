   <script>
	import { fade } from "svelte/transition";

        
        let varor = $state([{name:'banan',köpt:false, number:1}]);
        let Varor = ""
        let new_vara = $state('')
   function add_vara() {
        if (new_vara.trim() === "") return;
        varor.push({ name: new_vara, köpt: false ,number:1});
        new_vara = "";
        

    }

    $effect(()=> varor.sort((a,b)=> a.number -b.number))
    </script>
    

<main class='container'>
 
    <h1 style="text-align:center">
        Shoppinglist
    </h1>
    <div class ="categories_container" >
        <section>
        <h2>Varor att köpa</h2>
        <ol>
           {#each varor as vara, i }
           {#if !vara.köpt}
             <li transition:fade>
                {vara.name} <button onclick={()=> varor.splice(i,1)}>r</button>
                <button onclick={()=>vara.köpt=true}>köpt</button>
                <input type="number" bind:value={vara.number} min=1 max=4>
                
            </li>
           {/if}
           
           {/each}
        </ol>
        </section>
        <section>
        <h2>Köpta varor </h2>
        <ul>
             {#each varor as vara, i }
           {#if vara.köpt}
             <li transition:fade>
                {vara.name} <button onclick={()=> varor.splice(i,1)}>r</button>
                 <button onclick={()=>vara.köpt=false}>köp igen</button>
            </li>
           {/if}
           
           {/each}
        </ul>
    </section>

    </div>
    <div>
        <label for='vara'>Varor</label>
        <input type="varor" id="vara" bind:value={new_vara}>
        <button onclick={add_vara}>lägg till vara</button>
</div>
</main>
<style>


.container{
        
    display: grid;
    grid-template-rows: 1fr 9fr 1fr;    
    background-color: beige;
    width: 60vw;
    height: 70vh;
    border-radius: 20px;
    

    
}
li{
    border-bottom: 1px white solid;

}

.container h1 {
justify-self: center;
align-self: center;

}

.categories_container{
    background-color: rgba(204, 195, 16, 0.2);
    width: 100%;
    display: grid;
    grid-template-columns: repeat(2,1fr);
    grid-gap: 10px;
    height: 100%;
   list-style-type:circle;

}

.categories_container section h2{
    width: 100%;
    font-style:italic;
    text-align: center;
        background-color: rgba(0, 0, 0, 0.1); /* svart bakgrund med 10% opacitet */
 padding: 1em 0;
    margin: 0;
}

ul{
    list-style-type:square;
}

 .categories_container section:nth-child(odd){  /* vilket barn vill vi styla? */
    background-color: rgba(0, 0, 0, 0.1); /* svart bakgrund med 10% opacitet */
  }
 
  .categories_container section:nth-child(even){  /* vilket barn vill vi styla? */
    background-color: rgba(0, 0, 0, 0.3); /* svart bakgrund med 30% opacitet */
  }


</style>