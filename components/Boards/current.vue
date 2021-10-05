<template>
  <v-card
    class="ma-md-2"
    color="grey lighten-5"
    outlined
  >
    <div class="d-flex pa-3">
        <h4>Currently</h4>
    </div>

    <v-divider></v-divider>

    <v-list two-line color="grey lighten-5">
      <v-list-item-group
        v-model="selected"
        active-class="teal--text"
        multiple
      >
        <template v-for="(item, index) in items">
          <v-list-item :key="item.title">
            <template v-slot:default="{ active }">
              <v-list-item-content>
                <v-list-item-title v-text="item.title"></v-list-item-title>

                <v-list-item-subtitle
                  class="text--primary"
                  v-text="item.headline"
                ></v-list-item-subtitle>

                <v-list-item-subtitle v-text="item.subtitle"></v-list-item-subtitle>
              </v-list-item-content>

              <v-list-item-action>
                <v-list-item-action-text v-text="item.action"></v-list-item-action-text>

                <v-icon
                  v-if="!active"
                  color="grey lighten-1"
                >
                  mdi-check
                </v-icon>

                <v-icon
                  v-else
                  color="teal darken-1"
                >
                  mdi-check
                </v-icon>
              </v-list-item-action>
            </template>
          </v-list-item>

          <v-divider
            v-if="index < items.length - 1"
            :key="index"
          ></v-divider>
        </template>
      </v-list-item-group>
    </v-list>
  </v-card>
</template>


<script>
  export default {
    data: () => ({
      selected: [0,1,2],
      items: [
        {
          action: 'Jan 2021',
          headline: 'Brunch this weekend?',
          subtitle: `I'll be in your neighborhood doing errands this weekend. Do you want to hang out?`,
          title: 'Learn Advance JavaScript',
        },
        {
          action: 'Feb 2021',
          headline: 'Summer BBQ',
          subtitle: `Wish I could come, but I'm out of town this weekend.`,
          title: 'me, Scrott, Jennifer',
        },
        {
          action: 'jun 2021',
          headline: 'Oui oui',
          subtitle: 'Do you have Paris recommendations? Have you ever been?',
          title: 'Sandra Adams',
        },
        {
          action: 'Aug 2021',
          headline: 'Birthday gift',
          subtitle: 'Have any ideas about what we should get Heidi for her birthday?',
          title: 'Trevor Hansen',
        },
        {
          action: 'Sep 2021',
          headline: 'Recipe to try',
          subtitle: 'We should eat this: Grate, Squash, Corn, and tomatillo Tacos.',
          title: 'Britta Holt',
        },
      ],
    }),
  }
</script>