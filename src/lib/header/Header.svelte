<script lang="ts">  
	import logo from '$lib/images/logo.png';
	import github from '$lib/images/github.svg'

	let menuOpen: boolean = false;
  
	function toggleMenu(): void {
	  menuOpen = !menuOpen;
	}
  </script>
  
  <style>
	header {
	  background: linear-gradient(to right, #ff6700, #002f6c);
	  color: white;
	  padding: 15px 20px;
	  display: flex;
	  justify-content: space-between;
	  align-items: center;
	  box-shadow: 0px 4px 8px rgba(0, 0, 0, 0.1);
	}
  
	.logo-container {
	  display: flex;
	  align-items: center;
	  gap: 10px;
	}
  
	.logo {
	  height: 40px;
	}
  
	.site-name {
	  font-size: 1.8rem;
	  font-weight: bold;
	}
  
	.nav-links {
	  display: flex;
	  gap: 20px;
	}
  
	.nav-links a {
	  color: white;
	  text-decoration: none;
	  font-size: 1rem;
	  font-weight: bold;
	  transition: color 0.3s ease;
	}
  
	.nav-links a:hover {
	  color: #ffcc00;
	}
  
	/* GitHub Icon */
	.github-icon {
	  font-size: 1.5rem;
	  margin-left: 15px;
	  color: white;
	  transition: transform 0.2s;
	}
  
	.github-icon:hover {
	  transform: scale(1.2);
	}
  
	/* Mobile Menu */
	.menu-button {
	  display: none;
	  font-size: 1.5rem;
	  cursor: pointer;
	}
  
	@media (max-width: 768px) {
	  .nav-links {
		display: none;
		flex-direction: column;
		background: #002f6c;
		position: absolute;
		top: 60px;
		right: 0;
		width: 100%;
		padding: 10px;
		box-shadow: 0px 4px 8px rgba(0, 0, 0, 0.2);
	  }
  
	  .nav-links.open {
		display: flex;
	  }
  
	  .menu-button {
		display: block;
	  }
	}
  </style>
  
  <header>
	<!-- Logo & Site Name -->
	<div class="logo-container">
	  <img src={logo} alt="DutchInLevels" class="logo" />
	  <div class="site-name">DutchInLevels</div>
	</div>
  
	<!-- Mobile Menu Button -->
	<button class="menu-button" on:click={toggleMenu}>
	  ☰
	</button>
  
	<!-- Navigation Links -->
	<nav class="nav-links {menuOpen ? 'open' : ''}">
	  <a href="/">Home</a>
	  <a href="/about">Over Ons</a>
	  <a href="https://github.com/brenovit/dutch-in-levels" target="_blank"class="github-icon" aria-label="GitHub">
		<img src={github} alt="GitHub" />
	  </a>
	</nav>
  </header>
  