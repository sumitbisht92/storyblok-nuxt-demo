<template>
    <div class="flex px-4">
      <div class="w-1/6">Home</div>
      <div class="w-6/12">Image</div>
      <div class="w-2/12">Book</div>
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