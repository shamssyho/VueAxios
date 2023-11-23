<template>
    <h3 @mouseover="incrementButton">
        Hover Counter {{ count }}
    </h3>
</template>
  
<script>
import CounterMixin from '../Mixins/counter';
export default {
    name: "HoverCounter",
    mixins : [CounterMixin]
}
</script>
  
<style></style>