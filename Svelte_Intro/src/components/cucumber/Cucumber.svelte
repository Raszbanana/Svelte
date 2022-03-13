<script>
  let vegetable = "cucumber";
  let changePicture = { gif: false };
  function toggle() {
    changePicture.gif = !changePicture.gif;
  }
  const cucumberGif1 =
    "https://media0.giphy.com/media/0gaMFii5pKJVF2rtl0/giphy.gif?cid=ecf05e4746wfzlhr08yy7r07vs5dmmjk2qz23cqgb0gpjtbc&rid=giphy.gif&ct=g";
  const cucumberGif2 = "https://i.giphy.com/media/l3q2L3yM5UhxEnsvC/giphy.webp";
</script>

<button on:click={toggle}> change gif!</button>
<p>I am a {vegetable}</p>
{#if changePicture.gif}
  <img src={cucumberGif2} alt="dancing-cucumber1" />
{/if}

{#if !changePicture.gif}
  <img src={cucumberGif1} alt="dancing-cucumber2" />
{/if}

<style>
  p {
    font-size: larger;
    font-family: "Times New Roman", Times, serif;
  }

  img {
    border-style: solid;
    border-radius: 30px;
    width: 506px;
    height: 506px;
  }

  button {
    border-style: solid;
    border-radius: 30px;
    background-color: #7484ff;
    color: #fca8a8;
    width: 131px;
    height: 50px;
  }
</style>
