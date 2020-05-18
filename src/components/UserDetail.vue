<template>
    <div class="col-xs-12 col-sm-6">
        <div class="component">
            <h3>You may view the User Details here</h3>
            <p>Many Details</p>
            <p>User Name: {{ name }}</p>
            <p>My Name: {{ myName }}</p>
        </div>
    </div>
</template>

<script>
    export default {
        props: ['name', 'myName']
    }
</script>

<style scoped>
    div {
        background-color: lightcoral;
    }
</style>
