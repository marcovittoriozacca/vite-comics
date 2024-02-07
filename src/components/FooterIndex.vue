<script>


export default{
    name: 'FooterIndex',

    data(){
        return{
            footerList: [

                {
                    title: 'DC COMICS',
                    listElements:[
                        {
                            name: 'Characters',
                            url: '#'
                        },
                        {
                            name: 'Comics',
                            url: '#'
                        },
                        {
                            name: 'Movies',
                            url: '#'
                        },
                        {
                            name: 'TV',
                            url: '#'
                        },
                        {
                            name: 'GAMES',
                            url: '#'
                        },
                        {
                            name: 'Videos',
                            url: '#'
                        },
                        {
                            name: 'News',
                            url: '#'
                        },
                    ]
                },
                {
                    title: 'SHOP',
                    listElements:[
                        {
                            name: 'Shop DC',
                            url: '#'
                        },
                        {
                            name: 'Shop DC Collectibles',
                            url: '#'
                        },
                    ]
                },
                {
                    title: 'DC',
                    listElements:[
                        {
                            name: 'Terms Of Use',
                            url: '#'
                        },
                        {
                            name: 'Privacy policy (New)',
                            url: '#'
                        },
                        {
                            name: 'Ad Choices',
                            url: '#'
                        },
                        {
                            name: 'Advertising',
                            url: '#'
                        },
                        {
                            name: 'Jobs',
                            url: '#'
                        },
                        {
                            name: 'Subscriptions',
                            url: '#'
                        },
                        {
                            name: 'Talent Workshops',
                            url: '#'
                        },
                        {
                            name: 'CPSC Certificates',
                            url: '#'
                        },
                        {
                            name: 'Ratings',
                            url: '#'
                        },
                        {
                            name: 'Shope Help',
                            url: '#'
                        },
                        {
                            name: 'Contact Us',
                            url: '#'
                        },
                    ]
                },
                {
                    title: 'SITES',
                    listElements:[
                        {
                            name: 'DC',
                            url: '#'
                        },
                        {
                            name: 'MAD Magazine',
                            url: '#'
                        },
                        {
                            name: 'DC Kids',
                            url: '#'
                        },
                        {
                            name: 'DC Universe',
                            url: '#'
                        },
                        {
                            name: 'DC Power Visa',
                            url: '#'
                        },
                    ]
                },

            ]
            
        }
    }
}

</script>


<template>

<div class="footer-bg">
    <div class="container">
        <nav>
            <ul v-for="(list, index) in footerList" :key="index">
                <li class="listTitle">
                    {{ list.title }}
                </li>
                <li v-for="(listElement, index) in list.listElements" :key="index">
                    <a :href="listElement.url" class="listLink">
                        {{ listElement.name }}
                    </a>
                </li>
            </ul>
        </nav>
    
        <figure>
            <img src="../assets/img/dc-logo-bg.png" alt="">
        </figure>
    </div>
</div>

</template>



<style lang="scss" scoped>
@use '../assets/style/partials/variables' as *;
@use '../assets/style/partials/mixins' as *;

.footer-bg{
    background-image: url('../assets/img/footer-bg.jpg');
    @include background-reset;
    height: 400px;
    
    .container{
        @include container;
        display: flex;
        justify-content: space-between;
        align-items: center;
        height: 100%;
        overflow: hidden;

        nav{
            display: flex;
            flex-direction: column;
            flex-wrap: wrap;
            column-gap: 45px;
            max-height: 100%;

            ul{
                margin-block: 10px;
    
                .listTitle{
                    color: white;
                    font-size: 1.2rem;
                    margin-bottom: 10px;
                }
                
                li{
                    padding-block: 5px;
        
                    .listLink{
                        
                        color: gray;
                        font-size: 0.9rem;
                        &:hover{
                            color: white;
                        }
                    }
                }
            }
        }

    }

}
</style>
