<template>
  <!-- <div class="card">{{ content }}</div> -->
  <!-- <div class="card">
    <slot>Default Content</slot>
  </div> -->

  <!-- This code will be in the App.vue  <Card>
    <template v-slot:header>
      <h3 style="background-color: blue; color: yellowgreen">Header</h3>
    </template>
    <template v-slot:default>
      <img src="https://picsum.photos/200" alt="Picsum" />
    </template>
    <template v-slot:footer>
      <button style="background-color: red">View details</button>
    </template>
  </Card> -->

  <div class="card">
    <div id="card-header">
      <slot name="header"></slot>
    </div>
    <div id="card-content">
      <slot></slot>
    </div>
    <div id="card-footer">
      <slot name="footer"></slot>
    </div>
  </div>
</template>

<script>
export default {
  name: "Card",
  //   props: ["content"],
};
</script>

<style scoped>
.card {
  box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.2);
  transition: 0.3s;
  padding: 16px;
  margin-bottom: 20px;
  widows: 200px;
}
.card:hover {
  box-shadow: 0 8px 16px 0 rgba(0, 0, 0, 0.2);
}
</style>

// The App.vue code for the Card
