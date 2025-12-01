    <script>
        let colors = [{namn: "Blå", value: "blue"}, {namn: "Röd", value: "red"}, {namn: "Gul", value: "yellow"}]
        let color = "black"
        let name = "";
        let email = "";
        let password = "";

        function handleSubmit(){
            alert("Välkommen")
        }
    </script>

<main>
    <div class='container'>
       <h1>
            Registrering
       </h1> 
       <form on:submit|preventDefault={handleSubmit}>

               
        <label for="name">Namn:</label>
        <input type="namn" id= "name" bind:value ={name}>

        <label for="mail">Email:</label>
        <input type="email" id="mail" bind:value={email}>
        
        <label for='pass'>lösenord</label>
        <input type="password" id="pass">
        
        <label for="color"> favoritfärg : </label>
        <select bind:value={color}>
            {#each colors as c} 
             <option value={c.value}>{c.namn}</option>
            {/each}
        </select> 
        <div style="width: 100px; height: 100px; border-radius: 50%; overflow:hidden; background-color:{color};">

        </div>
        <input type="Submit" name="" id="Register">
       </form>
    </div>

</main>

<style>
form{
    display: flex;
    flex-direction: column;
    justify-content: center;

}
 .container{
            border: solid 5px rosybrown;
            border-radius: 10px;
            width: 35%;
            height: 80%;
            background-color: #ffffffff;
            margin: auto;
            display:flex;
            justify-content:space-around;
            align-items:center;
            flex-direction: column;
            
                       
    }     

 main{
        background-image: url("https://t4.ftcdn.net/jpg/05/21/65/59/360_F_521655929_N80d5GaCQJ2VP073PfTXJTe9mkvsNtHE.jpg");
        background-size: cover;
        width: 100%;
        height: 100%;
        padding: 5%;
    }
            
           

</style>