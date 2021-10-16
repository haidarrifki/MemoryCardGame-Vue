<template>
  <transition name="modal">
    <div class="modal-mask" v-if="this.showResult">
      <div class="modal-wrapper">
        <div class="modal-container">
          <div class="modal-body">Your score is {{ showResult }}</div>
        </div>
      </div>
    </div>
  </transition>
</template>
<script>
export default {
  name: "LeaderBoard",
  inject: ["players", "showResult"],
};
</script>
<style></style>
