<template>
    <div>
        <h1>Example of Life Cycle Component</h1>
    </div>
</template>

<script>
    export default {
        mounted: function() {
            console.log(`I am in mounted`);
        },
        beforeCreate: function() {
            console.log(`I am in beforeCreate`);
        },
        beforeMount: function() {
            console.log(`I am in beforeMount`);
        },
        created: function() {
            console.log(`I am in created`);
        },
    }
</script>

<style scoped>
    h1 {
        color: red;
    }
</style>