<template>
  <validate-component :num="0">
    <some-component>
      <validate-component :num="2"></validate-component>
    </some-component>
    
    <some-component>
      <validate-component :num="3">
        <validate-component :num="4"></validate-component>
      </validate-component>
    </some-component>

    <validate-component :num="5"></validate-component>
  </validate-component>
</template>

<script>
  import ValidateComponent from './components/validate'
  import SomeComponent from './components/some'
  export default {
    name: 'App',
    components: {
      ValidateComponent,
      SomeComponent
    }
  }
</script>

<style>
  div {
    font: 12px Arial, Helvetica, sans-serif;
    margin: 20px;
    border: 1px #ccc solid;
    position: relative;
    padding: 20px;
    border-radius: 20px;
  }
  span {
    display: inline-block;
    padding: 0 10px;
  }
  label {
    position: absolute;
    left: 20px;
    top: -12px;
    display: inline-block;
    padding: 5px 10px;
    border-radius: 20px;
    background: #999;
    color: #fff;
  }
</style>
