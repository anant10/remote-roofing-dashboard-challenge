<template>
  <a href>
    <div>
      <img class="image-20" v-bind:src="image" height="50" alt />
    </div>
  </a>
</template>

<script>
export default {
  name: "ImageComponent",
  props: ["image"],
};
</script>

<style scoped>
.image-20 {
  width: 82px;
  height: 30px;
  max-height: none;
  max-width: none;
}
</style>