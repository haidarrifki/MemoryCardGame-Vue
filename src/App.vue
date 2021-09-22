<template>
  <Title />
  <CardContainer />
  <Modal ref="Modal" />
  <LeaderBoard />
</template>

<script>
import Title from "./components/Title.vue";
import CardContainer from "./components/CardContainer.vue";
import Modal from "./components/Modal.vue";
import LeaderBoard from "./components/DashBoard.vue";

export default {
  name: "App",
  data() {
    return {
      players: [
        {
          name: null,
          score: null,
        },
      ],
    };
  },
  methods: {
    setPlayer(name) {
      this.players[0].name = name;
      this.$refs.Modal.closeModal();
      console.log(this.players);
    },
    setPoint(point) {
      this.players[0].score = point;
      this.$refs.Modal.openModal();
      console.log(this.players[0]);
    },
  },
  components: {
    Title,
    CardContainer,
    Modal,
    LeaderBoard,
  },

  provide() {
    return {
      players: this.players,
      setPlayer: this.setPlayer,
      setPoint: this.setPoint,
    };
  },
};
</script>

<style>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
#app {
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
  height: 100vh;
  background-color: #ff3cac;
  background-image: linear-gradient(
    225deg,
    #ff3cac 0%,
    #784ba0 50%,
    #2b86c5 100%
  );
}
</style>
