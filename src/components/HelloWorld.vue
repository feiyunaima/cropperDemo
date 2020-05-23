<template>
  <div class="hello">
    <div style="width:600px;height:600px;">
      <vueCropper
              ref="cropper"
              :img="option.img"
              :outputSize="option.outputSize"
              :outputType="option.outputType"
              :info="true"
              :full="option.full"
              :canMove="option.canMove"
              :canMoveBox="option.canMoveBox"
              :fixedBox="option.fixedBox"
              :original="option.original"
              :autoCrop="option.autoCrop"
              :autoCropWidth="option.autoCropWidth"
              :autoCropHeight="option.autoCropHeight"
              :centerBox="option.centerBox"
              :high="option.high"
              :infoTrue="option.infoTrue"
              :enlarge="option.enlarge"
              @realTime="realTime"
              @imgLoad="imgLoad"
              @cropMoving="cropMoving"></vueCropper>
    </div>
  </div>
</template>

<script>
  import { VueCropper }  from 'vue-cropper'
  export default {
    name: 'HelloWorld',
    components:{VueCropper},
    data () {
      return {
        //https://github.com/xyxiao001/vue-cropper/
        option:{
          img: 'http://img1.vued.vanthink.cn/vued751d13a9cb5376b89cb6719e86f591f3.png',//裁剪图片的地址
          outputSize: 1,//裁剪生成图片的质量
          full: false,//输出原图比例截图 props名full
          autoCrop:true,//    是否默认生成截图框
          outputType:'jpeg || png || webp',//裁剪生成图片的格式
          canMove:true,//上传图片是否可以移动
          canMoveBox:true,//截图框能否拖动
          fixedBox:true,//固定截图框大小 不允许改变
          original:false,//上传图片按照原始比例渲染
          autoCropWidth:'100',//默认生成截图框宽度
          autoCropHeight:'100',//默认生成截图框高度
          centerBox:true,//截图框是否被限制在图片里面
          high:true,//是否按照设备的dpr 输出等比例图片
          infoTrue:false,//true 为展示真实输出图片宽高 false 展示看到的截图框宽高
          enlarge:1,//图片根据截图框输出比例倍数
          maxImgSize:2000,//限制图片最大宽度和高度
        },
      }
    },
    methods:{
      realTime(){ },
      imgLoad(){ },
      cropMoving(){},
    }
  }
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
