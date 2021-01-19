<template>
    <div class="goal-item" v-bind:class="{'is-complete': goal.completed}">
        <p>
            <input type="checkbox" v-on:change="markComplete">
            {{goal.title}}</p>
    </div>
</template>

<script>
export default {
    name: "GoalItem",
    props: ["goal"],
    methods: {
        markComplete(){
            this.goal.completed = !this.goal.completed;
        }
    }
}
</script>

<style scoped>
    .goal-item {
        padding: 10px;
        border-bottom: 1px #ccc dotted;
    }

    .is-complete {
        text-decoration: line-through;
    }
</style>