
<html>
 <head>
 <title></title>
 
 <style>

div{
    font-size: 70px;
    background: grey;
    box-shadow: 0 4px 6px 0 #254117;
}

h1{
    font-size: 50px;
    color: black;
    background: darkgray;
    text-align: center;
    box-shadow: 0 10px 16px 0 yellow;
}

 html,
 body {
 width: 100vw;
 height: 50vh;
 margin: 0;
 border: 0;
 padding: 0;
 -webkit-box-sizing: border-box;
 -moz-box-sizing: border-box;
 box-sizing: border-box;
 background: #810541;
 
 }
 
 *,
 *::before,
 *::after {
 -webkit-box-sizing: inherit;
 -moz-box-sizing: inherit;
 box-sizing: inherit;
 }
 
 #app {
 width: 100%;
 height: 100%;
 background: #008080;
 
 display: flex;
 justify-content: center;
 align-items: center;
 }
 
 .flip-clock-container {
 display: flex;
 justify-content: center;
 align-items: center;
 
 font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Oxygen,
 Ubuntu, Cantarell, "Open Sans", "Helvetica Neue", sans-serif;
 font-size: 50px;
 line-height: 0;
 }
 
 .flip-clock-container * {
 -webkit-user-select: none;
 -moz-user-select: none;
 user-select: none;
 
 cursor: default;
 }
 
 .flip-clock {
 display: flex;
 
 -webkit-perspective: 1000px;
 -moz-perspective: 1000px;
 perspective: 1000px;
 }
 
 .digit {
 position: relative;
 
 width: 45px;
 height: 80px;
 
 box-shadow: 0 0 2px 1px rgba(0, 0, 0, 0.1);
 }
 
 .digit-left {
 margin-right: 1px;
 }
 
 .digit-right {
 margin-left: 1px;
 }
 
 .digit::before,
 .digit::after {
 position: absolute;
 z-index: 0;
 
 display: flex;
 justify-content: center;
 
 width: 100%;
 height: 50%;
 overflow: hidden;
 }
 
 .digit::before {
 content: attr(data-digit-before);
 
 bottom: 0;
 align-items: flex-start;
 }
 
 .digit::after {
 content: attr(data-digit-after);
 
 top: 0;
 align-items: flex-end;
 }
 
 .card {
 position: relative;
 z-index: 1;
 
 width: 100%;
 height: 50%;
 
 -webkit-transform-style: preserve-3d;
 -moz-transform-style: preserve-3d;
 transform-style: preserve-3d;
 
 -webkit-transform-origin: bottom;
 -moz-transform-origin: bottom;
 transform-origin: bottom;
 
 -webkit-transform: rotateX(0);
 -moz-transform: rotateX(0);
 transform: rotateX(0);
 
 -webkit-transition: transform 0.7s ease-in-out;
 -moz-transition: transform 0.7s ease-in-out;
 transition: transform 0.7s ease-in-out;
 }
 
 .card.flipped {
 transform: rotateX(-180deg);
 }
 
 .card-face {
 position: absolute;
 
 display: flex;
 justify-content: center;
 
 width: 100%;
 height: 100%;
 overflow: hidden;
 
 -webkit-backface-visibility: hidden;
 -moz-backface-visibility: hidden;
 backface-visibility: hidden;
 }
 
 .card-face-front {
 align-items: flex-end;
 }
 
 .card-face-back {
 align-items: flex-start;
 
 -webkit-transform: rotateX(-180deg);
 -moz-transform: rotateX(-180deg);
 transform: rotateX(-180deg);
 }
 
 .digit::before,
 .digit::after,
 .card-face-front,
 .card-face-back {
 background: white;
 color: black;
 }
 
 .digit,
 .digit::before,
 .digit::after,
 .card,
 .card-face {
 border-radius: 4px;
 }
 
 .digit::before,
 .card-face-back {
 background: linear-gradient(0, #aaa, #ccc 50%, #fafafa);
 color: #212121;
 
 border-top: 1px solid black;
 border-top-left-radius: 0;
 border-top-right-radius: 0;
 }
 
 .digit::after,
 .card-face-front {
 background: linear-gradient(0, #aaa, #bbb 50%, #f5f5f5);
 color: #212121;
 
 border-bottom: 1px solid black;
 border-bottom-left-radius: 0;
 border-bottom-right-radius: 0;
 }
 
 .digit-left,
 .digit-left::before,
 .digit-left::after,
 .digit-left .card,
 .digit-left .card-face {
 border-top-right-radius: 0;
 border-bottom-right-radius: 0;
 }
 
 .digit-right,
 .digit-right::before,
 .digit-right::after,
 .digit-right .card,
 .digit-right .card-face {
 border-top-left-radius: 0;
 border-bottom-left-radius: 0;
 }
 
 .colon {
 color: black;
 margin: 0 6px;
 padding-bottom: 9px;
 }
 
 </style>
 
 </head>
 
 <body>
 
 <h1>DIGITAL FLIPDOWN CLOCK</h1>
 
 <div id="app">
 <div class="flip-clock-container">
 <div class="flip-clock flip-clock-h">
 <div class="digit digit-left">
 <!-- ::before -->
 <div class="card">
 <div class="card-face card-face-front"></div>
 <div class="card-face card-face-back"></div>
 </div>
 <!-- ::after -->
 </div>
 <div class="digit digit-right">
 <!-- ::before -->
 <div class="card">
 <div class="card-face card-face-front"></div>
 <div class="card-face card-face-back"></div>
 </div>
 <!-- ::after -->
 </div>
 </div>
 
 <div class="colon">:</div>
 
 <div class="flip-clock flip-clock-m">
 <div class="digit digit-left">
 <!-- ::before -->
 <div class="card">
 <div class="card-face card-face-front"></div>
 <div class="card-face card-face-back"></div>
 </div>
 <!-- ::after -->
 </div>
 <div class="digit digit-right">
 <!-- ::before -->
 <div class="card">
 <div class="card-face card-face-front"></div>
 <div class="card-face card-face-back"></div>
 </div>
 <!-- ::after -->
 </div>
 </div>
 
 <div class="colon">:</div>
 
 <div class="flip-clock flip-clock-s">
 <div class="digit digit-left">
 <!-- ::before -->
 <div class="card">
 <div class="card-face card-face-front"></div>
 <div class="card-face card-face-back"></div>
 </div>
 <!-- ::after -->
 </div>
 <div class="digit digit-right">
 <!-- ::before -->
 <div class="card">
 <div class="card-face card-face-front"></div>
 <div class="card-face card-face-back"></div>
 </div>
 <!-- ::after -->
 </div>
 </div>
 </div>
 </div>
 
 <script>
 (function () {
 "use strict";
 
 const els = {
 s: initElements("s"),
 m: initElements("m"),
 h: initElements("h")
 };
 
 function initElements(type) {
 const els = [{}, {}];
 
 if (!["s", "m", "h"].includes(type)) return els;
 
 const target = document.querySelector(`.flip-clock-${type}`);
 
 if (!target) return els;
 
 let el;
 
 el = els[0];
 el.digit = target.querySelector(".digit-left");
 el.card = el.digit.querySelector(".card");
 el.cardFaces = el.card.querySelectorAll(".card-face");
 el.cardFaceA = el.cardFaces[0];
 el.cardFaceB = el.cardFaces[1];
 
 el = els[1];
 el.digit = target.querySelector(".digit-right");
 el.card = el.digit.querySelector(".card");
 el.cardFaces = el.card.querySelectorAll(".card-face");
 el.cardFaceA = el.cardFaces[0];
 el.cardFaceB = el.cardFaces[1];
 
 return els;
 }
 
 (function runClock() {
 const date = new Date();
 const now = {
 h: date.getHours(),
 m: date.getMinutes(),
 s: date.getSeconds()
 };
 const updateNow = (h, m, s) => {
 if (h) {
 now.h = h;
 now.h0 = now.h[0];
 now.h1 = now.h[1];
 }
 if (m) {
 now.m = m;
 now.m0 = now.m[0];
 now.m1 = now.m[1];
 }
 if (s) {
 now.s = s;
 now.s0 = now.s[0];
 now.s1 = now.s[1];
 }
 }
 updateNow(
 now.h < 10 ? `0${now.h}` : `${now.h}`,
 now.m < 10 ? `0${now.m}` : `${now.m}`,
 now.s < 10 ? `0${now.s}` : `${now.s}`,
 );
 console.log(`${now.h0}${now.h1}:${now.m0}${now.m1}:${now.s0}${now.s1}`);
 
 for (const t of Object.keys(els)) {
 for (const i of ["0", "1"]) {
 const curr = now[`${t}${i}`];
 let next = +curr + 1;
 if (t === "h") {
 if (i === "0") next = next <= 2 ? `${next}` : "0";
 if (i === "1") next = next <= 3 ? `${next}` : "0";
 }
 if (t === "m") {
 if (i === "0") next = next <= 5 ? `${next}` : "0";
 if (i === "1") next = next <= 9 ? `${next}` : "0";
 }
 if (t === "s") {
 if (i === "0") next = next <= 5 ? `${next}` : "0";
 if (i === "1") next = next <= 9 ? `${next}` : "0";
 }
 const el = els[t][i];
 if (el && el.digit) {
 if (!el.digit.dataset.digitBefore) {
 el.digit.dataset.digitBefore = curr;
 el.cardFaceA.textContent = el.digit.dataset.digitBefore;
 el.digit.dataset.digitAfter = next;
 el.cardFaceB.textContent = el.digit.dataset.digitAfter;
 } else if (el.digit.dataset.digitBefore !== curr) {
 el.card.addEventListener(
 "transitionend",
 function () {
 el.digit.dataset.digitBefore = curr;
 el.cardFaceA.textContent = el.digit.dataset.digitBefore;
 
 const cardClone = el.card.cloneNode(true);
 cardClone.classList.remove("flipped");
 el.digit.replaceChild(cardClone, el.card);
 el.card = cardClone;
 el.cardFaces = el.card.querySelectorAll(".card-face");
 el.cardFaceA = el.cardFaces[0];
 el.cardFaceB = el.cardFaces[1];
 
 el.digit.dataset.digitAfter = next;
 el.cardFaceB.textContent = el.digit.dataset.digitAfter;
 },
 { once: true }
 );
 if (!el.card.classList.contains("flipped")) {
 el.card.classList.add("flipped");
 }
 }
 }
 }
 }
 
 setTimeout(runClock, 1000);
 })();
 })();
 
 
 </script>
 
 </body>
 
 </html>


