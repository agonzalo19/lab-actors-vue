<template>
<caption>Iron Contacts</caption>
<td>
<th>Pictures</th>
<th>Name</th>
<th>popularity</th>
</td>
  <table v-for="contact in myContacts.slice(0, 5)" :key="contact"> 
    <td> <img :src="contact.pictureUrl" alt=""></td>
    <td>{{ contact.name }}</td>
    <td>{{ contact.popularity }}</td>
   </table>
</template>

<script setup>

import contacts from "./contacts.json";
const myContacts = contacts 
// (() => {
//   return contacts.lenght < 3
//     })
//console.log(myContacts.length);


</script>

<style>
th{
  padding: 20px;
}

img{
  height: 100px;
  width: 100%;
}

td{
  padding: 20px;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
