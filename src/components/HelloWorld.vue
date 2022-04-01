<template>
<v-app>
  <v-content>
  <v-container>
    <!-- <v-row align="center" justify="center" > -->
     <v-card class="elevation-10">
       <v-windows v-model="step">
         <v-windows-item :value="1" >
       <v-row>
               <v-col cols="6" md="7" >
                       <!-- <v-img :src="require('../assets/PDA.jpg')" class="my-7" contain height="500" /> -->
                    </v-col>
                    
         <v-col cols="5" md="16" >
          <v-card-text > 
               <v-flex >

             <v-img :src="require('../assets/logo_v1.png')" class="my-5"  contain height="200" />

                       <v-form>
                        <v-text-field label="Users" name="Users" type="text" />
                        <v-text-field label="Password" 
                          :type="showPassword ? 'text'  : 'password'" 
                          :append-icon="showPassword ? 'mdi-eye' : 'mdi-eye-off'"
                          @click:append="showPassword = !showPassword"/>
                          </v-form>
                          
                          <br>
                          <v-btn block >LOGIN</v-btn>
                     <br> 
                      <br>

                    <a>Forgot your Password?</a>
                    
                     <br>
                     <br>
                     <h3>Or</h3>
                     <br>

                     
                      <v-btn block ><img src="../assets/google.png" alt="" contain height="30">sing in with google</v-btn>
                        <br>
                        <v-btn  block ><img src="../assets/apple.png" alt="" contain height="30">apple id</v-btn>
                        <br>
                    </v-flex>
                    </v-card-text> 
                    </v-col>
                    </v-row>
</v-windows-item>
</v-windows>
</v-card>
<!-- </v-row> -->
</v-container>
</v-content>
</v-app>
</template>







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



<style scoped>
a{
    margin:0px 0px 0px 140px;

}
h3{
  margin:0px 0px 0px 205px;
}
.container{
    margin:  20px auto;
}
.v-card-text{
  border: 2px solid rgb(82, 0, 14);
}
.col-md-7.col-6{
background: url(../assets/PDA.jpg);
width: 700px;
height: 738px;
background-size: 1150px;
background-position-x: -100px;
}

</style>