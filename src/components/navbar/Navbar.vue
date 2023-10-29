<template>
    <va-navbar color="#34353a">
      <template #left>
        <va-navbar-item class="navbar-item-slot">
          VINICIUS MARTINS
        </va-navbar-item>
      </template>
      <template #right>
        <va-navbar-item class="navbar-item-slot">
         
        </va-navbar-item>
      </template>
      <template #center>
        <va-navbar-item class="navbar-item-slot item-slot">
            About 
        </va-navbar-item>
        <va-navbar-item class="navbar-item-slot item-slot">
          Portifolio 
        </va-navbar-item>
        <va-navbar-item class="navbar-item-slot item-slot">
          Contact 
        </va-navbar-item>
      </template>
    </va-navbar>
  </template>

  <style scoped>
.item-slot {
    width:fit-content;
    user-select: none;
  }
  .item-slot:hover {
    text-decoration:underline;
    cursor:pointer;
  }
    
  </style>