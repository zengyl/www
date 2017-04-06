<template>
  <div id="app">
    <img src="./assets/logo.png">
    <h1>{{ msg }}</h1>
 	<ul>
 		<li><router-link to="/first">点我跳转到第一页</router-link></li>
 		<li><router-link to="/second">点我跳转到第二页</router-link></li>
    <li><router-link to="/third">点我跳转到第三页</router-link></li>
 	</ul>
 	<router-view class="view"></router-view>
    <h2>--------------------------</h2>
    <me name="zengyl" age="22"></me>
    <firstcomponent></firstcomponent>
    <secondcomponent></secondcomponent>
  </div>
</template>

<script>
	import firstcomponent from './component/firstcomponent.vue'
	import secondcomponent from './component/secondcomponent.vue'
  import me from './component/me.vue'
	export default {
		data () {
			return {
				msg: 'hello Vue'
			}
		},
		components: { firstcomponent ,secondcomponent,me} // 挂载组件
	}
</script>

<style>
	body {
		font-family: Helvetica, sans-serif;
	}
</style>