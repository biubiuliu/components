<template>
  <div class="canvas_container">
    <canvas id="c" width="500" height="500">不支持canvas</canvas>
  </div>
</template>
<script>
import { fabric } from 'fabric'
import 'fabric-customise-controls'
export default {
  data() {
    return {
      url: 'https://ss1.bdstatic.com/70cFuXSh_Q1YnxGkpoWK1HF6hhy/it/u=3490585897,1596408482&fm=26&gp=0.jpg',
      imgs: '../../../static/dot-circle.png',
      mdr: '../../../static/rotate-mdr.png'
    }
  },
  mounted() {
    const card = new fabric.Canvas('c')
    fabric.Image.fromURL(this.url, function(oImg) {
      oImg.borderColor = 'black'
      oImg.cornerColor = 'green'
      oImg.cornerSize = 20
      oImg.transparentCorners = false
      card.add(oImg)
    })
    // card.backgroundColor = '#a5b1bd2e'
    var _this = this
    fabric.Object.prototype.customiseCornerIcons({
      settings: {
        borderColor: 'black',
        cornerSize: 22,
        cornerShape: 'circle',
        cornerBackgroundColor: 'white',
        cornerPadding: 0
      },
      tl: {
        icon: _this.imgs
      },
      tr: {
        icon: _this.imgs
      },
      bl: {
        icon: _this.imgs
      },
      br: {
        icon: _this.imgs
      },
      mr: {
        icon: _this.imgs
      },
      ml: {
        icon: _this.imgs
      },
      mt: {
        icon: _this.imgs
      },
      mb: {
        icon: _this.imgs
      },
      mtr: {
        icon: _this.mdr
      }
    }, function() {
      _this.card.renderAll()
    })
  },
  methods: {

  }
}
</script>

<style>
.canvas_container {
  width: 100%;
  height: 200px;
  background: antiquewhite;
}
</style>
