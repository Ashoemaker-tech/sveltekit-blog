<script context="module">
    export async function load({ fetch, params }) {
        const res = await fetch(`https://bloc-loon-60505.herokuapp.com/api/posts/${params.id}`)
        const post = await res.json()
            return {
                props: { post }
            }
    }
</script>

<script>
    export let post;
</script>
<svelte:head>
    <title>{post.title}</title>
</svelte:head>

<section class="section is-large">
    <h1 class="title">{post.title}</h1>
    <h2 class="subtitle">
    {post.excerpt}
    </h2>
    <p>{post.description}</p>
  </section>