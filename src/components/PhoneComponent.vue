<template>
  <div class="row">
    <div class="col-xs-2">
      <ImageComponentPhone v-bind:image="remoteRoofPhoneSymbol" v-bind:class="imageClass" />
    </div>
    <div class="col-xs-8">
      <a href="tel:2148658818" class="link-block-2 w-inline-block">
        <div>
          <strong class="phone-number-2">214-865-8818</strong>
        </div>
      </a>
    </div>
  </div>
</template>
<script>
import ImageComponentPhone from "./ImageComponentPhone";
export default {
  name: "PhoneComponent",
  components: {
    ImageComponentPhone,
  },
  data() {
    return {
      remoteRoofPhoneSymbol:
        "https://uploads-ssl.webflow.com/5f127ac8860f158e650f06b5/5f1297d1c3fecf36271c10a2_483947%403x.png",
      classObject: {
        active: true,
        "text-danger": false,
      },
    };
  },
};
</script>
<style scoped>
.phone-number-2 {
  border-style: solid;
  border-width: 0px;
  border-color: hsla(0, 0%, 100%, 0);
  font-family: AirbnbCerealBold, sans-serif;
  color: #fff;
  font-weight: 400;
}

.link-block-2 {
  border-style: solid;
  border-width: 1px;
  border-color: hsla(0, 0%, 100%, 0);
  color: rgba(247, 239, 239, 0);
}
.w-inline-block {
  max-width: 100%;
  display: inline-block;
}
.image-19 {
  max-width: 15px;
}
</style>