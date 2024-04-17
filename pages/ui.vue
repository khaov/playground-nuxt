<script setup lang="ts">
  const color = ref<string>()
  const size = ref<string>()
  const title = ref<string>()
</script>

<template>
  <h1>UI components</h1>

  <section>
    <h2>Buttons</h2>

    <form class="form" action="#">
      <fieldset class="form-controls">
        <div>
          <label class="form-label">Color: {{ color }}</label>

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
          <label class="form-label">Size: {{ size }}</label>

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
        <div>
          <label class="form-label">Title:</label>

          <input type="text" v-model="title">
        </div>
      </fieldset>
    </form>

    <div class="ui-component">
      <UiButton
        :color="color"
        :size="size"
      >
        {{ title }}
      </UiButton>
    </div>
  </section>
</template>

<style>
  .form-controls {
    display: flex;
    margin: 20px 0;
    padding: 0;
    border: 0;
  }
  .form-label {
    display: block;
  }
</style>
