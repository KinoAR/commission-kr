<template>
  <div id="main">
    <div class="row">
      <div class="col-12">
        Buttons
      </div>
      <div class="col-12">
        <div class="row">
          <div class="col-8">
            <div class="card">
              <div class="card-header">
                Main Content Area
              </div>
              <div class="card-body">
                <p class="card-text">
                  This is my landing page
                </p>
              </div>
            </div>
          </div>
        <div class="col-4"> 
          <div class="card">
          <div class="card-header"> Pricing </div>
          <div class="card-body">
            <p class="card-text">
              <ul class="price-list">
                <li v-for="item in prices" class="price-item">
                  {{item.title}} - {{item.price}}
                </li>
              </ul>
            </p>
          </div>
        </div>     
        </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Main",
  data() {
    return {
      prices: [
        {
          title: "Debugging", price: "15$"
        },
        {
          title: "Plugins", price: "20$"
        },
        {
          title: "Consulting", price: "20$ Hourly"
        },
        {
          title: "Websites", price: "100$"
        },
        {
          title: "Applications", price: "150$"
        }
      ]
    }
  }
};
</script>


<style>
.price-list {
  list-style-type: none;
}
</style>
