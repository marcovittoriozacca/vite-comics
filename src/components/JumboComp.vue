<script>
export default {
    name: 'JumboComp',

}

</script>


<template>

<div></div>

</template>

<style lang="scss" scoped>
@use '../assets/style/partials/mixins' as *;

div{
    height: 450px;
    background-image: url('../assets/img/jumbotron.jpg');
    @include background-reset;
    background-position-y: top;
}
</style>