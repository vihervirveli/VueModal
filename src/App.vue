<template>
 <h1>{{title}}</h1>
<MyModal />
</template>

<script>
import MyModal from "./components/MyModal.vue";

export default {
  name: 'App',
  components: { MyModal },
  data(){
    return {
      title: 'My 2nd Vue App'
    }
  },
  methods: {
    handleClick(){
      console.log(this.$refs.name);
      this.$refs.name.classList.add("active");
      this.$refs.name.focus();
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

.active {
  background: rgb(53, 53, 124);
  color: rgb(243, 242, 242);
}

h1 {
  border-bottom: 1px solid #ddd;
  display: inline-block;
  padding-bottom: 10px;
}
button, input {
  display: inline-block;
  margin: 10px;

}
</style>
