<script lang="ts">
  import { base } from "$app/paths";
  import Credits from "./Credits.svelte";
  import MarkdownRenderer from "./MarkdownRenderer.svelte";

  export let explore2: string | null;
  export let sonification: string | null;
  export let links: boolean = false;
</script>

{#if explore2}
  <MarkdownRenderer markdown={explore2} />
{/if}

{#if links}
  <p>
    Pour en savoir plus: <a href="{base}/narratifs"
      >les quatre visions contrastées du futur issues d'<b>Explore2</b>
    </a>
  </p>
  <p>
    Pour télécharger les données hydrologiques issues d'<b>Explore2</b>:
    <a
      href="https://drias-eau.fr/"
      target="_blank"
      title="DRIAS les futurs de l'eau"
    >
      https://drias-eau.fr/
    </a>
  </p>
  <p>
    Vous pouvez également consulter la
    <a href="{base}/stations">
      liste des stations présentées sur ce site web
    </a>
  </p>
{/if}

{#if sonification}
  <MarkdownRenderer markdown={sonification} />
{/if}

{#if links}
  <Credits />
{/if}
