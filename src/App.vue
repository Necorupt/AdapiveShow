<template>
  <div class="content__data">
    <div class="data__item">1</div>
    <div class="data__item">2</div>
    <div class="data__item">3</div>
    <div class="data__item">4</div>
    <div class="data__item">5</div>
    <div class="data__item">6</div>
    <div class="data__item">7</div>
    <div class="data__item">8</div>
    <div class="data__item">9</div>
    <div class="data__item">10</div>
  </div>
</template>

<style>
body {
  display: block;
  margin: 0;
  padding: 0;
}

#app {
  display: block;
  padding: 0;
  margin: 0;
  width: 100%;
}


/*

  Можно заранее определить часть свойств, если они будут переопределены ниже то они будут переопределены
*/
.data__item {
  padding-top: 40px;
  padding-bottom: 40px;
}

.content__data {
  width: 100vw;
}

/*
  Допустим размер экрана ПК начинается с 1280px

  для этого юзаем min-width: <От чего начинаем>px
  Тогда сделаем, так чтобы было по 4 элемна в строке
  и эти эдементы были зеленые

*/
@media screen and (min-width:1280px) {


  /*
    Тут мы пихаем весь код для данного выражения
  */

  .content__data {
    display: grid;
    grid-template-columns: repeat(4, 1fr);
    text-align: center;
    row-gap: 4px;
    column-gap: 4px;
  }

  .data__item {
    background-color: greenyellow;
    border-radius: 4px;
  }
}

/*
  Допустим размер экрана планшета начинается с 500px и заканчивается в 1280px

  для этого юзаем max-width: <До какого предела>px
  Тогда сделаем, так чтобы было по 2 элемна в строке
  и эти эдементы были ораньживые

*/
@media screen and (min-width:500px) and (max-width:1280px) {

  .content__data {
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    text-align: center;
    row-gap: 4px;
    column-gap: 4px;
  }

  .data__item {
    background-color: orangered;
    border-radius: 4px;
  }
}

/*
  Допустим размер экрана телефона  и заканчивается в 500px

  для этого юзаем max-width: <До какого предела>px
  Тогда сделаем, так чтобы было по 1 элемна в строке
  и эти эдементы были красные и тут бь я юзал display flex
*/
@media screen and (max-width:500px) {

  .content__data {
    display: flex;
    flex-direction: column;
    text-align: center;
    gap: 4px;
    width: 100%;
  }

  .data__item {
    background-color: orangered;
    border-radius: 4px;
  }
}
</style>
