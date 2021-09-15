<template>
  <div class="">
    <head-site></head-site>
      <div class="page container-my">
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
          <div class="about">
    ООО «МиксЭнерджи»

Юр. Адрес: 220007, г.Минск, ул. Артиллеристов, дом № 8, корпус 3, офис 17

Почтовый адрес: 220007, г.Минск, ул. Артиллеристов, дом № 8, корпус 3, офис 17

УНП: 193243351

Счет: BY20ALFA30122474210010270000

в ЗАО «АЛЬФА-БАНК» г. Минск, ул. Сурганова, 43-47

тел/факс: +375173926366

тел:+37529-377-47-10

mixenerdgy@mail.ru

Директор Михашонок Сергей Васильевич, на основании Устава

Приказ № 8-К от 19.02.2020г.
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
.container-my{
  margin-right: 10px;
  margin-left: 10px;
  margin-bottom: 4%;
}
@media screen and (min-width: 1023px) {
  .about{
    margin-left: 200px;
  }
}
@media screen and (max-width: 1023px) {
  .about{
    display: none;
  }
}
</style>
