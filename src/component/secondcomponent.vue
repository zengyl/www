<template>
  <div id="secondcomponent">
    <h1>I am another page[secondcomponent]</h1>
    <ul>
      <li v-for="article in articles">
        {{article.title}}
      </li>
    </ul>
    <p> 感谢 <a href="https://github.com/showonne">showonne</a>大神的技术指导</p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      author: "微信公众号 jinkey-love",
      articles: [],
    }
  },
  mounted: function() {
    this.$http.jsonp('https://api.douban.com/v2/movie/top250?count=10', {}, {
        headers: {

        },
        emulateJSON: true
    }).then(function(response) {
      // 这里是处理正确的回调

        this.articles = response.data.subjects
        // this.articles = response.data["subjects"] 也可以

    }, function(response) {
        // 这里是处理错误的回调
        console.log(response)
    });
  }
}

</script>

<style>
  #secondcomponent {
    border: 2px solid #00dbf5;
  }
</style>