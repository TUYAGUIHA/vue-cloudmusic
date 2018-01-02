<template>
  <div>
    <div class="slider">
      <slider v-bind="setting"></slider>
    </div>
    <div class="recomand">
      <h1>推荐歌单</h1>
      <dl>
        <dd>
          <div class="daliy">
            <h3>星期四</h3>
            <h2>23</h2>
          </div>
          <span >每日歌曲推荐</span>
        </dd>
      </dl>
    </div>

    <div class="proper">
      <h1>独家放送</h1>
      <dl>
        <cover down="true" width="30%" img-src="static/img/10.jpg" introduce="音乐专栏 这些超级音乐组合是如何制造混沌的？"></cover>
        <cover down="true" width="30%" img-src="static/img/11.jpg" introduce="音乐专栏 最暖心的十首父女之歌"></cover>
        <cover down="true" width="30%" img-src="static/img/12.jpg" introduce="征文大赛 有没有一首歌让你想起ta"></cover>
      </dl>
    </div>

  </div>
</template>
<script >
  import Cover from './cover'
  import Slider from 'vue-image-scroll'
  export default {
    components: {
      Cover,
      Slider
    },
    data () {
      return {
        setting: {
          styleObject: {
            width: '750',
            height: '250'
          },
          image: [
            {
              src: 'static/img/1-1.jpg',
              tagName: '活动',
              tagStyle: {
                backgroundColor: 'blue'
              }
            },
            {
              src: 'static/img/1-2.jpg',
              tagName: '专栏'
            },
            {
              src: 'static/img/1-3.jpg',
              tagName: '活动',
              tagStyle: {
                backgroundColor: 'blue'
              }
            },
            {
              src: 'static/img/1-4.jpg',
              tagName: '专栏'
            },
            {
              src: 'static/img/1-5.jpg',
              tagName: '活动',
              tagStyle: {
                backgroundColor: 'blue'
              }
            }
          ],
          interval: 4000
        }
      }
    }
  }
</script>
<style scoped>
  *{
    box-sizing: border-box;
  }

  .slider{
    margin-top: 20px;
  }

  .recomand{
    width: 100%;
    height: 450px;
  }

  .recomand > h1,
  .proper > h1{
    line-height: 40px;
    font-size: 20px;
    font-weight:200;
    border-bottom: 1px solid rgb(225,225,226);
  }

  .recomand dl{
    display: flex;
    flex-direction: row;
    flex-wrap: wrap;
    justify-content: space-between;
    align-items: flex-start;
    align-content: space-around;
    height: 380px;
  }

  dd{
    display: inline-block;
    width: 17%;
    height: 170px;
    font-size: 12px;
    line-height: 2;
    cursor: pointer;
  }

  .daliy{
    width: 100%;
    height: 140px;
    border: 1px solid rgb(225,225,226);
    text-align: center;
    color: rgb(102,102,102);
  }

  .daliy h3{
    height: 40px;
    line-height: 40px;
    font-size: 15px;
    font-weight: normal;
  }

  .daliy h2{
    height: 80px;
    line-height: 80px;
    font-size: 80px;
    color: rgb(198,47,47);
  }


  .proper{
    width: 100%;
    height: 280px;
  }

  .proper dl{
    display: flex;
    flex-direction: row;
    flex-wrap: wrap;
    justify-content: space-between;
    align-items: flex-start;
    align-content: space-around;
    height: 180px;
  }

</style>
