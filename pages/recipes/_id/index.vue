<template>
   <section class="single-recipe">
       <h1>Title: {{ recipe.title}}</h1>
       <div>
           <img class="recipe-image" :src="recipe.thumbnail" :alt="recipe.title">
       </div>
       <p>Description: {{recipe.descriptionText}}</p>
   </section>
</template>
<script>
export default {
     asyncData(context){
        return new Promise((resolve, reject) => {
            setTimeout(() => {
                resolve({
                    recipe:[
                        {
                            id: "1",
                            title: "Delcious Pizza",
                            previewText: "This is preview text",
                            descriptionText: "Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsu",
                            thumbnail: "https://upload.wikimedia.org/wikipedia/commons/5/53/Hot_chorizo_links.jpg"
                        },
                        {
                            id: "2",
                            title: "Delcious Chowmine",
                            previewText: "This is preview text",
                            descriptionText: "Contrary to popular belief, Lorem Ipsum is not simply random text. It has roots in a piece of classical Latin literature from 45 BC, making it over 2000 years old. Richard McClintock, a Latin professor at Hampden-Sydney College in Virginia, looked up one of the more obscure Latin words, consectetur, from a Lorem Ipsum passage, and going through the cites of the word in classical literature, discovered the undoubtable source. Lorem Ipsum comes from sections 1.10.32 and 1.10.33 of ",
                            thumbnail: "https://www.celebrationinmykitchen.com/uploads/4/8/6/2/48622077/noodles2_orig.jpg"
                        },
                        {
                            id: "3",
                            title: "Delcious burger",
                            previewText: "This is preview text",
                            descriptionText: "There are many variations of passages of Lorem Ipsum available, but the majority have suffered alteration in some form, by injected humour, or randomised words which don't look even slightly believable. If you are going to use a passage of Lorem Ipsum, you need to be sure there isn't anything embarrassing hidden in the middle of text. All the Lorem Ipsum generators on the Internet tend to repeat predefined chunks as necessary, making this the first true generator on the Internet. It uses a dictionary of over 200 Latin words, combined with a handful of model sentence structures, to generate Lorem Ipsum which looks reasonable. The generated Lorem Ipsum is therefore always free from repetition, injected humour, or non-characteristic words etc.",
                            thumbnail: "https://images.unsplash.com/photo-1571091718767-18b5b1457add?ixid=MnwxMjA3fDB8MHxzZWFyY2h8NXx8YnVyZ2VyfGVufDB8fDB8fA%3D%3D&ixlib=rb-1.2.1&w=1000&q=80"
                        }
                    ].find(el => el.id == context.params.id)
                })
            },1500);
        });
    }
}
</script>
<style scoped>
.single-recipe{
    display: flex;
    flex-flow: column;
    justify-content: center;
    align-items: center;
    text-align: center;
    padding: 30px;
}
.recipe-image{
    width: 100%;
    height: 400px;
}
</style>