<template>
  <v-app>
    <v-container fluid>
      <header class="header-text">
        <HelloWorld/>
      </header>
      <v-content>
        <v-card app class="counter-card">
          <v-card-actions app>
            <v-btn color="black" small dark fab v-on:click="increment">
              <span class="btn-text">+</span>
            </v-btn>
          </v-card-actions>
          <v-card-text app class="counter-card-text">
            <span class="text-lg-center display-3 font-weight-light">{{ count }}</span>
          </v-card-text>
          <v-card-actions app>
            <v-btn color="black" small dark fab @click="decrement">
              <span class="btn-text">-</span>
            </v-btn>
          </v-card-actions>
        </v-card>
      </v-content>
    </v-container>
  </v-app>
</template>

<script>
import HelloWorld from './components/HelloWorld';

export default {
  name: 'App',
  components: {
    HelloWorld
  },
  data() {
    return {
      count: 0
    };
  },
  methods: {
    increment() {
      return this.count++;
    },
    decrement() {
      if (this.count > 0) {
        return this.count--;
      }
    }
  }
};
</script>

<style>
div.container {
  max-width: 1040px;
}

.header-text {
  text-align: center;
  text-transform: uppercase;
  margin: 20px 2% 60px;
}

.counter-card {
  width: 200px;
  position: absolute;
  left: 50%;
  transform: translateX(-50%);
  border-radius: 10px;
  box-shadow: 2px 2px 12px darkgray;
}

.counter-card:hover {
  box-shadow: 0 0 10px 1px hotpink;
}

.counter-card-text {
  text-align: center;
}

button {
  position: absolute;
  left: 50%;
  transform: translate(-50%);
}
.btn-text {
  font-size: 2rem;
}
</style>


