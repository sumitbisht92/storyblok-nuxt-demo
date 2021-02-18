<template>
  <div>
    <div class="w-full  h-screen mb-20" :style="setHeroBackground()">
      <!-- <img class=" h-full w-full" :src="blok.imagelist.filename" alt="" /> -->
      <div
        class="flex"
        style="position:absolute;bottom:0%; left:9%  line-height:56px"
      >
        <h1 class="text-5xl font-normal text-white uppercase w-2/3 ml-4">
          Your <br />
          Wellness Journey <br />Starts Here
        </h1>
        <component
          v-for="blok in blok.body"
          :key="blok._uid"
          :blok="blok"
          :is="blok.component"
          class="w-1/3  bg-white p-2 mb-8 mr-6 "
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
  },
  methods: {
    setHeroBackground() {
      if (this.blok.imagelist && this.blok.imagelist.filename) {
        const bgUrl = this.blok.imagelist.filename;
        return {
          background: `linear-gradient(180deg, rgba(0, 0, 0, 0.34902) 0%, rgba(0, 0, 0, 0.0001) 100%), url(${bgUrl})`,
          backgroundSize: "cover"
        };
      }

      return {};
    }
  }
};
</script>
