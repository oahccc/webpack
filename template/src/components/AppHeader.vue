<template>
  <header id="header">
    <h1><a href="#">Baseline</a></h1>
    <a href="#">Login</a>
    <a href="#nav" v-on:click="toggle">Menu</a>
	</header>
</template>

<script>
export default {
  methods: {
    toggle: function (event) {
      let $nav = document.querySelector('#nav'), $navClose;

      event.preventDefault();
      event.stopPropagation();

      $nav.classList.toggle('visible');

      // Close.

      // Create element.
      $navClose = document.createElement('a');
      $navClose.href = '#';
      $navClose.className = 'close';
      $navClose.tabIndex = 0;
      $nav.appendChild($navClose);

      // Event: Hide on ESC.
      window.addEventListener('keydown', function (event) {

        if (event.keyCode == 27)
          $nav.classList.remove('visible');

      });

      // Event: Hide nav on click.
      $navClose.addEventListener('click', function (event) {

        event.preventDefault();
        event.stopPropagation();

        $nav.classList.remove('visible');

      });
	  }
  }
}
</script>

<style></style>
