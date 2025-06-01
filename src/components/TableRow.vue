<script setup>
const props = defineProps({
  titleHour: {
    type: String,
    required: true,
  },
  titleMinute: {
    type: String,
    required: true,
  },
  item: {
    type: String,
    required: false,
    default: "",
  },
});
</script>

<template>
  <tr v-if="props.titleHour && props.titleMinute">
    <th><span>{{ props.titleHour }}</span>:<span>{{ props.titleMinute }}</span></th>
    <td><slot></slot></td>
  </tr>
</template>

<style lang="scss" scoped>
tr {
  display: flex;
  padding: 10px;
  gap: 30px;
  // font-size: 0.875rem;
  color: var(--color-black);
  th {
    display: grid;
    grid-template-columns: 9fr 1fr 9fr;
    width: 40px;
    font-weight: bold;
    span {
      text-align: right;
    }
  }
}
@media screen and (min-width: 769px) {
  .p-a-top {
    max-width: 804px;
  }
}
</style>
