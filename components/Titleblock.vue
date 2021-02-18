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
        class="py-2 px-10 mb-4 bg-white pl-12 pr-6"
        style="position:absolute;z-index:2;left:25%;top:145%;width:600px "
      >
        <div class="text-5xl font-normal uppercase whitespace-pre text-justify -mb-10 pl-16">
          {{ blok.body[0].title }}
        </div>
        
       <div class=""> <Statistics :blok="blok.body[0].body" /></div>
        <div class="text-base font-normal leading-7 my-4">
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
               padding-left:16px;
               padding-top:12px"
            :blok="blok.body[1]"
          />
          <!-- <Button :blok="blok.body[1]"/> -->
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
