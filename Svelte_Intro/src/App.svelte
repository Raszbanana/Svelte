<script>
  import Cucumber from "./components/cucumber/Cucumber.svelte";
  import Clicker from "./components/clicker/Clicker.svelte";
  import Answers from "./components/answers/Answers.svelte";
  import Book from "./components/book/Book.svelte";
  import Links from "./components/links/Links.svelte";
  import Mouse from "./components/mouse/Mouse.svelte";

  const bookInfo = {
    book: "CHERUB: The Recruit",
    author: "Robert Muchamore",
    publisher: "Hodder",
    pages: 342,
    about: "a spy kid agency",
    year: "2004",
  };
</script>

<main>
  <div id="container">
    <h1 id="outhere">We out here</h1>
    <p id="why">I googled Svelte and found this background picture</p>
    <div id="cucumber">
      <Cucumber />
    </div>
    <div id="clicker"><Clicker /></div>
    <div id="answers">
      <Answers answer1={"1000 woods"} />
      <Book {...bookInfo} />
    </div>
    <div id="links">
      <Links />
    </div>
    <Mouse />
  </div>
</main>

<style>
  #container {
    border-style: double;
    border-top-left-radius: 35%;
    border-top-right-radius: 35%;
    border-bottom-left-radius: 8%;
    border-bottom-right-radius: 8%;
    border-color: black;
  }
  #cucumber {
    margin-top: 14rem;
  }

  #why {
    margin-right: 50px;
    font-family: monospace;
  }

  #clicker {
    border-style: groove;
    border-radius: 137px;
    border-color: aliceblue;
    background-color: #7484ff;
  }

  #answers {
    border-style: groove;
    border-radius: 137px;
    border-color: aliceblue;
    background-color: #fca8a8;
  }

  #outhere {
    margin-bottom: -70px;
    margin-left: 38%;
  }

  #links {
    border-style: groove;
    border-radius: 137px;
    border-color: aliceblue;
    background-color: #7484ff;
    color: #fca8a8;
  }

  main {
    text-align: center;
    padding: 1em;
    max-width: 240px;
    margin: 0 auto;
    background-image: url("https://scontent-cph2-1.xx.fbcdn.net/v/t1.6435-9/88363966_101899048095946_4118917651688849408_n.png?_nc_cat=101&ccb=1-5&_nc_sid=e3f864&_nc_ohc=7R9_DZLhrXUAX9-12Ua&tn=-AZ-hZnXx3jme0rp&_nc_ht=scontent-cph2-1.xx&oh=00_AT9OyhnCIumVkTAn7-qG7nWwzktrLNlo7mEoKQw-6HoObw&oe=62528FD3");
  }

  @media (min-width: 640px) {
    main {
      max-width: none;
    }
  }
</style>
