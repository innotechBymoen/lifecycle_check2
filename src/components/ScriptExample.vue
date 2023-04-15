<template>
    <div>
        <h1>I AM THE SCRIPT EXAMPLE</h1>
        <div class="script_container"></div>
    </div>
</template>

<script>
    export default {
        data() {
            return {
                tweets: [`This is the first tweet`,`Second Tweet`,`This is the last tweet`],
                num_friends: 2,
                logged_in: false,
            }
        },
        methods: {
            show_info: function() {
                let script_container = document.querySelector(`.script_container`);
                script_container.insertAdjacentHTML(`beforeend`, `<p>Friends: ${this.num_friends}</p>`);
                if(this.logged_in === true) {
                    script_container.insertAdjacentHTML(`beforeend`, `<p>You are logged in!</p>`);
                } else {
                    script_container.insertAdjacentHTML(`beforeend`, `<p>You are NOT logged in!</p>`);
                }
                for(let i=0; i<this.tweets.length; i++) {
                    script_container.insertAdjacentHTML(`beforeend`, `<p>${this.tweets[i]}</p>`);
                }
            }
        },
        mounted: function(){
            this.show_info();
        }
    }
</script>

<style scoped>

</style>