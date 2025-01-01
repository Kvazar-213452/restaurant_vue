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
    <a href="#" class="logo">Hamburger Menu</a>
    <nav>
      <!-- Menu Button -->
      <input class="menu-btn" type="checkbox" id="menu-btn" aria-label="Toggle Navigaton Menu">
      <!-- Icon -->
      <label class="menu-icon" for="menu-btn">
        <span class="navicon"></span>
      </label>
      <!-- Menu -->
      <ul class="menu">
        <li><a href="#home">Home</a></li>
        <li><a href="#about">About</a></li>
        <li><a href="#careers">Careers</a></li>
        <li><a href="#contact">Contact</a></li>
      </ul>
    </nav>
  </header>
</template>

<script>
export default {
  mounted() {
    
  },
};
</script>

<style>
/* Light Mode Color Scheme */
:root {
  --color-bg: #fff;
  --color-bg2: #f4f4f4;
  --color-toggle-accent: #ff7900;
  --color-text: #333333;
}



html {
  background-color: var(--color-bg);
  color: var(--color-text);
}

body {
  margin: 0;
  font-family: Helvetica, sans-serif;
}

/* Header */
.header {
  background-color: var(--color-bg);
  border-bottom: 2px solid var(--color-bg2);
  position: fixed;
  width: 100%;
  z-index: 3;
}

.header a {
  color: var(--color-text);
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

.header li a {
  display: block;
  padding: 20px 20px;
  border-right: 2px solid var(--color-bg2);
  text-decoration: none;
}

.header li:first-child {
  border-left: 2px solid var(--color-bg2)
}

.header li a:hover,
.header .menu-btn:hover {
  background-color: var(--color-bg2);
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
  transition: background .2s ease-out;

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
  .header li a {
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
