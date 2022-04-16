<template>
  <section class="py-0 py-lg-3 px-3">
    <div class="container-fluid">
      <div class="row">
        <div :class="`py-0 py-lg-3 px-3 ${list.isLong ? 'col-lg-8' : 'col-lg-4'}`" v-for="(list, index) in lists" :key="index" :id="list.title">
          <router-link :to="list.href">
            <div :class="`wrapper position-relative mb-3 mb-lg-0 ${list.isQuote ? 'image-overlay-full'
            : 'image-overlay'}`">
              <figure class="m-0">
                <img :class="`img-fluid w-100 o-8 ${list.isWide ? 'h-image-500px' : 'h-image-345px'}`" :src="list.image" :alt="list.title" />
              </figure>

              <div class="position-absolute top-0 end-0 p-3" v-show="list.isMostPicked">
                <p class="text-upercase px-5 py-2 bg-fade-black-1 text-white rounded-pill">
                  lorem
                </p>
              </div>

              <div class="position-absolute top-0 start-0 p-3 z-999" v-show="list.isVideo">
                <i class="far fa-3x fa-play-circle text-white"></i>
              </div>

              <div
                :class="`position-absolute ${list.isQuote ? 'top-50 start-50 translate-middle p-4 text-white z-999 fw-medium d-flex flex-column justify-content-between w-100 h-100' : 'bottom-0 start-0 p-4 text-white z-999 fw-medium'}`">
                <div v-if="list.isQuote">
                  <div class="invisible"></div>
                  <div class="text-center">
                    <p class="mp-0 text-uppercase">
                      <small>lorem</small>
                    </p>
                    <h2 class="fs-4 mb-3">
                      Man cannot discover new oceans unless he has the courage to
                      lose sight of the sore
                    </h2>
                  </div>
                </div>
                <div v-else>
                  <p class="mp-0 text-uppercase">
                    <small>{{ list.subtitle }}</small>
                  </p>
                  <h2 class="fs-4 mb-3">{{  list.title  }}</h2>
                </div>

                <div class="image d-flex">
                  <figure :class="`m-0 wh-image-50px ${index===0 ? '' : '-ms-20px' }`" v-for="(people, index) in list.peoples" :key="index" :id="people.name">
                    <img class="img-fluid wh-image-50px rounded-circle border-white-3px" :src="people.image"
                      :alt="people.name" />
                  </figure>
                </div>
              </div>
            </div>
          </router-link>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "ContentComponent",
  data() {
    return {
      lists: [
        {
          image: require("@/assets/source/image/img-1.jpg"),
          title: "A Guide To Rocky Mountain Vacations",
          subtitle: "LOREM",
          isMostPicked: true,
          isVideo: false,
          isQuote: false,
          isLong: true,
          isWide: false,
          href: "#",
          peoples: [
            {
              image: require("@/assets/source/image/people-1.jpg"),
              name: "lorem",
            },
            {
              image: require("@/assets/source/image/people-2.jpg"),
              name: "ipsum",
            },
            {
              image: require("@/assets/source/image/people-3.jpg"),
              name: "dolor",
            },
          ],
        },
        {
          image: require("@/assets/source/image/img-2.jpg"),
          title: "Travelling To USA",
          subtitle: "LOREM",
          isMostPicked: false,
          isVideo: true,
          isQuote: false,
          isLong: false,
          isWide: false,
          href: "#",
          peoples: [
            {
              image: require("@/assets/source/image/people-1.jpg"),
              name: "lorem",
            },
            {
              image: require("@/assets/source/image/people-3.jpg"),
              name: "dolor",
            },
          ],
        },
        {
          image: require("@/assets/source/image/img-3.jpg"),
          title: "Party Jokes STarting But Unnecessary",
          subtitle: "LOREM",
          isMostPicked: false,
          isVideo: false,
          isQuote: false,
          isLong: false,
          isWide: true,
          href: "#",
          peoples: [
            {
              image: require("@/assets/source/image/people-1.jpg"),
              name: "lorem",
            },
            {
              image: require("@/assets/source/image/people-2.jpg"),
              name: "ipsum",
            },
            {
              image: require("@/assets/source/image/people-3.jpg"),
              name: "dolor",
            },
          ],
        },
        {
          image: require("@/assets/source/image/img-4.jpg"),
          title: "Maui By Air The Best Way Around The Island",
          subtitle: "LOREM",
          isMostPicked: false,
          isVideo: false,
          isQuote: false,
          isLong: false,
          isWide: true,
          href: "#",
          peoples: [
            {
              image: require("@/assets/source/image/people-1.jpg"),
              name: "lorem",
            },
            {
              image: require("@/assets/source/image/people-2.jpg"),
              name: "ipsum",
            },
            {
              image: require("@/assets/source/image/people-3.jpg"),
              name: "dolor",
            },
          ],
        },
        {
          image: require("@/assets/source/image/img-5.jpg"),
          title:
            "Man cannot discover new oceans unless he has the courage to lose sight of the sore",
          subtitle: "LOREM",
          isMostPicked: false,
          isVideo: false,
          isQuote: true,
          isLong: false,
          isWide: true,
          href: "#",
          peoples: [
            {
              image: require("@/assets/source/image/people-1.jpg"),
              name: "lorem",
            },
            {
              image: require("@/assets/source/image/people-2.jpg"),
              name: "ipsum",
            },
          ],
        },
        {
          image: require("@/assets/source/image/img-6.jpg"),
          title: "Travelling To Barcelona",
          subtitle: "LOREM",
          isMostPicked: false,
          isVideo: true,
          isQuote: false,
          isLong: false,
          isWide: false,
          href: "#",
          peoples: [
            {
              image: require("@/assets/source/image/people-1.jpg"),
              name: "lorem",
            },
            {
              image: require("@/assets/source/image/people-3.jpg"),
              name: "dolor",
            },
          ],
        },
        {
          image: require("@/assets/source/image/img-7.jpg"),
          title: "A Guide To Rocky Mountain Vacations",
          subtitle: "LOREM",
          isMostPicked: true,
          isVideo: false,
          isQuote: false,
          isLong: true,
          isWide: false,
          href: "#",
          peoples: [
            {
              image: require("@/assets/source/image/people-1.jpg"),
              name: "lorem",
            },
            {
              image: require("@/assets/source/image/people-2.jpg"),
              name: "ipsum",
            },
            {
              image: require("@/assets/source/image/people-3.jpg"),
              name: "dolor",
            },
          ],
        },
        {
          image: require("@/assets/source/image/img-8.jpg"),
          title: "Party Jokes STarting But Unnecessary",
          subtitle: "LOREM",
          isMostPicked: false,
          isVideo: false,
          isQuote: false,
          isLong: false,
          isWide: true,
          href: "#",
          peoples: [
            {
              image: require("@/assets/source/image/people-1.jpg"),
              name: "lorem",
            },
            {
              image: require("@/assets/source/image/people-2.jpg"),
              name: "ipsum",
            },
            {
              image: require("@/assets/source/image/people-3.jpg"),
              name: "dolor",
            },
          ],
        },
        {
          image: require("@/assets/source/image/img-9.jpg"),
          title: "Maui By Air The Best Way Around The Island",
          subtitle: "LOREM",
          isMostPicked: false,
          isVideo: false,
          isQuote: false,
          isLong: false,
          isWide: true,
          href: "#",
          peoples: [
            {
              image: require("@/assets/source/image/people-1.jpg"),
              name: "lorem",
            },
            {
              image: require("@/assets/source/image/people-2.jpg"),
              name: "ipsum",
            },
            {
              image: require("@/assets/source/image/people-3.jpg"),
              name: "dolor",
            },
          ],
        },
        {
          image: require("@/assets/source/image/img-5.jpg"),
          title:
            "Man cannot discover new oceans unless he has the courage to lose sight of the sore",
          subtitle: "LOREM",
          isMostPicked: false,
          isVideo: false,
          isQuote: true,
          isLong: false,
          isWide: true,
          href: "#",
          peoples: [
            {
              image: require("@/assets/source/image/people-1.jpg"),
              name: "lorem",
            },
            {
              image: require("@/assets/source/image/people-2.jpg"),
              name: "ipsum",
            },
          ],
        },
      ]
    }
  }
}
</script>