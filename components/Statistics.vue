<template>
  <div :id="blok.id" class="flex flex-wrap text-center">
    <div v-for="item in blok" :key="item._uid" class="w-1/3">
      <div
        v-if="item.number"
        v-html="item.number"
        class="font-medium text-4xl"
      ></div>
      <div v-if="item.title" v-html="item.title.toUpperCase()" class="font-medium"></div>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    blok: {
      type: Array,
      default: null,
    },
  }
  
}
</script>