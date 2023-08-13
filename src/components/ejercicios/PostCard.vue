<template>
<div class="post-card">
    <h3>Título</h3>
    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Voluptates quo cumque eos quaerat ab repellendus commodi laudantium, sapiente eaque inventore exercitationem dolorum delectus vitae minima iste eveniet ipsa! Accusamus, quibusdam!</p>
    <PostButton></PostButton>
</div>
</template>

<script setup>
    import PostButton from './PostButton.vue';
</script>

<style scoped>
.post-card{
    border-radius: 15px;
    padding: 10px;
    margin: 5px;
    border: 1px solid #ccc;
}
</style>