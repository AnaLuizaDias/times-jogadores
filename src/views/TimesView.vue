<script>
export default {
  data() {
    return{
      times:[
        { id:"04f6600e-821e-4968-934b-29a3f600d8ed", name: "Time 1" },
        { id:"16b45733-887a-4226-98a5-4a658cbbfd36", name: "Time 2" },
        { id:"63163b6c-709d-479d-8190-68200c2bc98c", name: "Time 3" },
        { id:"1a167632-ccca-4314-921d-d2165a9fe8c1", name: "Time 4" },
      ],
    };
  },
};
</script>
<template>
  <div class="container">
    <div class="title">
      <h2> Gerenciamento de times</h2>
    </div>
    <div class="form-input">
      <input type="text" />
      <button>Salvar</button>
    </div>
    <div class="list-items">
      <table>
        <thead>
          <tr>
            <th>ID</th>
            <th>Nome</th>
            <th>Ações</th>
          </tr>
        </thead>
        <tbody>
        <tr v-for="time in times" :key="time.id">
          <td> {{ time.id }} </td>
          <td> {{ time.name }} </td>
          <td>???</td>
        </tr>
      </tbody>
      </table>
      
    </div>
  </div>
</template>

<style> </style>
