<template>
  <section class="c-details">
    <slot></slot>
  </section>
</template>

<style lang="sass">

.c-details
  @include unselectable
  display: flex
  flex-direction: column

  width: $details-width
  max-height: calc(100vh - #{$cell-line-height * 2} - 1rem)

  margin-left: ($details-width - $cell-width) / -2
  padding: 0.375rem

  background-color: $details-background
  color: #fff

  overflow-x: auto
  transition: opacity 200ms ease

  z-index: $z-details

  hr
    margin: 0.25rem 0
    border: solid $details-seperator
    border-width: 0 0 $_1px 0

  var
    font-style: normal

  .row
    border-left: 0.125rem solid transparent
    padding-left: 0.25rem

  .c-details-graph
    padding: 0.25rem 0
    height: 0.75rem

.details-group
  &.dps .row
    border-left-color: #FF6E2C
  &.healer .row
    border-left-color: #00E676
  &.tank .row
    border-left-color: #82B1FF

</style>
