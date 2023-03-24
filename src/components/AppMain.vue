<script>
    export default {
    data() {
        return {
            oggetti: [
            {
                img: "/img/buy-comics-digital-comics.png",
                text: "DIGITAL COMICS",
            },
            
            {
                img: "/img/buy-comics-merchandise.png",
                text: "DC MERCHANDISE",
            },

            {
                img: "/img/buy-comics-subscriptions.png",
                text: "SUBSCRIPTION",
            },

            {
                img: "/img/buy-comics-shop-locator.png",
                text: "COMIC SHOP LOCATOR",
            },

            {
                img: "/img/buy-dc-power-visa.svg",
                text: "DC POWER VISA",
            },
        ],
        }
    }
}
</script>

<template>
    <div id="corpo-pagina">
    contenuto immenso di questo fantastico sito
    </div>
    <div id="barra-celeste">
        <ul>
            <li v-for="oggetto in oggetti">
                <div>
                    <img :src="oggetto.img" alt="shop-pics">
                </div>
                <span>{{ oggetto.text }}</span>
            </li>
        </ul>
    </div>
</template>

<style lang="scss" scoped>
    #corpo-pagina {
        background-color: black;
        color: white;
        padding: 50px;
    }
    #barra-celeste {
        background-color: rgb(0, 78, 146);
        color: white;
        ul {
            display: flex;
            align-items: center;
            justify-content: center;
            list-style-type: none;
            gap: 20px;
            li {
                display: flex;
                align-items: center;
                gap: 10px;
                padding: 10px;
                img {
                    width: 35px;
                }
                span {
                    font-size: 10px;
                }
            }
        }
    }
</style>