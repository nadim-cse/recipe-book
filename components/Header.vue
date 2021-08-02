<template>
    <header>
        <nav>
            <ul>
                <li><nuxt-link to="/">Home</nuxt-link></li>
                <li><nuxt-link to="/about">About</nuxt-link></li>
                <li><nuxt-link to="/recipes">Recipes</nuxt-link></li>
            </ul>
        </nav>
    </header>
</template>
<style scoped>
nav{
     display: flex;
    flex-flow: column;
    justify-content: center;
    align-items: center;
    text-align: center;
    text-decoration: underline;
}
</style>