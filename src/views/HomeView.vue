<template>
  <div class="home">
    <!-- main-img -->
    <section class="main-img" />
    <!-- !main-img -->
    <section class="p-3">
      <b-row class="mx-0" align-v="stretch">
        <b-col class="px-0" cols="2">
          <h1 class="fw-900 text-38">
            Big Roof, <br />
            Big Circle.
          </h1>
        </b-col>
        <b-col class="px-0" cols="2">
          <h2 class="text-38 fw-900 mb-4">
            Live In <br />
            Safe and <br />
            Sound,
          </h2>
          <h2 class="text-38 fw-900">
            Grow <br />
            Your True Color.
          </h2>
        </b-col>
        <b-col class="px-0" cols="2" offset="2">
          <p class="text-16 fw-700">
            자기다움이 섞이고 <br />
            연결되는 풍요로운 집.
          </p>
        </b-col>
        <b-col class="px-0 d-flex align-items-start justify-content-between flex-column" cols="2" offset="1">
          <p class="text-16 fw-700 flex-grow-1">
            맹그로브는 <br />
            개인의 더 나은 일상과 <br />
            공동체를 위한 <br />
            <br />
            지속가능한 실천을 <br />
            만들어 갑니다.
          </p>
          <b-btn variant="text text-secondary p-0 fw-900 mt-auto d-flex align-items-center">
            <span class="text-18">Read more</span>
            <img class="ml-1" :src="require('../assets/img/icon-arrow-02.svg')" alt="" />
          </b-btn>
        </b-col>
      </b-row>
    </section>
    <section class="bg-light w-100 px-3 py-5">
      <b-row tag="header" aling-v="start" class="mb-4">
        <b-col cols="2"> <h1 class="fw-900 text-20">Location</h1> </b-col>
        <b-col cols="10">
          <h2 class="text-18 fw-700" :style="{ lineHeight: '27px' }">
            맹그로브는 지역마다 고유의 특성을 갖추고 있습니다. <br />
            각각의 맹그로브 코리빙 하우스의 매력을 살펴보세요.
          </h2>
        </b-col>
      </b-row>
      <div class="">
        <div class="horizon-scroll">
          <div class="d-flex align-items-start">
            <div class="empty"></div>
            <div v-for="(item, i) in locations" :key="i" class="">
              <figure class="d-flex flex-column location-item">
                <img :src="item.src" alt="" />
                <figcaption class="d-flex align-items-center justify-content-between">
                  <span>{{ item.title }}</span>
                  <div class="ml-auto d-flex align-items-center">
                    <div class="bg-secondary ml-2" v-for="(item2, l) in item.type" :key="l">
                      {{ item2 }}
                    </div>
                  </div>
                </figcaption>
              </figure>
            </div>
          </div>
        </div>
      </div>
    </section>
  </div>
</template>

<script>
// @ is an alias to /src

export default {
  name: "HomeView",
  components: {},
  data() {
    return {
      locations: [
        {
          src: require("../assets/img/Soongin_Image_minify-1@2x.png"),
          title: "맹그로브 숭인점",
          type: ["Co-Living"],
        },
        {
          src: require("../assets/img/Soongin_Image_minify-2@2x.png"),
          title: "맹그로브 신설점",
          type: ["Co-Living", "Stay"],
        },
        {
          src: null,
          title: "Coming Soon",
          type: [],
        },
      ],
    };
  },
};
</script>

<style scoped lang="scss">
.home {
  height: 4000px;
}
.main-img {
  width: 100%;
  padding-bottom: 38%;
  background-image: url("../assets/img/main-img.png");
  background-size: cover;
  background-repeat: no-repeat;
}

.horizon-scroll {
  max-width: 100%;
  overflow-x: auto;
  .location-item {
    width: 688px;
  }
  .empty {
    width: 688px;
  }
}
</style>
