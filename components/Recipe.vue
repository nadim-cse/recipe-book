<template>
     <nuxt-link :to="'recipes/'+ id">
         <article class="recipe">
            <div class="thumbnail" :style="{backgroundImage: 'url('+ thumbnail +')'}"></div>
            <h1>{{title}}</h1>
            <p>{{previewText}}</p>
        </article>
     </nuxt-link>
</template>

<script>
export default {
    props:['thumbnail', 'title', 'previewText', 'id']
}
</script>
<style scoped>
a{
    text-decoration: none;
    color:green;
}
.recipe{
    box-sizing: border-box;
    width: 280px;
    padding: 8px;
    border: 1px solid gray;
    box-shadow: 0 2px 2px #aaa;
    margin-left: 10px;
}
.thumbnail{
    background-position: center;
    background-size: cover;
    height: 200px;
}
</style>