<script>
    let posts = [];

    async function fetchPosts() {
        const res = await fetch('https://jsonplaceholder.typicode.com/posts')
        posts = await res.json();
    }

    fetchPosts();
</script>

<div>Posts: </div>

<div>
    <ul>
        {#each posts as post}
            <li>
                <a href={`/posts/${post.id}`}>{post.title}</a>

            </li>
        {/each}
    </ul>
</div>