<template>
  <div>
    <div v-editable="blok" class="p-2">
      <div class="text-sm font-bold">{{ blok.title }}</div>
      <div class="text-sm">{{ blok.subtitle }}</div>
    </div>
    <div class="flex text-xs font-bold space-x-4 text-white p-2 cursor-pointer">
      <Button
        style="background:#011E41;
               border-radius:25px;
               width:100px;
               height:40px;
               padding-left:26px;
               padding-top:12px"
        :blok="blok.body[0]"
      />
      <Button style="background:#011E41;
               border-radius:25px;
               width:136px;
               height:40px;
               padding-left:26px;
               padding-top:12px
              "
               :blok="blok.body[1]" />
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