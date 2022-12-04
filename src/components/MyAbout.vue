<template>
    <div>
        <h4> {{About}} </h4>
    </div>
    
</template>

<script>
export default {
    name: 'MyAbout',
    props:{
        About: String
    }
}
</script>

<style scoped>
div{
    text-align: center;
    border: 5px solid black;
    background-color: #f4a261;
    padding: 10px;
}
</style>