<script>
  let links = [
    { id: "aa", name: "Wikipedia", link: "https://www.wikipedia.org/" },
    { id: "aa", name: "Reddit", link: "https://www.reddit.com/" },
    { id: "aa", name: "Stackoverflow", link: "https://stackoverflow.com/" },
  ];

  function removeLink() {
    links = links.slice(0, -1);
  }

  let newName = "";
  let newLink = "";
  let i = 0;

  const addLink = (name, link) => {
    newLink = { id: i + 1, name: name, link: link };
    links.push(newLink);
    links = links;
  }
</script>

<h1>Useful links for nerds like me</h1>

<ul>
  {#each links as { id, name, link }, i}
    <li>
      <a href={link}>
        {i + 1}: {name}
      </a>
    </li>
  {/each}
</ul>
<button on:click={removeLink}>Remove a link if you think its too nerdy</button>
<div>
  <input  type ="text" placeholder="name" on:keydown={(e) => newName = e.target.value}>
  <input  type ="text" placeholder="link" on:keydown={(e) => newLink = e.target.value} />
  <button on:click= {addLink(newName, newLink) }
    >Or add a link if you feel like it could use some better ones</button
  >
</div>
<p>Make sure to include the whole url, like "https://stackoverflow.com/"</p>

<style>
  li {
    color: #fca8a8;
    width: 7%;
    margin-left: 52rem;
  }

  a {
    color: #fca8a8;
  }

  button {
    background-color: #fca8a8;
    border-style: solid;
    border-radius: 30px;

  }
</style>
