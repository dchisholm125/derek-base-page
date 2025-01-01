<script setup lang="ts">
// import all assets before passing them to underlying components
import drumkit from '~/assets/img/preview.png'
import thistledownRecoveryHome from '~/assets/img/thistledown-preview.png'

type CarouselCard = {
    imgSrc: typeof drumkit,
    title: string,
    contentText: string,
    btnLink: string, 
    btnText: string,
}

const cards: CarouselCard[] = [
    {
        imgSrc: drumkit,
        title: 'some title',
        contentText: 'some content',
        btnLink: '#', 
        btnText: 'some btn text',
    },
    {
        imgSrc: drumkit,
        title: 'Thistledown Recovery Home',
        contentText: 'A new website made from scratch with Vue.JS ( using the Nuxt framework) and Bootstrap CSS. The full build involved redirecting a Wix.com domain (thistledownrecovery.com), hosting a new website via GoDaddy.com (thistledownrecoveryhome.com), and leveraging Netlify.com for CI/CD.',
        btnLink: 'https://derekchisholm.com/Thistledown/', 
        btnText: 'View Webpage',
    }
]

const mounted = ref(false)

const carouselEl = ref()

const carouselWidth = computed(() => {
    if(mounted.value) {
        return carouselEl.value.offsetWidth
    }
})

const numOfCards = 9

function scroll(multiplier: number) {
    carouselEl.value.scrollLeft += multiplier * (carouselWidth.value / (numOfCards-1))
}

onMounted(() => {
    mounted.value = true
})
</script>

<template>
    <div class="d-flex flex-column">
    <div class="d-flex border border-solid" style="height: 40px">
        <small class="col-2 border text-center text-success">^ ^ ^ Name is a WIP</small>
        <small class="col-10"></small>
    </div>

    <main>
        <div class="container-fluid d-flex flex-column justify-content-center align-items-center bg-secondary py-5">
            <div class="d-flex flex-column align-items-center justify-content-center text-center">
                <h1>Personal Projects</h1>
                <h3>size of ref = {{ carouselWidth / numOfCards }}</h3>
            </div>
            <div class="d-flex align-items-center">
                <img src="~/assets/img/left-chevron.svg" class="scale-up" height="150" width="150" @click="scroll(-1)">
                <div class="p-3 light-bg rounded">
                    <div ref="carouselEl" class="d-flex overflow-hidden" style="width: 85vw; scroll-behavior: smooth;">
                        <div v-for="card in cards" class="col-2 mx-3">
                            <CarouselCard 
                                :imgSrc="card.imgSrc" 
                                :title="card.title" 
                                :contentText="card.contentText" 
                                :btnLink="card.btnLink" 
                                :btnText="card.btnText" 
                                    />

                        </div>
                    </div>
                </div>
                <img src="~/assets/img/right-chevron.svg" class="scale-up" height="150" width="150" @click="scroll(1)">
            </div>
            <CalloutUp class="my-1" text="Derek's semi-custom Bootstrap-y carousel thing" style="scale: 0.8;"/>
        </div>

    <section class="py-5 text-center container">
    <div class="row py-lg-5">
        <div class="col-lg-6 col-md-8 mx-auto">
        <h1 class="fw-light"><b>Derek Chisholm - Full Stack Engineer</b></h1>
        <h2 class="fw-light">Coder. Project Manager. Problem Solver.</h2>
        <p class="lead text-body-secondary">Started Construction on 9/20/2023 using Bootstrap styling, this is a work-in-progress.</p>
            <p>
            <a href="./philosophy-blog/index.html" class="btn btn-primary my-2">My Blog</a>
            <a href="https://www.linkedin.com/in/dchisholm125/" class="btn btn-secondary my-2" target="_blank">My LinkedIn</a>
            <a href="https://github.com/dchisholm125" class="btn btn-secondary my-2 pb-2" id="github" target="_blank">
                <img src="./assets/images/github-mark-white.png" height="20"></img>
                <img src="./assets/images/GitHub_Logo_White.png" height="20"></img>
            </a>
            <a href="../full-stack-portfolio/public/contact.html" class="btn btn-tertiary my-2 border-black fw-bold">Contact Me</a>
            </p>
        </div>
    </div>
    </section>

    <div class="px-4 pt-5 text-center border-bottom bg-light">
    <img src="./assets/images/dude-at-computer.png" class="mb-" alt="coding" height="75">
    <h1 class="display-4 fw-bold text-body-emphasis">Front-End Feature Samples</h1>
    <div class="col-lg-6 mx-auto">
        <p class="lead mb-4">For the sake of demonstrating some common UI elements, I've included a page 
        dedicated to specifically showcasing my ability to create them.
        </p>
        <a href="./ui-features/index.html" class="btn btn-primary my-2 mb-4">Check them out!</a>
    </div>
    </div>

    <div class="px-4 pt-5 text-center border-bottom bg-light">
    <img src="./assets/images/web-programming.png" class="mb-4" alt="coding" height="75">
    <h1 class="display-4 fw-bold text-body-emphasis">My Projects</h1>
    <div class="col-lg-6 mx-auto">
        <p class="lead mb-4">The below are built leveraging the M.E.R.N. stack
        (MongoDB, Express.JS, React.JS, Node.JS) or vanilla HTML/CSS/JavaScript.
        </p>
    </div>
    </div>

    <div class="album py-5 bg-body-tertiary">
    <div class="container">

        <div class="row row-cols-1 row-cols-sm-2 row-cols-md-3 g-3">
            <div class="col">
                <div class="card shadow-sm">
                <img src="./assets/images/resume-preview.png" max-height="250">
                <div class="card-body">
                    <p class="card-text"><b>Derek's Online Resume</b><hr>This is my print resume in HTML/CSS form.</p>
                    <div class="d-flex justify-content-between align-items-center">
                    <div class="btn-group">
                        <a href="https://dchisholm125.github.io/resume/" class="btn btn-outline-primary" tabindex="-1" role="button" aria-disabled="true">View</a>
                    </div>
                    <small class="text-body-secondary">9/20/2023</small>
                    </div>
                </div>
                </div>
            </div>

        <div class="col">
            <div class="card shadow-sm">
            <img src="./assets/images/tindog.png" max-height="250">
            <div class="card-body">
                <p class="card-text"><b>TinDog Website Design</b><hr>A fake app for dogs to meet other dogs. This is a small project made using Bootstrap open-source.</p>
                <div class="d-flex justify-content-between align-items-center">
                <div class="btn-group">
                    <a href="./tindog/index.html" class="btn btn-outline-primary" tabindex="-1" role="button" aria-disabled="true">View</a>
                </div>
                <small class="text-body-secondary">9/25/2023</small>
                </div>
            </div>
            </div>
        </div>

        <div class="col">
            <div class="card shadow-sm">
            <img src="./drum-kit/images/preview.PNG" max-height="250">
            <div class="card-body">
                <p class="card-text"><b>Drum Kit</b><hr>Use your mouse or a-s-w-d-j-k-l keys to make sounds!</p>
                <div class="d-flex justify-content-between align-items-center">
                <div class="btn-group">
                    <a href="./drum-kit/index.html" class="btn btn-outline-primary" tabindex="-1" role="button" aria-disabled="true">View</a>
                </div>
                <small class="text-body-secondary">9/27/2023</small>
                </div>
            </div>
            </div>
        </div>

        <div class="col">
            <div class="card shadow-sm">
            <img src="./assets/images/greesnpace-preview.png" max-height="250">
            <div class="card-body">
                <p class="card-text"><b>GreenSpace Social Media Platform Design</b><hr>A space for scientist to discover, share, and collborate at a professional level. I am using plain HTML and CSS for styling, but may integrate Bootstrap.</p>
                <div class="d-flex justify-content-between align-items-center">
                <div class="btn-group">
                    <a href="https://dchisholm125.github.io/greenspace/" class="btn btn-outline-primary" tabindex="-1" role="button" aria-disabled="true">View</a>
                </div>
                <small class="text-body-secondary"> started 9/27/2023</small>
                </div>
            </div>
            </div>
        </div>

        <div class="col">
            <div class="card shadow-sm">
            <img src="./assets/images/dice-preview.png" max-height="250">
            <div class="card-body">
                <p class="card-text"><b>1-vs-1 Dice Game</b><hr>A quick webpage showcasing external HTML/CSS/JS files. Great for resolving debates between friends, just roll the dice and see who gets the higher number!</p>
                <div class="d-flex justify-content-between align-items-center">
                <div class="btn-group">
                    <a href="./dice/index.html" class="btn btn-outline-primary" tabindex="-1" role="button" aria-disabled="true">View</a>
                </div>
                <small class="text-body-secondary">9/27/2023</small>
                </div>
            </div>
            </div>
        </div>
        <div class="col">
            <div class="card shadow-sm">
            <img src="./assets/images/mondrian-preview.png" max-height="250">
            <div class="card-body">
                <p class="card-text"><b>Mondrian Painting Project</b><hr>A fun project showcasing the use of flex + grid CSS styling.</p>
                <div class="d-flex justify-content-between align-items-center">
                <div class="btn-group">
                    <a href="./public/mondrian-painting.html" class="btn btn-outline-primary" tabindex="-1" role="button" aria-disabled="true">View</a>
                </div>
                <small class="text-body-secondary">9/21/2023</small>
                </div>
            </div>
            </div>
        </div>

        </div>
    </div>
    </div>

</main>
</div>
</template>

<style scoped>
@keyframes scaleUp {
    0% {
        scale: 1;
    }
    100% {
        scale: 1.2
    }
}

.light-bg {
    background-color: #ffffff09;
}

img.scale-up:hover {
   animation: 0.3s ease-in-out scaleUp;
   scale: 1.2;
}

.callout-font {
    font-family: 'Courier New', Courier, monospace
}
</style>