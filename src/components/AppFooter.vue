<script>
    export default {
    data() {
        return {
            referenze: [
                {
                    title: "DC COMICS",
                    link: [
                        'personaggi',
                        'fumetti',
                        'film',
                        'tv',
                        'giochi',
                        'video',
                        'notizie',
                    ]
                },

                
                {
                    title: "DC",
                    link: [
                        'Termini di Utilizzo',
                        'Accordo Riservatezza',
                        'Aggiungi scelta',
                        'Avvertenze',
                        'Impieghi',
                        'Iscrizioni',
                        'Laboratori Talenti',
                        'Certificati CPSC',
                        'Recensioni',
                        'Guida Acquisti',
                        'Contattaci',
                    ]
                },

                {
                    title: "RISORSE",
                    link: [
                        'DC',
                        'MAD magazine',
                        'DC & Ragazzi',
                        'Universo DC',
                        'DC Power Visa',
                    ]
                },

                {
                    title: "NEGOZIO",
                    link: [
                        'Negozio DC',
                        'Negozio DC Collezionabili',
                    ]
                },
            ],

            profili: [
                {
                    title: 'SEGUICI'
                },

                {
                    profilo: "/img/footer-facebook.png",
                },

                {
                    profilo: "/img/footer-periscope.png",
                },

                {
                    profilo: "/img/footer-pinterest.png",
                },

                {
                    profilo: "/img/footer-twitter.png",
                },

                {
                    profilo: "/img/footer-youtube.png",
                },
            ]
        }
    }
}
</script>

<template>
    <section class="sezioni sec-1">
        <div id="liste-link">
            <div class="links">
                <ul id="lista-cnt">
                    <li v-for="titoli in referenze">
                        <h4>{{ titoli.title }}</h4>
                        <ul>
                            <li v-for="pippo in titoli.link">
                                {{ pippo }}
                            </li>
                        </ul>
                    </li>
                </ul>
            </div>
            <div id="img-foot-cnt">
                <img src="/img/dc-logo-bg.png" alt="logo">
            </div>
        </div>
    </section>
    <section class="sezioni sec-2">
        <nav id="last-nav">
            <div id="btn-cnt">
                <button>
                    registrati orah!
                </button>
            </div>
            <div id="social-links">
                <ul v-for="elemento in profili">
                    <h4>{{ elemento.title }}</h4>
                    <li><a href=""><img :src="elemento.profilo" alt=""></a></li>
                    <!-- <h1 v-for="titolo in profili">{{ titolo.title }}</h1>
                    <li v-for="social in profili">{{ social.profilo }}</li> -->
                </ul>
            </div>
        </nav>
    </section>
</template>

<style lang="scss" scoped>
    .sec-1{
        // display: flex;
        // justify-content: space-between;
        // align-items: center;
        color: white;
        background-image: (url("/img/footer-bg.jpg"));
        background-repeat: repeat;
        
        #liste-link{
            width: 80%;
            margin: auto;
            padding: 40px 0;
            position: relative;
            .links {
                width: 70%;
                #lista-cnt {
                    list-style-type: none;
                    width: 55%;
                    display: flex;
                    justify-content: space-between;
                    flex-flow: row wrap;
                    ul {
                        padding-top: 10px;
                        list-style-type: none;
                        font-size: 10px;
                        li {
                            // padding-bottom: ;
                            color: grey;
                            padding-bottom: 5px;
                        }
                    }
                }
            }
            #img-foot-cnt {
                position: absolute;
                top: 10px;
                right: -95px;
                // z-index: 1;
                overflow: hidden;
                img {
                    width: 60%;
                }
            }
        }
    }
    .sec-2 {
        background-color: rgb(48, 48, 48);
        #last-nav {
            width: 80%;
            margin: auto;
            padding: 10px 0;
            display: flex;
            justify-content: space-between;
            align-items: center;
            #btn-cnt {
                button {
                    background-color: rgb(48, 48, 48);
                    color: white;
                    padding: 5px;
                    border: solid 2px rgb(6, 133, 255);
                }
            }
            #social-links {
                display: flex;
                // align-items: center;
                gap: 5px;
                ul {
                    display: flex;
                    align-items: center;
                    list-style-type: none;
                    h4 {
                        color: rgb(6, 133, 255);
                        padding: 0 10px 0 0;
                    }
                }
            }
        }
    }
</style>