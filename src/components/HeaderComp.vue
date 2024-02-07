<script>
export default{
    name: 'HeaderComp',

    data(){
        return{
            navLinks: [
                {
                    name: 'CHARACTERS',
                    link: '#',
                    activeLink: false,
                },
                {
                    name: 'COMICS',
                    link: '#',
                    activeLink: true,
                },
                {
                    name: 'MOVIES',
                    link: '#',
                    activeLink: false,
                },
                {
                    name: 'TV',
                    link: '#',
                    activeLink: false,
                },
                {
                    name: 'GAMES',
                    link: '#',
                    activeLink: false,
                },
                {
                    name: 'COLLECTIBLES',
                    link: '#',
                    activeLink: false,
                },
                {
                    name: 'VIDEOS',
                    link: '#',
                    activeLink: false,
                },
                {
                    name: 'FANS',
                    link: '#',
                    activeLink: false,
                },
                {
                    name: 'NEWS',
                    link: '#',
                    activeLink: false,
                },
                {
                    name: 'SHOP',
                    link: '#',
                    activeLink: false,
                },
            ]
        }
    }

}

</script>



<template>
  
  <header>
    <nav>
        <figure>
            <img src="/img/dc-logo.png" alt="DC-LOGO" width="80">
        </figure>

        <ul>
            <li v-for="(element, index) in navLinks" :key="index" :class="element.activeLink ? 'active':''">
            <a :href="element.link" target="_blank" >
                {{ element.name }}
            </a>
        </li>
        </ul>
    </nav>

  </header>

</template>

//


<style lang="scss" scoped>
@use '../assets/style/partials/variables' as *;
@use '../assets/style/partials/mixins' as *;

    header{

        nav{
            @include container;
            padding-block: 15px;

            background-color: white;
            font-weight: bold;

            display: flex;
            align-items: center;
            justify-content: space-between;

            ul{
                display: flex;
                column-gap: 30px;

                li{
                    position: relative;
                    &:hover::before{
                        content: '';
                        position: absolute;
                        bottom: -49px;
                        width: 100%;
                        height: 5px;
                        background-color: $blue-color;
                    }
                    a{
                        
                        color: rgb(97, 97, 97);
                        font-size: 0.8rem;
                        &:hover{
                            color: $blue-color;
                        }
                    }
                }
            }

        }
    }
    .active{
        &::before{
            content: '';
                position: absolute;
                bottom: -49px;
                width: 100%;
                height: 5px;
                background-color: $blue-color;
            }
        a{
            color: $blue-color;
        }
    }

</style>
