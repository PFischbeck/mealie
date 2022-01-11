<template>
  <client-only>
  <VJsoneditor
    :value="value"
    height="1500px"
    :options="options"
    :attrs="$attrs"
    @input="$emit('input', $event)"
  ></VJsoneditor>
    </client-only>
</template>

<script lang="ts">
import { defineComponent } from "@nuxtjs/composition-api";

export default defineComponent({
  props: {
    value: {
      type: Object,
      default: () => ({}),
    },
    options: {
      type: Object,
      default: () => ({}),
    },
  },
});
</script>
