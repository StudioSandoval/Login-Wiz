<template>
<v-app>
  <v-content>
  <v-container>
    <v-row align="center" justify="center" >
     <v-card class="elevation-0">
       <v-windows v-model="step">
         <v-windows-item :value="1" >
       <v-row>
               <!-- <v-col cols="6" md="7" >
                       <v-img :src="require('../assets/PDA.jpg')" class="my-7" contain height="500" />
                    </v-col> -->
                    
         <v-col cols="12" md="16" >
          <v-card-text > 
               <v-flex >

             <v-img :src="require('../assets/logo_v1.png')" class="my-16"  contain height="200" />

                       <v-form>
                        <!-- <v-text-field label="Users" name="Users" type="text" /> -->
                        <v-text-field label="New Password" 
                          :type="showPassword ? 'text'  : 'password'" 
                          :append-icon="showPassword ? 'mdi-eye' : 'mdi-eye-off'"
                          @click:append="showPassword = !showPassword"/>
                          <v-text-field label="Confirm New Password" 
                          :type="showPassword ? 'text'  : 'password'" 
                          :append-icon="showPassword ? 'mdi-eye' : 'mdi-eye-off'"
                          @click:append="showPassword = !showPassword"/>
                          </v-form>
                          
                          
                     <br> 

                    <a>The Passwords don´t match</a>
                    
                     <br>
                                  <br>
                          <v-btn block >send</v-btn>

                     <br>
                      
                    </v-flex>
                    </v-card-text> 
                    </v-col>
                    </v-row>
</v-windows-item>
<v-windows-item :value="2">




</v-windows-item>
</v-windows>
</v-card>
</v-row>
</v-container>
</v-content>
</v-app>
</template>




<style scoped>

.container{
    margin: 80px auto;
}

</style>


<script>
export default {
    data() {
        return {
            showPassword:false
        }
    },
    props: {
      souce: String
    }
};
</script>



