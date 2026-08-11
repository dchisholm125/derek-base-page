<script setup lang="ts">
const functions = [
  {
    title: 'Mental performance',
    text: 'Protect clarity, confidence, resilience, and sound judgment so ambitious work remains sustainable.'
  },
  {
    title: 'Career',
    text: 'Choose work that compounds technical capability, ownership, leadership, compensation, and future optionality.'
  },
  {
    title: 'Family',
    text: 'Treat presence, stability, connection, and shared experiences as core outcomes rather than side effects.'
  },
  {
    title: 'Health & energy',
    text: 'Build around sleep, movement, recovery, and sustainable energy instead of relying on short bursts of intensity.'
  },
  {
    title: 'Finance',
    text: 'Use money to create resilience and choices: protect liquidity, remove fragile debt, build reserves, and invest consistently.'
  },
  {
    title: 'Life & adventure',
    text: 'Keep room for skiing, golf, hiking, travel, outdoors, friends, curiosity, and fun while the bigger plan is being built.'
  },
  {
    title: 'Long-term dreams',
    text: 'Pursue ambitious projects and lifestyle goals from a strong foundation so success expands life instead of constraining it.'
  }
]
</script>

<template>
  <main>
    <section class="py-5 bg-dark text-light">
      <div class="container py-4">
        <p class="text-uppercase small mb-2 opacity-75">Personal operating system</p>
        <h1 class="display-4 fw-bold">Peak Derek</h1>
        <p class="lead col-lg-8 mb-0">
          Build a life that compounds capability, strong relationships, meaningful work, resilience, and genuine enjoyment.
          No single metric wins at the expense of the whole system.
        </p>
      </div>
    </section>

    <section class="py-5">
      <div class="container">
        <div class="row g-4">
          <div v-for="item in functions" :key="item.title" class="col-12 col-md-6 col-lg-4">
            <article class="card h-100 shadow-sm border-0">
              <div class="card-body p-4">
                <h2 class="h4">{{ item.title }}</h2>
                <p class="mb-0 text-body-secondary">{{ item.text }}</p>
              </div>
            </article>
          </div>
        </div>
      </div>
    </section>

    <section class="py-5 bg-body-tertiary border-top border-bottom">
      <div class="container">
        <div class="row g-5">
          <div class="col-lg-6">
            <h2 class="h3">Operating sequence</h2>
            <ol class="lead ps-4">
              <li class="mb-2">Protect the floor during uncertainty.</li>
              <li class="mb-2">Increase capability and reliable income.</li>
              <li class="mb-2">Remove fragile, expensive debt.</li>
              <li class="mb-2">Build meaningful reserves and resilience.</li>
              <li class="mb-2">Automate investing and quality of life.</li>
              <li>Fund major optional dreams from strength.</li>
            </ol>
          </div>
          <div class="col-lg-6">
            <h2 class="h3">Decision rules</h2>
            <ul class="lead ps-4">
              <li class="mb-2">Optimize the whole life, not one dashboard metric.</li>
              <li class="mb-2">Prefer optionality over fragile leverage.</li>
              <li class="mb-2">Separate facts from fear before irreversible decisions.</li>
              <li class="mb-2">Consistency beats unsustainable intensity.</li>
              <li>Quality of life belongs in the plan now.</li>
            </ul>
          </div>
        </div>
      </div>
    </section>

    <section class="py-5">
      <div class="container text-center col-lg-8">
        <h2 class="h3">Weekly question</h2>
        <p class="display-6 fw-semibold mb-3">What is the biggest constraint preventing the next version of me?</p>
        <p class="text-body-secondary mb-0">
          Identify it, make it the operating priority, and keep the rest of the system stable enough to support the work.
        </p>
      </div>
    </section>
  </main>
</template>
