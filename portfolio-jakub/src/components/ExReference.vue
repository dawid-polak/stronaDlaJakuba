<template>
     <div>
          <p v-if="show" class="text">{{ data.text }}</p>
          <p v-else class="text">{{ data.paragraph }}</p>
          <p class="author">{{ data.author }}</p>
          <button @click="handleShow" class="btn">{{ btnText }}</button>
     </div>
</template>

<script>
import { ref } from "vue";

export default {
     props: ["data"],
     setup(props) {
          const show = ref(false);
          const btnText = ref("more");

          const handleShow = () => {
               show.value = !show.value;

               if (btnText.value === "more") {
                    btnText.value = "less";
               } else {
                    btnText.value = "more";
               }
          };

          return { show, btnText, handleShow };
     },
};
</script>

<style lang="scss" scoped>
@import "../style/style.scss";

.text {
     font-style: italic;
     color: #929292;
     margin-bottom: 0px;
     display: inline-block;
     height: 30px;
     font-size: 14px;
     font-weight: 200;
     margin-left: 10px;
}

.author {
     margin: 0px 0px 0px 10px;
     font-size: 14px;
     font-weight: 400;
}

.btn {
     border: 0;
     background-color: $yellow;
     color: #fff;
     padding: 6px 10px 6px 10px;
     margin: 5px 0px 10px 10px;
     cursor: pointer;
     font-size: 12px;
}
</style>
