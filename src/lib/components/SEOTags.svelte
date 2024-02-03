<script lang="ts">
  import { HOST } from "$env/static/private";
  import
</script>

<!-- TODO: dynamic meta -->
<svelte:head>
  <meta name="description" content={m.description()} />

  <meta property="og:title" content={m.name()} />
  <meta property="og:description" content={m.description()} />
  <meta property="og:type" content="website" />
  <meta property="og:url" content={$page.url.href.split(/[?#]/)[0]} />
  <meta property="og:image" content="{$page.url.protocol}//{$page.url.host}{base}/thumbnail.png" />
  <meta property="og:image:type" content="image/png" />
  <meta property="og:image:width" content="1280" />
  <meta property="og:image:height" content="720" />

  <meta property="og:locale" content={languageTag()} />
  {#each availableLanguageTags as tag}
    {#if tag != languageTag()}
      <meta property="og:locale:alternative" content={tag} />
    {/if}
  {/each}

  <meta name="twitter:card" content="summary_large_image" />
  <meta name="twitter:site" content="@tnfshcec" />
</svelte:head>
