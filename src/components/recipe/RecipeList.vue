<template>
    <div class="recipe__list-recipe row" >

        <recipe-card v-for="recipe in recipes" :data="recipe">
        </recipe-card>

    </div>
</template>

<script setup>
    import RecipeCard from "./RecipeCard.vue";
    defineProps({
        recipes: Array
    })
</script>