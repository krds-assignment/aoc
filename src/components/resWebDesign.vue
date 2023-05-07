<template>
    <div class="parentElement">
      <div v-for="detail of templateJsonData" :key="detail.title"
      class="webLoopElement" :style="{'background-color': detail.bgColor}">
          <div class="cardHeadElement">
              <div class="detailsContent">
                  <div>
                      <img :src="detail.logo" :alt="detail.title">
                  </div>
                  <div>
                  <p class="title">
                      {{ detail.title }}
                  </p>
                  <p>
                      {{ detail.desc }}
                  </p>
              </div>
              </div>
              <div class="desktop">
                  <img :src="detail.image" :alt="detail.title">
              </div>
          </div>
          <div></div>
      </div>
      
    </div>
  </template>
  
  <script>
  import { loopData } from '@/js/data.js'
  export default {
      data() {
          return {
              templateJsonData: [],
          }
      },
      created() {
          this.templateJsonData = loopData;
      }
  }
  
  </script>