<script setup lang="ts">
  withDefaults(
    defineProps<{
      color: string
      size: string
    }>(),
    {
      color: "default",
      size: "default"
    },
  );
</script>

<template>
  <button
    :class="`button button--color--${color} button--size--${size}`"
  >
    <slot/>
  </button>
</template>

<style>
  .button {
    display: block;
    min-width: 250px;
    border: 0;
    border-radius: 20px;
    color: white;
  }

  .button--color--default {
    background-color: gray;
  }

 .button--color--primary {
    background-color: purple;
  }

 .button--color--secondary {
    background-color: navy;
  }

 .button--color--warning {
    background-color: orange;
  }

 .button--color--error {
    background-color: red;
  }

 .button--color--success {
    background-color: green;
  }

  .button--size--default {
    padding: 10px;
  }

 .button--size--2xs {
    padding:0 20px;
  }

 .button--size--xs {
    padding:4px 20px;
  }

 .button--size--sm {
    padding:6px 20px;
  }

 .button--size--md {
    padding:10px 20px;
  }

 .button--size--lg {
    padding:12px 20px;
  }

 .button--size--xl {
    padding:14px 20px;
  }
</style>
