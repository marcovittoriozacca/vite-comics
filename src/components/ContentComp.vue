<script>

export default{
    name: 'ContentComp',
}

</script>


<template>

    <div class="content-background">
        <div>
            <h1> --&gt Content goes here &lt-- </h1>
        </div>
    </div>

</template>



<style lang="scss" scoped>
@use '../assets/style/partials/variables' as *;
@use '../assets/style/partials/mixins' as *;

.content-background{
    color: white;
    background-color: $content-black;

    div{
        @include container;
        
        h1{
            padding-block: 40px;
        }
    }

}

</style>
