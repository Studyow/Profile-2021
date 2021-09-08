<template>
    <div class="dashboard">
        <h1 class="subheading grey--text">Dashboard</h1>
        <v-container class="my-5">

            <v-layout row wrap>
                <v-flex xs12 md12>
                    <v-btn outline block class="primary">1
                    </v-btn>
                </v-flex>
                <v-flex xs6 md3>
                    <v-btn outline block class="primary">2</v-btn>
                </v-flex>
                <v-flex xs12 md6>
                    <v-btn outline block class="primary">Front end</v-btn>
                    <v-card flat class="mx-lg-auto" v-for="project in projects" :key="project.title">
                        <v-layout wrap class="pa-2">
                            <v-flex xs4 md4>
                                <div class="caption gray--text">Design tool</div>
                                <div>{{ project.title }}</div>
                            </v-flex>
                            <v-flex xs4 sm4 md5>
                                <div class="caption gray--text">progress</div>
                                <v-progress-linear
                                v-model="project.progress"
                                color="teal accent-4"
                                height="12"
                                class="mt-2"
                                >
                                <template v-slot:default="{ value }">
                                    <strong class="caption black--text">{{ Math.ceil(value) }}%</strong>
                                </template>
                                </v-progress-linear>
                            </v-flex>
                            <v-flex xs4 md3 class="pl-2">
                                <div class="float-right">
                                    <v-chip
                                    :class="`project ${project.status}`"
                                    class="ma-2 font-weight-light"
                                    small
                                    >
                                    {{ project.status }}
                                    </v-chip>
                                </div>
                            </v-flex>
                        </v-layout>
                        <v-divider></v-divider>
                    </v-card>
                </v-flex>
                <v-flex xs6 md3>
                    <v-btn outline block class="primary">2</v-btn>
                </v-flex>
            </v-layout>

            <v-layout row wrap justify-center>
                <v-flex xs4 md3>
                    <v-btn outline block class="success">1</v-btn>
                </v-flex>
                <v-flex xs4 md3>
                    <v-btn outline block class="success">2</v-btn>
                </v-flex>
            </v-layout>

        </v-container>        
    </div>
</template>

<script>
export default {
    data() {
        return {
            projects: [
                {tool: 'adobe', title: 'Illustrator', progress: '95', status: 'always'},
                {tool: 'adobe', title: 'Photoshop', progress: '90', status: 'always'},
                {tool: 'js framework', title: 'Vue JS', progress: '88', status: 'always'},
                {tool: 'modern js', title: 'JavaScript', progress: '80', status: 'always'},
                {tool: 'css', title: 'SASS/CSS', progress: '90', status: 'always'},
                {tool: 'dom', title: 'HTML 5', progress: '90', status: 'always'},
                {tool: 'framework', title: 'Bootstrap', progress: '80', status: 'not-always'},
                {tool: 'adobe', title: 'Animate', progress: '80', status: 'not-always'},
                {tool: 'blog', title: 'Wordpress DIVI', progress: '95', status: 'always'},
            ]
        }
    }
}
</script>

<style>
.project.always {
    border: 1px solid #1DE9B6;
    color: #1DE9B6;
}
.project.not-always {
    border: 1px solid #D4E157;
    color: #D4E157;
}
</style>