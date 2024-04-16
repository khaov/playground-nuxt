<script setup>
  import { ref } from 'vue'

  const color = ref('')
  const size = ref('')
</script>

<template>
  <h1>UI components</h1>

  <section>
    <h2>Buttons</h2>

    <div class="ui-controls">
      <div>
        <h3>Color: {{ color }}</h3>

        <select v-model="color">
          <option disabled value="">Please select color</option>
          <option>primary</option>
          <option>secondary</option>
          <option>warning</option>
          <option>error</option>
          <option>success</option>
        </select>
      </div>
      <div>
        <h3>Size: {{ size }}</h3>

        <select v-model="size">
          <option disabled value="">Please select size</option>
          <option>2xs</option>
          <option>xs</option>
          <option>sm</option>
          <option>md</option>
          <option>lg</option>
          <option>xl</option>
        </select>
      </div>
    </div>

    <div class="ui-component">
      <UiButton
        :color="color"
        :size="size"
      />
    </div>
  </section>
</template>

<style>
  .ui-controls {
    display: flex;
    margin: 20px 0;
  }

  .button {
    display: block;
    min-width: 250px;
    padding: 10px;
    background-color: gray;
    border-radius: 20px;
    color: white;
  }

 .button--primary {background-color: purple;}
 .button--secondary {background-color: navy;}
 .button--warning {background-color: orange;}
 .button--error {background-color: red;}
 .button--success {background-color: green;}

 .button--2xs {padding:0 20px;}
 .button--xs {padding:4px 20px;}
 .button--sm {padding:6px 20px;}
 .button--md {padding:10px 20px;}
 .button--lg {padding:12px 20px;}
 .button--xl {padding:14px 20px;}
</style>
