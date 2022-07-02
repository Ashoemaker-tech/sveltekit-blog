<script>
    export let posts
    console.log(posts);
</script>

{#each posts as post }
<div class="block">
    <div class="card">
            <section class="section">
                <div class="columns">
                    <div class="column is-8 is-offset-2">
                        <div class="content is-medium">
                            <h1 class="title is-spaced">{post.title}</h1>
                            <p class="subtitle">{post.excerpt}</p>
                            <a href={'/posts/'+post.id} class="button is-white">Read more</a>
                        </div>
                    </div>
                </div>
            </section>
    </div>
</div>
    {/each}
  
  <hr>