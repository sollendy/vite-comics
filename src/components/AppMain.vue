<script>
    import AppAlbi from './AppAlbi.vue';
    export default {
    data() {
        return {
            albi: [
                {
                    thumb: "https://www.coverbrowser.com/image/action-comics/1-1.jpg",
                    price: "$19.99",
                    series: "Action Comics",
                    type: "comic book"
                },
                {
                    thumb: "https://www.panini.it/media/catalog/product/cache/a5b5dd3adfe0d321084804c738f29601/M/1/M1BLLA015ISBN_0.jpg",
                    price: "$3.99",
                    series: "American Vampire 1976",
                    type: "comic book"
                },
                {
                    thumb: "https://media.wired.com/photos/593384dad80dd005b42b2817/master/w_2560%2Cc_limit/Aquaman-16.jpg",
                    price: "$16.99",
                    series: "Aquaman",
                    type: "graphic novel"
                },
                {
                    thumb: "https://d29xot63vimef3.cloudfront.net/image/batgirl/1-1.jpg",
                    price: "$2.99",
                    series: "Batgirl",
                    type: "comic book"
                },
                {
                    thumb: "https://static.posters.cz/image/750/locandine-film-in-plexiglass-batman-prowl-comic-cover-i69653.jpg",
                    price: "$3.99",
                    series: "Batman",
                    type: "comic book"
                },
                {
                    thumb: "https://static.wikia.nocookie.net/marvel_dc/images/5/50/Batman_Beyond_v.1_1.jpg",
                    price: "$2.99",
                    series: "Batman Beyond",
                    type: "comic book"
                },
                {
                    thumb: "https://static.wikia.nocookie.net/marvel_dc/images/0/0d/Batman_Superman_Vol_1_1.jpg",
                    price: "$3.99",
                    series: "Batman/Superman",
                    type: "comic book"
                },
                {
                    thumb: "https://static.wikia.nocookie.net/marvel_dc/images/c/cf/Batman_Superman_Annual_Vol_2_1.jpg",
                    price: "$4.99",
                    series: "Batman/Superman Annual",
                    type: "comic book"
                },
                {
                    thumb: "https://static.wikia.nocookie.net/marvel_dc/images/5/54/Batman_The_Joker_War_Zone_Vol_1_1.jpg",
                    price: "$5.99",
                    series: "Batman: The Joker War Zone",
                    type: "comic book"
                },
                {
                    thumb: "https://static.wikia.nocookie.net/marvel_dc/images/6/64/Batman_Three_Jokers_Collected.jpg",
                    price: "$6.99",
                    series: "Batman: Three Jokers",
                    type: "comic book"
                },
                {
                    thumb: "https://static.wikia.nocookie.net/marvel_dc/images/f/f8/Batman_White_Knight_Presents_Harley_Quinn_Vol_1_1.jpg",
                    price: "$4.99",
                    series: "Batman: White Knight Presents: Harley Quinn",
                    type: "comic book"
                },
                {
                    thumb: "https://static.wikia.nocookie.net/marvel_dc/images/c/c8/Catwoman_Vol_2_1.jpg",
                    price: "$16.99",
                    series: "Catwoman",
                    type: "graphic novel"
                }
            ],
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
        };
    },
    components : {
        AppAlbi,
    }
}
</script>

<template>
    <div id="corpo-pagina">
        <div class="banner-serie">
            SERIE IN CORSO
        </div>
        <div id="comic-cont">
            <AppAlbi v-for="albo in albi" :img="albo.thumb" :prezzo="albo.price" :serie="albo.series" :tipologia="albo.type"></AppAlbi>
        </div>
        <div class="mostra">
            MOSTRA ALTRO
        </div>
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
        padding-top: 20px;
        background-color: black;
        color: white;
        position: relative;
        // display: flex;
        .banner-serie {
            background-color: rgb(0, 78, 146);
            font-size: 12px;
            font-weight: bold;
            // height: 13.5px;
            width: 130px;
            padding: 5px;
            position: absolute;
            top: -12px;
            left: 95px;
            text-align: center;
        }
        .mostra {
            background-color: rgb(0, 78, 146);
            width: 130px;
            padding: 5px;
            font-size: 10px;
            display: flex;
            justify-content: center;
            position: absolute;
            margin-left: auto;
            margin-right: auto;
            left: 0;
            right: 0;
            bottom: 10px;
            text-align: center;
            // text-align: center;
        }
        #comic-cont {
            padding-bottom: 15px;
            width: 80%;
            margin: 0 auto;
            display: flex;
            flex-flow: row wrap;
            // img {
            //     width: 100px;
            // }
        }

    }
    #barra-celeste {
        background-color: rgb(0, 78, 146);
        color: white;
        // z-index: 5;
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