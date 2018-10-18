<template lang="pug">
  div.main-root
    div.ed-grid.cols-l-4.main-section.l-section
      aside.span-l-1.main-sidebar.sidebar-first
        TopicMenu
      main.span-l-3.main-main
        slot(name="main")
</template>

<script>
import TopicMenu from '@/components/TopicMenu';

export default {
  name: 'Main',
  components: { TopicMenu }
};
</script>

<style scoped>
</style>
