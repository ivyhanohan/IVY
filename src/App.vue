
<template>
  <div>
    <h2>Active List</h2>
    <ul>
      <li v-for="item in items" :key="item.id">
        {{ item.name }}
        <span v-if="item.isActive">(Active)</span>
        <span class="nigga" v-else>(Offline)</span>
      </li>
    </ul>
    <p>Total Active Person: {{ activeItemCount }}</p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      items: [
        { id: 1, name: "Harvey Quibol", isActive: true },
        { id: 2, name: "Ivy Quino", isActive: true },
        { id: 3, name: "Jeric Polison", isActive: false },
        { id: 4, name: "Jerico Pasana", isActive: true },
      ],
    };
  },
  computed: {
    filteredItems() {
      return this.items.filter(item => item.isActive);
    },
    activeItemCount() {
      return this.filteredItems.length;
    },
  },
};
</script>

<style scoped>
h2 {
  color: #42b983;
  margin-left: 90px;
  margin-top: 50px;
}
ul {
  list-style-type: none;
  padding: 0;
  margin-left: 70px;
  
}
li {
  margin: 5px 0;
  
}
span {
  color: rgb(112, 206, 112);
  font-weight: bold;
}
div {
  border: 1px solid black;
  height: 300px;
  width: 300px;
  border-radius: 20px;
  justify-content: center;
}
p{
  margin-left: 70px;
  margin-top: 10px;
}
.nigga{
  color: white;
}

</style>