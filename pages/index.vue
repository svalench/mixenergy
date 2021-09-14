<template>
<div>
  <el-carousel height="150px">
      <el-carousel-item v-for="item in 4" :key="item">
        <h3 class="small">{{ item }}</h3>
      </el-carousel-item>
    </el-carousel>
  <el-row style="margin-top: 3%;" :justify="'center'" :align="'middle'">
    <el-col style="text-align: center" :xs="24"  :span="12">
      <span style="line-height: 20em;"><h3 style="font-size: 32px">Сантехника</h3></span>

    </el-col>
    <el-col style="text-align: center" :xs="24" :span="12">
      <ul>
<li>Запорная арматура;</li>
<li>Водонагреватели;</li>
<li>Смесители и комплектующие;</li>
<li>Ванны;</li>
<li>Поддоны;</li>
<li>Санфаянс (унитазы, умывальники, писсуары);</li>
<li>Полотенцесушители водяные и электрические;</li>
<li>Трубы и фитинги;</li>
<li>Комплектующие для сантехники;</li>
<li>Отопительное оборудование;</li>
<li>Канализационное оборудование;</li>
<li>Контрольно-измерительные приборы;</li>
<li>Уплотнительные и смазывающие материалы;</li>
<li>Защитные и теплоизоляционные материалы;</li>
<li>Сопутствующие товары;</li>
<li>Специнструмент, спецодежда;</li>
<li>Насосное оборудование;</li>
<li>Детали трубопровода;</li>

      </ul>
    </el-col>
  </el-row>
  <el-row style="margin-top: 3%;" :justify="'center'" :align="'middle'">
    <el-col style="text-align: center" :xs="24" :span="12">
      <ul>
<li>Светильники;</li>
<li>Лампы;</li>
<li>Стабилизаторы напряжения;</li>
<li>Электроустановочные и электромонтажные изделия;</li>
<li>Модульная автоматика;</li>
<li>Силовое оборудование;</li>
<li>Электрощитовое оборудование;</li>
<li>Кабеленесущие системы;</li>
<li>Кабель и провод;</li>
<li>Метизная продукция;</li>
<li>Сухие трансформаторы ТСЗ;</li>
<li>Электродвигателя;</li>
<li>Вентиляторы;</li>
<li>Молниезащита и заземление;</li>
      </ul>
    </el-col>
    <el-col style="text-align: center" :xs="24"  :span="12">
      <span style="line-height: 20em;"><h3 style="font-size: 32px">Электрика</h3></span>
    </el-col>
  </el-row>
</div>

</template>

<script>
export default {}
</script>
<style>
li {
    list-style-type: none; /* Убираем маркеры */
   }
.el-carousel__container{
  margin-top: 2%;
  min-height: 70vh;
}

  .el-carousel__item h3 {
    color: #475669;
    font-size: 14px;
    opacity: 0.75;
    line-height: 150px;
    margin: 0;
  }

  .el-carousel__item:nth-child(2n) {
    background-color: #99a9bf;
    background-repeat: no-repeat;
    background-size: cover;
    background-image: url("https://aquatower.by/wp-content/uploads/2018/07/bathroom-1982011_1920-1500x1200-1300x360.jpg");
  }

  .el-carousel__item:nth-child(2n+1) {
    background-color: #d3dce6;
    background-repeat: no-repeat;
    background-size: cover;
    background-image: url("https://lk-bauservice.de/wp-content/uploads/2018/01/sanitaerarbeiten-slide-1920x1080.jpg");
  }
.head-block-index{
  display: flex;
  height: 100%;
}
</style>
