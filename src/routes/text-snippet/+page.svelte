<svelte:head>
	<title>Text-Snippet</title>
	<meta name="description" content="Text snippet loading" />
</svelte:head>

<div class="loading">
  <span>Loading</span>
</div>

<style>
  .loading {
    font-family: "Arial Black", "Arial Bold", Gadget, sans-serif;
    text-transform: uppercase;
    width: 150px;
    text-align: center;
    line-height: 50px;
    position: absolute;
    left: 0;
    right: 0;
    top: 50%;
    margin: auto;
    transform: translateY(-50%);
  }
  .loading span {
    position: relative;
    z-index: 999;
    color: #fff;
  }
  .loading::before {
    content: '';
    background-color: var(--color-theme-1);
    width: 128px;
    height: 36px;
    display: block;
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    margin: auto;
    animation: 2s loadingAnimation infinite ease-in-out;
  }
  .loading::after {
    content: '';
    background-color: var(--color-theme-2);
    width: 14px;
    height: 72px;
    display: block;
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    margin: auto;
    animation: 2s loadingAnimation2 infinite ease-in-out;
  }
  @keyframes loadingAnimation {
    0% {
      transform: translateX(-14px);
    }
    50% {
      transform: translateX(14px);
    }
    100% {
      transform: translateX(-14px);
    }
  }
  @keyframes loadingAnimation2 {
    0% {
      transform: translateX(-48px);
    }
    50% {
      transform: translateX(48px);
    }
    100% {
      transform: translateX(-48px);
    }
  }
</style>
