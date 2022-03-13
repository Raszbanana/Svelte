<script>
  let m = { x: 0, y: 0 };

  let style = "background-color: #fca8a8";

  function handleMousemove(event) {
    m.x = event.clientX;
    m.y = event.clientY;

    if (m.x < 939 && m.y < 920) {
      style = "background-color: #fca8a8";
    } else  {
      style = "background-color: #7484ff";
    }
  }
</script>
<div on:mousemove={handleMousemove} {style}>
  <h1>Something about using the mouse positioning</h1>
  The mouse position is {m.x} x {m.y}
  <p>You can change the color of this div by moving left and right</p>
</div>

<style>
  div {
    width: 100%;
    height: 20rem;
    border-style: solid;
    border-radius: 137px;
  }
</style>
