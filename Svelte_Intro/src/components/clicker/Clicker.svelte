<script>
  let count = 0;

  function incrementClick() {
    count += 1;
  }

  function decrementClick() {
    count -= 1;
  }

  $: timesTen = count * 10;
</script>

<button on:click={incrementClick}>Click to increment</button>
<div id="counter">
  <p>The count is {count}</p>
  <p>{count} times 10 is {timesTen}</p>
</div>
<button on:click={decrementClick}>Click to decrement</button>

<style>
  button {
    border-style: solid;
    border-radius: 30px;
    background-color: #fca8a8;
  }

  p {
    background-color: #1a1f23;
    border-style: solid;
    border-radius: 20px;
    color: #fca8a8;
    font-weight: solid;
    font-size: 30px;
  }

  #counter {
    width: 20%;
    margin-left: 40%;
  }
</style>
