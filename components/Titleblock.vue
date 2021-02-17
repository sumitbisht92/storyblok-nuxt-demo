<template>
  <div>
    <div class="w-full  h-screen relative">
      <img
        style="float:right;right:0px;margin-top:80px"
        :src="blok.image.filename"
        alt=""
      />
      <div
      v-editable="blok"
      class="p-2 bg-white pl-12 pr-6"
      style="position:absolute;z-index:2;left:25%;top:145% "
    >
      <div class="text-5xl font-normal uppercase">{{ blok.body[0].title }}</div>
      <div class="text-base font-normal leading-7">
        {{ blok.body[0].subtitle }}
      </div>
      <div
        class="flex text-xs font-bold space-x-4 text-white p-2 cursor-pointer"
      >
        <Button
          style="background:#011E41;
               border-radius:25px;
               width:100px;
               height:40px;
               padding-left:26px;
               padding-top:12px"
          :blok="blok.body"
        />
      </div>
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
