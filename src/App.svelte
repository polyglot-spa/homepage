<script>
    import CreditModal from "./components/credit-modal.svelte";
    let isOpen = false;

    let singleSpaSVGSrc = "http://localhost:5001/assets/images/single-spa-mark-magenta.svg";
    let vueLogoSrc = "http://localhost:5001/assets/images/vue-logo.png";
    let angularLogoSrc = "http://localhost:5001/assets/images/angular-logo.svg";
    let reactLogoSrc = "http://localhost:5001/assets/images/React-icon.svg";
    let svelteLogoSrc = "http://localhost:5001/assets/images/svelte-logo-horizontal.svg";
    let bootstrapLogoSrc = "http://localhost:5001/assets/images/Bootstrap_logo.svg";
</script>

<style>
    .bd-placeholder-img {
        font-size: 1.125rem;
        text-anchor: middle;
        -webkit-user-select: none;
        -moz-user-select: none;
        user-select: none;
    }

    @media (min-width: 768px) {
        .bd-placeholder-img-lg {
            font-size: 3.5rem;
        }
    }


    /* CUSTOMIZE THE CAROUSEL
    -------------------------------------------------- */

    /* Carousel base class */
    .carousel {
        margin-bottom: 4rem;
    }
    /* Since positioning the image, we need to help out the caption */
    .carousel-caption {
        bottom: 3rem;
        z-index: 10;
    }

    /* Declare heights because of positioning of img element */
    .carousel-item {
        height: 24rem;
    }
    .carousel-item > img {
        position: absolute;
        top: 0;
        left: 0;
        min-width: 100%;
        height: 32rem;
    }


    /* MARKETING CONTENT
    -------------------------------------------------- */

    /* Center align the text within the three columns below the carousel */
    .marketing .col-lg-4 {
        margin-bottom: 1.5rem;
        text-align: center;
    }
    .marketing h2 {
        font-weight: 400;
    }
    /* rtl:begin:ignore */
    .marketing .col-lg-4 p {
        margin-right: .75rem;
        margin-left: .75rem;
    }
    /* rtl:end:ignore */


    /* Featurettes
    ------------------------- */

    .featurette-divider {
        margin: 5rem 0; /* Space out the Bootstrap <hr> more */
    }

    .featurette-divider:last-of-type {
        margin: 5rem 0 1rem;
    }

    /* Thin out the marketing headings */
    .featurette-heading {
        font-weight: 300;
        line-height: 1;
        /* rtl:remove */
        letter-spacing: -.05rem;
    }


    /* RESPONSIVE CSS
    -------------------------------------------------- */

    @media (min-width: 40em) {
        /* Bump up size of carousel content */
        .carousel-caption p {
            margin-bottom: 1.25rem;
            font-size: 1.25rem;
            line-height: 1.4;
        }

        .featurette-heading {
            font-size: 50px;
        }
    }

    @media (min-width: 62em) {
        .featurette-heading {
            margin-top: 7rem;
        }
    }
    #single-spa-svg {
        width: 30px;
    }
    #svelte-logo {
        width: 180px;
    }
    #bootstrap-logo {
        width: 50px;
    }

</style>
   <CreditModal bind:isOpen={isOpen}></CreditModal>
    <div id="myCarousel" class="carousel slide" data-bs-ride="carousel">
        <div class="carousel-indicators">
            <button type="button" data-bs-target="#myCarousel" data-bs-slide-to="0" class="active" aria-current="true" aria-label="Slide 1"></button>
            <button type="button" data-bs-target="#myCarousel" data-bs-slide-to="1" aria-label="Slide 2"></button>
            <button type="button" data-bs-target="#myCarousel" data-bs-slide-to="2" aria-label="Slide 3"></button>
        </div>
        <div class="carousel-inner">
            <div class="carousel-item active">
                <svg class="bd-placeholder-img" width="100%" height="100%" xmlns="http://www.w3.org/2000/svg" aria-hidden="true" preserveAspectRatio="xMidYMid slice" focusable="false"><rect width="100%" height="100%" fill="#777"/></svg>

                <div class="container">
                    <div class="carousel-caption text-start">
                        <h1>single-spa <img id="single-spa-svg" src={singleSpaSVGSrc}/> </h1>
                        <p>A javascript router for front-end microservices.</p>
                        <p><a class="btn btn-lg btn-primary" href="https://single-spa.js.org/" target="_blank" rel="noopener noreferrer">Learn More</a></p>
                    </div>
                </div>
            </div>
            <div class="carousel-item">
                <svg class="bd-placeholder-img" width="100%" height="100%" xmlns="http://www.w3.org/2000/svg" aria-hidden="true" preserveAspectRatio="xMidYMid slice" focusable="false"><rect width="100%" height="100%" fill="#777"/></svg>

                <div class="container">
                    <div class="carousel-caption">
                        <h1>Web Components</h1>
                        <p>Web components are a set of web platform APIs that allow you to create new custom, reusable, encapsulated HTML tags to use in web pages and web apps.</p>
                        <p><a class="btn btn-lg btn-primary" href="https://www.webcomponents.org/" target="_blank" rel="noopener noreferrer">Learn more</a></p>
                    </div>
                </div>
            </div>
            <div class="carousel-item">
                <svg class="bd-placeholder-img" width="100%" height="100%" xmlns="http://www.w3.org/2000/svg" aria-hidden="true" preserveAspectRatio="xMidYMid slice" focusable="false"><rect width="100%" height="100%" fill="#777"/></svg>

                <div class="container">
                    <div class="carousel-caption text-end">
                        <h1>Javascript Frameworks</h1>
                        <p>JavaScript frameworks are application frameworks written in JavaScript where programmers can manipulate the functions and use them for their convenience.</p>
                        <p><button class="btn btn-lg btn-primary" on:click={()=> (isOpen = true)}>Credits</button></p>
                    </div>
                </div>
            </div>
        </div>
        <button class="carousel-control-prev" type="button" data-bs-target="#myCarousel" data-bs-slide="prev">
            <span class="carousel-control-prev-icon" aria-hidden="true"></span>
            <span class="visually-hidden">Previous</span>
        </button>
        <button class="carousel-control-next" type="button" data-bs-target="#myCarousel" data-bs-slide="next">
            <span class="carousel-control-next-icon" aria-hidden="true"></span>
            <span class="visually-hidden">Next</span>
        </button>
    </div>


    <!-- Marketing messaging and featurettes
    ================================================== -->
    <!-- Wrap the rest of the page in another container to center all the content. -->

    <div class="container marketing">
        <div class="d-flex mb-3">
            <h1 class="mx-auto">The Featured Players</h1>
        </div>
        <!-- Three columns of text below the carousel -->
        <div class="row">
            <div class="col-lg-4">
                <svg class="bd-placeholder-img rounded-circle" width="140" height="140" xmlns="http://www.w3.org/2000/svg" role="img" aria-label="Placeholder: 140x140" preserveAspectRatio="xMidYMid slice" focusable="false"><title>Placeholder</title><rect width="100%" height="100%" fill="#777"/><text x="50%" y="50%" fill="#777" dy=".3em">140x140</text>
                    <image class="w-75" x="12.5%" y="13%" xlink:href={ angularLogoSrc }/>
                </svg>

                <h2 class="mt-1">Angular</h2>
                <p>The modern web developer's platform</p>
                <p><a class="btn btn-secondary" href="https://angular.io/" target="_blank" rel="noopener noreferrer">View documentation &raquo;</a></p>
            </div><!-- /.col-lg-4 -->
            <div class="col-lg-4">
                <svg class="bd-placeholder-img rounded-circle" width="140" height="140" xmlns="http://www.w3.org/2000/svg" role="img" aria-label="Placeholder: 140x140" preserveAspectRatio="xMidYMid slice" focusable="false"><title>Placeholder</title><rect width="100%" height="100%" fill="#777"/><text x="50%" y="50%" fill="#777" dy=".3em">140x140</text>
                    <image class="w-100" y="15%" xlink:href={ reactLogoSrc }/>
                </svg>

                <h2 class="mt-1">React</h2>
                <p>A JavaScript library for building user interfaces</p>
                <p><a class="btn btn-secondary" href="https://reactjs.org/" target="_blank" rel="noopener noreferrer">View documentation &raquo;</a></p>
            </div><!-- /.col-lg-4 -->
            <div class="col-lg-4">
                <svg class="bd-placeholder-img rounded-circle" width="140" height="140" xmlns="http://www.w3.org/2000/svg" role="img" aria-label="Placeholder: 140x140" preserveAspectRatio="xMidYMid slice" focusable="false"><title>Placeholder</title><rect width="100%" height="100%" fill="#777"/><text x="50%" y="50%" fill="#777" dy=".3em">140x140</text>
                    <image class="w-75" x="12.5%" y="17.5%" xlink:href={ vueLogoSrc }/>
                </svg>

                <h2 class="mt-1">Vue.js</h2>
                <p>The Progressive JavaScript Framework</p>
                <p><a class="btn btn-secondary" href="https://v3.vuejs.org/" target="_blank" rel="noopener noreferrer">View documentation &raquo;</a></p>
            </div><!-- /.col-lg-4 -->

        </div><!-- /.row -->


        <!-- START THE FEATURETTES -->

        <hr class="featurette-divider">
        <div class="d-flex mb-3">
            <h1 class="mx-auto">The Supporting Cast</h1>
        </div>

        <div class="row featurette">
            <div class="col-md-7">
                <h2 class="featurette-heading"><img id="svelte-logo"src={svelteLogoSrc}/> <span class="text-muted">Cybernetically enhanced web apps</span></h2>
                <p class="lead mt-2">Svelte is a radical new approach to building user interfaces. Whereas traditional frameworks like React and Vue do the bulk of their work in the browser, Svelte shifts that work into a compile step that happens when you build your app.</p>
            </div>
            <div class="col-md-5 position-relative">
                <p><a style="width: 230px;" class="btn btn-lg btn-primary position-absolute top-50 start-50 translate-middle mt-4" href="https://svelte.dev/" target="_blank" rel="noopener noreferrer">View Documentation</a></p>
            </div>
        </div>

        <hr class="featurette-divider">

        <div class="row featurette">
            <div class="col-md-7 order-md-2">
                <h2 class="featurette-heading"> <img id="bootstrap-logo" src={bootstrapLogoSrc}/> Bootstrap v5.x.x <span class="text-muted">Build fast, responsive sites with Bootstrap</span></h2>
                <p class="lead mt-2">Quickly design and customize responsive mobile-first sites with Bootstrap, the world’s most popular front-end open source toolkit, featuring Sass variables and mixins, responsive grid system, extensive prebuilt components, and powerful JavaScript plugins.</p>
            </div>
            <div class="col-md-5 order-md-1 position-relative">
                <p><a style="width: 230px;" class="btn btn-lg btn-primary position-absolute top-50 start-50 translate-middle mt-4" href="https://getbootstrap.com/" target="_blank" rel="noopener noreferrer">View Documentation</a></p>

            </div>
        </div>

        <hr class="featurette-divider">
        <div class="d-flex mb-3">
            <h1 class="mx-auto">And as Custom Element</h1>
        </div>
        <div class="row featurette">
            <div class="col-md-7">
                <h2 class="featurette-heading">chessboard-element <span class="text-muted">A &lt;chess-board&gt; element for your web pages</span></h2>
                <p class="lead mt-2">
                    The purpose of this application was to gain experience using custom elements within an Angular, React or Vue library/framework.
                    Therefore, it is only possible to play as white, though you can change the board orientation, and the moves made by the application are <a href="https://github.com/jhlywa/chess.js" target="_blank" rel="noopener noreferrer">random</a>.
                    If you would like to play another game refresh the page. More functionality will be added in the future.
                    Custom elements' compatibility with different libraries/frameworks can be viewed
                    <a href="https://custom-elements-everywhere.com/" target="_blank" rel="noopener noreferrer">here</a>.
                </p>
            </div>
            <div class="col-md-5 position-relative">
                <p><a style="width: 230px;" class="btn btn-lg btn-primary position-absolute top-50 start-50 translate-middle mt-4" href="https://justinfagnani.github.io/chessboard-element/" target="_blank" rel="noopener noreferrer">View Documentation</a></p>

            </div>
        </div>

        <hr class="featurette-divider">

        <!-- /END THE FEATURETTES -->

    </div><!-- /.container -->
