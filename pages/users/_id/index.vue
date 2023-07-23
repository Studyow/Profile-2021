<template>
  <div>A single user, with id: {{ $route.params.id }}</div>
</template>


<script>
export default {
  validate (data) {
    return data.params.id == 1 
  }
}
</script>