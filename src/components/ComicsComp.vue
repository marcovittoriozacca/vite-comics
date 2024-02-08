<script>

import SingleComic from './SingleComic.vue';

export default{
    name: 'ComicsComp',

    components:{
        SingleComic,
    },

    data() {
        return {
            comicsList:[
                {

                    "thumb": "https://www.coverbrowser.com/image/action-comics/1-1.jpg",

                    "price": "$19.99",

                    "series": "Action Comics",

                    "type": "comic book",

                },

                {

                    "thumb": "https://www.panini.it/media/catalog/product/cache/a5b5dd3adfe0d321084804c738f29601/M/1/M1BLLA015ISBN_0.jpg",

                    "price": "$3.99",

                    "series": "American Vampire 1976",

                    "type": "comic book",

                },

                {

                    "thumb": "https://media.wired.com/photos/593384dad80dd005b42b2817/master/w_2560%2Cc_limit/Aquaman-16.jpg",

                    "price": "$16.99",

                    "series": "Aquaman",

                    "type": "graphic novel",

                },

                {

                    "thumb": "https://d29xot63vimef3.cloudfront.net/image/batgirl/1-1.jpg",

                    "price": "$2.99",

                    "series": "Batgirl",

                    "type": "comic book",

                },

                {

                    "thumb": "https://static.posters.cz/image/750/locandine-film-in-plexiglass-batman-prowl-comic-cover-i69653.jpg",

                    "price": "$3.99",

                    "series": "Batman",

                    "type": "comic book",

                },

                {

                    "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/5/50/Batman_Beyond_v.1_1.jpg",

                    "price": "$2.99",

                    "series": "Batman Beyond",

                    "type": "comic book",

                },

                {

                    "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/0/0d/Batman_Superman_Vol_1_1.jpg",

                    "price": "$3.99",

                    "series": "Batman/Superman",

                    "type": "comic book",

                },

                {

                    "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/c/cf/Batman_Superman_Annual_Vol_2_1.jpg",

                    "price": "$4.99",

                    "series": "Batman/Superman Annual",

                    "type": "comic book",

                },

                {

                    "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/5/54/Batman_The_Joker_War_Zone_Vol_1_1.jpg",

                    "price": "$5.99",

                    "series": "Batman: The Joker War Zone",

                    "type": "comic book",

                },

                {

                    "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/6/64/Batman_Three_Jokers_Collected.jpg",

                    "price": "$6.99",

                    "series": "Batman: Three Jokers",

                    "type": "comic book",

                },

                {

                    "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/f/f8/Batman_White_Knight_Presents_Harley_Quinn_Vol_1_1.jpg",

                    "price": "$4.99",

                    "series": "Batman: White Knight Presents: Harley Quinn",

                    "type": "comic book",

                },

                {

                    "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/c/c8/Catwoman_Vol_2_1.jpg",

                    "price": "$16.99",

                    "series": "Catwoman",

                    "type": "graphic novel",

                },

                ],
        }
    },
}

</script>


<template>

    <div class="content-background">
        <div class="container">
            <span class="series">current series</span>
            <div class="comics-row">
                <SingleComic  v-for="(comic, index) in comicsList" :key="index"
                    :propsThumb="comic.thumb"
                    :propsTitle="comic.series"
                />
            </div>
            <div class="loadMore">
                <button type="button">load more</button>
            </div>
        </div>
    </div>

</template>



<style lang="scss" scoped>
@use '../assets/style/partials/variables' as *;
@use '../assets/style/partials/mixins' as *;

.content-background{
    color: white;
    background-color: $content-black;

    .container{
        @include container;
        padding-block: 40px 20px;
        position: relative;

        .comics-row{
            display: flex;
            flex-wrap: wrap;
            row-gap: 80px;
            column-gap: 35px;
            margin-bottom: 100px;
        }

    }

}

.series{
    background-color: $blue-color;
    text-transform: uppercase;
    font-weight: bolder;
    font-size: 1.2rem;
    padding: 10px 25px;
    position: absolute;
    top: -20px;
    left: -10px;
}

.loadMore{
    margin:0 auto;
    width: fit-content;
    button{
        border: none;
        color: white;
        padding: 10px 60px;
        background-color: $blue-color;
        text-transform: uppercase;
        font-weight: bolder;
        cursor: pointer;
    }
}

</style>
