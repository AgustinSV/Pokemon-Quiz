<script>
    import { page } from '$app/stores';

    const post_id = $page.params.post_id;
    let post = {};

    async function fetchPost() {
        const res = await fetch(`https://jsonplaceholder.typicode.com/posts/${post_id}`);
        post = await res.json();
        console.log(post);        
    }

    fetchPost();
</script>

<div>{post.title}</div>
<div>--------------</div>
<div>{post.body}</div>