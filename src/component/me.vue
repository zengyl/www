<!-- <template>
    <div id="me">
    	<h2>父组件</h2>
        <myname name="jack"></myname>
        <myage age="18"></myage>
    </div>
</template>

<script>
    import age  from "./myage.vue";
    import name  from "./myname.vue";

    export default{
        components:{"myname":name, "myage":age}
    }
</script>

<style>
	#me {
		border:1px solid red;
	}
</style> -->

<template>
    <div id="me">
        <myname v-bind:name="name"></myname>
        <myage v-bind:age="age"></myage>
    </div>
</template>

<script>
    import age  from "./myage.vue";
    import name  from "./myname.vue";

    export default{
        props:["name","age"],
        components:{"myname":name, "myage":age}
    }
</script>