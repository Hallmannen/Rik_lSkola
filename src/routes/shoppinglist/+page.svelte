<main class='container'>
    <h1 style="text-align:center">
        Shoppinglist
    </h1>
    <div class ="categories_container" >
        <section>
        <h2>Varor att köpa</h2>
        <ol>
            <li>
                Vara 1
            </li>
            <li>
                Vara 2  
            </li>
        </ol>
        </section>
        <section>
        <h2>Köpta varor </h2>
        <ul>
            <li>
                Vara1
            </li>
            <li>
                Vara2
            </li>
        </ul>
    </section>
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
   

}

.categories_container section h2{
    width: 100%;
    font-style:italic;
    text-align: center;
        background-color: rgba(0, 0, 0, 0.1); /* svart bakgrund med 10% opacitet */
 padding: 1em 0;
    margin: 0;
}

 .categories_container section:nth-child(odd){  /* vilket barn vill vi styla? */
    background-color: rgba(0, 0, 0, 0.1); /* svart bakgrund med 10% opacitet */
  }
 
  .categories_container section:nth-child(even){  /* vilket barn vill vi styla? */
    background-color: rgba(0, 0, 0, 0.3); /* svart bakgrund med 30% opacitet */
  }


</style>