<template>
  <div class="hero-div-2">
    <div>
      <h1 class="sub-heading-title-2">{{ subheading }}</h1>
    </div>
    <div>
      <p class="text-block-25">{{ subdesc }}</p>
    </div>

    <div class="input-group input-group-lg mb-3">
      <div class="input-group-prepend">
        <span class="input-group-text span-img-1" id="basic-addon1">
          <img
            src="https://uploads-ssl.webflow.com/5f127ac8860f158e650f06b5/5f13618db066ca1a332318d1_home%403x.png"
            class="img-responsive"
            alt="Responsive image"
            width="30"
            height="30"
          />
        </span>
      </div>
      <input
        type="text"
        class="form-control"
        autocomplete="on"
        v-model="state"
        v-bind:placeholder="textspacedesc"
        @input="filterStates"
        aria-label="textspacedesc"
        aria-describedby="basic-addon1"
      />
      <!-- <div v-if="filteredStates">
        <ul v-if="filteredStates">
          <li
            v-bind:key="filteredState"
            v-for="filteredState in filteredStates"
          >
            {{ filteredState }}
          </li>
        </ul>
      </div> -->
      <div class="input-group-append">
        <button class="btn btn-primary btn-lg" type="button" id="button-addon2">
          Button
        </button>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Home',
  // components: {
  //   HelloWorld,
  // },
  data() {
    return {
      subheading: 'Roof inspections made remote and easy',
      subdesc:
        'Get your roof inspected remotely and connect with our trusted roofers',
      textspacedesc: 'Enter your Address',
      buttondesc: 'Get Inspection',
      state: '',
      states: ['Florida', 'Alabama', 'Texas', 'Alaska'],
      filteredStates: [],
    };
  },
  methods: {
    filterStates() {
      this.filteredStates = this.states.filter((state) => {
        return state.toLowerCase().startsWith(this.state.toLowerCase());
      });
    },
  },
};
</script>

<style scoped>
.sub-heading-title-2 {
  margin-top: 40px;
  font-family: AirbnbCerealBold, sans-serif;
  color: #fff;
  font-weight: 700;
}
.text-block-25 {
  font-family: AirbnbCerealLight, sans-serif;
  color: #fff;
  font-size: 18px;
  line-height: 1.5em;
  font-weight: 700;
}
.hero-div-1 {
  padding-bottom: 30%;
}
.hero-div-2 {
  padding-right: 10px;
  padding-left: 10px;
  padding-bottom: 10%;
}
.span-img-1 {
  background-color: #fff;
}

.block-1 {
  padding-left: 15%;
  padding-right: 15%;
  padding-top: 5%;
  background-color: blue;
}
</style>
