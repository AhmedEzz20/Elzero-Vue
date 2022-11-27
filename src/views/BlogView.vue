<template>
    <div class="blog">
      <h1>{{ PageName }}</h1>
      <p>{{ PageDescription }}</p>
      <div class="container">
        <div class="row">
          <div class="col-md-8">
            <div class="posts-area">
              <BlogPosts v-for="post in posts" 
              :key="post.id" 
              :views="post.views" 
              :title="post.title" 
              :date="post.date" 
              :content="post.content" 
              :category="post.category"
              :author="post.author"/>
            </div>
          </div>
          <div class="col-md-4">
            <div class="sidebar">
              <BlogSidebar />
            </div>
          </div>
        </div>
      </div>
    </div>
  </template>
  
  <script>
  import BlogPosts from '@/components/Blog/BlogPosts.vue';
  import BlogSidebar from '@/components/Blog/BlogSidebar.vue';
  import JsonPost from '../json/blog_posts.json';

  export default {
    data: function() {
      return {
        PageName: "Blog Page",
        PageDescription: "This is the blog page",
        posts: JsonPost
      };
    },
    name: "blog",
    components: {
      BlogPosts,
      BlogSidebar
    }
  };
  </script>
  