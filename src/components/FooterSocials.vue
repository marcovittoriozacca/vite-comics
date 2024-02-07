<script>

export default{
    name: 'FooterSocials',

    data(){
        return{
            socials:[
                {
                    name: 'Facebook',
                    icon: '/img/footer-facebook.png',
                    url: '#'
                },
                {
                    name: 'Twitter',
                    icon: '/img/footer-twitter.png',
                    url: '#'
                },
                {
                    name: 'YouTube',
                    icon: '/img/footer-youtube.png',
                    url: '#'
                },
                {
                    name: 'Pinterest',
                    icon: '/img/footer-pinterest.png',
                    url: '#'
                },
                {
                    name: 'Periscope',
                    icon: '/img/footer-periscope.png',
                    url: '#'
                },
            ]
        }
    }
}

</script>



<template>
        
    <div class="footer-socials-background">

        <div class="container">

            <a href="#" class="signUp" target="_blank">
                SIGN-UP NOW!
            </a>

            <div class="socials">
                <a href="#" class="followUs" target="_blank">FOLLOW US</a>
                <a :href="social.url" v-for="(social, index) in socials" :key="index" target="_blank">
                    <figure>
                        <img :src="social.icon" :alt="social.name">
                    </figure>
                </a>
            </div>

        </div>
    </div>

</template>



<style lang="scss" scoped>
@use '../assets/style/partials/variables' as *;
@use '../assets/style/partials/mixins' as *;

.footer-socials-background{
    background-color: #303030;
    .container{
        @include container;
        display: flex;
        justify-content: space-between;
        align-items: center;
        padding-block: 30px;
    }
    .signUp{
        color: white;
        padding: 15px;
        border: 2px solid $blue-color;
    }
    .socials{
        display: flex;
        align-items: center;
        column-gap: 15px;

        .followUs{
            color:  $blue-color;
            font-weight: bold;
            font-size: 1.1rem;
            margin-right: 20px;
        }
    }
}
</style>
