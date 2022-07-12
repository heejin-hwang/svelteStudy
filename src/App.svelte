<script>
  let t = new Date()
  let now = new Date()
  let timer

  let laps = []

  $: tick = now - t
  

  const 시작 = () => {
    console.log('시작');
  }

  const 종료 = () => {
    console.log('종료');
  }

  const LAP = () => {
    laps = [...laps, `${hour}:${min}:${sec}`]
  }
</script>

<main>
  <div>
    <div>00:00:00</div>
  </div>

  <button on:click={시작}>시작</button>
  <button on:click={종료}>종료</button>
  <button on:click={LAP}>LAP</button>
</main>

<style>
  :root {
    font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen,
      Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
  }

  main {
    text-align: center;
    padding: 1em;
    margin: 0 auto;
  }

  img {
    height: 16rem;
    width: 16rem;
  }

  h1 {
    color: #ff3e00;
    text-transform: uppercase;
    font-size: 4rem;
    font-weight: 100;
    line-height: 1.1;
    margin: 2rem auto;
    max-width: 14rem;
  }

  p {
    max-width: 14rem;
    margin: 1rem auto;
    line-height: 1.35;
  }

  @media (min-width: 480px) {
    h1 {
      max-width: none;
    }

    p {
      max-width: none;
    }
  }
</style>
