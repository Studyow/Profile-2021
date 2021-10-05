<template>
    <div class="dashboard">
        <h1 class="subheading grey--text">Dashboard</h1>
        <div caption>
            <h5 color="green darken-2">
            <v-icon
                small
                color="teal"
                >
                mdi-calendar-month
            </v-icon>
                September 9, 2020
            </h5>
        </div>
        <v-container class="my-5">

            <v-layout row wrap class="d-flex justify-center">
                <v-flex xs12 md12>
                    <DashHeader/>
                </v-flex>

                <v-flex xs6 md3>
                    <Profile_dev/>
                    <Contact/>
                </v-flex>

                <v-flex xs12 md6>
                    <About/>
                    <FrontEnd/>
                </v-flex>

                <v-flex xs6 md3>
                    <Current/>
                </v-flex>
            </v-layout>


        </v-container>        
    </div>
</template>

<script>
import FrontEnd from '../components/Boards/front-end.vue'
import Current from '../components/Boards/current.vue'
import DashHeader from '../components/Boards/dash-header.vue'
import Profile_dev from '../components/Boards/profile-dev.vue'
import About from '../pages/about/index.vue'
import Contact from '../components/Boards/contact.vue'

export default {
  components: { FrontEnd, Current, DashHeader, Profile_dev, About, Contact },
    
}
</script>
