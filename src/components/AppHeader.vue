<script>
export default {
    data() {
        return {
            links: [
          'personaggi',
          'fumetti',
          'film',
          'tv',
          'giochi',
          'collezionabbili',
          'video',
          'fan',
          'notizie',
          'negozio'
        ],
        }
    }
}
</script>

<template>
    <div class="head-cnt">
        <nav>
            <div class="nav-img">
                <img src="/img/dc-logo.png" alt="dc-logo">
            </div>
            <ul id="lista-nav">
                <li v-for="link in links">
                    {{ link }}
                </li>
            </ul>
        </nav>
    </div>
</template>                                 

<style lang="scss" scoped>
    .head-cnt {
        
        border-bottom: 1px solid blue;
        // width: 100%;
        nav {
            width: 80%;
            margin: auto;
            display: flex;
            gap: 20%;

            .nav-img {
                padding-top: 10px;
                padding-bottom: 10px;
                img {
                    width: 70px;
                }
            }
            
            ul {
                list-style-type: none;
                display: flex;
                align-items: center;
                text-transform: uppercase;
                li {
                    padding: 10px;
                    font-size: 10px;
                    font-weight: bold;
                    color: rgb(68, 68, 68);
                }
            }
        }
    }
</style>