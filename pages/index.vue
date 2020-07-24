<template>
  <div class="center examplex">
    <vs-navbar center-collapsed color="primary" v-model="active">
      <template #left>
        <img src="/logo2.png" alt="" />
      </template>
      <vs-navbar-item :active="active == 'guide'" id="guide">
        Guide
      </vs-navbar-item>
      <vs-navbar-item :active="active == 'docs'" id="docs">
        Documents
      </vs-navbar-item>
      <vs-navbar-item :active="active == 'components'" id="components">
        Components
      </vs-navbar-item>
      <vs-navbar-item :active="active == 'license'" id="license">
        license
      </vs-navbar-item>
      <template #right>
        <vs-button flat>Login</vs-button>
        <vs-button>Get Started</vs-button>
      </template>
    </vs-navbar>
    <div class="square">
      <div class="child">
        <div class="mt-base">
          <div class="container">
            <div class="center grid">
              <vs-row>
                <vs-col sm="12" lg="8" w="8" class="bo">
                  <!-- <div class="vx-card mt-base">
                    <div class="card-body">
                      <div>
                        <div class="post-header flex mb-4 justify-between">
                          <div class="items-center flex">
                            <div>
                              <vs-avatar circle class="align-items-none">
                                <img src="https://via.placeholder.com/700x500" alt="" />
                              </vs-avatar>
                            </div>
                            <div class="ml-4">
                              <div class="center content-inputs">
                                <textarea class="vs-textarea" v-model="value" placeholder="Name" ></textarea>
                              </div>
                            </div>
                          </div>
                        </div>
                      </div>
                    </div>
                  </div> -->
                  <card v-for="post of data" :key="post._id" :item="post" />
                </vs-col>
                <vs-col sm="12" lg="4" w="4" class="bo">
                  <list />
                </vs-col>
              </vs-row>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import axios from "axios";
import Card from "~/components/Card";
import List from "~/components/List";
export default {
  components: {
    Card,
    List
  },
  data() {
    return {
      data: null,
      active: "guide"
    };
  },
  mounted() {
    axios.get("http://127.0.0.1:3100/post").then(response => {
      this.data = response.data.post;
      console.log(response.data.post);
    });
  }
};
</script>

<style>
.vs-textarea {
    resize: none;
    border-radius: 6px;
    border: 0 solid transparent;
    display: block;
    padding: 9px;
    color: rgba(0,0,0,.8);
    font-size: .8rem;
    width: 100%;
    max-width: 100%;
    min-width: 100%;
    background: transparent;
}
.fixed {
  position: fixed;
  z-index: 100;
}
.mt-base {
  margin-top: 2.2rem !important;
}
.container {
  width: 100%;
  /* padding-right: 15px; */
  /* padding-left: 15px; */
  margin-right: auto;
  margin-left: auto;
}
@media (min-width: 576px) {
  .container {
    max-width: 540px;
  }
}

@media (min-width: 768px) {
  .container {
    max-width: 720px;
  }
  .bo {
    padding-left: 10px;
    padding-right: 10px;
  }
}

@media (min-width: 992px) {
  .container {
    max-width: 960px;
  }
}

@media (min-width: 1200px) {
  .container {
    max-width: 960px;
  }
}
</style>
