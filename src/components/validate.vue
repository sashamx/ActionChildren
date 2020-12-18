<template>
  <div>
    <label>Validate</label>
    <button @click="clickFunc">Click start children action - {{num}}</button>
    <span>{{text}}</span>
    <slot></slot>    
  </div>
</template>

<script>
export default {
  name: 'Validate',
  props: ['num'],
  data(){
    return {
      text: ''
    }
  },
  created: function() {
    this.$parent.$on('update', this.action);
    this.$parent.$parent.$on('update', this.action);    
  },
  methods: {
    action(){
        return this.text = `methods action - ${this.num}`
    },
    clickFunc(){
      this.$emit('update');
    }    
  },
}
</script>