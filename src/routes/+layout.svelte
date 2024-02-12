<script>
	import 'bootstrap/dist/css/bootstrap.min.css';
	import Navbar from '../components/Navbar.svelte';

	let isOpened = false;

	function toggleOpen() {
		isOpened = !isOpened;
	}
</script>

<nav class="navbar navbar-expand-lg bg-body-tertiary">
	<div class="container-fluid">
		<a class="navbar-brand" href="/">PoyuK's site</a>
		<button
			on:click={toggleOpen}
			class="navbar-toggler"
			type="button"
			data-bs-toggle="collapse"
			data-bs-target="#navbarNav"
			aria-controls="navbarNav"
			aria-expanded="false"
			aria-label="Toggle navigation">
			<span class="navbar-toggler-icon"></span>
		</button>
		<div class:show={isOpened} class="collapse navbar-collapse" id="navbarNav">
			<ul class="navbar-nav">
				<li class="nav-item">
					<Navbar path="/" title="Home" />
				</li>
				<li class="nav-item">
					<Navbar path="/about" title="About" />
				</li>
				<li class="nav-item">
					<Navbar path="/contact" title="Contact" />
				</li>
			</ul>
		</div>
	</div>
</nav>

<main class="container">
	<slot />
</main>