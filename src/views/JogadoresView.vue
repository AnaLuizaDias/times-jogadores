<script>
import { v4 as uuid} from "uuid";
export default {
  data() {
    return{
      novo_jogador:"",
      jogadores:[
        { id:"1a167632-ccca-4314-921d-d2165a9fe8c1", name: "jogador 1" },
        { id:"2c2672d6-c492-407d-9b42-b09733f4edc9", name: "jogador 2" },
        { id:"e7bd7d32-71f8-4a68-ae7b-53a02a7db443", name: "jogador 3" },
        { id:"90e7e11b-0075-4090-ab9a-232bbc7bfe6a", name: "jogador 4" },
      ],
    };
  },
  methods: {
    salvar(){
      const novo_id = uuid();
      this.jogadores.push({
        id: novo_id,
        name: this.novo_jogador,
      });
    },
  },
};

</script>
<template>
  <div class="container">
    <div class="title">
      <h2> Gerenciamento de jogadores</h2>
    </div>
    <div class="form-input">
      <input type="text" placeholder="Nome" v-model="novo_jogador"/>
      <input type="text" placeholder="Time"/>
      <button @click="salvar">Salvar</button>
    </div>
    <div class="list-items">
      <table>
        <thead>
          <tr>
            <th>ID</th>
            <th>Nome</th>
            <th>Time ID</th>
          </tr>
        </thead>
        <tbody>
        <tr v-for="jogador in jogadores" :key="jogadores.id">
          <td> {{ jogador.id }} </td>
          <td> {{ jogador.name }} </td>
          <td>???</td>
        </tr>
      </tbody>
      </table>
    </div>
  </div>
</template>

<style scoped> </style>

