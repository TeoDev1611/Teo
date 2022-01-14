<script>
  export let name;
  import { onMount } from "svelte";
  let apiData = new Object();
  onMount(async () => {
    await fetch("https://api.quotable.io/random")
      .then((r) => r.json())
      .then((data) => {
        apiData = data;
        console.log(apiData);
      });
  });
  // Random emojis
  const emojis = ["( ͡❛ ͜ʖ ͡❛)", "( ͡▀̿ ̿ ͜ʖ ͡▀̿ ̿ )", "┏( ͡❛ ͜ʖ ͡❛)┛", "¯_( ͡▀̿ ̿ ͜ʖ ͡▀̿ ̿ )_/¯"];
  const emoji_bottom = emojis[Math.floor(Math.random() * emojis.length)];
  // Css Styles
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
<main class="u-max-full-width">
  <header>
    <!-- Fonts -->
    <link href="//fonts.googleapis.com/css?family=Raleway:400,300,600" rel="stylesheet" type="text/css" />
    <!-- Icons  -->
    <link rel="stylesheet" href="https://cdn.iconmonstr.com/1.3.0/css/iconmonstr-iconic-font.min.css" />
  </header>
  <div class="home">
    <h1>Hello I'm <strong>{name}</strong></h1>
    <div class="desc">
      <h5>
        I'm a developer and open source lover ❤. I like Deno, Golang, Lua and the terminal editors. I'm working in many
        projects some of this projects are <a href="https://github.com/TeoDev1611/astro.nvim"> astro.nvim,</a>
        <a href="https://github.com/TeoDev1611/octorg">octorg,</a>
        <a href="https://github.com/TeoDev1611/batman">batman</a> and some open source libraries. If you want help to my
        projects you can star and share this projects thanks for your help. Wanna talk about something? DM me on Twitter.
      </h5>
    </div>
    <div class="social">
      <a href="https://github.com/TeoDev1611/" class="emoji"><i class="im im-github" /></a>
      <a href="https://twitter.com/TeoDev1611" class="emoji"><i class="im im-twitter" /></a>
    </div>
    <div class="quote">
      <h6>Random quote <i>Why ? Why not :)</i></h6>
      <table class="u-full-width">
        <thead>
          <tr>
            <th>Author</th>
            <th>Content</th>
            <th>Tags</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <td>{apiData.author}</td>
            <td>{apiData.content}</td>
            <td>{apiData.tags}</td>
          </tr>
        </tbody>
      </table>
    </div>
    <footer class="footer">
      <h6>Made with ❤ in Ecuador {emoji_bottom}</h6>
    </footer>
  </div>
</main>

<style>
  * {
    /* border: 5px solid; */
    background-color: #f5f6fa;
  }
  .home {
    text-align: left;
    padding-top: 4%;
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
  .quote {
    padding-top: 3%;
    padding-bottom: 3%;
    width: 70%;
  }
  .footer {
    position: fixed;
    left: 0;
    bottom: 0;
    width: 100%;
    text-align: center;
  }
</style>
