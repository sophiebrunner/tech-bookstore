<template>
  <tr class="table-item__table-row">
    <td class="table-item__table-head-name">{{ title }}</td>
    <td class="table-item__table-head-isbn">{{ isbn }}</td>
    <td><BaseButton text="Add Bookmark" variant="secondary" /></td>
  </tr>
</template>

<script>
import BaseButton from "./BaseButton.vue";

export default {
  name: "BookListRow",
  props: ["title", "isbn"],
  components: { BaseButton },
};
</script>

<style scoped>
.table-item__table td {
  padding: 12px 15px;
}
</style>
