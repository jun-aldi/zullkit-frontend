<script setup>

import {ref} from 'vue'
import CategoriesCard from '@/components/CategoriesCard.vue'

const categories = ref([
    {id:1, title: 'Mobile UI KIT', count: 731, image:'categories-1.jpg'},
    {id:2, title: 'Font', count: 657, image:'categories-2.jpg'},
    {id:3, title: 'Icon Set', count: 83559, image:'categories-3.jpg'},
    {id:4, title: 'Website Ui kit', count: 74800, image:'categories-4.jpg'}
])


</script>

<template >
    <div class="container px-4 mx-auto my-16 md:px-12 categories" id="categories">
        <h2 class="mb-4 text-xl font-medium md:mb-0 md:text-lg">
            Top Categories
        </h2>
        <div class="flex flex-wrap -mx-1 lg:-mx-4">
            <CategoriesCard v-for="category in categories " 
            :key="category.id" 
            :title="category.title" 
            :count="category.count" 
            :image="category.image" />
        </div>
    </div>
</template>