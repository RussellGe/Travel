<template>
  <div class="icons" >
  <swiper ref="mySwiper" :options="swiperOptions" >
    <swiper-slide v-for="(page,index) of pages" :key="index">
    <div class="icon" v-for="item of page" :key='item.id'>
      <div class="icon-img">
         <img class="icon-img-content" :src="item.imgUrl" alt="">
      </div>
      <p class="icon-desc">{{item.desc}}</p>
    </div></swiper-slide>
    <div class="swiper-pagination" slot="pagination"></div>
    </swiper>
    
  </div>
</template>

<script>
export default {
  name: 'HomeIcons',
  data () {
      return {
          iconList: [{
              id: '0001',
              imgUrl: "http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20209/158387fe5376294f3776d01358d6b73b.png",
              desc: '景点门票'
          },{
              id: '0002',
              imgUrl: "http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20209/69e8b07cb2d438c5530aebd4c8e3abd3.png",
              desc: '一日游'
          },
          {
              id: '0003',
              imgUrl: "http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20209/b7a5e6b1774eda4fc9e32588f1d00c94.png",
              desc: '踏青赏花'
          },
          {
              id: '0004',
              imgUrl: "http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20209/c4c5c620f20535ff358788a508c20921.png",
              desc: '主题乐园'
          },{
              id: '0005',
              imgUrl: "http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20209/59bc59a3c38261e9a3f2f991a9ce0d21.png",
              desc: '深圳必游'
          },{
              id: '0006',
              imgUrl: "http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20209/931f626a44f714d055f9a0f8235170fa.png",
              desc: '海滨海岛'
          },{
              id: '0007',
              imgUrl: "http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20209/557ba25df01d7dbf1419b095a11d1319.png",
              desc: '泡温泉'
          },{
              id: '0008',
              imgUrl: "http://img1.qunarzz.com/piao/fusion/1803/b6/37560ece9c62b502.png",
              desc: '城市观光'
          },{
              id: '0009',
              imgUrl: "http://img1.qunarzz.com/piao/fusion/1803/b6/37560ece9c62b502.png",
              desc: '高空景观'
          },{
              id: '0010',
              imgUrl: "http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20193/a40ee278d67000f2a29d2e20f6a029b3.png",
              desc: '自然风光'
          },]
      }
  },
  computed: {
      pages () {
          const pages = []
          this.iconList.forEach((item,index)=> {
              const page = Math.floor(index/8)
              if(!pages[page]){
                  pages[page] = []
              }
              pages[page].push(item)
          })
          return pages
      }
  }
}
</script>

<style lang='stylus' scoped>
  @import '~styles/varibles.styl'
  @import '~styles/mixin.styl'
  .icons >>> .swiper-container
    height: 0
    padding-bottom: 50%
  .icon
      height: 0
      position: relative
      overflow: hidden
      float: left
      width: 25%
      padding-bottom: 25%
      .icon-img
        position: absolute
        top: 0
        left: 0
        right: 0
        box-sizing: border-box
        padding: .1rem
        bottom: .44rem
        .icon-img-content
          display: block
          height: 100%
          margin: 0 auto
      .icon-desc
        position: absolute
        left: 0
        right: 0
        bottom: 0
        height: .44rem
        line-height: .44rem
        color: $darkTextColor
        text-align: center
        ellipsis()
</style>
