<script context="module">
    export async function load({ fetch }) {
        const res = await fetch('https://bloc-loon-60505.herokuapp.com/api/posts')
        const data = await res.json()
            return {
                props: { posts: data }
            }
    }
</script>

<script>
    import PostCard from "../components/PostCard.svelte";
    export let posts;
</script>
<svelte:head>
    <title>My Blog</title>
</svelte:head>

<PostCard {posts} />



