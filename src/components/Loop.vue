<template>
    <div>
      <h1>Total Price: ${{ totalPrice }}</h1>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        items: [
          { name: 'Laptop', price: 1000 },
          { name: 'Phone', price: 500 },
          { name: 'Tablet', price: 300 }
        ]
      };
    },
    computed: {
      // A computed property to calculate the total price of all items
      totalPrice() {
        return this.items.reduce((sum, item) => sum + item.price, 0);
      }
    }
  };
  </script>
  
  create a web application that demonstrate how to loop aover arrays, conditionally display HTML and prepare computed properties