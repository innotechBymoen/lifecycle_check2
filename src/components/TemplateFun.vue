<template>
    <div>
        <button @click="toggle_post">TOGGLE POST</button>
        <div v-for="(post, i) in posts" :key="i">
            <article v-if="show_post === true">
                <button button @click="hack_post">Hack Blog</button>
                <h3>{{ post[`blog_title`] }}</h3>
                <p>{{ post[`blog_content`] }}</p>
                <img :src="post[`blog_image_url`]" alt="Blog Image">
            </article>
        </div>
        
    </div>
</template>

<script>
    export default {
        methods: {
            hack_post: function() {
                this.blog_content = this.blog_content + `I was injected`;
            },
            toggle_post: function() {
                this.show_post = !this.show_post
            }
        },
        data() {
            return {
                show_post: true,
                posts: [
                    {
                        blog_title: `Jeff Blog`,
                        blog_image_url: `https://images.unsplash.com/photo-1486312338219-ce68d2c6f44d?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1172&q=80`,
                        blog_content: `We gotta burn the rain forest, dump toxic waste, pollute the air, and rip up the OZONE! 'Cause maybe if we screw up this planet enough, they won't want it anymore! We gotta burn the rain forest, dump toxic waste, pollute the air, and rip up the OZONE! 'Cause maybe if we screw up this planet enough, they won't want it anymore!`
                    },
                    {
                        blog_title: `Jeff Blog 2`,
                        blog_image_url: `https://images.unsplash.com/photo-1486312338219-ce68d2c6f44d?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1172&q=80`,
                        blog_content: `2 We gotta burn the rain forest, dump toxic waste, pollute the air, and rip up the OZONE! 'Cause maybe if we screw up this planet enough, they won't want it anymore! We gotta burn the rain forest, dump toxic waste, pollute the air, and rip up the OZONE! 'Cause maybe if we screw up this planet enough, they won't want it anymore!`
                    }
                ]
            }
        },
    }
</script>

<style scoped>

</style>