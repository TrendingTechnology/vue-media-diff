<template>
  <div id="app">
    <div class="intro">
      A useful component to diff media (image, video) by import <a href="https://github.com/MKFMIKU/vue-media-diff">vue-media-diff</a>
      <br>
      <br>
      <img src="http://forthebadge.com/images/badges/built-with-love.svg" alt="">
      <img src="http://forthebadge.com/images/badges/uses-js.svg" alt="">
    </div>

    <div class="demo">
      <section>
        <span>simple diff with image</span>
        <br>
        <br>
        <MediaDiff :origin="origin"
                   :diff="diff"
                   style="width: 540px; height: 400px">
        </MediaDiff>
      </section>

      <section>
        <span>diff image with a cursor</span>
        <br>
        <br>
        <MediaDiff :origin="origin"
                   :diff="diff"
                   cursor="circle"
                   style="width: 540px; height: 400px">
        </MediaDiff>
      </section>

      <section>
        <span>diff video with a cursor</span>
        <br>
        <br>
        <MediaDiff :origin="origin_video"
                   :diff="diff_video"
                   cursor="circle"
                   style="width: 480px; height: 360px">
        </MediaDiff>
      </section>

      <section>
        <span>auto diff video</span>
        <br>
        <br>
        <MediaDiff :origin="origin_video"
                   :diff="diff_video"
                   cursor="circle"
                   style="width: 480px; height: 360px">
        </MediaDiff>
      </section>

    </div>
  </div>
</template>

<script>

  import MediaDiff from './Component.vue';

  export default {
    name: 'app',
    data() {
      return {
        origin: "src/assets/origin.jpg",
        diff: "src/assets/diff.jpg",
        origin_video: "src/assets/diff.mp4",
        diff_video: "src/assets/origin.mp4",
      }
    },
    components: {
      MediaDiff
    },
  }
</script>

<style lang="scss">
  *{
    margin: 0;
    padding: 0;
  }
  #app{
    width: 100%;
    background-color: #fff;
    font-family: Tahoma, Helvetica, Arial, "Microsoft Yahei","微软雅黑", STXihei, "华文细黑", sans-serif;
    a{
      color: #42b883;
    }
  }

  .intro{
    width: 100%;
    text-align: center;
    margin-top: 80px;
  }

  .demo{
    width: 100%;
    padding: 20px;
    margin: 20px auto;
    background-color: #f9f9f9;
    text-align: center;

    section{
      width: 100%;
      text-align: center;
      padding: 36px;
      box-sizing: border-box;
      span{
        font-size: 18px;
        color: #42b883;
      }
    }
  }
</style>
