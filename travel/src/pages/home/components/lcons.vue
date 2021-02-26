<template>
  <div class="icons">
    <swiper >
      <swiper-slide v-for="(page, index) of pages" :key="index">
        <div class="icon" v-for="item of page" :key = item.id>
          <div class="icon-img">
            <img class="icon-img-connent" :src="item.imgUrl">
          </div>
          <p class="icon-title">{{item.title}}</p>
        </div>
      </swiper-slide>

    </swiper>
  </div>
</template>

<script>
export default {
  name: 'HomeIcons',
  data () {
    return {
      iconsList: [{
        id: '001',
        title: '景点门票',
        imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png'
      }, {
        id: '002',
        title: '一日游',
        imgUrl: 'http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20193/f0f00d6dfe038c044dbc9a437f58b0eb.png'
      }, {
        id: '003',
        title: '北京必游',
        imgUrl: 'http://img1.qunarzz.com/piao/fusion/1804/ff/fdf170ee89594b02.png'
      }, {
        id: '004',
        title: '水上乐园',
        imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/3e/86314b2af03b7502.png'
      }, {
        id: '005',
        title: '爬长城',
        imgUrl: 'http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20191/0334cf5430b9b5505fd79e2b8d7e8670.png'
      }, {
        id: '006',
        title: '故宫',
        imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/6c/9e54a8540fee0102.png'
      }, {
        id: '007',
        title: '动植物园',
        imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/76/eb88861d78fb9902.png'
      }, {
        id: '008',
        title: '野生动物园',
        imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/fa/2548667cb6e902.png'
      }, {
        id: '009',
        title: '北京世园会',
        imgUrl: 'http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20194/b4511345827006994aa1980a3886f0ac.png'
      }]
    }
  },
  computed: {
    pages () {
      const pages = []
      this.iconsList.forEach((item, index) => {
        const page = Math.floor(index / 8)
        if (!pages[page]) {
          pages[page] = []
        }
        pages[page].push(item)
      })
      return pages
    }
  }
}
</script>

<style lang="stylus" scoped>
@import '~styles/varibles.styl'
@import '~styles/mixins.styl'
  .icons >>> .swiper-container
    width : 100%
    height : 0
    padding-bottom : 50%
  .icons
    overflow : hidden
    width : 100%
    height : 0
    padding-bottom : 50%
    // background green
    .icon
      width 25%
      float left
      height 0
      padding-bottom 25%
      position relative
      .icon-img
        overflow hidden
        position absolute
        top 0
        right 0
        left 0
        bottom .4rem
        box-sizing border-box
        padding .1rem
        .icon-img-connent
          height 100%
          margin 0 auto
          display block
      .icon-title
        height .4rem
        bottom 0
        left 0
        right 0
        position absolute
        text-align center
        line-height .4rem
        color $darkTextColor
        ellipsis()
      // background red
</style>
