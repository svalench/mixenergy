<template>
<el-header style="padding: 0; margin-bottom: 20px;">
      <div class="container head ">
        <nuxt-link to="/">
        <div class="box logo">
          <el-image src="http://mixenerdgy.by/wp-content/uploads/2019/07/Logo-miksenerdzhi-N.png"></el-image>
        </div>
          </nuxt-link>
        <div class="box mobile-hide"><h1 style="font-size: 18px;">ООО "МиксЭнерджи"</h1></div>
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
                <th>день</th>
                <th>время</th>
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
          <span style="margin-right: 5%;"><a href="tel:+375173926366">8 (017) 39-26-366</a></span>
         <el-button style="background: #7c69ef; border:#537cf2;" icon="el-icon-phone" type="primary"></el-button>
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
</style>
