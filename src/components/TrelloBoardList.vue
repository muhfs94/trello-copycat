<template>
  <div>
    <v-card
      class="mx-auto"
      :flat="flat"
      :loading="loading"
      :outlined="outlined"
      :elevation="elevation"
      :raised="raised"
      :width="width"
      :height="height"
      style="flex-direction: row"
    >
      <v-card-title>Create List</v-card-title>
      <v-form @keydown.prevent.enter>
        <v-text-field
          label="Name"
          required
        ></v-text-field>
        <v-btn type="submit">Create list</v-btn>
      </v-form>
      <!-- <v-card-text>I'm card text</v-card-text> -->
      <v-card-actions>
        <!-- <v-btn icon>
          <v-icon>mdi-heart</v-icon>
        </v-btn> -->
        <v-btn text>Click</v-btn>
        <v-btn outlined>Click</v-btn>
      </v-card-actions>
    </v-card>
  </div>
</template>

<script>
export default {
  data: () => ({
    flat: false,
    media: true,
    loading: false,
    actions: true,
    outlined: false,
    elevation: undefined,
    raised: false,
    width: 344,
    height: undefined,
  }),
}
</script>

<style scoped>
.v-input__slider {
  width: 100%;
}
</style>