<template>
  <div>
    <v-btn elevation="2" v-on:click="AddMember">AddMember</v-btn>
    <v-btn elevation="2" icon
      ><v-img src="../resources/shuffle.png" max-height="30" max-width="30"
    /></v-btn>
    <v-text-field ref="count" label="Number of Groups" type="number" />
    <NameInput v-for="member in members" v-bind:key="member.component" />
  </div>
</template>
<script>
import NameInput from "./components/NameInput.vue";
export default {
  name: "App",

  data: () => ({
    members: [],
  }),
  methods: {
    AddMember: function () {
      this.members.push({ component: "<br>" });
    },
  },
  components: {
    NameInput,
  },
};
</script>
