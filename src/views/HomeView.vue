<template>
  <div class="home">
    <div class="row mx-0">
      <div class="col-lg-6">
        <div class="img-cont">
          <img alt="Vue logo" src="../assets/img/FB-Logo.svg" />
          <h2 class="text-center text-lg-start">
            Connect with friends all around the world
          </h2>
        </div>
      </div>
      <div class="col-lg-6">
        <card-comp :btns="btnArray" class="mx-auto card-comp">
          <template #default>
            <form action="">
              <div class="mb-3 mt-2">
                <input
                  type="email"
                  class="form-control"
                  placeholder="Email address"
                />
              </div>
              <div class="mb-3 mt-2">
                <input
                  type="password"
                  class="form-control"
                  placeholder="Password"
                />
              </div>
            </form>
          </template>
          <template #footer>
            <hr/>
            <button class="btn btn-success">Sign up</button>
          </template>
        </card-comp>
      </div>
    </div>
  </div>
</template>

<script>
import CardComp from "@/components/CardComp.vue";
export default {
  name: "HomeView",
  components: {
    CardComp,
  },
  data() {
    return {
      btnArray: [
        {
          txt: "Login",
          class: "btn-primary",
        },
        {
          txt: "I forgot my password",
          class: "",
        },
      ],
    };
  },
};
</script>

<style scoped>
.home {
  max-width: 895px;
  margin: auto;
}

h2 {
  max-width: 470px;
  margin: auto;
  font-size: 1.8rem;
}

.card-comp {
  max-width: 398px;
}

.img-cont {
  display: flex;
  flex-direction: column;
}

img {
  max-width: 315px;
  margin: 1em auto 0 auto;
}

.btn-success{
  margin: auto;
  min-width: 120px;
}

@media (min-width: 992px) {
  .home {
    margin: 4em auto;
  }

  img {
    margin: 0;
    margin-top: 4em;
  }

  h2 {
    margin: 0;
    margin-top: 0.1em;
    margin-left: 0.8em;
  }

  .card-comp {
    margin-top: 3rem;
  }
}
</style>
