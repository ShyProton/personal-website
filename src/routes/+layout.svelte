<script>
  import "../app.scss";
  import Navbar from "$lib/components/navbar/Navbar.svelte";
  import Footer from "$lib/components/footer/Footer.svelte";
</script>

<svelte:head>
  <title>Shayan | Portfolio</title>
  <link rel="preconnect" href="https://fonts.googleapis.com" />
  <link rel="preconnect" href="https://fonts.gstatic.com" />
  <link
    href="https://fonts.googleapis.com/css2?family=Fira+Code:wght@400;700&amp;family=Fira+Sans:ital,wght@0,400;0,700;1,400;1,700&amp;display=swap"
    rel="stylesheet"
  />
  <link
    href="https://www.nerdfonts.com/assets/css/webfont.css"
    rel="stylesheet"
    type="text/css"
  />
</svelte:head>

<Navbar />
<slot />
<Footer />
