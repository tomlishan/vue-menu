<template>
  <v-sheet
    height="89vh"
    width="117vw"
    class="overflow-hidden"
    style="position: relative;"
  >
          <v-row
          align="end"
          no-gutters
          style="height:170vh;"
        >
    <v-container 
    class="fill-height  lighten-3 mb-12"
>
      <v-footer 
      padless 
      width="100vw"
      color="#C0C0C0"
      >
    <v-col
      class="text-center"
      cols="12"
    >
      {{ new Date().getFullYear() }} — <strong>Vuetify</strong>
    </v-col>
    
  </v-footer>

    </v-container>
</v-row>
    <v-navigation-drawer
      v-model="drawer"
      absolute
      dark 
      color="#000000"   
    >
      <v-divider></v-divider>

      <v-list dense>
        <v-list-item
          v-for="item in items"
          :key="item.title"
          link
        >
          <v-list-item-icon>
            <v-icon>{{ item.icon }}</v-icon>
          </v-list-item-icon>

          <v-list-item-content>
            <v-list-item-title>{{ item.title }}</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list>

        <v-list-group
          :value="true"
          no-action
          sub-group
        >
          <template v-slot:activator>
            <v-list-item-content>
              <v-list-item-title>Admin</v-list-item-title>
            </v-list-item-content>
          </template>

          <v-list-item
            v-for="([title, icon], i) in admins"
            :key="i"
            link
          >
            <v-list-item-title v-text="title"></v-list-item-title>

            <v-list-item-icon>
              <v-icon v-text="icon"></v-icon>
            </v-list-item-icon>
          </v-list-item>
        </v-list-group>


        <template v-slot:append>
          <div class="pa-2">
            <v-btn block color="#abcdef">
              Logout
            </v-btn>
          </div>
        </template>


    </v-navigation-drawer>
  </v-sheet>
  
</template>

<script>
  export default {
    data () {
      return {
        drawer: true,
        items: [
          { title: 'Home', icon: 'mdi-view-dashboard' },
          { title: 'About', icon: 'mdi-forum' },
        ],
        admins: [
        ['Management', 'mdi-account-multiple-outline'],
        ['Settings', 'mdi-cog-outline'],
      ],
      cruds: [
        ['Create', 'mdi-plus-outline'],
        ['Read', 'mdi-file-outline'],
        ['Update', 'mdi-update'],
        ['Delete', 'mdi-delete'],
      ],
      }
    },
  }
</script>