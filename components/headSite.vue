<template>
<el-header style="padding: 0; margin-bottom: 20px;">
      <div class="container head ">
        <nuxt-link to="/">
        <div class="box logo" style="margin-right: 20px">
          <el-image style="width: 150px;" :src="require('@/assets/img/Group.svg')"></el-image>
        </div>
          </nuxt-link>
        <div @click="$router.push('/catalog')" class="box mobile-hide"><span class="menu-btn">Каталог</span></div>
        <div @click="$router.push('/sertificates')" class="box mobile-hide"><span class="menu-btn">Сертификаты</span></div>
        <div @click="$router.push('/about')" class="box mobile-hide"><span class="menu-btn">Контакты</span></div>
        <div style="width: 40%" class="box right-block">
           <el-popover
            placement="bottom"
            title="График работы"
            width="200"
             trigger="click"
            content="this is content, this is content, this is content">
            <span style="cursor: pointer; margin-right: 10px;" slot="reference">График работы</span>
             <div>
              <table border="1">
                <thead>
                <tr>
                <th>день</th>
                <th>время</th>
                </tr>
                </thead>
                <tbody>
                <tr>
                  <td>понедельник</td>
                  <td>8.00-12.00</td>
                </tr>
                <tr>
                  <td>вторник</td>
                  <td>8.00-12.00</td>
                </tr>
                <tr>
                  <td>среда</td>
                  <td>8.00-12.00</td>
                </tr>
                <tr>
                  <td>четверг</td>
                  <td>8.00-12.00</td>
                </tr>
                <tr>
                  <td>пятница</td>
                  <td>8.00-12.00</td>
                </tr>
                <tr>
                  <td>суббота</td>
                  <td>Выходной</td>
                </tr>
                <tr>
                  <td>воскресенье</td>
                  <td>Выходной</td>
                </tr>
                </tbody>
              </table>
             </div>
          </el-popover>
          <span style="margin-right: 5%; "><a href="tel:+375173926366">8 (017) 39-26-366</a></span>
           <el-popover
            placement="bottom"
            title="Контактные телефоны"
            width="280"
             trigger="click">
             <div style="text-align: right; font-size: 18px;">
               <ul>
                 <li><span style="margin-right: 10px">МТС<i class="el-icon-phone-outline"></i></span><a href="tel:+3758854654455">+3758854654455</a></li>
                 <li><span style="margin-right: 10px">А1<i class="el-icon-phone-outline"></i></span><a href="tel:+3758854654455">+3758854654455</a></li>
                 <li><span style="margin-right: 10px">Viber<i class="el-icon-phone-outline"></i></span><a href="viber:+3758854654455">+3758854654455</a></li>
               </ul>
             </div>
         <el-button class="shhh"  slot="reference" style="background: #7c69ef; border:#537cf2;" icon="el-icon-phone" type="primary"></el-button>
           </el-popover>
          <a href="mailto:info@mixenerdgy.by">
        <span class="mobile-hide" style="align-self: center; padding: 10px; margin-left: 50px;">info@mixenerdgy.by</span>
            </a>
        </div>

      </div>
    </el-header>
</template>

<script>
export default {
  name: "headSite"
}
</script>

<style scoped>
.menu-btn{
  padding: 12px;
  border-radius: 10px;
  font-size: 18px;
  font-weight: 600;
}
.menu-btn:hover{
  /*box-shadow: 1rem 1rem 2rem 1rem rgba(41, 39, 39, 0.2);*/
  text-shadow: 6px 5px 5px rgba(54, 46, 46, 0.59);;
  color: #240531;
  cursor: pointer;
}
.shhh{
   transition: 1s;
  animation-duration: 6s;
  animation: shake  1.6s;
  animation-delay: 0.33s;
  animation-iteration-count: infinite;
  animation-timing-function: cubic-bezier(.1,-.6,.2,0);
}
@keyframes shake {
    0% { transform: translate(0, 0); }
    10% { transform: translate(0, 0); }
    20% { transform: translate(0, 0); }
    30% { transform: translate(0, 0); }
    33% { transform: translate(-3px, 0px) rotate(1deg); }
    38% { transform: translate(3px, 2px) rotate(0deg); }
    42% { transform: translate(1px, -1px) rotate(1deg); }
    48% { transform: translate(-1px, 2px) rotate(-1deg); }
    54% { transform: translate(-3px, 1px) rotate(0deg); }
    60% { transform: translate(3px, 1px) rotate(-1deg); }
    70% { transform: translate(0, 0); }
    80% { transform: translate(0, 0); }
    90% {transform: translate(0, 0); }
    100% {transform: translate(0, 0); }
}
</style>
