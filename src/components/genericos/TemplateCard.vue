<template>
  <v-card
    class="mx-auto my-10"
    width="350"
  >

    <v-img align="center">
      <slot name="imagem"></slot>
    </v-img>
    
    <v-card-title>
        <slot name="titulo"></slot>
    </v-card-title>

    <v-card-text>
      <v-row
        align="center"
        class="mx-0"
      >
        <v-rating
          :value="5.0"
          color="amber"
          dense
          half-increments
          readonly
          size="14"
        ></v-rating>

        <div class="grey--text ms-4">
          5.0
        </div>
      </v-row>

      <div class="my-4 text-subtitle-1 red--text">
        <slot name="preco"></slot>
      </div>

      <div class="my-4 text-subtitle-1">
        <slot name="codigo"></slot>
      </div>

      <div>
        <slot name="modelo"></slot>
      </div>

      <div>
        <slot name="capacidade"></slot>
      </div>

      <div>
        <slot name="marca"></slot>
      </div>
      
      <div>
        <slot name="desc1"></slot>
      </div>
      <div>
        <slot name="desc2"></slot>
      </div>
      <div>
        <slot name="desc3"></slot>
      </div>
      <div>
        <slot name="desc4"></slot>
      </div>
      <div>
        <slot name="desc5"></slot>
      </div>

      <div>
        <slot name="garantia"></slot>
      </div>
    </v-card-text>
  </v-card>
</template>


<script lang="ts">
import Vue from "vue";
import { Component } from "vue-property-decorator";

@Component
export default class templateCard extends Vue {}
</script>

<style lang="scss">
</style>