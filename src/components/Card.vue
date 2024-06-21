<template>
  <div class="card" >
    <div class="card-header">
        <slot name="cardHeader"></slot>
    </div>
    <div class="card-body">
        <slot name="cardBody"></slot>
    </div>
  </div>
</template>

<script>

export default {
  name: 'CardComp',
  props: ["gender"]
}

</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.card .card-header{
  height: 80%;
}

.card .card-body{
  height: 20%;
}
</style>
