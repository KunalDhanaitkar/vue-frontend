<template>

    <div class="resourcebox">
       
        <div v-for="resource in resources" :key="resource.id">
            
            <ResourceItem :resource="resource"/>

        </div>
        
        

    </div>

</template>

<script>

import ResourceItem from "./ResourceItem.vue"

export default {
    name: 'ResourceBox',
    components: {
    ResourceItem,
},
    props:{
        resources: Array,
    }
}
</script>

<style scoped>

.resourcebox{
    display: grid;
    grid-template-columns: 1fr 1fr 1fr 1fr;
    grid-gap: 0.2rem;
    padding: 1em;
    background-image: url("@/assets/bg.jpg");
}

</style>