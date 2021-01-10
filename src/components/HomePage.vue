<template>
    <div class="page">
        <h1>{{msg}}</h1>
    </div>
</template>

<script>
export default {
    name: "HomePage",
    props: {
        msg: String
    }
}
</script>

<style scoped>
h1 {
    color: #42b983;
}
</style>