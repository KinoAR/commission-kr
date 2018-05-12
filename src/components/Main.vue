<template>
  <div id="main" class="container">
    <div class="row">
      <div class="col-12 full-navigation">
        <div class="row">
          <div class="col-6">
          <ul class="nav nav-pills">
            <li v-bind:key="link.title" v-for="link in leftNav" class="nav-item">
              <a v-bind:href="link.link" class="nav-link"> {{link.title}}</a>
            </li>
          </ul>
        </div>
        <div class="col-6 justify-content-right">
          <ul class="nav nav-pills justify-content-end">
            <li v-bind:key="link.title" v-for="link in rightNav" class="nav-item">
              <a v-bind:href="link.link" class="nav-link"> {{link.title}} </a>
            </li>
          </ul>
        </div>
        </div>
      </div>
      <div class="col-12">
        <div class="row main-area">
          <div class="col-8 main-content">
            <div class="card">
              <div class="card-header main-card-header">
                Main Content Area
              </div>
              <div class="card-body  main-card-body">
                <p class="card-text">
                  This is my landing page
                </p>
              </div>
            </div>
          </div>
        <div class="col-4 price-content"> 
          <div class="card">
          <div class="card-header main-card-header"> Pricing </div>
          <div class="card-body main-card-body">
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
.full-navigation {
  border: 1px solid #ff696e;
}
.main-area {
  border-right: 1px solid #ff696e;
  border-left: 1px solid #ff696e;
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
