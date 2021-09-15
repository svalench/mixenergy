<template>
<div>
  <el-row style="margin-top: 5%;">
    <el-col :span="12">
      <el-row>
        <el-col  class="block-name electricity" style="text-align: center" :xs="24"  :span="24">
      <div @click="$router.push('/electrika')" style="flex: 1;">
        <span  style="line-height: 20em;"><h3 style="font-size: 32px">Электрика</h3></span>
      </div>
        </el-col>
        <el-col class="block-name pipe" style="text-align: center" :xs="24"  :span="24">
      <span  @click="$router.push('/santehnika')" style="line-height: 20em;"><h3 style="font-size: 32px">Сантехника</h3></span>
    </el-col>
      </el-row>
    </el-col>
    <el-col>

    </el-col>
  </el-row>
</div>
</template>

<script>
export default {
  name: "catalog"
}
</script>

<style scoped>
ul li{
   list-style-type: none;
  font-size: 18px;
  text-align: center;
   line-height: 50px;
}
li:hover{
  text-shadow: 10px 10px 5px rgba(41, 39, 39, 0.42);
  cursor: pointer;
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
  animation: shake  1.3s;
  animation-delay: 0.77s;
   animation-iteration-count: infinite;
  animation-timing-function: cubic-bezier(.1,-.6,.2,0);

}
.pipe{
  background-image: url("");
  transition: 1s;
  animation-duration: 3s;
  animation: shake  1.6s;
  animation-delay: 0.33s;
  animation-iteration-count: infinite;
  animation-timing-function: cubic-bezier(.1,-.6,.2,0);
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
