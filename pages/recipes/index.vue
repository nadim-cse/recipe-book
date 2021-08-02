<template>
    <section class="recipes">
        <Recipe 
        v-for="recipe in recipes"
         :key="recipe.id"
            :thumbnail="recipe.thumbnail"
            :title="recipe.title"
            :id="recipe.id"
            :previewText="recipe.previewText"
        />
        
    </section>
</template>

<script>
import Recipe from '@/components/Recipe';
export default {
    components:{
        Recipe
    },
    asyncData(){
        return new Promise((resolve, reject) => {
            setTimeout(() => {
                resolve({
                    recipes:[
                        {
                            id: "1",
                            title: "Delcious Pizza",
                            previewText: "This is preview text",
                            thumbnail: "https://upload.wikimedia.org/wikipedia/commons/5/53/Hot_chorizo_links.jpg"
                        },
                        {
                            id: "2",
                            title: "Delcious Chowmine",
                            previewText: "This is preview text",
                            thumbnail: "https://www.celebrationinmykitchen.com/uploads/4/8/6/2/48622077/noodles2_orig.jpg"
                        },
                        {
                            id: "3",
                            title: "Delcious burger",
                            previewText: "This is preview text",
                            thumbnail: "https://images.unsplash.com/photo-1571091718767-18b5b1457add?ixid=MnwxMjA3fDB8MHxzZWFyY2h8NXx8YnVyZ2VyfGVufDB8fDB8fA%3D%3D&ixlib=rb-1.2.1&w=1000&q=80"
                        }
                    ]
                })
            },1500);
        });
    }
}
</script>

<style scoped>

.recipes{
    display: flex;
    flex-flow: row wrap;
    justify-content: center;
    align-items: center;
}

</style>