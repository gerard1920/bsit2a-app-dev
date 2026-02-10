<template>
  <div>
    
    <v-row>
   <v-col cols="12" md="3">
    <v-card height="120" color="red">
      <v-card-text>
        <v-row>
          <v-cols cols="6">
            <v-icon size="80">mdi-account</v-icon>
          </v-cols>
          <v-col cols="50">
            
           <v-row no-gutters>
            <v-col  cols="12" class="text-h6 text-right text-uppercase ">Student</v-col>
            <v-col  cols="12" class="text-h4 text-right font-weight-bold">120</v-col>

            </v-row>
          </v-col>
        </v-row>
      </v-card-text>
    </v-card>

    </v-col>
    
    
     
  
   <v-col cols="12" md="3">
    <v-card height="120" color="blue">
      <v-card-text>
        <v-row>
          <v-cols cols="6">
            <v-icon size="80">mdi-account</v-icon>
             </v-cols>
            <v-col cols="50">
           
              <v-row no no-gutters>
              <v-col cols="12" class="text-h6 text-right text-uppercase ">Account</v-col>
               <v-col cols="12" class="text-h4 text-right font-weigth-bold">123</v-col>
            </v-row>
            </v-col>
         
        </v-row>
      </v-card-text>
    </v-card>
   </v-col>

   
   <v-col cols="12" md="3">
    <v-card height="120" color="yellow">
      <v-card-text>
        <v-row>
          <v-cols cols="6">
            <v-icon size="80">mdi-account</v-icon>
             </v-cols>
            <v-col cols="50">
           
              <v-row no no-gutters>
              <v-col cols="12" class="text-h6 text-right text-uppercase">Account</v-col>
               <v-col cols="12" class="text-h4 text-right font-weigth-bold">150</v-col>
            </v-row>
            </v-col>
         
        </v-row>
      </v-card-text>
    </v-card>
   </v-col>


   <v-col cols="12" md="3">
    <v-card height="120" color="gray">
      <v-card-text>
        <v-row>
          <v-cols cols="6">
            <v-icon size="80">mdi-account</v-icon>
             </v-cols>
            <v-col cols="50">
           
              <v-row no no-gutters>
              <v-col cols="12" class="text-h6 text-right text-uppercase">Account</v-col>
               <v-col cols="12" class="text-h4 text-right font-weigth-bold">228</v-col>
            </v-row>
            </v-col>
         
        </v-row>
      </v-card-text>
    </v-card>
   </v-col>
    </v-row>

    <v-row>
        <v-col cols="12" md="8">
            <v-card height="500" color="#EEEEEE" elevation="0">
                
                <v-card-text>
                    <v-data-table
    :headers="headers"
    :items="plants"
    density="compact"
    item-key="name"
  ></v-data-table>
                </v-card-text>
            </v-card>
        </v-col>

        <v-col>
            <v-row>
                <v-col cols="12">
                     <v-card color="#385F73">
                <v-card-title class="text-h5">
                  Unlimited music now
                </v-card-title>

                <v-card-subtitle>
                  Listen to your favorite artists and albums whenever and wherever, online and offline.
                </v-card-subtitle>

                <v-card-actions>
                  <v-btn text="Listen Now" variant="text"></v-btn>
                </v-card-actions>
              </v-card>
                </v-col>
            </v-row>

            <v-row>
                <v-col cols="12">
                 <v-card color="#1F7087">
                <div class="d-flex flex-no-wrap justify-space-between">
                  <div>
                    <v-card-title class="text-h5">
                      Supermodel
                    </v-card-title>

                    <v-card-subtitle>Foster the People</v-card-subtitle>

                    <v-card-actions>
                      <v-btn
                        class="ms-2"
                        size="small"
                        text="START RADIO"
                        variant="outlined"
                      ></v-btn>
                    </v-card-actions>
                  </div>

                  <v-avatar
                    class="ma-3"
                    rounded="0"
                    size="125"
                  >
                    <v-img src="https://cdn.vuetifyjs.com/images/cards/foster.jpg"></v-img>
                  </v-avatar>
                </div>
              </v-card>
                </v-col>
            </v-row>

            <v-row>
                <v-col cols="12">
                     <v-card color="#952175">
                <div class="d-flex flex-no-wrap justify-space-between">
                  <div>
                    <v-card-title class="text-h5">
                      Halcyon Days
                    </v-card-title>

                    <v-card-subtitle>Ellie Goulding</v-card-subtitle>

                    <v-card-actions>
                      <v-btn
                        class="ms-2"
                        icon="mdi-play"
                        variant="text"
                      ></v-btn>
                    </v-card-actions>
                  </div>

                  <v-avatar
                    class="ma-3"
                    rounded="0"
                    size="125"
                  >
                    <v-img src="https://cdn.vuetifyjs.com/images/cards/halcyon.png"></v-img>
                  </v-avatar>
                </div>
              </v-card>
                </v-col>
            </v-row>
        </v-col>

    </v-row>

    <v-fab>
    </v-fab>

    <v-dialog
      v-model="dialog"
      max-width="600"
    >
      <template v-slot:activator="{ props: activatorProps }">
        <v-btn
          class="text-none font-weight-regular"
          prepend-icon="mdi-account"
          text="Edit Profile"
          variant="tonal"
          v-bind="activatorProps"
        ></v-btn>
      </template>

      <v-card
        prepend-icon="mdi-account"
        title="User Profile"
      >
        <v-card-text>
          <v-row dense>
            <v-col
              cols="12"
              md="4"
              sm="6"
            >
              <v-text-field
                label="First name*"
                required
              ></v-text-field>
            </v-col>

            <v-col
              cols="12"
              md="4"
              sm="6"
            >
              <v-text-field
                hint="example of helper text only on focus"
                label="Middle name"
              ></v-text-field>
            </v-col>

            <v-col
              cols="12"
              md="4"
              sm="6"
            >
              <v-text-field
                hint="example of persistent helper text"
                label="Last name*"
                persistent-hint
                required
              ></v-text-field>
            </v-col>

            <v-col
              cols="12"
              md="4"
              sm="6"
            >
              <v-text-field
                label="Email*"
                required
              ></v-text-field>
            </v-col>

            <v-col
              cols="12"
              md="4"
              sm="6"
            >
              <v-text-field
                label="Password*"
                type="password"
                required
              ></v-text-field>
            </v-col>

            <v-col
              cols="12"
              md="4"
              sm="6"
            >
              <v-text-field
                label="Confirm Password*"
                type="password"
                required
              ></v-text-field>
            </v-col>

            <v-col
              cols="12"
              sm="6"
            >
              <v-select
                :items="['0-17', '18-29', '30-54', '54+']"
                label="Age*"
                required
              ></v-select>
            </v-col>

            <v-col
              cols="12"
              sm="6"
            >
              <v-autocomplete
                :items="['Skiing', 'Ice hockey', 'Soccer', 'Basketball', 'Hockey', 'Reading', 'Writing', 'Coding', 'Basejump']"
                label="Interests"
                auto-select-first
                multiple
              ></v-autocomplete>
            </v-col>
          </v-row>

          <small class="text-caption text-medium-emphasis">*indicates required field</small>
        </v-card-text>

        <v-divider></v-divider>

        <v-card-actions>
          <v-spacer></v-spacer>

          <v-btn
            text="Close"
            variant="plain"
            @click="dialog = false"
          ></v-btn>

          <v-btn
            color="primary"
            text="Save"
            variant="tonal"
            @click="dialog = false"
          ></v-btn>
        </v-card-actions>
      </v-card>
    </v-dialog>
    
  
  </div>
</template>

<script setup>
const headers = [
    { title: 'Plant', align: 'start', sortable: false, key: 'name' },
    { title: 'Light', align: 'end', key: 'light' },
    { title: 'Height', align: 'end', key: 'height' },
    { title: 'Pet Friendly', align: 'end', key: 'petFriendly' },
    { title: 'Price ($)', align: 'end', key: 'price' },
  ]

  const plants = [
    {
      name: 'Fern',
      light: 'Low',
      height: '20cm',
      petFriendly: 'Yes',
      price: 20,
    },
    {
      name: 'Snake Plant',
      light: 'Low',
      height: '50cm',
      petFriendly: 'No',
      price: 35,
    },
    {
      name: 'Monstera',
      light: 'Medium',
      height: '60cm',
      petFriendly: 'No',
      price: 50,
    },
    {
      name: 'Pothos',
      light: 'Low to medium',
      height: '40cm',
      petFriendly: 'Yes',
      price: 25,
    },
    {
      name: 'ZZ Plant',
      light: 'Low to medium',
      height: '90cm',
      petFriendly: 'Yes',
      price: 30,
    },
    {
      name: 'Spider Plant',
      light: 'Bright, indirect',
      height: '30cm',
      petFriendly: 'Yes',
      price: 15,
    },
    {
      name: 'Air Plant',
      light: 'Bright, indirect',
      height: '15cm',
      petFriendly: 'Yes',
      price: 10,
    },
    {
      name: 'Peperomia',
      light: 'Bright, indirect',
      height: '25cm',
      petFriendly: 'Yes',
      price: 20,
    },
    {
      name: 'Aloe Vera',
      light: 'Bright, direct',
      height: '30cm',
      petFriendly: 'Yes',
      price: 15,
    },
    {
      name: 'Jade Plant',
      light: 'Bright, direct',
      height: '40cm',
      petFriendly: 'Yes',
      price: 25,
    },
  ]
</script>

<style>

</style>
