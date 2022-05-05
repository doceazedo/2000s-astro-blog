<div class="eyes">
  <span id="eyeL"></span>
  <span id="eyeR"></span>
</div>

<style lang="sass">
  .eyes
    position: absolute
    bottom: 46px
    left: 11px
    display: flex
    gap: 13px
    
    span
      position: relative
      display: inline-block
      border-radius: 50%
      height: 12px
      width: 12px
      background: #eee

      &::after
        content: ''
        position: absolute
        bottom: 6.5px
        right: 4.5px
        width: 4px
        height: 4px
        background: #000
        border-radius: 50%
</style>