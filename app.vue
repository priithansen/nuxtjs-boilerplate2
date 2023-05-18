<template>
  <div>
    <div>Check developer console!</div>
    <pre>
      {{ config.public.example }}
    </pre>
  </div>
</template>
<script setup>
const config = useRuntimeConfig()
console.log('Runtime config:', config.public.example)
if (process.server) {
  console.log('Server:', config.public.example)
}
</script>
