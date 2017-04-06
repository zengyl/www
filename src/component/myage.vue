<style>
    #myage{color:red}
</style>

<template>
    <div id="myage">子组件--我的名字是{{age}}</div>
</template>

<script>
    export default{
        props: ["age"]
    }
</script>