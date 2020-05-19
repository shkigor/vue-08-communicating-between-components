<template>
    <div class="col-xs-12 col-sm-6">
        <div class="component">
            <h3>You may edit the User here</h3>
            <p>Edit me!</p>
            <p>User Age: {{ userAge }}</p>
            <button @click="editAge">Edit Age</button>
        </div>
    </div>
</template>

<script>
    import { eventBus } from '../main';

    export default {
        props: ['userAge'],
        methods: {
            editAge() {
                // this.$emit('ageWasEdited', 30)
                // eventBus.$emit('ageWasEdited', 30);
                eventBus.changeAge(30);
            }
        }
    }
</script>

<style scoped>
    div {
        background-color: lightgreen;
    }
</style>
