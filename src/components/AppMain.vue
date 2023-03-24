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
            }
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
                    {{ oggetto.img }}
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
        }
    }
</style>