<script>
	import Router from 'svelte-spa-router';
  import Footer from './component/footer.svelte';
  import Guides from './component/guidesCompo.svelte';
  import Navbarb from './component/navbarb.svelte';
  import Blogs from './Pages/blogs.svelte';
  import Index from './Pages/index.svelte';
  import NotFound from './Pages/NotFound.svelte';
	let routes= {
		'/': Index,
		'/guide': Guides,
		'/blogs':Blogs,
		'/*': NotFound
	};
</script>

<main class="container-fluid">

	<div class="conatiner">

		<div class="row">
            <div class="col-lg-8  mx-auto">
				<div >
					<Navbarb/>
				   </div>
				<Router routes={routes} />

				<div>
					<Footer/>
				   </div>

			</div>
		</div>

	</div>

</main>


