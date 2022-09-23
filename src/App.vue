<template>
  <h2>Little Indian Restro</h2>
  <ul>
    <dish-details
      v-for="dish in dishes"
      :key="dish.id"
      :name="dish.name"
      :description="dish.description"
      :head="dish.head"
      :productImage="dish.productImage"
      :id="dish.id"
    />
  </ul>
</template>

<script>
import DishDetails from "./components/DishDetails.vue";
export default {
  name: "App",
  components: { DishDetails },
  data() {
    return {
      dishes: [
        {
          id: "1",
          name: "Gulab Jamun",
          description: 
           "Gulab Jamun Recipe | How to make Soft Gulab Mamun with Milk Powder in a detailed photo and video recipe.perhaps one of the most popular Indian sweet recipes across India. it is one such dessert which is not only liked by all age groups but can also be attempted by all age groups. traditionally the Gulab jamoon is made with store-bought pre-mix, but the same can be made by combining the milk powder, plain flour and baking powder.",
           head: "Steps in making Gulab Jamun",
           productImage: require("@/assets/food/j.jpeg"),
        },
        {
          id: "2",
          name: "Paneer Tikka",
          description:
          "The process is pretty simple, you marinate the paneer with spices and yogurt, let it sit for a bit so that the flavors mix well together and then arrange the paneer cubes along with onion and peppers in a skewer and grill.However, the taste of paneer tikka lies in its marination of course.So to make a good paneer tikka you first need to make a very good marinade.My marinade includes lots of spices and Greek yogurt. Now if you can’t find Greek yogurt that’s okay. You may use regular yogurt too, just make sure to strain it for 3-4 hours before using.You really need thick yogurt to marinate the panner cubes.",
          head: "Steps in maKing Paneer Tikka",
          productImage: require("@/assets/food/p.jpeg"),
        },
        {
          id: "3",
          name: "Butter Dosa",
          description:
            "Dosa is a traditional food item in South India. Typically, it is prepared from a batter comprised of rice and urad dhal which is kept overnight for fermentation. However, this version of dosa called butter dosa, originated in Devanagari, Karnataka which has made the batter unique by adding puffed rice to it to make the dosa extra soft. This dosa is just one of the many varieties prevalent in the South Indian cuisine; it has a thick base yet is thin and crispy with a soft texture.   This dosa’s popularity is due in large part to the fact that it is served with a generous topping of fresh butter or benne along with a spiced potato dish.",
          head: "Steps in maKing Dosa",
          productImage: require("@/assets/food/d.jpeg"),
        },
      ],
    };
  },
};
</script>

<style>
#app h2{
  font-family: Arial;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: white;
  margin-top: 60px;
  background-color:green; 
  font-size: 50px;
} 
</style>