<template>
  <div id="firstcomponent">
    <h1>I am a title.[firstcomponent]</h1>
    <a> written by {{ author }} </a>
  </div>
</template>

<script type="text/javascript">
export default {
  data () {
    return {
      author: "微信公众号 zeyoln"
    }
  }
}
</script>

<style>
	#firstcomponent {
		border: 2px solid #00dbf5;
	}
</style>