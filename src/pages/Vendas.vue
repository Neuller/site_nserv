<template>
  <div class="vendasProdutos">
    <!-- CAROUSEL -->
    <div 
    offset-y
    text-center
    class="desktop"
    >
      <v-carousel 
      v-model="model"
      cycle
      height="500"
      >
        <v-carousel-item
          v-for="(item, i) in items"
          :key="i"
          :src="item.src"
        >
            <v-row
              class="fill-height"
              align="center"
              justify="center"
            >
            </v-row>
        </v-carousel-item>
      </v-carousel>
    </div>

    <!-- COMPUTADORES -->
    <v-row>
      <v-col cols="12">
        <titleH2 class="mt-16">
          <template v-slot:titulo>Computadores</template>
        </titleH2>
        <computadores></computadores>
      </v-col>
    </v-row>

    <!-- ALL IN ONE -->
    <v-row>
      <v-col cols="12">
        <titleH2 class="mt-16">
          <template v-slot:titulo>All In One</template>
        </titleH2>
        <allInOne></allInOne>
      </v-col>
    </v-row>

    <!-- PROCESSADORES -->
    <v-row>
      <v-col cols="12">
        <titleH2 class="mt-16">
          <template v-slot:titulo>Processadores</template>
        </titleH2>
        <processadores></processadores>
      </v-col>
    </v-row>

    <!-- PLACAS MAE -->
    <v-row>
      <v-col cols="12">
        <titleH2 class="mt-16">
          <template v-slot:titulo>Placas Mãe</template>
        </titleH2>
        <placasMae></placasMae>
      </v-col>
    </v-row>

    <!-- MEMORIAS -->
    <v-row>
      <v-col cols="12">
        <titleH2 class="mt-16">
          <template v-slot:titulo>Memórias</template>
        </titleH2>
        <memorias></memorias>
      </v-col>
    </v-row>

    <!-- DISCOS RIGIDOS -->
    <v-row>
      <v-col cols="12">
        <titleH2 class="mt-16">
          <template v-slot:titulo>Discos Rígidos</template>
        </titleH2>
        <discosRigidos></discosRigidos>
      </v-col>
    </v-row>

    <!-- PLACAS DE VIDEO -->
    <v-row>
      <v-col cols="12">
        <titleH2 class="mt-16">
          <template v-slot:titulo>Placas de Vídeo</template>
        </titleH2>
        <placasVideo></placasVideo>
      </v-col>
    </v-row>

    <!-- IMPRESSORAS -->
    <v-row>
      <v-col cols="12">
        <titleH2 class="mt-16">
          <template v-slot:titulo>Impressoras</template>
        </titleH2>
        <impressoras></impressoras>
      </v-col>
    </v-row>
    
    <!-- MONITORES E TVs -->
    <v-row>
      <v-col cols="12">
        <titleH2 class="mt-16">
          <template v-slot:titulo>Monitores e TVs</template>
        </titleH2>
        <monitores></monitores>
      </v-col>
    </v-row>

  </div>
</template>

<script lang="ts">
import Vue from "vue";
import { Component } from "vue-property-decorator";

@Component
export default class Produtos extends Vue {
    model = 0;
    loading = false;
    selection = 1;
    items = [
        {
          src: "/vendas/SLIDE1.png",
        },
        {
          src: "/vendas/SLIDE2.png",
        }
    ];

    reserve() {
      this.loading = true;
      setTimeout(() => (this.loading = false), 2000);
    }
}
</script>

<style lang="scss">
.v-expansion-panel-content > div {
  padding: 0 !important;
}
@media(max-width: 760px) {
  .desktop {
    display: none;
  }
}
</style>