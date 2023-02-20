<template>
     <div class="item-experiences">
          <div class="left">
               {{ data.year }}
          </div>
          <div class="right">
               <h1>{{ data.year }}</h1>
               <h2>{{ data.company }}</h2>
               <p>{{ data.description }}</p>
              
               <div v-for="reference in data.references" :key="reference.id" class="references">
                    <ExReference v-if="reference.text !== ''" :data="reference"/>
               </div>
          </div>
     </div>
</template>

<script>
import { ref } from "vue";
import ExReference from './ExReference.vue'

export default {
     props: ["data"],
     components: {
        ExReference
     },
     setup(props) {
          const data = ref(null);
          data.value = props.data;

          //more

          return { data };
     },
};
</script>

<style lang="scss" scoped>
@import "../style/style.scss";

.item-experiences {
     width: 100%;
     border-top: 1px solid #929292;
     display: flex;

     .left {
          color: $yellow;
          font-size: 30px;
          font-weight: 600;
          margin-left: 10px;
          margin-top: 10px;
          width: 30%;
     }

     .right {
          width: 70%;

          h1 {
               display: none;
          }

          h2 {
               margin-top: 15px;
          }

          p {
               font-size: 20px;
               font-weight: 200;
               margin-left: 10px;
          }

          .references {
               margin-left: 10px;
          }
     }
}

@media only screen and (max-width: 1000px) {
     .item-experiences {
          .right {
               h2 {
                    margin-top: 15px;
                    font-size: 20px;
               }

               p {
                    font-size: 18px;
               }
          }
     }
}

@media only screen and (max-width: 750px) {
     .item-experiences {
          .left {
               display: none;
          }
          .right {
               width: 95%;

               h1 {
                    display: block;
                    color: $yellow;
                    margin-bottom: 0px;
               }

               h2 {
                    margin-top: 15px;
                    margin-left: 20px;
                    font-size: 20px;
               }

               p {
                    font-size: 18px;
                    margin-left: 40px;
               }

               .references {
                    margin-left: 40px;
               }
          }
     }
}
</style>
