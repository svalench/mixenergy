<template>
<div>
  <el-row>
    <el-col :span="4">
      <div  style="max-height: 70vh;" class="menu-block">
        <input v-model="searchMenu" type="text" placeholder="введите категорию"></input> <br>
        <ul>
          <li v-for="(i,k) in menu" :key="k"><el-row>
            <el-col :span="4">
            <el-image  style="width: 100px" :src="i.img"></el-image>
            </el-col>
            <el-col :span="20">
              <el-popover
            placement="right"
            :title="i.name"
            width="1200"
             trigger="hover"
            content="this is content, this is content, this is content">
              <div class="text-class"  slot="reference">{{i.name}}</div>
                <div style="display: flex;">
                  <div class="cart-menu" v-for="(ch,k) in i.child" :key="k">
                    <el-image style="width: 100px" :src="ch.img"></el-image>
                    <div>{{ch.name}}</div>
                  </div>
                </div>
              </el-popover>
            </el-col>
          </el-row>
          </li>

        </ul>

      </div>
    </el-col>
    <el-col :span="20">
  <el-carousel height="150px">
      <el-carousel-item v-for="item in 2" :key="item">
       <div>
         <span style="font-size: 38px; font-weight: 800; color: #d3dce6; position: absolute; top:20%; left: 40%;">МиксЭнерджи</span>
         <div  style="font-size: 26px; font-weight: 400; color: #d3dce6; position: absolute; top:35%; left: 28%;">
           <span>Ваш проводник в Мир сантехники  и электрики.</span>
         </div>
         <div style="font-size: 26px; font-weight: 400; color: #d3dce6; position: absolute; top:45%; left: 8%;">
           <span> Профессиональные консультанты помогут Вам выбрать именно то что Вы ищете</span>
         </div>

       </div>
      </el-carousel-item>
    </el-carousel>
      </el-col>
    </el-row>
  <el-row style="margin-top: 3%;" :justify="'center'" :align="'middle'">
    <el-col :class="showPipe?'block-name pipe  pipe1':'block-name pipe'"  style="text-align: center" :xs="24"  :span="12">
      <span ref="santehnika"  @click="$router.push('/santehnika')" style="line-height: 20em;"><h3 style="font-size: 32px">Сантехника</h3></span>
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
    <el-col  :class="showElect?'block-name electricity  electricity1':'block-name electricity'" style="text-align: center" :xs="24"  :span="12">
      <div @click="$router.push('/electrika')" style="flex: 1;">
        <span ref="electrika" style="line-height: 20em;"><h3 style="font-size: 32px">Электрика</h3></span>
      </div>

    </el-col>
  </el-row>
</div>

</template>

<script>
export default {
  data(){
    return{
      menu: [
        {name:"трубопроводная арматура",
          child:[
            {name:"краны шаровые", img:""},
            {name:"вентили", img:""},
            {name:"коллекторы", img:""},
            {name:"клапаны обратные", img:""},
          ],
          icon:"https://www.san.team/upload/resize_cache/iblock/8d0/35_35_1/8d01764e550606adf9b71473c41f827c.jpg"},
        {name:"фитинги резьбовые",
          child:[
            {name:"водоотводы", img:""},
            {name:"крестовины", img:""},
            {name:"заглушки", img:""},
            {name:"муфты", img:""},
            {name:"контргайки", img:""},
          ],
          icon:"https://www.san.team/upload/resize_cache/iblock/a53/35_35_1/a532110ad95d4084e05124d5abe1e246.jpg"},
        {name:"металлопластиковые трубы и фитинги",
          child:[
            {name:"металлопластиковые трубы", img:""},
            {name:"фитинги обжимные", img:""},
          ],
          icon:""},
        {name:"подводка гибкая",
          child:[],
          icon:""},
        {name:"муфта диэлектрическая",
          child:[],
          icon:""},
        {name:"водяной теплый пол",
          child:[],
          icon:""},
        {name:"коллекторные группы и комплектующие",
          child:[],
          icon:""},
        {name:"отопительное оборудование",
          child:[],
          icon:""},
        {name:"полипропиленовые трубы и фитинги",
          child:[],
          icon:""},
        {name:"прочее", child:[], icon:""},
      ],
      baseMenu: [
        {name:"трубопроводная арматура",
          child:[
            {name:"краны шаровые", img:""},
            {name:"вентили", img:""},
            {name:"коллекторы", img:""},
            {name:"клапаны обратные", img:""},
          ],
          icon:"https://www.san.team/upload/resize_cache/iblock/8d0/35_35_1/8d01764e550606adf9b71473c41f827c.jpg"},
        {name:"фитинги резьбовые",
          child:[
            {name:"водоотводы", img:""},
            {name:"крестовины", img:""},
            {name:"заглушки", img:""},
            {name:"муфты", img:""},
            {name:"контргайки", img:""},
          ],
          icon:"https://www.san.team/upload/resize_cache/iblock/a53/35_35_1/a532110ad95d4084e05124d5abe1e246.jpg"},
        {name:"металлопластиковые трубы и фитинги",
          child:[
            {name:"металлопластиковые трубы", img:""},
            {name:"фитинги обжимные", img:""},
          ],
          icon:""},
        {name:"подводка гибкая",
          child:[],
          icon:""},
        {name:"муфта диэлектрическая",
          child:[],
          icon:""},
        {name:"водяной теплый пол",
          child:[],
          icon:""},
        {name:"коллекторные группы и комплектующие",
          child:[],
          icon:""},
        {name:"отопительное оборудование",
          child:[],
          icon:""},
        {name:"полипропиленовые трубы и фитинги",
          child:[],
          icon:""},
        {name:"прочее", child:[], icon:""},
      ],
      searchMenu: "",
      showElect:false,
      showPipe:false,
    }
  },
  watch:{
    searchMenu(nv){
      let f = this.menu.filter(x=>x.name.includes(`${nv}`));
      console.log(f)
      if (f){
        this.menu = f;
      }
      if(!nv){
        this.menu = this.baseMenu;
      }
    }
  },
  async fetch(){
      this.getCategories()
  },
  mounted() {
    // Setup the event listener and execute it once in case we are already scrolled
    window.addEventListener('scroll', this.scrollHandler);
    this.scrollHandler();
  },
  beforeDestroy() {
    window.removeEventListener('scroll', this.scrollHandler);
  },
  methods: {
    async getCategories(){
        let data = await this.$axios.get('/catalog/categories/');
        this.menu = data.data.results;
    },
    scrollHandler(e) {
      let wh = window.innerHeight;
      let elec = this.$refs.electrika.getBoundingClientRect();
      let pipes = this.$refs.santehnika.getBoundingClientRect();
      this.showElect = (elec.y- wh)<(0-elec.height+10)
      this.showPipe = (pipes.y- wh)<(0-pipes.height-10)

    }
  }
}
</script>
<style>
.cart-menu{
   margin: 2%;
  padding: 15px;
  border-radius: 3px;
  transition: all .5s;
  cursor: pointer;
}
.cart-menu:hover{
  -webkit-box-shadow: 5px 5px 6px rgba(70, 39, 141, 0.49);
}
.menu-block ul{
  padding: 0px;
}
.menu-block input{
  padding: 0px;
  border-radius: 10px;
  text-align: center;
}
.menu-block{
  justify-content: center;
  align-items: center;
  flex-wrap: wrap;
  margin-top: 10%;
  position: relative;
  width: 100%;
  display: flex;
  overflow-y: auto;
  overflow-x: hidden;
   float: left;

}
.menu-block li{
  transition: all .3s;
   -webkit-box-shadow: inset 5px 5px 6px rgba(70, 39, 141, 0.49);
  text-align: center;
  font-weight: 600;
  font-size: 14px;
  padding: 20px;
  margin: 5px;
}
.box-show{
  width:0px;
  height:0px;
  background:rgba(0,0,0,.8);
  visibility: hidden;

  transition:ease-out .3s;
}
.menu-block li:hover .box-show{
  width: 100%;
  height: 400px;
   display: block;
  margin-top: 10%;
  visibility: revert;
}
.menu-block li:hover{
  background-color: #5e5a95;
  color: #d3dce6;

}
.text-class{
  cursor: pointer;
}
.menu-block::-webkit-scrollbar {
  width: 10px;
  background-color: #d3cdd9;
}

.menu-block::-webkit-scrollbar-thumb {
  border-radius: 10px;
  background-color: #5e5a95;
}

.menu-block::-webkit-scrollbar-track {
  -webkit-box-shadow: inset 0 0 6px rgba(0,0,0,0.2);
  border-radius: 10px;
  background-color: #c4c2e8;
}
li {
    list-style-type: none; /* Убираем маркеры */
   }
.el-carousel__container{
  margin-top: 2%;
  min-height: 70vh;
  max-height: 70vh;
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
    background-image: url("@/assets/img/pipes.jpg");
  }

  .el-carousel__item:nth-child(2n+1) {
    background-color: #d3dce6;
    background-repeat: no-repeat;
    background-size: cover;
    background-image: url("@/assets/img/bathroom.jpg");
  }
.head-block-index{
  display: flex;
  height: 100%;
}
.block-name:hover{
box-shadow: 1rem 1rem 2rem 1rem rgba(41, 39, 39, 0.2);
  color: #240531;
  cursor: pointer;
  /*background-repeat: no-repeat;*/
  /*  background-size: cover;*/
}
.electricity{
  transition: 1.5s;
  overflow: hidden;
  background-position: 0px 800px;
  background-size: cover;
  background-repeat: no-repeat;
  background-image: url("@/assets/img/electika.jpg");
}
.electricity1{
  color: #ea0000;
background-position: 0px -10px !important;

}
.pipe{
  background-image: url("@/assets/img/santeh.jpg");
  transition: 1.5s;
  background-size: cover;
  background-repeat: no-repeat;
  background-position: 0px -900px !important;

}

.electricity:hover span{
  text-shadow: 10px 10px 5px rgba(41, 39, 39, 0.42);
}
.pipe:hover span{
  text-shadow: 10px 10px 5px rgba(41, 39, 39, 0.42);
}
.pipe1{
  color: #d50000;
background-position: 0px 0px !important;

}

</style>
