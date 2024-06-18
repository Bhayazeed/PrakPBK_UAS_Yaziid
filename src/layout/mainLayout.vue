<template>
    <q-layout view="hHh lpR fFf">
      <q-header elevated class="bg-primary text-white">
        <q-toolbar>
          <q-toolbar-title align="left">
            Weather API 
          </q-toolbar-title>
          <q-space />
          <div class="tasks-section">
            <q-select
              v-model="selectedTask"
              :options="tasks"
              label="Select Task"
              emit-value
              map-options
            />
            <q-btn @click="navigateToTask" label="Go to Task" color="primary" />
          </div>
        </q-toolbar>
      </q-header>
      <q-page-container>
        <router-view />
      </q-page-container>
      <q-footer elevated align="left" class="bg-secondary text-white">
        <q-toolbar>
          <q-toolbar-title>
            M.Bhayaziid Amalin - 223510209 4E
          </q-toolbar-title>
        </q-toolbar>
      </q-footer>
    </q-layout>
  </template>

<script setup>
import {ref} from 'vue'
const tasks = ref([
  { label: "Tugas 1", value: "https://yazeed-projectcv.netlify.app/" },
  {
    label: "Tugas 2", value: "https://palindrome-yaziid.netlify.app/",
  },
  { label: "Tugas 3", value: "https://223510209-yaziid.netlify.app/todos" },
  {
    label: "Tugas 4", value: "https://photogallery-yaziid.netlify.app/",
  },
  { label: "Tugas 5", value: "https://yaziid-223510209-eracoffee.netlify.app/" 
  },
  { label: "Tugas 6", value: "https://223510209-yaziid-prakpbkt6.netlify.app/" },
]);

const selectedTask = ref(null);

const navigateToTask = () => {
  if (selectedTask.value) {
    window.open(selectedTask.value, '_blank');
  }
};
</script>

<style scoped>
.tasks-section {
  display: flex;
  align-items: center;
  gap: 10px;
}
</style>