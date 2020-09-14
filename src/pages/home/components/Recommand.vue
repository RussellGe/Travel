<template>
    <div>
      <div class="recommand-title">热销推荐</div>
      <ul>
        <li class="item" v-for='item of recommendList' :key='item.id'>
        <div class="item-img-wrapper">
            <img  class="item-img" :src="item.imgUrl" alt="">
        </div>
        <div class="item-info">
            <p class="item-title">{{item.title}}</p>
            <p class="item-desc">{{item.desc}}</p>
            <button class="item-button">查看详情</button>
        </div>
        </li>
      </ul>
    </div>
</template>

<script>
export default {
  name: 'HomeRecommand',
  data () {
    return {
      recommendList: [{
        id: '0001',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1508/2e/d9363ce50a88c8c5ff5a138c67687cd4.water.jpg_200x200_1c15c8f5.jpg',
        title: '世界之窗',
        desc: '全球微缩景观，精彩演绎娱乐项目应有尽有'
      }, {
        id: '0002',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1902/f2/f2e0213052717f7ca3.water.jpg_200x200_816c1b48.jpg',
        title: '世界之窗',
        desc: '全球微缩景观，精彩演绎娱乐项目应有尽有'
      }, {
        id: '0003',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1902/f2/f2e0213052717f7ca3.water.jpg_200x200_816c1b48.jpg',
        title: '世界之窗',
        desc: '全球微缩景观，精彩演绎娱乐项目应有尽有'
      }, {
        id: '0004',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1902/f2/f2e0213052717f7ca3.water.jpg_200x200_816c1b48.jpg',
        title: '世界之窗',
        desc: '全球微缩景观，精彩演绎娱乐项目应有尽有'
      }]
    }
  }
}
</script>

<style lang="stylus" scoped>
  @import '~styles/mixin.styl'
  .recommand-title
    line-height: .8rem
    background: #eeeeee
    text-indent: .2rem
    margin-top: .2rem
  .item
    display: flex
    height: 1.9rem
    overflow: hidden
    .item-img
      width: 1.7rem
      height: 1.7rem
      padding: .1rem
    .item-info
      flex: 1
      padding: .1rem
      min-width: 0
      .item-title
        line-height: .54rem
        font-size: .32rem
        ellipsis()
      .item-desc
        line-height: .4rem
        color: #ccc
        ellipsis()
      .item-button
        line-height: .44rem
        color: #ffffff
        margin-top: .16rem
        background: #ff9300
        padding: 0 .2rem
        border-radius: .06rem

</style>
