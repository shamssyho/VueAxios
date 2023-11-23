<script>
import CreatePost from './components/CreatePost.vue';
import PostList from './components/PostList.vue';
import TemplateRef from './components/TemplateRef.vue';
import ClickCounter from './components/ClickCounter.vue';
import HoverCounter from './components/HoverCounter.vue';

export default {
  components: {
    PostList,
    CreatePost,
    TemplateRef,
    ClickCounter,
    HoverCounter,
  }
}
</script>

<template>
  <div>
    <h2>Ref</h2>
    <TemplateRef />
    <hr />
    <h2>Mixins</h2>
    <ClickCounter />
    <HoverCounter />
    <hr />
    <h2>GET and POST Request</h2>
    <PostList />
    <CreatePost />
  </div>
</template>
