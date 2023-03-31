<script>
	import Router from 'svelte-spa-router';
  import Footer from './component/footer.svelte';
  import Guides from './component/guidesCompo.svelte';
  import Modal from './component/modal.svelte';
  import Navbarb from './component/navbarb.svelte';
  import Blogs from './Pages/blogs.svelte';
  import Index from './Pages/index.svelte';
  import NotFound from './Pages/NotFound.svelte';
  import User from './Pages/USERS/user.svelte';
  import { onMount } from 'svelte';
	let routes= {
		'/': Index,
		'/guide': Guides,
		'/blogs':Blogs,
		"/user":User,
		'/*': NotFound
	};
	function openModal() {
    const modal = document.querySelector('#myModal');
    const modalInstance = new bootstrap.Modal(modal);
    modalInstance.show();
  }
 
//   onMount(() => {
//     openModal();
//   });
</script>

<main class="container-fluid">

	<div class="conatiner">

		<div class="row">
            <div class="col-lg-8  mx-auto">
				<div >
					<Navbarb/>
					
				<Router routes={routes} />

				<div>
					<Footer/>
				   </div>

			</div>
		</div>

	</div>

</main>


