<script setup>
const headingStyle = 'color:blue'
const paraStyle = 'text-decoration:underline'
const imagePath = '../public/images/02.png'
</script>
 
<template>
    <h1 v-bind:style = "headingStyle">INT203</h1>
    <p :style = "paraStyle">Thanawat</p>
    <img src="./assets/logo.png"/>
    <img :src="imagePath" alt="" srcset=""/>

</template>
 
<style>

</style>