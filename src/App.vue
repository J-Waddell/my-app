<template>
  <body style>
    <div id="app-inner">
      <header class="header hide-in-preloading header--expanded" style="opacity: 1;visibility: inherit;">
        <div class="container">
          <!-- brand logo -->
          <div class="brandLogo">
            <h2 class="brandLogo__title" title="Jesse">
              <a class="brandLogo__link">Jesse.</a>
            </h2>
          </div>
          <!-- navbar -->
          <nav class="navbar">
            <ul class="navbar__links">
              <li class="navbar__links__item">
                <a class="navbar__links__link">Home</a>
              </li>
              <li class="navbar__links__item">
                <a class="navbar__links__link">About</a>
              </li>
              <li class="navbar__links__item">
                <a class="navbar__links__link">Skills</a>
              </li>
              <li class="navbar__links__item">
                <a class="navbar__links__link">Portfolio</a>
              </li>
              <li class="navbar__links__item">
                <a class="navbar__links__link">Contact</a>
                <ul class="langsDropdown__menu">

                </ul>
              </li>
            </ul>
          </nav>
          <!-- action items -->
          <ul class="header__actionsIcons">
            <li class="header__actionsIcons__item langSwitcher">
              <div class="langsDropdown">
                <a class="langsDropdown__toggle">EN</a>
                <ul class="langsDropdown__menu">
                  <li class="langsDropdown__menu__item">
                    <a>EN</a>
                  </li>
                  <li class="langsDropdown__menu__item">
                    <a>SP</a>
                  </li>
                </ul>
              </div>
            </li>
          </ul>
        </div>
      </header>
    </div>
  </body>
</template>

<script>

export default {
  name: 'App',
  data() {
    return {
      name: "Jesse Waddell"
    };
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

#app-inner {
    min-height: 100vh;
    width: 100%;
    background-color: hsl(var(--bg-color-one));
    color: hsl(var(--t-color-two));
    font-family: var(--body-font-family);
    line-height: 1.5rem;
    padding-top: var(--space-above-hero);
    overflow-x: hidden;
    -webkit-transition: background var(--global-transition), padding-top var(--global-transition);
    transition: background var(--global-transition), padding-top var(--global-transition);
}

.container {
    --bs-gutter-x: 1.5rem;
    width: 100%;
    padding-right: calc(var(--bs-gutter-x) * 0.5);
    padding-left: calc(var(--bs-gutter-x) * 0.5);
    margin-right: auto;
    margin-left: auto;
}

.header {
    position: fixed;
    z-index: 2000;
    left: 0;
    right: 0;
    width: 100%;
    -webkit-transition: all 0.3s ease-in-out;
    transition: all 0.3s ease-in-out;
}

.header:not(.header--minimized) {
    top: 0;
}

.header>.container {
    display: -webkit-box;
    display: -ms-flexbox;
    display: flex;
    -webkit-box-align: center;
    -ms-flex-align: center;
    align-items: center;
    -webkit-box-pack: justify;
    -ms-flex-pack: justify;
    justify-content: space-between;
    height: 20px;
    -webkit-transition: all 0.3s ease-in-out;
    transition: all 0.3s ease-in-out;
    width: auto;
}

.brandLogo__title {
    display: -webkit-box;
    display: -ms-flexbox;
    display: flex;
    -webkit-box-align: baseline;
    -ms-flex-align: baseline;
    align-items: baseline;
    width: -webkit-fit-content;
    width: -moz-fit-content;
    width: fit-content;
    color: hsl(var(--bg-color-reverse));
    font-family: var(--logo-font-family);
    font-size: 2rem;
    margin: 0;
}

.navbar__links {
    display: -webkit-box;
    display: -ms-flexbox;
    display: flex;
    -webkit-box-align: center;
    -ms-flex-align: center;
    align-items: center;
}

html[dir=ltr] .navbar__links__item:not(:last-of-type) {
    margin-right: 1.6rem;
}

html[dir=ltr] .navbar__links__link::before {
    left: 0;
}

html[dir=ltr] .navbar__links__link::after {
    margin-left: 0.1em;
}

.navbar__links__link {
    position: relative;
}

.navbar__links__link {
    font-weight: bold;
    padding: 0.4rem 0.2rem;
}

.navbar__links__link::before {
    content: "";
    position: absolute;
    top: 50%;
    -webkit-transform: translateY(-50%);
    transform: translateY(-50%);
    height: 0.15rem;
    width: 0;
    background-color: hsl(var(--main-color-one));
    -webkit-transition: all 0.3s ease-in-out;
    transition: all 0.3s ease-in-out;
}

.navbar__links__link::after {
    content: "";
    display: inline-block;
    height: 0.2em;
    width: 0.2em;
    background-color: hsl(var(--t-color-one));
    border-radius: 50%;
}

a, a:hover {
    color: inherit;
    text-decoration: none;
}

ol, ul {
    list-style-type: none;
    margin: 0;
    padding: 0;
}

.header__actionsIcons {
    display: -webkit-box;
    display: -ms-flexbox;
    display: flex;
    -webkit-box-align: center;
    -ms-flex-align: center;
    align-items: center;
}

html[dir=ltr] .header__actionsIcons__item:not(:last-of-type) {
    margin-right: 1rem;
}

.header__actionsIcons__item.langSwitcher {
    -webkit-transition: opacity var(--off-canvas-menu-transition);
    transition: opacity var(--off-canvas-menu-transition);
}

.langsDropdown {
    position: relative;
}

.langsDropdown__toggle {
    font-weight: bold;
}

html[dir=ltr] .langsDropdown__toggle::after {
    margin-left: 0.5rem;
}

.langsDropdown__toggle::after {
    content: "\f107";
    font-family: "Font Awesome 6 Free";
    font-size: 0.875rem;
}

.langsDropdown__menu {
    background-color: hsl(var(--bg-color-two));
    z-index: -1;
}

.langsDropdown__menu__link {
    display: block;
    font-weight: bold;
    padding: 0 0.875rem;
}
</style>
