<template>
  <div max-width="100%">
  <v-card
    class="ma-2 mb-4"
    color="grey lighten-5"
    outlined
  >
    <v-img
      src="https://scontent.fdvo2-1.fna.fbcdn.net/v/t1.6435-9/119518678_145686613864372_4202716177398651583_n.jpg?_nc_cat=100&ccb=1-5&_nc_sid=174925&_nc_ohc=n85sGWWalboAX_Jfn_0&_nc_ht=scontent.fdvo2-1.fna&oh=e9bdb6808e41b8cb89928a85225d2abd&oe=617ECC71"
      height="200px"
    ></v-img>

    <v-card-title>
      <h5>LEVZ T. BONIFACIO</h5>
    </v-card-title>

    <v-card-subtitle>
      jr Developer
    </v-card-subtitle>

    <v-card-actions>
      <v-btn
        color="teal"
        text
      >
        Dev languages
      </v-btn>

      <v-spacer></v-spacer>

      <v-btn
        icon
        @click="show = !show"
      >
        <v-icon>{{ show ? 'mdi-chevron-up' : 'mdi-chevron-down' }}</v-icon>
      </v-btn>
    </v-card-actions>

    <v-expand-transition>
      <div v-show="show">
        <v-divider></v-divider>

        <v-card-text>
           <v-card
                class="mx-auto"
                max-width="500"
                outlined
            >
                <v-list subheader>
                <v-subheader>Recent language</v-subheader>

                <v-list-item
                    v-for="chat in recent"
                    :key="chat.title"
                >
                    <v-list-item-avatar>
                    <v-img
                        :alt="`${chat.title} avatar`"
                        :src="chat.avatar"
                    ></v-img>
                    </v-list-item-avatar>

                    <v-list-item-content>
                    <v-list-item-title v-text="chat.title"></v-list-item-title>
                    </v-list-item-content>

                </v-list-item>
                </v-list>
            </v-card>
        </v-card-text>
      </div>
    </v-expand-transition>
  </v-card>
  </div>
</template>

<script>
  export default {
    data: () => ({
      show: false,
      recent: [
        {
          active: true,
          avatar: 'https://mpng.subpng.com/20190627/ttx/kisspng-javascript-computer-icons-scalable-vector-graphics-list-of-javascript-enhancements-fandom-developers-5d145895b06253.7824611015616144857225.jpg',
          title: 'Java Script',
        },
        {
          avatar: 'https://i.stack.imgur.com/KGl5c.png',
          title: 'Nuxt JS',
        },
        {
          avatar: 'https://w7.pngwing.com/pngs/70/60/png-transparent-vue-js-javascript-library-github-github-angle-text-triangle.png',
          title: 'Vue JS',
        },
        {
          avatar: 'https://e7.pngegg.com/pngimages/119/167/png-clipart-firebase-cloud-messaging-google-developers-software-development-kit-google-angle-triangle-thumbnail.png',
          title: 'Fire Base',
        },
        {
          avatar: 'https://banner2.cleanpng.com/20180412/kye/kisspng-python-programming-language-computer-programming-language-5acfdc3636bac7.8891188615235717662242.jpg',
          title: 'Python',
        },
        {
          avatar: 'https://www.clipartmax.com/png/middle/218-2181371_logo-git-git-icon.png',
          title: 'Git',
        },
      ],
      previous: [{
        title: 'Travis Howard',
        avatar: 'https://cdn.vuetifyjs.com/images/lists/5.jpg',
      }],
    }),
  }
</script>

<style scoped>
.v-progress-circular {
  margin: 1rem;
}
</style>