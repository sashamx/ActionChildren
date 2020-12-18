<template>
  <div>
    <label>Some</label>
    <slot>
      <validate-component></validate-component>
    </slot>
  </div>
</template>

<script>
import ValidateComponent from './validate'
export default {
  name: 'Some',
  components: {
    ValidateComponent
  }
}
</script>

<style scoped>

</style>
