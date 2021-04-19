<script>
    // Dependecies
    import Router from "svelte-spa-router";

    // Pages
    import SignIn from './pages/SignIn.svelte'
	import SignUp from './pages/SignUp.svelte'

    const routes = {
        "/signin": SignIn,
        "/signup": SignUp
    };
</script>

<Router {routes} />
