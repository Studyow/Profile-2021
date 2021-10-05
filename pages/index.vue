<template>
  <v-card
    class="mx-auto"
    max-width="344"
  >
    <v-img
      src="https://scontent.fdvo2-1.fna.fbcdn.net/v/t1.6435-9/119518678_145686613864372_4202716177398651583_n.jpg?_nc_cat=100&ccb=1-5&_nc_sid=174925&_nc_ohc=n85sGWWalboAX_Jfn_0&_nc_ht=scontent.fdvo2-1.fna&oh=e9bdb6808e41b8cb89928a85225d2abd&oe=617ECC71"
      height="200px"
    ></v-img>

    <v-card-title>
      LEVZ T. BONIFACIO
    </v-card-title>

    <v-card-subtitle>
      jr Developer
    </v-card-subtitle>

    <v-card-actions>
      <v-btn
        color="orange lighten-2"
        text
      >
        As i
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
          I would love to work for a company that would help me grow my career, skillset and as a person.
          A job that will continue to inspire me to develop cool things each and everyday day.
          A company that will mold me personally whilst making the world a better place.  
           <div
              align="center"
              justify="space-around"
            >
            <v-btn
              elevation="2"
            >
            <NuxtLink to="/about">About Me</NuxtLink>
            </v-btn>
          </div>
        </v-card-text>
      </div>
    </v-expand-transition>
  </v-card>
</template>

<script>
  export default {
    data: () => ({
      show: false,
    }),
  }
</script>