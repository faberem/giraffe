<template>
  <div>
    <div>
      <v-container>
        <v-row>
          <v-col cols="8">
            <v-card height="300px">
              <v-list-item two-line>
                <v-list-item-content class="item-class">

                  <h1 class="header-class">MI in a Nutshell</h1>
                  <p class = "p-class"> Ziel ist es einen Überblick über die verschiedenen Projekte / Aktivitäten der Institute für Medizininformatik oder relevante Themen
                    der Medizininformatik kennenzulernen. Im Rahmen dieser Events sollen Konzepte, technische Hintergründe und Zusammenhänge kurz vorgestellt werden.</p>
                </v-list-item-content>
              </v-list-item>
            </v-card>
          </v-col>
          <v-col cols="4">
            <v-card height="300px">
              <div class="img-class">
                <v-img
                    dark
                    height="160px"
                    src="/src/images/IMI_Logo.png"
                />
              </div>
            </v-card>
          </v-col>
        </v-row>
      </v-container>
    </div>
    <div class="pt-16">



    </div>
    <v-row>
      <v-col cols="12" lg="12" xl="8">
        <div>
          <div class="pt-16">
            <h2 class="text-h4 font-weight-bold pb-4">Nächste Vorträge</h2>

            <v-row>
              <v-col v-for="i in 3" :key="i" cols="12" lg="4" md="6">
                <v-hover
                    v-slot:default="{ hover }"
                    close-delay="50"
                    open-delay="50"
                >
                  <div>
                    <v-card
                        :color="hover ? 'white' : 'transparent'"
                        :elevation="hover ? 12 : 0"
                        flat
                        hover
                        to="/detail"
                    >
                      <v-img
                          :aspect-ratio="16 / 9"
                          class="elevation-2"
                          gradient="to top, rgba(25,32,72,.4), rgba(25,32,72,.0)"
                          height="200px"
                          src="https://unsplash.com/photos/hGV2TfOh0ns"
                          style="border-radius: 16px"
                      >
                        <!--                        <v-card-text>
                                                  <v-btn color="accent" to="category">TIPS</v-btn>
                                                </v-card-text>-->
                      </v-img>

                      <v-card-text>
                        <div class="text-h5 font-weight-bold primary--text">
                          DiGA - Digitale Gesundheitsapp
                        </div>

                        <div class="text-body-1 py-4">
                          Ultrices sagittis orci a scelerisque. Massa placerat
                          duis ultricies lacus sed turpis
                        </div>

                        <!--                        <div class="d-flex align-center">
                                                  <v-avatar color="accent" size="36">
                                                    <v-icon dark>mdi-feather</v-icon>
                                                  </v-avatar>

                                                  <div class="pl-2">Yan Lee · 22 July 2019</div>
                                                </div>-->
                      </v-card-text>
                    </v-card>
                  </div>
                </v-hover>
              </v-col>
            </v-row>
          </div>

          <!--          <div class="pt-16">
                      <h2 class="text-h4 font-weight-bold pb-4">Featured</h2>

                      <v-row>
                        <v-col v-for="i in 3" :key="i" cols="6" lg="4">
                          <v-card dark flat>
                            <v-img
                                :aspect-ratio="16 / 9"
                                class="elevation-2 fill-height"
                                gradient="to top, rgba(25,32,72,.4), rgba(25,32,72,.0)"
                                height="600px"
                                src="https://cdn.pixabay.com/photo/2019/10/29/14/46/landscape-4587079_1280.jpg"
                            >
                              <div
                                  class="d-flex flex-column justify-space-between fill-height"
                              >
                                <v-card-text>
                                  <v-btn color="accent">ANIMALS</v-btn>
                                </v-card-text>

                                <v-card-text>
                                  <div
                                      class="text-h5 py-3 font-weight-bold"
                                      style="line-height: 1.2"
                                  >
                                    15 things I have always wondered about birds
                                  </div>

                                  <div class="d-flex align-center">
                                    <v-avatar color="accent" size="36">
                                      <v-icon dark>mdi-feather</v-icon>
                                    </v-avatar>

                                    <div class="pl-2">Yan Lee · 03 Jan 2019</div>
                                  </div>
                                </v-card-text>
                              </div>
                            </v-img>
                          </v-card>
                        </v-col>
                      </v-row>
                    </div>-->

          <div class="pt-16">
            <h2 class="text-h4 font-weight-bold">Vergangene Vorträge</h2>

            <div>
              <v-row v-for="i in 6" :key="i" class="py-4">
                <v-col cols="12" md="4">
                  <v-card flat height="100%">
                    <v-img
                        :aspect-ratio="16 / 9"
                        height="90%"
                        src="/src/images/xDT.png"
                    ></v-img>
                  </v-card>
                </v-col>

                <v-col>
                  <div>
                    <v-btn color="accent" depressed>Download</v-btn>

                    <h3 class="text-h4 font-weight-bold pt-3">
                      xDT - Datenaustauschformate im deutschen Gesundheitswesen
                    </h3>



                    <!--                    <div class="d-flex align-center">
                                          <v-avatar color="accent" size="36">
                                            <v-icon dark>mdi-feather</v-icon>
                                          </v-avatar>

                                          <div class="pl-2">Yan Lee · 03 Jan 2019</div>
                                        </div>-->
                  </div>
                </v-col>
              </v-row>
            </div>
          </div>
        </div>
      </v-col>

      <v-col>
        <div class="pt-16">
          <siderbar/>
        </div>
      </v-col>
    </v-row>
  </div>
</template>

<script>
export default {
  name: "Home",
  components: {
    siderbar: () => import("@/components/details/sidebar"),
  },
};
</script>

<style>
.item-class{

}
.p-class{
  font-size: 20px;
  padding-top: 40px;
}
.header-class {
  padding-top: 35px;
  font-size: 80px;
  font-weight: 600;
}

.img-class {
  padding-top: 50px;

}
</style>
