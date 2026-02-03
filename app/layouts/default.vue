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
            prepend-avatar="https://scontent.fmnl25-1.fna.fbcdn.net/v/t39.30808-6/484779936_1650326232520749_4904272279880181454_n.jpg?_nc_cat=103&ccb=1-7&_nc_sid=a5f93a&_nc_ohc=nnDAqjqzy4IQ7kNvwFXqedQ&_nc_oc=Adnh1gEwlsEo9QsptmmeSrms3f6CCml03PWMQcS8tsLVMl-kWnKSuhIfRMG-uSbbIQ4&_nc_zt=23&_nc_ht=scontent.fmnl25-1.fna&_nc_gid=-_fTywgf8c9ieHS8knawxg&oh=00_AftNFQlCSUR-jysQLrB_t2yx7714EVn9cg16vfrbYYdrBw&oe=69870E93"
            subtitle="Logged in"
            title="Arwin balasubas"
          ></v-list-item>
        </template>

        <v-divider></v-divider>

        <v-list density="compact" nav>
          <v-list-item prepend-icon="mdi-home-city" title="Home" value="home"></v-list-item>
          <v-list-item prepend-icon="mdi-account" title="My Account" value="account"></v-list-item>
          <v-list-item prepend-icon="mdi-account-group-outline" title="Users" value="users"></v-list-item>
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