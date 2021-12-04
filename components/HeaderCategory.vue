<template>
  <div>
    <center>
      <div class="categoryArea">
        <NuxtLink
          :to="goToNuxtPage('')"
          class="categoryNuxtLink"
          :class="{ categoryActive: activePageName.length <= 3 }"
        >
          <span class="categoryItem">{{ $t("categories.home") }}</span>
        </NuxtLink>
        <NuxtLink
          :to="goToNuxtPage('bestsellers')"
          class="categoryNuxtLink"
          :class="{ categoryActive: activePageName.includes('bestsellers') }"
        >
          <span class="categoryItem">{{ $t("categories.bestsellers") }}</span>
        </NuxtLink>
        <NuxtLink
          :to="goToNuxtPage('category')"
          class="categoryNuxtLink"
          :class="{ categoryActive: activePageName.includes('category') }"
        >
          <span class="categoryItem">{{ $t("categories.category") }}</span>
        </NuxtLink>
        <NuxtLink
          :to="goToNuxtPage('store')"
          class="categoryNuxtLink"
          :class="{ categoryActive: activePageName.includes('store') }"
        >
          <span class="categoryItem">{{ $t("categories.store") }}</span>
        </NuxtLink>
        <NuxtLink
          :to="goToNuxtPage('blog')"
          class="categoryNuxtLink"
          :class="{ categoryActive: activePageName.includes('blog') }"
        >
          <span class="categoryItem">{{ $t("categories.blog") }}</span>
        </NuxtLink>
      </div>
    </center>
  </div>
</template>

<script>
export default {
  computed: {
    activeRouteName() {
      return this.$route.params.category;
    },
    activePageName() {
      return this.$route.path;
    },
  },
  methods: {
    goToNuxtPage(data) {
      if(data == '') return "/" + this.$i18n.locale;
      return "/" + this.$i18n.locale + "/" + data;
    },
  },
};
</script>

<style scoped>
.categoryArea {
}
.categoryNuxtLink {
  display: inline-block;
  text-decoration: none;
  color: #bac0c5;
  font-size: 17px;
  margin-right: 20px;
  transition: 0.3s;
}
.categoryActive {
  color: var(--color);
}
.categoryNuxtLink:hover {
}
.categoryItem {
}

@media only screen and (max-width: 800px) {
  .categoryNuxtLink {
    font-size: 12px;
    margin-right: 14px;
  }
}
</style>
