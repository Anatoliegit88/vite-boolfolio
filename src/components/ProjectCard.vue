<script>
import { store } from "../store";

export default {
  name: "ProjectCard",
  data() {
    return {
      contentMaxLength: 150,
      store,
    };
  },
  props: {
    project: Object,
  },
  created: {
    contentPreview() {
      if (
        this.project.content &&
        this.project.content.length > this.contentMaxLength
      ) {
        return this.project.content.substr(0, this.contentMaxLength) + "...";
      }
      return this.project.content;
    },
  },
};
</script>
<template>
  <div class="card mb-3">
    <div class="card-body">
      <div class="row justify-content-between">
        <div class="col-4">
          <img
            v-if="project.cover_image"
            class="w-100"
            :src="`${this.store.apiBaseUrl}/storage/${project.cover_image}`"
            alt="" />
          <div v-else>Not Image Found</div>
          <div class="col-7">
            <div class="card-title">
              <h2>{{ project.title }}</h2>
              <p class="card-text">{{ project.content }}</p>
              <a class="btn btn-primary" href="">Discover</a>
              <p class="caed-text">
                {{ contentPreview }}
              </p>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
