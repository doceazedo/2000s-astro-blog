<script>
  export let title;
</script>

<div class="container">
  <header class="header">
    <img src="/assets/img/doceazedo.gif" alt="" />
  </header>
  <marquee class="marquee" width="800">
    Este texto vai "rolar" da direita para esquerda
  </marquee>
  <section class="section">
    <aside class="sidebar">
      <a href="/">Home</a>
      <a href="/blog">Blog</a>
      <a href="/">Links</a>
      <a href="/">About me</a>
      <a href="/">Music</a>
      <a href="/">Games</a>
      <a href="/">Art</a>
    </aside>
    <main class="main">
      <h1 class="main-title">{title}</h1>
      <div class="main-content">
        <slot />
      </div>
    </main>
  </section>
</div>

<style lang="sass">
  .container
    display: flex
    flex-direction: column
    gap: 15px
    width: 800px
    height: 700px

    .header
      display: flex
      justify-content: center
      padding: 15px 15px 35px
      border: 2px solid #ff75ba
      border-radius: 10px
      background-image: url('/assets/img/bg-overlay.png')

    .marquee
      padding: 10px 15px 20px
      border: 2px solid #ff75ba
      border-radius: 10px
      background-image: url('/assets/img/bg-overlay.png')

    .section
      display: flex
      gap: 15px
      height: 100%

      .sidebar
        display: flex
        flex-direction: column
        flex-shrink: 0
        width: 200px
        height: 100%
        border: 2px solid #ff75ba
        border-radius: 10px
        background-image: url('/assets/img/bg-overlay.png')

        a
          display: flex
          justify-content: center
          padding: 0.5rem 0
          font-family: 'IBM Plex Serif', serif
          font-style: italic
          white-space: pre
          text-decoration: none
          color: #fff
          border-bottom: 1px solid #ff75ba

          &:nth-child(odd)::before,
          &:nth-child(odd)::after
            content: '  ♡  '

          &:nth-child(even)::before,
          &:nth-child(even)::after
            content: '  ✰  '

          &:hover
            background-color: rgba(#ff75ba, .25)

    .main
      flex-grow: 1
      height: 100%
      border: 2px solid #ff75ba
      border-radius: 10px
      background-image: url('/assets/img/bg-overlay.png')
      overflow: auto

      &-title
        padding: 5px 10px
        font-weight: 700
        border-bottom: 2px solid #ff75ba
        background-color: rgba(#ff75ba, .5)

      &-content
        padding: 5px 10px

        :global(p:not(:last-child))
          margin-bottom: 5px

        :global(.astro-code)
          overflow-x: auto
          border-radius: 5px
          padding: 10px 15px
</style>