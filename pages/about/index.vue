<template>
  <v-container>
    <v-row justify="space-around">
      <v-card width="400">
        <v-img
        height="200px"
        src="https://scontent.fcgy1-1.fna.fbcdn.net/v/t39.30808-6/240663095_391432195665100_1323342280268819862_n.jpg?_nc_cat=102&ccb=1-5&_nc_sid=09cbfe&_nc_ohc=gHPBeINbQhEAX9VGuRq&_nc_ht=scontent.fcgy1-1.fna&oh=9227f15aef7d550227f0d5a9502ffc13&oe=61329269"
        >
          <v-app-bar
            flat
            color="rgba(0, 0, 0, 0)"
          >

            <v-toolbar-title class="text-h6 white--text pl-0">
              About Me
            </v-toolbar-title>

            <v-spacer></v-spacer>

            <v-btn
              color="white"
              icon
            >
              <v-icon>mdi-dots-vertical</v-icon>
            </v-btn>
          </v-app-bar>

          <v-card-title class="white--text mt-8">
            <v-avatar size="56">
              <img
                alt="user"
                src="https://scontent.fcgy1-1.fna.fbcdn.net/v/t1.6435-9/148506460_270336911107963_6828876521119950891_n.jpg?_nc_cat=109&ccb=1-5&_nc_sid=174925&_nc_ohc=gdZbEjRiv1UAX-4w594&_nc_ht=scontent.fcgy1-1.fna&oh=4ec5cf005053394a5136dc0eef215965&oe=615453C4"
              >
            </v-avatar>
            <p class="ml-3">
              Levz tibayan
            </p>
          </v-card-title>
        </v-img>

        <v-card-text>
          <div class="font-weight-bold ml-8 mb-2">
            My Experience
          </div>

          <v-timeline
            align-top
            dense
          >
            <v-timeline-item
              v-for="message in messages"
              :key="message.time"
              :color="message.color"
              small
            >
              <div>
                <div class="font-weight-normal">
                  <strong>{{ message.from }}</strong> <br>
                   <v-chip
                    class="ma-2"
                    color="teal lighten-2"
                    outlined
                    x-small
                    >
                    <v-icon left>
                        mdi-clock-time-eight-outline
                    </v-icon>
                    {{ message.time }}
                    </v-chip>
                </div>
                <div>{{ message.message }}</div>
              </div>
            </v-timeline-item>
          </v-timeline>
        </v-card-text>
      </v-card>
    </v-row>
  </v-container>
</template>


<script>
  export default {
    data: () => ({
    overlay: false,

      messages: [
        {
          from: 'DMSF Davao Medical School Foundation',
          message: `Information technology Professional`,
          time: '2016 – 2017',
          color: 'teal darken-2',
        },
        {
          from: 'SAMATOSA SOFTWARE COMPANY',
          message: 'FRONT END JUNIOR GRAPHIC DESIGNER, A software company focused on web & mobile',
          time: '2017 – 2018',
          color: 'teal accent-3',
        },
        {
          from: 'MYBraveTrueHero Web-Solutions',
          message: 'WEB DEV | UI | UX DESIGNER, building websites and optimization',
          time: '2016 – 2017',
          color: 'teal darken-2',
        },
        {
          from: 'DETAIL ONLINE agile tech company',
          message: 'GRAPHIC DESIGNER & FRONT-END ANALYSIS, Homebase, smart search tech and artificial intelligence',
          time: '2019 – 2020',
          color: 'teal accent-3',
        }
      ],
    }),
  }
</script>