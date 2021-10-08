<template>

<div style="background-color: red">
    <header>
        <slot name="header"></slot>
    </header>
    <footer>
        <slot name="footer"></slot>
    </footer>
    <!-- <slot></slot> -->
</div>
  
</template>

<script>
export default {
    name: 'Form',
}
</script>

<style>

</style>