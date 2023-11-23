<template>
  <button @click="incrementButton">
    increment {{ count }}
  </button>
</template>

<script>
import CounterMixin from '../Mixins/counter';
export default {
    name : "ClickCounter",
    mixins : [CounterMixin]
}
</script>

<style>

</style>