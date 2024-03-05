<template>
   <div>
      <div class="card" :class="item.class">
         <a
            :href="item.url"
            :target="item.target"
            >
            <div class="card-content">
               <div class="media">
                  <div class="media-left" :class="item.background">
                     <figure class="image is-48x48">
                        <img :src="item.logo" :alt="`${item.name} logo`" />
                     </figure>
                  </div>
                  <div class="media-content">
                     <div>
                        <p class="title is-4">{{ currentTime }}</p>
                        <p class="subtitle is-6" v-if="item.subtitle">{{ item.subtitle }}</p>
                     </div>
                  </div>
               </div>
               <div class="tag" :class="item.tagstyle" v-if="item.tag">
                  <strong class="tag-text">#{{ item.tag }}</strong>
               </div>
            </div>
         </a>
      </div>
   </div>
</template>


<script>
export default {
  name: "Clock",
  props: {
    item: Object,
  },
  data: () => ({
    currentDateTime: null
  }),
  computed: {
    currentTime() {
      if (!this.currentDateTime) return '';
      const date = new Date(this.currentDateTime);
      return date.toLocaleTimeString();
    }
  },
  mounted() {
    setInterval(() => {
      this.currentDateTime = new Date();
    }, 1000);
  },
};
</script>
