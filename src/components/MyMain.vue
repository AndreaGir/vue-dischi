<template>
    <div class="main">
        <div class="dentromain">
            <ListaCd class="carta" />
        </div>

    </div>
</template>


<script>

import ListaCd from './ListaCd.vue'

export default {
    components: {
        ListaCd
    }

}
</script>


<style lang="scss" scoped>
*{
    padding: 0;
    margin: 0;
    box-sizing: border-box;
}
.main{
    width: 100%;
    min-height: 90vh;
    display: flex;
    align-items: center;
    background-color: rgba(0, 0, 0, 0.781);
}
.dentromain{
    width: 85%;
    height: 80%;
    border: 1px solid red;
    margin: 0 auto;
    display: flex;
    flex-wrap: wrap;
}
.carta {
    max-width: 18%;
}

</style>