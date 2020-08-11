<template>
  <div class="container-fluid">
    <div class="row">
      <div class="col-auto mr-auto">
        <ImageComponent v-bind:image="remoteRoofIcon" />
      </div>
      <div class="col-auto">
        <PhoneComponent />
      </div>
    </div>
  </div>
</template>

<script>
import ImageComponent from './ImageComponent';
import PhoneComponent from './PhoneComponent';
export default {
  name: 'TopHeader',
  components: {
    ImageComponent,
    PhoneComponent,
  },
  data() {
    return {
      remoteRoofIcon:
        'https://uploads-ssl.webflow.com/5f127ac8860f158e650f06b5/5f12985a91b23596370f7a81_logo-72-dc-7-f-0-f%402x.png',
    };
  },
};
</script>

<style scoped></style>
