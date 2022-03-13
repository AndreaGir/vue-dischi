<template>
    <div>

        <albums v-for="(dischi,i) in album" :key="i" :albums="dischi">    
        </albums>

    </div>
</template>


<script>
import axios from 'axios'

import albums from './dischiAlbum.vue'

export default {
    components:{
        albums,
    },
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