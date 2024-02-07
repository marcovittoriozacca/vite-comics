<script>

export default{
    name: 'ServicesComp',

    data(){
        return{
            services:[
                {
                    icon: '../assets/img/buy-comics-digital-comics.png',
                    title: 'DIGITAL COMICS',
                    link: '#',
                },
                {
                    icon: '../assets/img/buy-comics-merchandise.png',
                    title: 'DC MERCHANDISE',
                    link: '#',
                },
                {
                    icon: '../assets//img/buy-comics-subscriptions.png',
                    title: 'SUBSCRIPTION',
                    link: '#',
                },
                {
                    icon: '../assets//img/buy-comics-shop-locator.png',
                    title: 'COMIC SHOP LOCATOR',
                    link: '#',
                },
                {
                    icon: '../assets//img/buy-dc-power-visa.svg',
                    title: 'DC POWER VISA',
                    link: '#',
                },
            ]

        }
    },
    methods:{

        getImagePath: function (imgPath) {
            let url = new URL(imgPath, import.meta.url).href;
            return url
        }
    }
}

</script>


<template>

    <div class="services-background">
        <div class="container">

            <div v-for="(service, index) in services" :key="index">
                <a :href="service.link" target="_blank">
                    <figure>
                        <img :src="getImagePath(service.icon)" :alt="service.title">
                    </figure>
                    <p>{{ service.title }}</p>
                </a>
            </div>


        </div>
    </div>

</template>



<style lang="scss" scoped>
@use '../assets/style/partials/variables' as *;
@use '../assets/style/partials/mixins' as *;


.services-background{
    background-color: $blue-color;
}
.container{
    @include container;

    display: flex;
    padding-inline: 20px;
    justify-content: space-between;
    align-items: center;
    
    div{
        padding-block: 50px;

        a{
            color: white;
            font-size: 0.8rem;

            display: flex;
            align-items: center;
            column-gap: 20px;

            img{
                height: 50px;
                max-width: 50px;
            }
        }
    }
    
}

</style>
