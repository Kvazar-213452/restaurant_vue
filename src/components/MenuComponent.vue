<template>
  <!-- ⠀⠀⠀⠀⠀⠀⠀⠀⠀⣤⣄⡀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀
      ⠀⠀⠀⠀⠀⠀⠀⠀⢠⣿⣿⣿⣷⣦⠄⠀⠀⠀⣐⣆⣄⣤⣴⣶⣾⣿⠀⠀
      ⠀⠀⢀⣤⣴⣦⠀⠀⠘⣿⣿⡿⠋⢀⠄⠀⢂⠅⣀⠔⠀⠉⠻⣿⣿⡿⠀⠀
      ⠀⣰⣿⣿⡿⠃⠀⠀⠀⣿⠋⠀⡰⠁⢀⠔⢁⠜⠁⣰⢀⢇⠀⡈⢿⠃⠀⠀
      ⢰⣿⣿⠟⠁⠀⠀⠀⣴⠃⢠⢰⠄⣠⢊⡤⠏⢠⠌⢆⠌⠈⣆⣹⠸⡆⠀⠀
      ⣾⣿⡿⠀⠀⠀⠀⠜⠇⣄⣈⣋⠮⣧⡞⢰⡔⠃⣜⠊⢀⠀⠋⠙⢀⡇⠀⠀
      ⢿⣿⣷⠀⠀⠀⠀⢀⡇⣿⡸⢏⢹⢻⡿⠻⣶⢾⡿⡧⢤⣤⣼⣦⣄⡇⠀⠀
      ⠸⣿⣿⣧⡀⠀⢠⣎⣿⢿⣧⣾⣠⣟⣡⣅⢿⢸⠃⣭⣿⢸⡇⣼⢿⡇⠀⠀
      ⠀⠘⢿⣿⣿⣶⢡⠿⡹⡴⡻⡢⢀⠀⠈⠉⠉⠉⠙⠛⢛⢲⡶⣿⣼⠩⡂⠀
      ⠀⠀⠀⠈⠛⢏⠼⡀⠣⣥⢹⣷⣤⠀⢰⡟⠛⡖⠀⠀⣠⣯⡶⢫⠟⣆⢳⠀
      ⠀⠀⠀⠀⢰⠉⠒⠬⠔⣁⣙⢯⢿⣷⣤⣀⢂⣡⣤⣞⠭⢯⢴⠛⢲⣗⠣⡀
      ⠀⠀⠀⠀⡏⡄⢂⠀⡆⠢⡁⡜⢮⢱⣙⠻⠿⡟⡡⣪⢢⠀⠃⡔⢁⠜⡊⢢
      ⠀⠀⠀⠀⠀⠐⠈⠢⡈⢄⢱⠐⡞⠒⡶⡩⣁⠰⣷⠁⢀⠈⠐⠔⢡⠀⠀⠘
      ⠀⠀⠀⠀⠀⠀⠀⠁⠈⠂⠋⠀⠈⠃⠁⠀⠀⠐⠙⠂⠀⠁⠂⠀⠀⠀⠀⠀ -->
  <header class="header">
    <!-- Logo -->
    <a href="#" class="logo">Hamburger</a>
    <nav>
      <!-- Menu Button -->
      <input class="menu-btn" type="checkbox" id="menu-btn" aria-label="Toggle Navigaton Menu">
      <!-- Icon -->
      <label class="menu-icon" for="menu-btn">
        <span class="navicon"></span>
      </label>
      <!-- Menu -->
      <ul class="menu">
        <li @click="scrollToSection('Pizza')"><span>Pizza</span></li>
        <li @click="scrollToSection('Sushi')"><span>Sushi</span></li>
        <li @click="scrollToSection('Hot menu')"><span>Hot menu</span></li>
        <li @click="scrollToSection('Drinks')"><span>Drinks</span></li>
      </ul>
    </nav>
  </header>
</template>

<script>
export default {
  methods: {
    scrollToSection(id) {
      const element = document.getElementById(id);
      if (element) {
        element.scrollIntoView({ behavior: "smooth", block: "start" });
      } else {
        console.warn(`Element with id "${id}" not found.`);
      }
    },
  },
};
</script>

<style>
/* Light Mode Color Scheme */
:root {
  --color-bg: #111111;
  --color-bg2: #111111;
  --color-text: #ffffff;
}

/* Header */
.header {
  background-color: var(--color-bg);
  border-bottom: 2px solid var(--color-bg2);
  position: fixed;
  width: 100%;
  z-index: 3;
}

.header span {
  color: var(--color-text);
  cursor: pointer;
}

.header .logo {
  display: block;
  float: left;
  font-size: 2em;
  padding: 10px 20px;
  text-decoration: none;
}

.header ul {
  margin: 0;
  padding: 0;
  list-style: none;
  overflow: hidden;
  background-color: var(--color-bg);
}

.header li span {
  display: block;
  padding: 20px 20px;
  border-right: 2px solid var(--color-bg2);
  text-decoration: none;
  transition: all .3s;
}

.header li:first-child {
  border-left: 2px solid var(--color-bg2)
}

.header li span:hover,
.header .menu-btn:hover {
  opacity: 0.5;
}

/* Nav Menu */
.header .menu {
  clear: both;
  max-height: 0;
  transition: max-height .2s ease-out;
}

/* Menu Icon */
.header .menu-icon {
  cursor: pointer;
  display: inline-block;
  float: right;
  padding: 28px 20px;
  position: relative;
  user-select: none;
}

.header .menu-icon .navicon {
  background: var(--color-text);
  display: block;
  height: 2px;
  width: 18px;
  position: relative;
  transition: all .3s;
}
  
.header .menu-icon .navicon:before,
.header .menu-icon .navicon:after {
  background: var(--color-text);
  content: '';
  display: block;
  height: 100%;
  position: absolute;
  transition: all .2s ease-out;
  width: 100%;
}

.header .menu-icon .navicon:before {
  top: 5px;
}

.header .menu-icon .navicon:after {
  top: -5px;
}

/* Menu Button */
.header .menu-btn {
  display: none;
  transition: all .3s;
}

.header .menu-btn:checked ~ .menu {
  max-height: 240px;
}

.header .menu-btn:checked ~ .menu-icon .navicon {
  background: transparent;
}

.header .menu-btn:checked ~ .menu-icon .navicon:before {
  transform: rotate(-45deg);
}

.header .menu-btn:checked ~ .menu-icon .navicon:after {
  transform: rotate(45deg);
}

.header .menu-btn:checked ~ .menu-icon:not(.steps) .navicon:before,
.header .menu-btn:checked ~ .menu-icon:not(.steps) .navicon:after {
  top: 0;
}

/* 48em = 768px */

@media (min-width: 48em) {
  .header li {
    float: left;
  }
  .header li span {
    padding: 20px 30px;
  }
  .header .menu {
    clear: none;
    float: right;
    max-height: none;
  }
  .header .menu-icon {
    display: none;
  }
}
</style>
