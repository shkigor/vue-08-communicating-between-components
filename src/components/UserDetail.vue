<template>
    <div class="col-xs-12 col-sm-6">
        <div class="component">
            <h3>You may view the User Details here</h3>
            <p>Many Details</p>
            <p>User Name: {{ switchName() }}</p>
            <p>My Name: {{ myName }}</p>
            <p>User Age: {{ userAge }}</p>
            <button @click="resetName">Reset Name</button>
            <button @click="resetFn()">Reset Name</button>
        </div>
    </div>
</template>

<script>
    export default {
        props: {
            name: {
                type: String,
                required: true,
                // default: 'Max'
            },
            myName: [String, Array],
            resetFn: Function,
            userAge: Number
        },
        methods: {
            switchName() {
                return this.name.split("").reverse().join("");
            },
            resetName() {
                // this.name = 'Max'; // vue.runtime.esm.js?2b0e:619 [Vue warn]: Avoid mutating a prop directly since the value will be overwritten whenever the parent component re-renders. Instead, use a data or computed property based on the prop's value. Prop being mutated: "name"
                this.$emit('nameWasReset', 'Max');
            }
        }
    }
</script>

<style scoped>
    div {
        background-color: lightcoral;
    }
</style>
