<script lang="ts" conext="module">
    import type { Load } from '@sveltejs/kit';
    import type { Post } from '$lib/types';
    import { goto } from '$app/navigation';

    export const load: Load = async ({ fetch }) => {
      const res = await fetch('/posts');
      const data = await res.json();

      return { props: {posts: data } };
    };
    
    export let poasts: any
</script>


<div class="my-4">
  <h1 class="text-center text-3xl font-bold">
    My wonderful blog
  </h1>
</div>