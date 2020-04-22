<template>
  <div class="hello">
    <imgCut class="upload" ref="Uppicinput" @callback="callback" :width="200" :height="200">
        <div>上传按钮</div>
    </imgCut>
    <img :src="imgsrc" class="previewImg">
  </div>
</template>

<script>
import {imgCut} from 'vue-imgcut'

export default {
  name:'HelloWrold',
    data(){
        return{
            imgsrc:'',
            rate:'4:3'
        }
    },
    components:{
        imgCut
    },
    methods:{
        callback(img){
            this.imgsrc=img
            console.log(img)// 获取的是base64格式的图片
        }
    }
}
</script>
<style scoped>
.upload{
    width: 50vw !important;
    border-radius: 1vw;
    line-height: 5vh;
    box-shadow: inset 0 0 10px #CCC;
    margin: 20vh auto 3vh auto;
}

</style>
