<template>
  <v-card
    class="mx-auto"
    max-width="475"
  >
    <v-toolbar
      color="teal"
      dark
    >
      <v-app-bar-nav-icon></v-app-bar-nav-icon>

      <v-toolbar-title>Settings</v-toolbar-title>
    </v-toolbar>

    <v-list lines="two">
      <v-list-subheader>General</v-list-subheader>

      <v-list-item>
        <v-list-item-title>Profile photo</v-list-item-title>
        <v-list-item-subtitle>Change your Google+ profile photo</v-list-item-subtitle>
      </v-list-item>

      <v-list-item>
        <v-list-item-title>Show your status</v-list-item-title>
        <v-list-item-subtitle>Your status is visible to everyone</v-list-item-subtitle>
      </v-list-item>
    </v-list>

    <v-divider></v-divider>

    <v-list v-model="settings" lines="two" select-strategy="leaf">
      <v-list-subheader>Hangout notifications</v-list-subheader>

      <v-list-item>
        <template v-slot:default="{ active, }">
          <v-list-item-action>
            <v-checkbox
              :model-value="active"
              color="primary"
            ></v-checkbox>
          </v-list-item-action>

          <v-list-item-header>
            <v-list-item-title>Notifications</v-list-item-title>
            <v-list-item-subtitle>Allow notifications</v-list-item-subtitle>
          </v-list-item-header>
        </template>
      </v-list-item>

      <v-list-item>
        <template v-slot:default="{ active }">
          <v-list-item-action>
            <v-checkbox
              :model-value="active"
              color="primary"
            ></v-checkbox>
          </v-list-item-action>

          <v-list-item-header>
            <v-list-item-title>Sound</v-list-item-title>
            <v-list-item-subtitle>Hangouts message</v-list-item-subtitle>
          </v-list-item-header>
        </template>
      </v-list-item>

      <v-list-item>
        <template v-slot:default="{ active }">
          <v-list-item-action>
            <v-checkbox
              :model-value="active"
              color="primary"
            ></v-checkbox>
          </v-list-item-action>

          <v-list-item-header>
            <v-list-item-title>Video sounds</v-list-item-title>
            <v-list-item-subtitle>Hangouts video call</v-list-item-subtitle>
          </v-list-item-header>
        </template>
      </v-list-item>

      <v-list-item>
        <template v-slot:default="{ active }">
          <v-list-item-action>
            <v-checkbox
              :model-value="active"
              color="primary"
            ></v-checkbox>
          </v-list-item-action>

          <v-list-item-header>
            <v-list-item-title>Invites</v-list-item-title>
            <v-list-item-subtitle>Notify when receiving invites</v-list-item-subtitle>
          </v-list-item-header>
        </template>
      </v-list-item>
    </v-list>
  </v-card>
</template>

<script setup>
  import { ref } from 'vue'

  const settings = ref([])
</script>

<script>
  export default {
    data: () => ({
      settings: [],
    }),
  }
</script>
