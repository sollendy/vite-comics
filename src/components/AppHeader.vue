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
        padding: 5px 0 10px 0;
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
                    position: relative;
                }
                li:hover {
                    color: rgb(2, 130, 249);
                    // border-bottom: 3px solid rgb(2, 130, 249);
                }
                li:hover::before {
                    content: "";
                    position: absolute;
                    bottom: -42px;
                    left: 50%;
                    transform: translateX(-50%);
                    width: 50%;
                    height: 3px;
                    background-color: rgb(2, 130, 249);
                }
            }
        }
    }
</style>