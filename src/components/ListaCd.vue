<template>
    <div>

        <div v-for="(dischi,i) in album" :key="i"> 
            {{dischi.title}}
            
        </div>

    </div>
</template>


<script>
import axios from 'axios'

export default {
    data() {
        return {
            album: []
        }
    },
    methods: {
        fetchAlbum: function() {
            
            axios.get('https://flynn.boolean.careers/exercises/api/array/music')
            .then( res => {
                this.album = res.data.response
            })
        }
    },
    mounted() {
        this.fetchAlbum()
    }
    
}
</script>


<style lang="scss" scoped>

</style>