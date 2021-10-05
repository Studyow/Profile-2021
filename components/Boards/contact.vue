<template>
  <v-card
    class="ma-2 mb-4"
    color="grey lighten-5"
    outlined
  >
    <v-toolbar
      color="teal"
      dark
    >

      <v-toolbar-title >Contact</v-toolbar-title>
    </v-toolbar>

    <v-list color="grey lighten-5">
      <v-list-group
        v-for="item in items"
        :key="item.title"
        v-model="item.active"
        :prepend-icon="item.action"
        no-action
      >
        <template v-slot:activator>
          <v-list-item-content>
            <v-list-item-title v-text="item.title"></v-list-item-title>
          </v-list-item-content>
        </template>

        <v-list-item
          v-for="child in item.items"
          :key="child.title"
        >
          <v-list-item-content>
            <v-list-item-title v-text="child.title"></v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list-group>
    </v-list>
  </v-card>
</template>


<script>
  export default {
    data: () => ({
      items: [
        {
          action: 'mdi-cellphone',
          items: [{ title: '09126321772' }],
          title: 'Cell Number',
        },
        {
          action: 'mdi-facebook',
          active: false,
          items: [{ title: 'fb.com/caped.man.9/' }],
          title: 'Facebook',
        },
        {
          action: 'mdi-skype',
          items: [{ title: 'Johnlevybonifacio' }],
          title: 'skype',
        },
        {
          action: 'mdi-gmail',
          items: [{ title: 'tibayanlevz@gmail.com' }],
          title: 'Email',
        },
      ],
    }),
  }
</script>