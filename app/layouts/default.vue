<template>
  <v-app>
    <v-navigation-drawer
        v-model="drawer":rail="rail"
        permanent
        @click="rail = true"
      >
        <template v-slot:prepend>
          <v-list-item
            lines="two"
            prepend-avatar="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcT4dQWBhZkH9I_u8LeoxE2ml7HTd-hC9Rh0SQ&s"
            subtitle="Logged in"
            title="Arwin balasubas"
          ></v-list-item>
        </template>

        <v-divider></v-divider>

        <v-list density="compact" nav>
          <v-list-item prepend-icon="mdi-home-city" title="Home" value="home" to=""></v-list-item>
          <v-list-item prepend-icon="mdi-account" title="My Account" value="account"></v-list-item>
          <v-list-item prepend-icon="mdi-alert-circle" title="Users" value="users" to="/"></v-list-item>
          <v-list-item prepend-icon="mdi-bell" title="Dashboard" value="dashboard" to="/dashboard"></v-list-item>
          <v-list-item prepend-icon="mdi-menu" title="Prelim" value="prelim" to="/prelim"></v-list-item>
          
        </v-list>
      </v-navigation-drawer>
      <v-app-bar :elevation="2">
  <template v-slot:prepend>
    <v-app-bar-nav-icon  @click="rail = !rail"></v-app-bar-nav-icon>
  </template> 

  <v-app-bar-title>Application Bar</v-app-bar-title>
      </v-app-bar>
      <v-main>
        <v-container fluid>
           <slot />
           </v-container>
      </v-main>
      
  </v-app>
</template>

<script setup>
const drawer = ref(true)
  const rail = ref(true)

</script>

<style>

</style>