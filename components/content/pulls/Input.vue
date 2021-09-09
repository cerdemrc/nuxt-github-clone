<template>
  <div class="pulls-top-cage">
    <div class="pulls-top-cage-filter">
      <ul>
        <li><a href="#">Created</a></li>
        <li><a href="#">Assigned</a></li>
        <li><a href="#">Mentioned</a></li>
        <li><a href="#">Review requests</a></li>
      </ul>
    </div>
    <div class="pulls-top-cage-input">
      <div class="pulls-top-cage-input-icon">
        <svg
          aria-hidden="true"
          height="16"
          viewBox="0 0 16 16"
          version="1.1"
          width="16"
          fill="#8b949e"
          data-view-component="true"
          class="octicon octicon-search subnav-search-icon"
        >
          <path
            fill-rule="evenodd"
            d="M11.5 7a4.499 4.499 0 11-8.998 0A4.499 4.499 0 0111.5 7zm-.82 4.74a6 6 0 111.06-1.06l3.04 3.04a.75.75 0 11-1.06 1.06l-3.04-3.04z"
          ></path>
        </svg>
      </div>
      <input
        type="text"
        placeholder="is:open is:pr author:cerdemrc archived:false "
      />
    </div>
  </div>
</template>