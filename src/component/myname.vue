<template>
    <div id="myname">子组件--我的名字是{{name}}</div>
</template>

<script>
    export default{
        props: ["name"]
    }
</script>