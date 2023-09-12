<template>
  <h3 v-for="name in names" :key="name.firstName">
    <slot :firstName="name.firstName" :lastName="name.lastName"></slot>
  </h3>
</template>

<script>
export default {
  name: "NameList",
  data() {
    return {
      names: [
        {
          firstName: "Bruce",
          lastName: "Wayne",
        },
        {
          firstName: "Clerk",
          lastName: "Kent",
        },
        {
          firstName: "Samuel",
          lastName: "Fanu",
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped></style>
