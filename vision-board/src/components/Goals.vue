<template>
    <div>
        <h1>Goals</h1>
        <div v-bind:key="goal.id" v-for="goal in goals">
            <GoalItem v-bind:goal="goal" />
        </div>
    </div>
    
</template>

<script>
import GoalItem from './GoalItem.vue';
export default {
    name: "Goals",
    components: {
        GoalItem
    },
    props: ["goals"]
    
}
</script>

<style scoped>
h3 {
    margin-top: 10px;
}

</style>