<script>
	
	import gsap from "gsap";
	import LocomotiveScroll from 'locomotive-scroll';

	// const locomotiveScroll = new LocomotiveScroll();
</script>

<svelte:head>
	<title>Home</title>
	
</svelte:head>

<main>
	<ul>
		<li id="cover-1"><a href="#cover-2">1</a></li>
		<li id="cover-2"><a href="#cover-3">2</a></li>
		<li id="cover-3"><a href="#cover-4">3</a></li>
		<li id="cover-4"><a href="#cover-5">4</a></li>
		<li id="cover-5"><a href="#cover-1">5</a></li>
		
		
		
		
		
	</ul>
</main>

<style>
	
	/* @import 'node_modules/locomotive-scroll/dist/locomotive-scroll'; */

/*  Only necessary with horizontal scrolling */ 

*,
*::before,
*::after,
html,
:global(body){
  box-sizing: border-box;
  margin: 0;
  padding: 0;
  list-style: none;
  appearance: none;
  text-decoration: none;
  scroll-behavior: smooth;
  scrollbar-gutter: stable;
  scrollbar-width: thin;  

}




main{
	width: 100%;
	height: 100vh;
	background-color: rgb(88, 88, 88);
	/* overflow-x: scroll ;
	overflow-y: hidden; */

}

ul{
	
	display: flex;
	/* flex-direction: row; */
	background-color: rgba(0, 128, 0, 0.455);
	overflow-x: auto;
	/* overflow-y: hidden; */
	scroll-snap-type: inline proximity;
	scroll-behavior: smooth;
}

li{
	position: relative;
	display: flex;
	flex: 0 0 100vw;
	width: 100vw;
	height: 100vh;
	outline: solid blue;
	scroll-snap-align: center;
	scroll-snap-stop:always;
	
	margin-inline: 2.5px;
	scroll-margin-inline: 2.5px;
	align-items: center;
    justify-content: center;
    font-size: 3rem;
}

li:nth-of-type(1){--color:rgba(255, 0, 0, 0.532); background-color:var(--color);color: var(--color);}
li:nth-of-type(2){--color:rgba(255, 255, 0, 0.508); background-color:var(--color);color: var(--color);}
li:nth-of-type(3){--color:rgba(255, 166, 0, 0.485); background-color:var(--color);color: var(--color);}
li:nth-of-type(4){--color:rgba(245, 245, 220, 0.445); background-color:var(--color);color: var(--color);}

li a{
	width: 100%;
	height:100%;
	/* background-color: whitesmoke ; */
	scroll-behavior: smooth;

}
</style>