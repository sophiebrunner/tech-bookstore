<template>
  <LayoutHeader />
  <BookList />
</template>

<script>
export default {
  name: "App",
  components: {
    BookList,
    LayoutHeader,
  },
};
import BookList from "./components/BookList.vue";
import LayoutHeader from "./components/LayoutHeader.vue";
</script>
