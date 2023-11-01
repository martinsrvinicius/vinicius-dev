<template>
  <va-navbar color="#34353a">
    <template #left>
      <va-navbar-item class="navbar-item-slot">
        <img src="../../assets/developer.svg" alt="Vinicius">
      </va-navbar-item>
    </template>
    <template #right>
      <va-navbar-item class="navbar-item-slot">

      </va-navbar-item>
    </template>
    <template #center>
      <va-navbar-item class="navbar-item-slot item-slot">
        <a href="#about">About </a>
      </va-navbar-item>
      <va-navbar-item class="navbar-item-slot item-slot">
        <a href="#portifolio">Portifolio </a>
      </va-navbar-item>
      <va-navbar-item class="navbar-item-slot item-slot">
        <a href="#contact">Contact </a>
      </va-navbar-item>
    </template>
  </va-navbar>
</template>

<style scoped>
.item-slot {
  width: fit-content;
  user-select: none;
}

.item-slot:hover {
  text-decoration: underline;
  cursor: pointer;
}

img {
  width: 40px;
  margin-left: 50px
}

img:hover {
  cursor: pointer;
}

a {
  color: white
}
</style>