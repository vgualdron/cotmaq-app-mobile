<template>
  <root>
    <app-navigation></app-navigation>
  </root>
</template>

<script>
import { createAppContainer, createStackNavigator } from "vue-native-router";

import { Root } from "native-base";

import Home from "./views/Home.vue";
import Login from "./views/Login.vue";

const StackNavigator = createStackNavigator(
  {
    Home: {
      screen: Home,
    },
    Login: {
      screen: Login,
    },
  },
  {
    initialRouteName: "Login",
    headerMode: "none",
  }
);

const AppNavigation = createAppContainer(StackNavigator);

export default {
  components: {
    AppNavigation,
    Root,
  },
};
</script>