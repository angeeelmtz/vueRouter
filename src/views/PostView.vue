<template>
    <div class="post">
        <h1>Post view del elemento : {{ postId }}</h1>
    </div>
</template>

<script setup>
    import { onMounted, ref } from 'vue'
    import { useRoute } from 'vue-router'

    let postId = ref('')

    onMounted( () => {
        const route = useRoute()
        postId.value = route.params.id
    })

</script>

<style scoped>
</style>