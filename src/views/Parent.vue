<template>
  <div>
    <p>I'm parent.</p>

    <p>This can work: {{right}} -> (<ChildPage/>)</p>
    <p>This can't work: {{wrong}} -> (<child-page/>)</p>

    <p>Because I coded 'const childPage = ref(null)'. If I delete it, they both can show.</p>
  </div>
</template>
<script setup>
import ChildPage from './ChildPage.vue'
import { ref } from 'vue'

const right = ref(`<ChildPage/>`)
const wrong = ref(`<child-page/>`)

const childPage = ref(null)
</script>
<style></style>
