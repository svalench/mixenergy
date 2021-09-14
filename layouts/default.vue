<template>
  <div>
    <head-site></head-site>
      <div class="page">
        <Nuxt style="min-height: 85vh;"/>
      </div>
    <el-footer style="padding: 0;">
      <div class="container footer ">
        <div style="width: 300px" class="box">
       ООО "МиксЭнерджи"  © 2021
          </div>
        <div class="box mobile-hide" style="width:150px; padding-left: 100px;">
          <iframe src="https://yandex.ru/map-widget/v1/?um=constructor%3Ad0f82ac64f3dd42a610f1377d049a782b659e73cfd5f932d24d949e17ddd0b0b&amp;source=constructor" width="300" height="250" frameborder="0"></iframe>
           </div>
        <div class="mobile-show">
          <el-button type="text" @click="dialogTableVisible = true">
            <i class="el-icon-location"></i>
            карта</el-button>
        </div>
      </div>
    </el-footer>


<el-dialog title="Shipping address" :visible.sync="dialogTableVisible">
  <div style="min-width: 400px; min-height: 350px;">
    <iframe src="https://yandex.ru/map-widget/v1/?um=constructor%3Ad0f82ac64f3dd42a610f1377d049a782b659e73cfd5f932d24d949e17ddd0b0b&amp;source=constructor" width="550" height="500" frameborder="0"></iframe>
  </div>

</el-dialog>
    </div>
</template>

<script>

import HeadSite from "../components/headSite";
export default {
  name: "default",
  data(){
    return{
      dialogTableVisible: false,
    }
  },
  components:{
    HeadSite
  },
   head() {
        return {

        }
    },
}
</script>
<style>

</style>
