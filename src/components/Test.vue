<script lang="ts">
import { Component, Vue, Mixins } from 'vue-property-decorator'

@Component
export default class Test extends Mixins() {
  get default() {
    return 1;
  }
  // default
  defaultModel = {
    test: 'x',

  }

  private defaults = {
    key: 'value',
  }
  
  created() {
    this.defaultModel.test = this.defaults.key;
  }
}
</script>

<template>
  <div class="example">
    <p>
      BUG?
      <pre>{{ defaults }}</pre>
      <pre>{{ defaultModel }}</pre>
      
      <code>components/Test.vue</code> to test hot module replacement.
    </p>
  <hr />  
  </div>
  
</template>

<style lang="scss" scoped>
  .example {
    border: 1px solid red;
    padding: 1rem;
    border-radius: 1rem;
    text-align: left;
  }
</style>
