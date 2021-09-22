<template>
  <div class="d-flex flex-row justify-content-center py-3">
    <div class="turns p-3">
      <span class="btn btn-info"
        >Turns :
        <span class="badge" :class="finish ? 'badge-success' : 'badge-light'">
          {{ turns }}</span
        >
      </span>
    </div>
    <div class="totalTime p-3">
      <span class="btn btn-info"
        >Total Time :
        <span class="badge" :class="finish ? 'badge-success' : 'badge-light'"
          >{{ min }} : {{ sec }}</span
        ></span
      >
    </div>
  </div>
</template>
<script>
export default {
  props: ["min", "sec", "turns", "finish"],
};
</script>
<style>
.badge-success {
  background-color: green;
}
.badge-light {
  background-color: red;
}
</style>
