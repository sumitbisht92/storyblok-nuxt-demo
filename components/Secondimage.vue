<template>
  <div>
    <div class="w-full  h-screen relative">
      <img style="float:right;right:0px;width:955px;height:982px" :src="blok.image.filename" alt="" />

      <img
        style="position:absolute;z-index:1; top:50px;left:50px"
        :src="blok.body[0].image.filename"
        alt=""
      />
    </div>
    <div
      v-editable="blok"
      class="p-2 bg-white pl-12 pr-6"
      style="position:absolute;z-index:22;width:565px;height:300px "
    >
      <div class="text-5xl font-normal uppercase">{{ blok.body[0].title }}</div>
      <div class="text-base font-normal leading-7">{{ blok.body[0].subtitle }}</div>
       <div class="flex text-xs font-bold space-x-4 text-white p-2 cursor-pointer">
      <Button
        style="background:#011E41;
               border-radius:25px;
               width:195px;
               height:48px;
               padding-left: 53px;
               padding-top: 15px;"
        :blok="blok.body[0].body[0]"
      />
     
    </div>
    </div>
   
  </div>
</template>

<script>
export default {
  props: {
    blok: {
      type: Object,
      required: true
    }
  }
};
</script>
