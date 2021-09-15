<template>
<div>
  <el-carousel height="150px">
      <el-carousel-item v-for="item in 2" :key="item">
       <div>
         <span style="font-size: 38px; font-weight: 800; color: #d3dce6; position: absolute; top:20%; left: 42%;">МиксЭнерджи</span>
         <div  style="font-size: 26px; font-weight: 400; color: #d3dce6; position: absolute; top:35%; left: 38%;">
           <span>Ваш проводник в Мир сантехники  и электрики.</span>
         </div>
         <div style="font-size: 26px; font-weight: 400; color: #d3dce6; position: absolute; top:45%; left: 20%;">
           <span> Профессиональные консультанты помогут Вам выбрать именно то что Вы ищете</span>
         </div>

       </div>
      </el-carousel-item>
    </el-carousel>
  <el-row style="margin-top: 3%;" :justify="'center'" :align="'middle'">
    <el-col class="block-name pipe" style="text-align: center" :xs="24"  :span="12">
      <span  @click="$router.push('/santehnika')" style="line-height: 20em;"><h3 style="font-size: 32px">Сантехника</h3></span>
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
    <el-col  class="block-name electricity" style="text-align: center" :xs="24"  :span="12">
      <div @click="$router.push('/electrika')" style="flex: 1;">
        <span  style="line-height: 20em;"><h3 style="font-size: 32px">Электрика</h3></span>
      </div>

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
.block-name:hover{
box-shadow: 1rem 1rem 2rem 1rem rgba(41, 39, 39, 0.2);
  color: #240531;
  cursor: pointer;
  background-repeat: no-repeat;
    background-size: cover;
}
.electricity{
  background-image: url("");
  transition: 1s;
  animation-name: Appearance;
  animation-duration: 3s;
  background-position: 0px 800px;
  animation-timing-function: cubic-bezier(.1,-.6,.2,0);

}
.pipe{
  background-image: url("");
  transition: 1s;
  animation-duration: 3s;
  animation-timing-function: cubic-bezier(.1,-.6,.2,0);
  animation: headerLanePipeNone 12s  alternate infinite;
  background-position: 0px -900px !important;

}
.electricity:hover{
  color: #ea0000;
  animation: headerLane 12s linear infinite alternate;
background-position: 0px 70% !important;
background-size: cover;
}
.electricity:hover span{
  text-shadow: 10px 10px 5px rgba(41, 39, 39, 0.42);
}
.pipe:hover span{
  text-shadow: 10px 10px 5px rgba(41, 39, 39, 0.42);
}
.pipe:hover{
  color: #d50000;
  animation: headerLanePipe 12s linear alternate infinite;
background-position: 0px 80% !important;
background-size: cover;
}
@keyframes headerLane {
    0% {
       background-image: url("https://lh3.googleusercontent.com/proxy/kEVZI-rYk6IRUuwhOCUV6y6CNUaiO0Tl8ZivQ9lYGNTqClQ6CUxNKKBcchMC4lujZYk_IVKC7XxuX0zRu1dP_4-wrMtG21zQj-Xx_ge7fmVePCTOZEgu9pTbdTvrt9ymrMFttw");

    }
    33% {
       background-image: url("https://lh3.googleusercontent.com/proxy/kEVZI-rYk6IRUuwhOCUV6y6CNUaiO0Tl8ZivQ9lYGNTqClQ6CUxNKKBcchMC4lujZYk_IVKC7XxuX0zRu1dP_4-wrMtG21zQj-Xx_ge7fmVePCTOZEgu9pTbdTvrt9ymrMFttw");

    }
    66% {
       background-image: url("https://lh3.googleusercontent.com/proxy/kEVZI-rYk6IRUuwhOCUV6y6CNUaiO0Tl8ZivQ9lYGNTqClQ6CUxNKKBcchMC4lujZYk_IVKC7XxuX0zRu1dP_4-wrMtG21zQj-Xx_ge7fmVePCTOZEgu9pTbdTvrt9ymrMFttw");

    }
    100% {
       background-image: url("https://lh3.googleusercontent.com/proxy/kEVZI-rYk6IRUuwhOCUV6y6CNUaiO0Tl8ZivQ9lYGNTqClQ6CUxNKKBcchMC4lujZYk_IVKC7XxuX0zRu1dP_4-wrMtG21zQj-Xx_ge7fmVePCTOZEgu9pTbdTvrt9ymrMFttw");

    }
}

@keyframes headerLanePipe {
    0% {
       background-image: url("https://salexy.kz/images/img_kz/700/8b/80/8b807b9dc299fb2a70611d7ce9ac4fb5.jpg");
    }
    33% {
       background-image: url("https://salexy.kz/images/img_kz/700/8b/80/8b807b9dc299fb2a70611d7ce9ac4fb5.jpg");
    }
    66% {
     background-image: url("https://salexy.kz/images/img_kz/700/8b/80/8b807b9dc299fb2a70611d7ce9ac4fb5.jpg");
    }
    100% {
       background-image: url("https://salexy.kz/images/img_kz/700/8b/80/8b807b9dc299fb2a70611d7ce9ac4fb5.jpg");
    }
}

</style>
