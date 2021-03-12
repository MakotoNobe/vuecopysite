<template>
  <div>
    <v-navigation-drawer app v-model="isOpenSideBar" right>
      <v-list-item>
          <v-list-item-title class="title">ToDo</v-list-item-title>
      </v-list-item>
     <v-divider></v-divider>

      <v-list-group color="primary">
      <v-list rounded>
        <v-list-item @click="switchCreateTaskDialog(true)">          
          <v-list-item-content>
            <v-list-item-title><v-icon>mdi-plus</v-icon>タスクを追加</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
        
        <v-list-item v-for="(event,index)in events" :key="index" @click="toEventPage(event, eventNo)">
          <v-list-item-content>
            <v-list-item-title>
                {{event.taskNo}}:{{event.name}}
                </v-list-item-title>
          </v-list-item-content>
        </v-list-item>
        
      </v-list>
    </v-list-group>
    </v-navigation-drawer>
  </div>
</template> 

<script>
export default {
    data: () => ({
      isOpenSideBar: false,
      // group: null,
    }),

    watch: {
      group () {
        this.isOpenSideBar = false
      },
    },
  }

//     data(){
//         return{}
//     },
//     computed:{
//         isOpenSideBar:{
//             get(){
//                 return this.$store.state.isOpenSideBar;
//             },
//             set(value){
//                 this.$store.dispatch("switchSidebar",value);
//             }
//         }
//     },
//     event:{
//         get(){
//           return this.$store.state.event.events;
//           }
//     },
//     methods:{
//               switchCreateTaskDialog(value){
//               this.$store.dispatch("switchCreateTaskDialog",value);
//               },
//               toEventPage(eventNo){
//               this.$router.push(`/event/${eventNo}`)
//               }
//     }
// };
</script>