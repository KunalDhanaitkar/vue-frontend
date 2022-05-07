<template>

    <div class="pTitle">
        <h1>{{pageTitle}}</h1>   
    </div>

    <div class="pDesc">
        <h2>{{pageDesc}}</h2>
    </div>

</template>

<script>

export default{
    name: 'AppHeader',
    props:{
        pageTitle: String,
        pageDesc: String
    }
}    

</script>

<style scoped>

div{
    text-align: center;
}

h1{
    color: green;
    font-size: 50px;
    font-weight: 1000;
    text-decoration: underline;
    padding-bottom: 2px;
}

h2{
    color: rgb(0, 81, 255);
    padding-bottom: 2px;
}

</style>