<template>
  <div id="vendedores">
    <img
      v-for="vendedor in vendedores"
      :src="vendedor.photoUrl"
      class="image-vendedor"
    />
  </div>
</template>
<script>
import { defineComponent } from "vue";

export default defineComponent({
  name: "Vendedores",
  data: () => {
    return {
      vendedores: [
        {
          photoUrl:
            "https://i.pinimg.com/736x/e7/e2/8a/e7e28ae48f7f3e9d35dc92c35f1166ab.jpg",
        },
        {
          photoUrl:
            "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcRC2av3ndnbtkAVbirqjTzNk8a1J1wAypGapw&usqp=CAU",
        },
        {
          photoUrl: "https://pbs.twimg.com/media/FFpJ_QpXIAAANvm.png",
        },
        {
          photoUrl:
            "https://www.estrelando.com.br/uploads/2020/08/03/dwayne-johnson-the-rock-1596491732.jpg",
        },
      ],
    };
  },
});
</script>

<style>
#vendedores {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-evenly;
  margin: 20px;
}
.image-vendedor {
  height: 60px;
  width: 50px;
  border-radius: 50%;
}
</style>
