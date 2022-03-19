<template>
  <div class="teste-for">
    <h2>Teste For</h2>
    <ul>
      <li v-for="animal of animais" :key="animal.id">
          <img :src="animal.url" :alt="animal.nome">
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "TesteFor",
  data() {
    return {
      animais: [
        {
          id: 1,
          nome: "Gatinho",
          url: "https://www.petz.com.br/blog/wp-content/uploads/2020/04/meu-primeiro-gato.jpg",
        },
        {
          id: 2,
          nome: "Cachorrinho",
          url: "https://image.cachorrogato.com.br/thumb/1200/630/1/imagens/original/imagem858.jpg",
        },
      ],
    };
  },
};
</script>

<style scoped>
    img{
        width: 400px;
        height: auto;
    }
    li{
        list-style-type: none;
    }
</style>