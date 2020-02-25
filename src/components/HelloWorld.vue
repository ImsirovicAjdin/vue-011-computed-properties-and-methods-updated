<template>
  <div class="hello">
    <p>
      Enter owner name:
      <input v-model.lazy="ownerName" placeholder="enter owner">
    </p>
    <p>
      Enter thing owned:
      <input v-model.lazy="thing" placeholder="enter thing">
    </p>
    <h1 v-if="ownerName && thing">{{ ownerHasThing }}</h1>
  </div>
</template>

<script>
export default {
  name: "HelloWorld",
  data() {
    return {
      ownerName: "",
      thing: ""
    };
  },
  computed: {
    // a computed getter
    ownerHasThing: function() {
      // `this` points to the Vue instance's data option
      return this.ownerName + " has a " + this.thing;
    }
  }
};
</script>

