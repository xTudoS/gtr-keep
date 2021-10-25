<template>
  <v-app>
    <NavBar/>
    <v-main>
      <v-container class="mt-3">
        <Create />

        <div class="text-center mt-2" v-if="loading">
          <v-progress-circular :size="50" color="primary" indeterminate></v-progress-circular>
        </div>

        <Notes v-else />

        <NoteModal />

        <v-snackbar v-model="snackbar.open" :color="snackbar.color">{{ snackbar.text }}</v-snackbar>
      </v-container>
    </v-main>
  </v-app>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator';
import Create from './components/Create.vue';
import Notes from './components/Notes.vue';
import NoteModal from './components/NoteModal.vue';
import { namespace } from 'vuex-class';
import { Snackbar, Note } from './store/types';
import NavBar from './components/NavBar.vue';

const notesModule = namespace('notes');
const globalModule = namespace('global');

@Component({
  components: {
    Create,
    Notes,
    NoteModal,
    NavBar,
  },
})
export default class App extends Vue {
  loading = true;
  refreshLoading = false;

  async created() {
    this.loading = true;
    await this.getNotes();
    this.loading = false;
  }

  async refresh() {
    this.refreshLoading = true;
    await this.getNotes();
    this.refreshLoading = false;
  }

  @globalModule.State
  snackbar!: Snackbar;

  @notesModule.Action
  getNotes!: () => Promise<Note[]>;
}
</script>
