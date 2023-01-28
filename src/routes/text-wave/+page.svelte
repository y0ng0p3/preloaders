<script>
  const loading = 'Loading';
</script>

<svelte:head>
	<title>Text-Wave</title>
	<meta name="description" content="Text-Wave loading" />
</svelte:head>

<span class="back">
  {#each loading as letter, i (i)}
  <span>{letter}</span>
  {/each}
</span>

<style>
  @import url(https://fonts.googleapis.com/css?family=Roboto:300);

  .back {
    margin: 1em auto;
    font-family: "Roboto";
  }
  .back span {
    font-size: 3em;
    color: var(--color-theme-2);
    /* background-color: var(--color-bg-1); */
    display: table-cell;
    box-shadow: inset 0 0 5px rgba(0,0,0,0.3), 0 5px 0 #ccc;
    padding: 0 15px;
    line-height: 100px;
    animation: loadingAnimation 2s infinite;
  }
  @keyframes loadingAnimation {
    0% {
      transform: translateY(0px);
    }
    50% {
      transform: translateY(30px);
      box-shadow: 0 15px 0 var(--color-bg-2);
    }
    100% {
      transform: translateY(0px);
    }
  }
  .back span:nth-child(1) {
    animation-delay: 0s;
  }
  .back span:nth-child(2) {
    animation-delay:.1s;  
  }
  .back span:nth-child(3) {
    animation-delay:.2s;
  }
  .back span:nth-child(4) {
    animation-delay:.3s;  
  }
  .back span:nth-child(5) {
    animation-delay:.4s;
  }
  .back span:nth-child(6) {
    animation-delay:.5s;  
  }
  .back span:nth-child(7) {
    animation-delay:.6s;
  }

</style>
