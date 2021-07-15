<template>
    <h1> users ID pages </h1>
</template>

<script>
export default {
    validate(context) {
        // '20a' -> NaN -> false -> !false ->true
        if(!Number(context.params.userId)) {
            return false;
        }   
        return true ;
        
        }
}
</script>