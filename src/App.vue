<template>
     <div class="svgDiagramm">
          <img id = "svgidimg" svg-inline class="icon" src="./assets/test.svg" alt="svg-dynamic-diagram" />

     </div>
     <hr>
     <div class="buttonRow">
        <button class="setbtn" v-on:click="setRectFillBlue">Залить диаграмму синим</button>
        <button class="setbtn" v-on:click="setRectFillRed">Залить диаграмму красным</button>
        <button class="setbtn" v-on:click="setRectFillGreen">Залить диаграмму зеленым</button>
        <button class="setbtn" v-on:click="setRectFillNone">Вернуть</button>
     </div>
     <hr>
     <div class="buttonRow">
        <button class="setbtn" v-on:click="setLIineColorBlue">Синии линии</button>
        <button class="setbtn" v-on:click="setLIineColorRed">Красные линии</button>
        <button class="setbtn" v-on:click="setLIineColorGreen">Зеленые линии</button>
        <button class="setbtn" v-on:click="setLIineColorBlack">Вернуть</button>
        
     </div>
     <hr>

     
</template>

<script>
import { SVG } from '@svgdotjs/svg.js'

import svgimg from '@/assets/test.svg'

export default{

     components: {
          svgimg
     },

     data() {
          return{ 
               redColor: "red",
               greenColor: "green",
               blueColor: "blue",
          }
     
     },
     
     methods: {
          setRectFillBlue() {
               var rectFill_svg = SVG('#svgidimg path')
               rectFill_svg.fill('blue')
          },
          setRectFillRed() {
               var rectFill_svg = SVG('#svgidimg path')
               rectFill_svg.fill('red')
          },
          setRectFillGreen() {
               var rectFill_svg = SVG('#svgidimg path')
               rectFill_svg.fill('green')
          },
          setRectFillNone() {
               var rectFill_svg = SVG('#svgidimg path')
               rectFill_svg.fill('none')
          },
          setLIineColorBlue() {
               var line_svg = SVG('#svgidimg g')
               line_svg.stroke('blue')
          },
          setLIineColorRed() {
               var line_svg = SVG('#svgidimg g')
               line_svg.stroke('red')
          },
          setLIineColorGreen() {
               var line_svg = SVG('#svgidimg g')
               line_svg.stroke('green')
          },
          setLIineColorBlack() {
               var line_svg = SVG('#svgidimg g')
               line_svg.stroke('black')
          },
     },

     mounted() {

     }
}


</script>

<style>
.svgDiagramm {
     display: flex;
     justify-content: center;
}
.buttonRow {
    padding: 3px;
    display: flex;
}

.setbtn {
    font-size: 14px;
    text-decoration: none;
    cursor: pointer;
    display:block;
    width:200px;
    height: 40px;
    font-weight: bold;
    margin:3px auto;
    text-align:center;
    padding: 1px 5px;
    color: #717171;
    -webkit-border-radius: 4px;
    -moz-border-radius: 4px;
    border-radius: 4px;
    text-shadow: 0 1px 0 rgba(255, 255, 255, 0.3);
    -webkit-box-shadow: inset 0 0 0 1px rgba(255, 255, 255, 0.2), inset 0 0 6px 0 rgba(255, 255, 255, 0.3), 0 1px 2px rgba(0, 0, 0, 0.4);
    -moz-box-shadow: inset 0 0 0 1px rgba(255, 255, 255, 0.2), inset 0 0 6px 0 rgba(255, 255, 255, 0.3), 0 1px 2px rgba(0, 0, 0, 0.4);
    box-shadow: inset 0 0 0 1px rgba(255, 255, 255, 0.2), inset 0 0 6px 0 rgba(255, 255, 255, 0.3), 0 1px 2px rgba(0, 0, 0, 0.4);
    background: #f6f6f6;
    background: -webkit-gradient(linear, left top, left bottom, from(#f6f6f6), to(#d4d4d4));
    background: -webkit-linear-gradient(#f6f6f6, #d4d4d4);
    background-image: -moz-linear-gradient(top, #f6f6f6, #d4d4d4);
    background-image: -moz-gradient(top, #f6f6f6, #d4d4d4);
    border: 1px solid #a1a1a1;
}

.setbtn:hover {
    background: #f6f6f6;
    background: -webkit-gradient(linear, left top, left bottom, from(#f6f6f6), to(#ececec));
    background: -webkit-linear-gradient(#f6f6f6, #ececec);
    background-image: -moz-linear-gradient(top, #f6f6f6, #ececec);
    background-image: -moz-gradient(top, #f6f6f6, #ececec);
}
</style>
