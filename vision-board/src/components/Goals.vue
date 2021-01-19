<template>
    <div>
        <h1>Goals</h1>
        <div v-bind:key="goal.id" v-for="goal in goals">
            <h3>{{goal.title}}</h3>
        </div>
    </div>
    
</template>

<script>
export default {
    name: "Goals",
    props: ["goals"]
    
}
</script>

<style scoped>
h3 {
    margin-top: 10px;
}

</style>