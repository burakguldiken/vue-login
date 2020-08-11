<template>
  <v-app>
    <v-card style="margin:auto" max-width="1000" class="mx-auto elevation-12 corners">
      <v-row>
        <v-col align="center" justify="center" cols="6">
          <v-card-text align="center" justify="center">
            <v-row align="center" justify="center">
              <v-col style="margin-top:50px" cols="12">
                <span class="login-left-span">Welcome Back!</span>
              </v-col>
              <v-col cols="2">
                <v-btn fab>
                  <v-icon size="25" style="color:blue">fab fa-facebook-f</v-icon>
                </v-btn>
              </v-col>
              <v-col cols="2">
                <v-btn fab>
                  <v-icon size="30" style="color:#833AB4">fab fa-instagram</v-icon>
                </v-btn>
              </v-col>
              <v-col cols="2">
                <v-btn fab>
                  <v-icon size="40" style="color:#1DA1F2">fab fa-twitter</v-icon>
                </v-btn>
              </v-col>
              <v-col class="login-email" cols="10">
                <v-text-field
                  v-model="email"
                  :rules="[() => !!email || 'This field is required']"
                  label="*Email"
                  placeholder="Your Email Address"
                  required
                  append-icon="fas fa-envelope"
                ></v-text-field>
              </v-col>
              <v-col cols="10">
                <v-text-field
                  v-model="password"
                  :rules="[() => !!password || 'This field is required']"
                  label="*Password"
                  placeholder="Your Password"
                  required
                  append-icon="fas fa-lock"
                ></v-text-field>
              </v-col>
              <v-btn class="login-button" style="border-radius:20px">
                <span style="color:white;">SING IN</span>
              </v-btn>
            </v-row>
          </v-card-text>
        </v-col>
        <v-col cols="6" class="login-col-right">
          <v-card-text align="center" justify="center" style="height:500px">
            <v-row align="center" justify="center">
              <span style class="login-right-span">Create Account</span>
              <span class="login-sub-span">You can join us to learn English and improve yourself</span>
              <v-btn class="login-singin-button" style="border-radius:20px">
                <span style="color:white">SIGN UP</span>
              </v-btn>
            </v-row>
          </v-card-text>
        </v-col>
      </v-row>
    </v-card>
    <ul class="circles">
      <li v-for="item in animationArr" :key="item.count"></li>
    </ul>
  </v-app>
</template>


<script>
export default {
  data() {
    return {
      email: "",
      password: "",
      animationArr: []
    };
  },

  methods: {},

  created() {
    for (var count = 0; count < 10; count++) {
      let animationObj = {
        count: count
      };
      this.animationArr.push(animationObj);
    }
    console.log(this.animationArr);
  }
};
</script>

<style scoped>
@import './css/login.css';
</style>

