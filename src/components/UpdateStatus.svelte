<style lang="scss">
  .main__update-status {
    border: solid 0.2px rgb(80, 80, 80);

    position: absolute;
    width: 70%;
    height: auto;
    bottom: 40px;
    left: 40px;
  }
  .play {
    position: absolute;
    bottom: -30px;
    right: -200px;
    font-size: 2.5em;
	border: solid white 0.3px;
	padding:8px 25px!important;
  }
   .play:hover{
	//   background-color:rgb(19, 19, 19);
	  cursor: pointer;
  }
  progress {
		display: block;
		width: 100%;
        height:40px;
    
	}
</style>
<script>
	import { tweened } from 'svelte/motion';
	import { cubicOut } from 'svelte/easing';

	const progress = tweened(0, {
		duration: 400,
		easing: cubicOut
	});
</script>
<div class="main__update-status">
<progress value={$progress}></progress>
    <!-- <h1 class="play">Play</h1> -->
    <button class="play" on:click="{() => progress.set(1)}">
	Play
</button>

</div>
