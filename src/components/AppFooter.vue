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
                    title: "NEGOZIO",
                    link: [
                        'Negozio DC',
                        'Negozio DC Collezionabili',
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
            ],
        }
    }
}
</script>

<template>
    <section class="sezioni">
        <div id="liste-link">
            <div class="links">
                <ul id="lista-cnt">
                    <li v-for="titoli in referenze">
                        <h5>{{ titoli.title }}</h5>
                        <ul>
                            <li v-for="pippo in titoli.link">
                                {{ pippo }}
                            </li>
                        </ul>
                    </li>
                </ul>
            </div>
        </div>
    </section>
    <section class="sezioni">

    </section>
</template>

<style lang="scss" scoped>
    .sezioni{
        #liste-link{
            .links {
                #lista-cnt {
                    display: flex;
                    list-style-type: none;
                    ul {
                        list-style-type: none;
                    }
                }
            }
        }
    }
</style>