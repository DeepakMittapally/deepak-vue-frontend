<template>
    <div>
        <h1>{{titleName}}</h1>
        <h2>{{details}}</h2>
    </div>
    </template>
    
    <script>
    export default {
        name: 'MyHeader',
        props:{
            titleName: String,
            details:String
        }   
    }
    </script>
    
    <style scoped>
    div{
        text-align: center;
        border: 5px solid black;
        padding: 2px;
        background-color: #264653;
    }
    h1{
        color: black;
    }
    
    </style>