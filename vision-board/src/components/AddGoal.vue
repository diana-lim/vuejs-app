<template>
    <div>
        <form @submit="addGoal">
            <input type="text" v-model="title" name="title" placeholder="Add Goal...">
            <input type="submit" value="Submit" class="btn">
        </form>
    </div>
</template>

<script>
import uuid from 'uuid';
export default {
    name: "AddGoal",
    data() {
        return {
            title: ''
        }
    },
    methods: {
        addGoal(e) {
            e.preventDefault();
            const newGoal = {
                id: uuid.v4(),
                title: this.title,
                completed: false
            }
            // Send up to parent
            this.$emit('add-goal', newGoal);
        }
    }
    
}
</script>

<style scoped>

    form {
        display: flex;
    }

    input[type="text"]{
        flex: 10;
        padding: 5px;
    }

    input[type="submit"]{
        flex: 2;
    }

</style>