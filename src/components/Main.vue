<template>
  <div id="main" class="container">
    <div class="row">
      <div class="col-12">
        <div class="col-6">
          <ul class="nav nav-pills">

          </ul>
        </div>
        <div class="col-6">
          <ul class="nav nav-pills">

          </ul>
        </div>
      </div>
      <div class="col-12">
        <div class="row main-area">
          <div class="col-8 main-content">
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
        <div class="col-4 price-content"> 
          <div class="card">
          <div class="card-header"> Pricing </div>
          <div class="card-body">
            <p class="card-text">
              <ul class="price-list">
                <li v-bind:key="item.title" v-for="item in prices" class="price-item">
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
      leftNav: [
        {
          title: "About Me", link:"/",
        },
        {
          title:"Work Examples", link:"/workExamples", 
        },
        {
          title: "Side Projects", link:"/sideProjects"
        }
      ],
      rightNav: [
        {title:"Contact Me", link: ""},
      ],
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
.main-area {
  border-top: 1px solid #ff696e;
}
.main-content {
  padding-right: 0px !important;
}

.price-content {
  padding-left: 0px !important;
  border-left: 1px solid #ff696e;
}
.price-list {
  padding-left: 0px;
  list-style-type: none;
}
</style>
