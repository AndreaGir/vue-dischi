<template>
    <div class="carta">
        <li class="carte album">
        <figure class="immagine">
            <img :src="albums.poster" alt="">
        </figure>

    <div class="informazioni">
        <h4> {{albums.title}} </h4>
        <p> {{albums.author}} </p>
        <p> {{albums.year}} </p>
    </div>
    
    </li>
    </div>
    

    
</template>


<script>
export default {
    props: {
        albums: {
            type: Object,
            required: true,
        }
    }
    
}
</script>


<style lang="scss" scoped>

.carte{
    list-style: none;
}
.informazioni{
    text-align: center;
}
.carta{
    max-width: 18%;
}

</style>