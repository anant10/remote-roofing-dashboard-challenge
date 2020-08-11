<template>
  <a href>
    <div>
      <img class="image-20" v-bind:src="image" height="50" alt />
    </div>
  </a>
</template>

<script>
export default {
  name: "ImageComponentPhone",
  props: ["image"],
};
</script>

<style scoped>
.image-20 {
  padding-right: 4px;
  max-width: 19px;
  max-height: 15px;
}
</style>