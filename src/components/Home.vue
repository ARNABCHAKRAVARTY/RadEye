<template>
  <div class="home">
    <v-container class="grey lighten-5">
      <v-row>
        <v-col :key="1" :cols="3" sm="4">
          <v-card>
            <v-expansion-panels>
              <v-expansion-panel>
                <v-expansion-panel-header v-slot="{ open }">
                  <v-row no-gutters>
                    <v-col cols="4">Ouput of Model</v-col>
                    <v-col cols="8" class="text--secondary">
                      <v-fade-transition leave-absolute>
                        <span v-if="open">Other options</span>
                        <v-row v-else no-gutters style="width: 100%">
                          <v-col cols="6">Confidence of Model</v-col>
                        </v-row>
                      </v-fade-transition>
                    </v-col>
                  </v-row>
                </v-expansion-panel-header>
                <v-expansion-panel-content>
                  <v-row justify="space-around" no-gutters>
                    <v-col cols="3"></v-col>

                    <v-col cols="3"></v-col>
                  </v-row>
                </v-expansion-panel-content>
              </v-expansion-panel>
              <v-expansion-panel>
                <v-expansion-panel-header v-slot="{ open }">
                  <v-row no-gutters>
                    <v-col cols="4">Ouput of Model</v-col>
                    <v-col cols="8" class="text--secondary">
                      <v-fade-transition leave-absolute>
                        <span v-if="open">Other options</span>
                        <v-row v-else no-gutters style="width: 100%">
                          <v-col cols="6">Confidence of Model</v-col>
                        </v-row>
                      </v-fade-transition>
                    </v-col>
                  </v-row>
                </v-expansion-panel-header>
                <v-expansion-panel-content>
                  <v-row justify="space-around" no-gutters>
                    <v-col cols="3"></v-col>

                    <v-col cols="3"></v-col>
                  </v-row>
                </v-expansion-panel-content>
              </v-expansion-panel>
              <v-expansion-panel>
                <v-expansion-panel-header v-slot="{ open }">
                  <v-row no-gutters>
                    <v-col cols="4">Ouput of Model</v-col>
                    <v-col cols="8" class="text--secondary">
                      <v-fade-transition leave-absolute>
                        <span v-if="open">Other options</span>
                        <v-row v-else no-gutters style="width: 100%">
                          <v-col cols="6">Confidence of Model</v-col>
                        </v-row>
                      </v-fade-transition>
                    </v-col>
                  </v-row>
                </v-expansion-panel-header>
                <v-expansion-panel-content>
                  <v-row justify="space-around" no-gutters>
                    <v-col cols="3"></v-col>

                    <v-col cols="3"></v-col>
                  </v-row>
                </v-expansion-panel-content>
              </v-expansion-panel>
            </v-expansion-panels>
          </v-card>
        </v-col>


        <v-col :key="2" :cols="12" sm="4">
          <v-file-input
            v-model="files"
            placeholder="Upload your documents"
            label="File input"
            multiple
            prepend-icon="mdi-paperclip"
          >
            <template v-slot:selection="{ text }">
              <v-chip small label color="primary">{{ text }}</v-chip>
            </template>
          </v-file-input>
          <v-btn right color="primary">UPLOAD</v-btn>
        </v-col>


        <v-col :key="3" :cols="3" sm="4">
          <v-card>
            <v-switch
              v-model="switch1"
              :label="`Mask 1: ${switch1.toString()}`"
            ></v-switch>
            <v-switch
              v-model="switch2"
              :label="`Mask 2: ${switch2.toString()}`"
            ></v-switch>
            <v-switch
              v-model="switch3"
              :label="`Mask 3: ${switch3.toString()}`"
            ></v-switch>
          </v-card>
        </v-col>
      </v-row>
    </v-container>
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from "@/components/HelloWorld.vue";

export default {
  name: "home",
  components: {
    HelloWorld
  },
  data: () => ({
    date: null,
    trip: {
      name: "",
      location: null,
      start: null,
      end: null
    },
    locations: [
      "Australia",
      "Barbados",
      "Chile",
      "Denmark",
      "Equador",
      "France"
    ],
    switch1: true,
    switch2: true,
    switch3: true,
  })
};
</script>
