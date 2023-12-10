<template>
  <div class="hello">
    <ul>
      <li v-for="(skill,index) in skills" :key="index">{{ skill.name }}</li>
    </ul>
    <button v-on:click="changeName" v-bind:disabled="btnStatus">
      Click me
    </button>
  </div>
</template>

<script>
export default {
  name: "SkillsView",
  props: {
    msg: String,
  },
  data() {
    return {
      skills: [{ name: "Vue" }, { name: "React" }],
      btnStatus: true,
    };
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  padding: 0;
}
li {
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
