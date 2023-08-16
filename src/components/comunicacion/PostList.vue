<template>
    <div class="container">
        <h1 style="text-align:center">Listado de Posts</h1>
        <div class="row">
            <div class="col-md-6 mx-auto">

                <PostComponent v-for="(post, index) in data" :key="index" :title="post.title" :content="post.content"
                    @sayHi="showAlert" :number="index" />
            </div>
        </div>
    </div>
</template>

<script setup>
//import {ref} from 'vue'
import PostComponent from './PostComponent.vue'

let data = [
    {
        title: 'Título 1',
        content: 'Contenido de post 1',
    },
    {
        title: 'Título 2',
        content: 'Contenido de post 2',
    },
    {
        title: 'Título 3',
        content: 'Contenido de post 3',
    },
    {
        title: 'Título 4',
        content: 'Contenido de post 4',
    }
]

function showAlert(msg) {
    alert("este es un mensaje generado desde el padre con el mensaje: " + msg);
}

</script>

<style scoped></style>