<template>
  <nav class="qa-top-menu c-top-menu">
    <div class="c-top-menu__inner-container">
      <Title :text="title" type="h3" />
      <div class="c-top-menu__content">
        <slot></slot>
      </div>
    </div>
  </nav>
</template>

<script>
import Title from "@/components/Title/Title.vue";

export default {
  name: "TopMenu",
  props: {
    title: {
      type: String,
      default: "",
    },
  },
  components: {
    Title,
  },
};
</script>

<style lang="scss">
.c-top-menu {
  display: grid;
  grid-template-columns: repeat(5, 1fr);
  grid-template-rows: 30px;
  width: 100%;
  box-shadow: -7px 9px 6px -8px rgb(0 0 0 / 29%);
  padding: 20px 10px;
  background-color: white;

  .c-top-menu__inner-container {
    grid-column: 2 / 5;
    display: flex;
    justify-content: space-between;
  }

  .c-top-menu__content {
    display: flex;
    align-items: center;
    gap: 10px;
  }
}
</style>
