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
    <section class="sezioni">

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
                    width: 45%;
                    display: flex;
                    justify-content: space-between;
                    flex-flow: row wrap;
                    ul {
                        padding-top: 10px;
                        list-style-type: none;
                        font-size: 10px;
                        li {
                            // padding-bottom: ;
                        }
                    }
                }
            }
            #img-foot-cnt {
                position: absolute;
                top: 0;
                right: -90px;
                img {
                    width: 60%;
                }
            }
        }

    }
</style>