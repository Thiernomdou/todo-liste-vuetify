<template>
  <div class="home">
    <v-list class="pt-0" flat>
      <div v-for="(langage, index) in langages" :key="index">
      
        <v-list-item @click="finiLangage(langage.index)">
          <template v-slot:default>
            <v-list-item-action>
              <v-checkbox
                :input-value="langage.fini"
                color="primary"
              ></v-checkbox>
            </v-list-item-action>

            <v-list-item-content>
              <v-list-item-title>{{ langage.title }}</v-list-item-title>
            </v-list-item-content>
          </template>
        </v-list-item>
      
        <v-divider></v-divider>

      </div>
    </v-list>
  </div>
</template>

<script>
  
  export default {
    name: 'Todo',
    data() {
      return {
        langages: [
          {id: 1, title: 'JavaScript', fini: false},
          {id: 2, title: 'C#.NET', fini: false},
          {id: 3, title: 'Python', fini: false},
          {id: 4, title: 'PHP', fini: false}
        ]
      }
    },
    methods: {
      finiLangage(id) {
        let langage = this.langages.filter(langage => langage.id === index)[0];
        langage.fini = !langage.fini;
      }
    },
    components: {

    },
  }
</script>
