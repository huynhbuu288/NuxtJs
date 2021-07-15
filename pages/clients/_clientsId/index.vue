<template>
    <h1> clients pages -id= {{ $route.params.clientsId }} </h1>
</template>

<script>
export default {
    mounted() {
        console.log(this.$route.params.clientsId);
    },
}
</script> 