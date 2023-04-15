<template>
    <div>
        <h3>{{ blog_title }}</h3>
        <p>{{ blog_content }}</p>
        <img :src="blog_image_url" alt="Blog Image">
    </div>
</template>

<script>
    export default {
        data() {
            return {
                blog_title: `Jeff Blog`,
                blog_image_url: `https://images.unsplash.com/photo-1486312338219-ce68d2c6f44d?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1172&q=80`,
                blog_content: `We gotta burn the rain forest, dump toxic waste, pollute the air, and rip up the OZONE! 'Cause maybe if we screw up this planet enough, they won't want it anymore! We gotta burn the rain forest, dump toxic waste, pollute the air, and rip up the OZONE! 'Cause maybe if we screw up this planet enough, they won't want it anymore!`
            }
        },
    }
</script>

<style scoped>

</style>