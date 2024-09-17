<script>
	/** @type {import('./$types').PageData} */
	// import gsap from "gsap";
	// import LocomotiveScroll from 'locomotive-scroll';
	// import '../styles/main.css';
	export let data;
	let people = data.people
	export let peep = people? people.find(person => person.id == 40) : 'not found';

	console.log(peep);
	

	// console.log('lol',Peep);
	
	
	

	// const locomotiveScroll = new LocomotiveScroll();
</script>

<svelte:head>
	<title>welcome to your-tribe-for-life-profile-card</title>
	<link rel="preload" href="https://brilletjes-squad-page.onrender.com" as="document">
	<link rel="preload" href="https://book-of-potions.onrender.com" as="document">
</svelte:head>

<main>
	<section id="cover-1" class="covers" tabindex="0">
		<a href="#cover-2" class="frame">
			<div class="pics-container">
				<!-- <span class="profile profile-1">
					<img  src="{peep.avatar}" alt="">
				</span> -->
				<span class="profile profile-2 flower" >
					<img src="/25acb22a-22a3-41d5-a0eb-c91529c4c6c8.jpg" width=300 alt="image of {peep.name}">
					<!-- <img src="https://portfolio-lti-production.s3.eu-west-1.amazonaws.com/cvq44juv5nrywjfbnlgdrwaweabo?response-content-disposition=inline%3B%20filename%3D%226992026a-4ec4-4399-a36a-c18411945cb2.JPG%22%3B%20filename%2A%3DUTF-8%27%276992026a-4ec4-4399-a36a-c18411945cb2.JPG&response-content-type=image%2Fjpeg&X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIAZUHNSBLFH5JMYGQV%2F20240915%2Feu-west-1%2Fs3%2Faws4_request&X-Amz-Date=20240915T210806Z&X-Amz-Expires=43200&X-Amz-SignedHeaders=host&X-Amz-Signature=131003c97f68d35b7ea57099e9da85018ae1decef2bad55b4a8a12c7fc12e219" width=300 alt="image of {peep.name}"> -->
				</span>

			</div>
			
			<h1 class="name">{peep.name} {peep.surname}</h1>
		</a>
	</section>
	<section id="cover-2" class="covers " tabindex="0">
		<a href="#cover-3" class="frame">
			<div class="side-info scalloped-box">
				<ul>
					<li> squad-id {peep.squad_id}</li>
					<li> role {peep.role}</li>
					<li> hobbies {peep.bio}</li>
					<li> and more </li>
				</ul>
			</div>
			<div class="bio">
				<p>	bio {peep.bio}</p>
				<p>
					Lorem ipsum dolor sit amet consectetur adipisicing elit. Vitae rem vero nobis perferendis, quas id! Debitis nostrum, delectus culpa voluptates veritatis voluptatibus earum ratione dignissimos id magni, inventore molestiae ducimus.
					Lorem ipsum dolor sit amet consectetur adipisicing elit. Vitae rem vero nobis perferendis, quas id! Debitis nostrum, delectus culpa voluptates veritatis voluptatibus earum ratione dignissimos id magni, inventore molestiae ducimus.
				</p>
			</div>
			<div class="side-pic">
				<img src="/IMG_8452.JPEG" alt="{peep.name}">
			</div>
			<!-- <div class="about-shape scalloped-box">

			</div> -->
		</a>
	</section>
	<section id="cover-3" class="covers frame" tabindex="0">
		
			<section class="mainG">
				<article class="top top_1">
					<iframe src="https://book-of-potions.onrender.com/brew" frameborder="0" tabindex="-1"></iframe>
				</article>  
				<article class="top top_2">2</article>
				<article class="top top_3">3</article>
					
				<article class="mid mid_1">4</article>  
				<article class="mid mid_2">
					<a href="#cover-5" class="frame stamp box" style="color: transparent;">
						next
					</a>

					
				</article>
				<article class="mid mid_3">6</article>
					
				<article class="down down_1">
					<a href="https://github.com/christoph3r3w">
						<img src="/GitHub_Logo.png" alt="github logo" width="300">
					</a>
				</article>  
				<article class="down down_2">
					<iframe height="300" style="width: 100%;" scrolling="no" title="Untitled" src="https://codepen.io/Christopher-the-animator/embed/NWmxrpY?default-tab=" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true" tabindex="-1">
						See the Pen <a href="https://codepen.io/Christopher-the-animator/pen/NWmxrpY">
						Untitled</a> by Christopher (<a href="https://codepen.io/Christopher-the-animator">@Christopher-the-animator</a>)
						
					  </iframe>				
				</article>
				<article class="down down_3">
					<iframe src="https://brilletjes-squad-page.onrender.com" tabindex="-1"></iframe>
				</article>
			</section> 
		
	</section>
	<!-- <section id="cover-4" class="covers" tabindex="0">
		<a href="#cover-5" class="frame">4</a>
	</section> -->
	<section id="cover-5" class="covers" tabindex="0">
		<a href="#cover-1" class="frame">
			
			<ul>
				<li>insta</li>
				<li>github</li>
				<li>linkedin</li>
				<li>arena</li>
			</ul>
		</a>
	</section>
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