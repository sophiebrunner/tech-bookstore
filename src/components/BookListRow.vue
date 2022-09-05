<template>
  <tr class="table-item__table-row">
    <td class="table-item__table-head-name">{{ title }}</td>
    <td class="table-item__table-head-isbn">{{ isbn }}</td>
    <td>
      <slot
        name="actionCol"
        :title="title"
        :isbn="isbn"
        :isBookmarked="isBookmarked"
      />
      <!--
      <BaseButton
        :text="buttonTxt"
        variant="secondary"
        @buttonClick="onToggleBookmark"
      />
    </td>
    --></td>
  </tr>
</template>

<script>
//import BaseButton from "./BaseButton.vue";

export default {
  name: "BookListRow",
  props: {
    title: String,
    isbn: String,
    isBookmarked: Boolean,
  },
  //components: { BaseButton },
  /*
  methods: {
    onToggleBookmark() {
      this.$emit("toggleBookmark", this.isbn);
    },
  },
  computed: {
    buttonTxt() {
      return this.isBookmarked ? "Remove Bookmark" : "Add Bookmark";
    },
  },
  emits: ["toggleBookmark"],*/
};
</script>

<style scoped>
.table-item__table td {
  padding: 12px 15px;
}
</style>
