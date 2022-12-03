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
        border: 5px solid #4C5270;
        padding: 2px;
    }
    h1{
        color: #DB1F48;
    }
    
    </style>