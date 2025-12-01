<script>
let image = "https://picsum.photos/id/70/367/267"
let photo = "https://picsum.photos/id/88/367/267"
let picture = "https://picsum.photos/id/93/367/267"
</script>

<h1>Nouh</h1>
<h2>Nouh</h2>




<div class='photos'>
    <div class='image-wrapper'>
        <img  src={image} alt="Flexbox egenskaper"/></div>
    <div class='image-wrapper'>
        <img src={photo}/></div>
    <div class='image-wrapper'>

        <img src={picture}/></div>
         
</div>
<style>
    
h1{
    text-align: center;
    font-size: 50px;
    margin: 20px;
    color: rgb(255, 0, 0);
}
    .photos {
        display: flex;
        width: 90vw;
        align-items: center;
        justify-content: center;
        flex-wrap: wrap;

}
img{
    width: 100%;
}
 .image-wrapper img {
    width: 100%;
    margin:10px;
    height: 100%;
    border-radius: 20px;
 }

 .image-wrapper{
    flex-grow: 1;
    height: 50vh;
    flex-basis: 300px;
    
 }
.image-wrapper:hover { flex-grow:2; }
.image-wrapper:active { transform: scale(0.9); }
</style>