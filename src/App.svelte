<script>
	export const web = {
		name: "Teo!",
		emoji_bottom: "( ͡▀̿ ̿ ͜ʖ ͡▀̿ ̿ )",
		url: {
			github: "https://github.com/TeoDev1611/",
			twitter: "https://twitter.com/TeoDev1611",
		},
	};
	export let name;
	import "../assets/styles/normalize.css";
	import "../assets/styles/skeleton.css";
</script>

<svelte:head>
	<title>Home - Teo</title>
	<html lang="en">
		<meta charset="UTF-8" />
		<meta http-equiv="X-UA-Compatible" content="IE=edge" />
		<meta name="viewport" content="width=device-width, initial-scale=1.0" />
	</html></svelte:head
>
<main>
	<header>
		<!-- Fonts -->
		<link
			href="//fonts.googleapis.com/css?family=Raleway:400,300,600"
			rel="stylesheet"
			type="text/css"
		/>
		<!-- Icons  -->
		<link
			rel="stylesheet"
			href="https://cdn.iconmonstr.com/1.3.0/css/iconmonstr-iconic-font.min.css"
		/>
	</header>
	<div class="home">
		<h1>Hello I'm <strong>{name}</strong></h1>
		<div class="desc">
			<h5>
				I'm a developer and open source lover ❤. I like Deno, Golang,
				Lua and the terminal editors. I'm working in many projects some
				of this projects are <a
					href="https://github.com/TeoDev1611/astro.nvim"
				>
					astro.nvim,</a
				> <a href="https://github.com/TeoDev1611/octorg">octorg,</a>
				<a href="https://github.com/TeoDev1611/batman">batman</a> and some
				open source libraries. If you want help to my projects you can star
				and share this projects thanks for your help. Wanna talk about something?
				DM me on Twitter.
			</h5>
		</div>
		<div class="social">
			<a href="https://github.com/TeoDev1611/" class="emoji"
				><i class="im im-github" /></a
			>
			<a href="https://twitter.com/TeoDev1611" class="emoji"
				><i class="im im-twitter" /></a
			>
		</div>
		<footer class="footer">
			<h6>Made with ❤ in Ecuador {web.emoji_bottom}</h6>
		</footer>
	</div>
</main>

<style>
	main {
		/* border: 5px solid; */
		background-color: #f5f6fa;
	}
	.home {
		text-align: left;
		padding-top: 7%;
		padding-left: 20%;
	}
	.emoji {
		color: black;
		padding-left: 1%;
	}
	.emoji:hover {
		opacity: 65%;
		transition: opacity 0.5s;
	}
	.desc {
		padding-top: 2%;
		width: 70%;
	}
	.footer {
		padding-top: 12%;
		width: auto;
		padding-left: 25%;
	}
</style>
