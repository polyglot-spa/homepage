<script>
    import Modal from "sv-bootstrap-modal";
    export let isOpen;
</script>



<style>
    .modal-title {
        font-family: Bananas-Personal;
        font-size: 60px;
    }
</style>


<Modal bind:open={isOpen} dialogClasses="modal-dialog-centered">
    <div class="modal-header">
        <h5 class="modal-title">Credits</h5>
        <button type="button" class="close" on:click={() => (isOpen = false)}>
            <span aria-hidden="true">&times;</span>
        </button>
    </div>
    <div class="modal-body">
        <div class="mb-2">
            <h2>single-spa</h2>
            <span>It provides a layout engine. The layout engine is responsible for creating, destroying, and rearranging dom elements during route transitions.</span>
        </div>
        <div class="mb-2">
            <h2>Bootstrap</h2>
            <span>It provides css transitions and tools to aid in the stying elements.</span>
        </div>
        <div class="mb-2">
            <h2>Vue</h2>
            <span>It is used in a microfrontend that is active when the route equals 'vue-chess'.</span>
        </div>
        <div class="mb-2">
            <h2>React</h2>
            <span>It is used in a microfrontend that is active when the route equals 'react-chess'.</span>
        </div>
        <div class="mb-2">
            <h2>Angular</h2>
            <span>It is used in a microfrontend that is active when the route equals 'angular-chess'.</span>
        </div>
        <div class="mb-2">
            <h2>Svelte</h2>
            <span>It is used in multiple microfrontends and is active in the navbar, footer and homepage.</span>
        </div>
        <div class="mb-2">
            <h2>chessboard-element</h2>
            <span>It is the custom element that is at the center of the Vue, React and Angular microfrontends.</span>
        </div>
    </div>
    <div class="modal-footer">
        <button type="button" class="btn btn-secondary" on:click={() => (isOpen = false)}>Close</button>
    </div>
</Modal>