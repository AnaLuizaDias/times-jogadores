<script>
export default {
  data() {
    return{
      jogadores:[
        { id:1, name: "jogador 1" },
        { id:2, name: "jogador 2" },
        { id:3, name: "jogador 3" },
        { id:4, name: "jogador 4" },
      ],
    };
  },
};
</script>
<template>
  <div class="container">
    <div class="title">
      <h2> Gerenciamento de jogadores</h2>
    </div>
    <div class="form-input">
      <input type="text" placeholder="Nome"/>
      <input type="text" placeholder="Time"/>
      <button>Salvar</button>
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

