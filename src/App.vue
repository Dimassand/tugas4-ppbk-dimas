<template>
  <div class="app">
    <h1>Tugas 4 Dimas Andreananda</h1>
    <p>Data from Child: {{ parentData }}</p>

    <ChildOne @sendData="handleData"/>
    <ChildTwo @sendData="handleData"/>

    <NestedComponent>
      <template v-slot:default>
        <p>This is a slot content from Parent</p>
      </template>
    </NestedComponent>
  </div>
</template>

<script>
import ChildOne from './components/ChildOne.vue';
import ChildTwo from './components/ChildTwo.vue';
import NestedComponent from './components/NestedComponent.vue';

export default {
  components: {
    ChildOne,
    ChildTwo,
    NestedComponent,
  },
  data() {
    return {
      parentData: '',
    };
  },
  methods: {
    handleData(data) {
      this.parentData = data;
    }
  }
};
</script>

<style scoped>
.app {
  font-family: Arial, sans-serif;
  padding: 20px;
  max-width: 800px;
  margin: 0 auto;
  background-color: #f9f9f9;
  border-radius: 8px;
  box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
}

h1 {
  color: #333;
}

p {
  color: #666;
  font-size: 18px;
}
</style>
