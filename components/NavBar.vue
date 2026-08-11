<template>
  <nav class="navbar navbar-expand-md navbar-dark bg-dark" aria-label="Primary navigation">
    <div class="container-fluid">
      <NuxtLink class="navbar-brand fw-semibold" to="/">Derek Chisholm</NuxtLink>

      <button
        class="navbar-toggler"
        type="button"
        data-bs-toggle="collapse"
        data-bs-target="#primaryNav"
        aria-controls="primaryNav"
        aria-expanded="false"
        aria-label="Toggle navigation"
      >
        <span class="navbar-toggler-icon"></span>
      </button>

      <div id="primaryNav" class="collapse navbar-collapse">
        <ul class="navbar-nav me-auto mb-2 mb-md-0">
          <li class="nav-item">
            <NuxtLink class="nav-link" to="/">Home</NuxtLink>
          </li>
          <li class="nav-item">
            <NuxtLink class="nav-link" to="/peak-derek">Operating Principles</NuxtLink>
          </li>
          <li class="nav-item">
            <a class="nav-link" href="https://github.com/dchisholm125" target="_blank" rel="noreferrer">GitHub</a>
          </li>
          <li class="nav-item">
            <a class="nav-link" href="https://www.linkedin.com/in/dchisholm125/" target="_blank" rel="noreferrer">LinkedIn</a>
          </li>
        </ul>
      </div>
    </div>
  </nav>
</template>
