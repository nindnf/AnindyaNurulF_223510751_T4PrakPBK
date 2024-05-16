<!-- ParentComponent.vue -->
<template>
  <div class="parent-component">
    <h2 style="color: #ff0066;">Parent Component</h2>
    <ChildComponent @childData="handleChildData" />
    <SlotComponent>
      <template v-slot:default>
        <p>Data from slot: {{ slotData }}</p>
      </template>
    </SlotComponent>
    <p>Data from child: {{ childData }}</p>
  </div>
</template>

<script>
import ChildComponent from './components/ChildComponent.vue';
import SlotComponent from './components/SlotComponent.vue';

export default {
  components: {
    ChildComponent,
    SlotComponent
  },
  data() {
    return {
      childData: '',
      slotData: 'Parent And Child Componen'
    };
  },
  methods: {
    handleChildData(data) {
      this.childData = data;
    }
  }
};
</script>

<style scoped>
.parent-component {
  background-color: #78beff;
  padding: 20px;
  border-radius: 8px;
}
</style>
