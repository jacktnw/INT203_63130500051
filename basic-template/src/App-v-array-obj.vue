<script setup>
const subjects = ['INT201', 'INT202', 'INT203', 'INT204']
const product = {
    productId: 111,
    productName: 'Computer',
    productName: 5000
}
</script>
 
<template>
<ul>
    <li v-for = "(subject, index) in subjects" :key="index">
        index {{ index }}-{{ subject}} 
    </li>
</ul>

<ul>
    <li v-for = "(value, name, index) in product" :key="product.productId">
        productId.
</ul>
</template>
 
<style>

</style>