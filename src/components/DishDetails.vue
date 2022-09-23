<template>
<table>
  <tr style="border:">
    <th style="border:">
  <ul class="one">
  <li>
    <button @click="toggleDetails">
      {{ showDetails ? " " : " " }}
      {{ id }}<br>
      {{ name }}
      <div>
          <img v-bind:src="productImage">
        </div>
    </button>
    </li>
    </ul>
    </th>

    
    <th style="border:">
    <ul class="two" v-if="showDetails">
      <li>
        <h3>{{ name }}</h3>
      </li>
      <li>
        <div>
          <img v-bind:src="productImage">
        </div>
      </li>
      <li>
        {{ head }}
      </li>
      <br>
      <li>{{ description }}}</li>

      <p></p>
    </ul>
    </th>

  </tr>

</table>
  
</template>

<script>
export default {
  props: {
    id: {
      type: String,
      required: true,
    },
    name: {
      type: String,
      required: true,
    },
    description: {
      type: String,
      required: true,
    },
    head: {
      type: String,
      required: true,
    },
    productImage:{
    

    },
  },
  data() {
    return {
      showDetails: false,
    };
  },
  methods: {
    toggleDetails() {
      this.showDetails = !this.showDetails;
    },
  },
};
</script>

<style>
li {
  list-style-type: none;
  padding-left: 0px;
  text-align: center; 
}


</style>