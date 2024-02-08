<script>
export default {
    name: 'SingleComic',

    props: {
        propsThumb: String,
        propsTitle: String,

    }
}

</script>

<template>
    <div class="comic-box">
        <figure>
            <a href="#">
                <img :src="propsThumb" :alt="propsTitle">
                <p>{{ propsTitle }}</p>
            </a>
        </figure>
    </div>
</template>

<style lang="scss" scoped>

.comic-box{
    margin: 0 auto;
    width: calc( 100% / 6 - 30px );
    aspect-ratio: 1/1.2;

    figure{
        width: 100%;
        height: 100%;
        img{
            width: 100%;
            height: 100%;
            object-fit: fill;
        }
    }
}

a{
    color: white;
    text-transform: uppercase;
    p{
        margin-top: 15px;
        font-size: 0.9rem;
    }
}

</style>