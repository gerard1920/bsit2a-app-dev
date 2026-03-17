<template>
<div class="d-flex justify-center align-center" style="height: 100vh;">
    <v-card width="400" class="text-center" elevation="12">
        <v-icon style="font-size: 50px;" color="red" class="mt-10">mdi-login</v-icon>
        <v-card-text class="py-10">
            <v-text-field 
            variant="outlined"
            v-model="Username"
            flat
            label="Username" prepend-inner-icon="mdi-account" 
            clearable>
            
            </v-text-field>


            <v-text-field 
            variant="outlined" 
            v-model="Password"
            flat
            label="Password" prepend-inner-icon="mdi-lock" 
            type="password"
            clearable>
            </v-text-field> 

            <v-btn color="red" @click="login()" block>Sign in</v-btn>

        </v-card-text>
    </v-card>

 </div>
</template>

<script setup>
definePageMeta({
    layout: 'auth',
});
const defaultUsername = ref("admin");
const defaultPassword = ref("admin123");
const Username = ref("");   
const Password = ref("");

function login() {
 alert("Mali ka ng tinama tropa!");
 if (Username.value === defaultUsername)
}   
</script>