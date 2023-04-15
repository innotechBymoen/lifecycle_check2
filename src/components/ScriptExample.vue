<template>
    <div>
        <h1>I AM THE SCRIPT EXAMPLE</h1>
        <div class="script_container"></div>
        <p>Friends: {{num_friends}}</p>
        <p v-if="logged_in === true">You are logged in!</p>
        <p v-else>You are NOT logged in!</p>
        <p v-for="(tweet, i) in tweets" :key="i">{{tweet}}</p>
    </div>
</template>

<script>
    export default {
        data() {
            return {
                tweets: [`This is the first tweet`,`<h1>Second Tweet</h1>`,`This is the last tweet`],
                num_friends: 2,
                logged_in: true,
            }
        },
    }
</script>

<style scoped>
    p {
        margin: 30px;
    }
</style>