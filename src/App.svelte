<script>
  import { Router, Link, Route } from "svelte-navigator";
  import Timer from "./lib/Timer.svelte";
  import Gallery from "./lib/Gallery.svelte";
  import Gratitude from "./lib/Gratitude.svelte";
  import Para from "./lib/Para.svelte";
</script>

<main>
  <Router>
    <nav>
      <div class="title">
        <h4>Happy Monthversary</h4>
      </div>
      <div class="links">
        <Link class="link" to="/">Home</Link>
        <Link class="link" to="para">Para</Link>
        <Link class="link" to="gallery">Gallery</Link>
        <Link class="link" to="gratitude">Gratitude</Link>
      </div>
    </nav>
    <div>
      <Route path="/">
        <Timer />
      </Route>
      <Route path="para" component={Para} />
      <Route path="gallery" component={Gallery} />
      <Route path="gratitude" component={Gratitude} />
    </div>
  </Router>
</main>

<style>
  nav {
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    align-items: center;
    background-color: #282c34;
    color: #abaab2;
    padding: 10px;
  }

  .title {
    margin-left: 20px;
  }

  .links {
    display: flex;
    flex-direction: row;
  }

  .links :global(.link) {
    text-decoration: none;
    margin-right: 30px;
    color: #abaab2;
  }
</style>
