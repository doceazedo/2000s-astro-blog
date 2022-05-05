<script>
  export let posts = [];
</script>

<ul>
  {#each posts as post}
    <li>
      <a href={post?.url}>
        {new Date(post?.frontmatter?.publishDate).toLocaleDateString()} » {post?.frontmatter?.title}
      </a>
    </li>
  {/each}
</ul>

<style lang="sass">
  ul
    list-style: disc outside
    margin-left: 2rem
    margin-top: 1rem

    li::marker
      color: #ff75ba

    a
      color: #fff

      &:not(:hover)
        text-decoration: none
</style>