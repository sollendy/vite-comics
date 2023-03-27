<script>
    export default {
        name: "AppAlbi",
        data() {

        },
        props: {
            img: String,
            prezzo: Number,
            serie: String,
            tipologia: String,
        },
    }
</script>

<template>

    <div class="albi">
        <img :src="img" alt="fumetto">
        <div class="prezzo">{{prezzo}}</div>
        <div class="serie">{{serie}}</div>
        <div class="tipologia">{{tipologia}}</div>
    </div>

</template>

<style lang="scss">
    .albi {
        width: 130px;
        padding: 10px 10px;
        font-size: small;
        // display: flex;
        img {
            width: 100%;
            height: 60%;
        }
    }
</style>