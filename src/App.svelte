<script>
  import Selection from "./components/Selection.svelte";
  import Friends from "./components/Friends.svelte";
	import News from "./components/News.svelte";
	import UpdateStatus from "./components/UpdateStatus.svelte";
  let name = "ICode4fun";
</script>

<style lang="scss">
h1{
    padding:0!important;
    margin:0!important;
    }
  .user {
    // position: absolute;
    // top: 0;
    // left: 10px;
	margin-left:40px!important;
	margin-top:20px!important;
    font-size: 1em;
  }
  
 
  .main {
    display: flex;
    justify-content: center;
    align-items: center;
    height: 95vh;
    background-color: black;
  }
  .main__inner {
    border: solid white 0.3px;
    width: 65%;
    height: 70%;
    position: relative;
	display:inherit;
	justify-content: space-between;
  }
  .main__inner__controls {
    display: flex;
    justify-content: flex-end;
  }
</style>

<div class="main">

  <div class="main__inner">
    
	<Friends/>
	<News/>
	<UpdateStatus/>
    <!-- <div class="main__inner__controls">
      <Selection />
    </div> -->
  </div>
</div>
