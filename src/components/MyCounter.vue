<template>
  <h1>Soy el componente Contador y tengo el valor de {{ contador }}</h1>
  <div>
    <button v-on:click="suma1">Suma +1</button>
    <button @click="resta1">Resta -1</button>
    <button @click="$emit('selection', data)">Emit</button>
    <!-- //https://vuejs-org.translate.goog/guide/components/events.html?_x_tr_sl=en&_x_tr_tl=es&_x_tr_hl=es&_x_tr_pto=sc#defining-custom-events -->
  </div>
  <div class="separador">
    <input v-model="data" type="text" />
    <h1>{{ data }}</h1>
    <h1 v-if="contador > 10">Es mayor a 10</h1>
    <ul id="example-1">
      <li v-for="(item, index) in items" :key="index.id">
        {{ item.mensaje }}
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  data() {
    return {
      contador: 0,
      data: "",
      items: [],
    };
  },

  methods: {
    suma1() {
      this.contador++;
      this.items.push(this.contador);
      console.log(this.items);
    },
    resta1() {
      this.contador--;
    },
  },
};
</script>

<style>
.separador {
  margin-top: 50px;
}
</style>