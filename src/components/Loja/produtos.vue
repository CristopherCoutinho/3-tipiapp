<template>
  <h3>Mais Vendidos -></h3>
  <br />

  <div id="cards-container">
    <ion-card v-for="produto in produtos">
      <img :src="produto.photoUrl" class="image-produto" />
      <ion-card-header>
        <ion-card-title>{{ produto.name }}</ion-card-title>
        <ion-card-subtitle>Valor: {{ produto.price }}</ion-card-subtitle>
      </ion-card-header>
    </ion-card>
  </div>
</template>

<script>
import { defineComponent } from "vue";

export default defineComponent({
  name: "Produtos",
  data: () => {
    return {
      produtos: [
        {
          name: "Nike Air Force",
          photoUrl:
            "https://conteudo.imguol.com.br/c/entretenimento/72/2019/05/22/nike-air-force-1-porto-rico-1558528147715_v2_900x506.jpg",
          price: 890.9,
        },
        {
          name: "Adidas Super Star",
          photoUrl:
            "https://artwalk.vteximg.com.br/arquivos/ids/261008-380-380/GX184-0-100-1.jpg?v=637929057994870000",
          price: 399.9,
        },
        {
          name: "Olimpikus Corre 2",
          photoUrl:
            "https://static.hupishop.com.br/public/hupibikes/imagens/produtos/tenis-olympikus-corre-2-unissex-multicolor-20990.jpg",
          price: 499.9,
        },
        {
          name: "Derby CNS 2702 Preto",
          photoUrl:
            "https://encrypted-tbn0.gstatic.com/shopping?q=tbn:ANd9GcREJcSfXE_0RBN7wDsSP4hrFh_pYTdPZoGIaTpvrzZUu_Ubvkr8Vahueg4cPWgYNXnZU8qsNXhd&usqp=CAc",
          price: 499.9,
        },
      ],
    };
  },
});
</script>
<style>
#cards-container {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-evenly;
}
ion-card {
  border-radius: 25px;
  border: 2px solid #77ccff;
  margin: 5px 0;
  height: 240px;
  width: calc(40% - 15px);
  text-align: center;
}
ion-card-title {
  font-size: small;
}
ion-card-header.ios {
  display: flex;
  flex-flow: column-reverse;
}

.image-produto {
  height: 50%;
  width: 200px;
  border-bottom: 2px solid #77ccff;
}
</style>
