<template>
  <div
    class="grid-container overflow-x-auto"
    id="scroll-target"
    height="100%"
  >
    <v-row
      v-for="n in 5"
      :key="n"
      height="1000px"
    >
      <v-card
        class="pa-1 mb-100"
        color="blue-grey lighten-4"
        width="300px"
        v-scroll:#scroll-target="onScroll"
      >
        <v-text-field
          light
          label="Solo"
          placeholder="Enter list title..."
          solo
          clearable
          autofocus
          hide-details
          class="pa-2 ma-0"
        ></v-text-field>
        <v-card-actions class="ma-0">
          <v-btn
            rounded
            small
            color="primary"
            class="body-2 text-none font-weight-regular"
          >Add list</v-btn>
          <v-btn
            rounded
            text
            small
            class="body-2 text-none font-weight-regular"
          >Cancel</v-btn>
        </v-card-actions>
      </v-card>
    </v-row>
  </div>
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
  margin: 5px;
}
.grid-container {
  display: grid;
  grid-auto-flow: column;
  grid-gap: 10px;
  grid-auto-columns: 300px;
  align-items: start;
  /* overflow: auto; */
}
</style>