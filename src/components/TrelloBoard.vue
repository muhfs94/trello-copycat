<template>
  <v-container fluid>
    <v-slide-y-transition mode="out-in">
      <v-layout
        row
        align-center
        wrap
      >
        <v-flex
          sm3
          v-for="board in 3"
          :key="board._id"
          pa-2
        >
          <TrelloBoardList />
        </v-flex>
      </v-layout>
    </v-slide-y-transition>
  </v-container>
</template>

<script>
import TrelloBoardList from './TrelloBoardList';
export default {
  components: {
    TrelloBoardList
  }
}
</script>

<style scoped>
div {
  margin-top: 20px;
}
</style>