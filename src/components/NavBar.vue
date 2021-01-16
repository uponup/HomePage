<template>
	<nav class="navbar">
		<div class="container">
			<div class="navbar-brand">
				<a href="/">
					<img class="custom-logo" src="../assets/logo_left_right.png" />
				</a>
			</div>
			<div id="customNavBar" class="navbar-menu">
				<div class="navbar-end">
					<a class="navbar-item" href="https://www.baidu.com">Support</a>
					<a class="navbar-item" href="https://github.com/uponup" target="_blank">
						<i class="icon icon-github"></i>
					</a>
					<a class="navbar-item" href="https://www.instagram.com/hexiliu_ou/" target="_blank">
						<i class="icon icon-ins"></i>
					</a>
				</div>
			</div>
		</div>
	</nav>
</template>

<script>
</script>

<style>
	.navbar {
		align-items: stretch;
		display: flex;
		flex-direction: row;
		box-sizing: inherit;
		padding: 16px 0;
		border-bottom: 1px solid #ebeaeb;
		top: 0;
		position: fixed;
	}
	
	.container {
		flex-grow: 1;
		display: flex;
		position: relative;
		margin-left: 30px;
		margin-right: 30px;
	}
	
	.navbar-menu {
		margin-right: -.75rem;
		flex-grow: 1;
		flex-shrink: 0;
		align-items: stretch;
		display: flex;
	}
	
	.navbar-brand {
		align-items: center;
		display: flex;
		flex-shrink: 0;
		min-height: 3.25rem;
		box-sizing: inherit;
		line-height: 1.5;
		width: 136px;
	}
	
	.navbar-brand img {
		max-width: 100%;
	}
	
	.navbar-menu {
		align-items: stretch;
		display: flex;
	}
	
	.navbar-end {
		justify-content: flex-end;
		margin-left: auto;
		align-items: stretch;
		display: flex;
	}
	
	.navbar-item {
		margin-left: -.25rem;
		margin-right: -.25rem;
		color: #1b1b1b;
		font-size: 18px;
		display: flex;
		align-items: center;
		flex-grow: 0;
		flex-shrink: 0;
		line-height: 1.5;
		padding: .5rem .75rem;
		position: relative;
	}
	
	a {
		text-decoration: inherit;
	}
	
	a.navbar-item {
		cursor: pointer;
	}

	.icon {
		background-repeat: no-repeat;
		height: 24px;
		width: 24px;
		background-size: cover;
	}

	.icon-ins {
		background-image: url(../assets/instagram.svg);
	}

	.icon-github {
		background-image: url(../assets/github.svg);
	}
</style>
