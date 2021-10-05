<template>
  <v-container>
    <v-row justify="space-around">
      <v-card
      class="ma-2 mb-2"
      color="grey lighten-5"
      outlined
      width="100%"
      >
        <v-card-text>
          <div class="font-weight-bold mb-2">
            <h4>My Experience</h4>
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