<script context="module">
    export async function load({fetch}) {
        const res = await fetch('https://jsonplaceholder.typicode.com/guides')
        const guides = await res.json();

        if (res.ok) {
            console.log("okay")
            return {
                props: {
                    guides
                }
            }
        }

        return {
            status: res.status,
            error: new Error('Could not fetch guides')
        }
    }
</script>

<script>
    export let guides;
</script>
<div class="guides">
    <ul>
        {#each guides as guide}
            <li>
                <a href="/">{guide.title}</a>

            </li>
        {/each}
    </ul>
</div>
<a href="/about/user">g</a>