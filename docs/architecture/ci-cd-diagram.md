---
layout: default
title: CI/CD Architecture Diagram
mermaid: true
---

<!--
{% if page.mermaid %}
<script type="module">
  import mermaid from "https://cdn.jsdelivr.net/npm/mermaid@10/dist/mermaid.esm.min.mjs";

  mermaid.initialize({
    startOnLoad: false,
    theme: "base",
    themeVariables: {
      /* Omkraft brand */
      primaryColor: "#3A98F1",
      primaryTextColor: "#ffffff",
      primaryBorderColor: "#05004E",
      lineColor: "#05004E",

      /* Flowchart-specific (REQUIRED) */
      nodeBorder: "#05004E",
      nodeTextColor: "#05004E",
      clusterBorder: "#05004E",
      clusterBkg: "#F6F9FF",
      edgeLabelBackground: "#ffffff",

      /* Typography */
      fontFamily:
        "-apple-system, BlinkMacSystemFont, 'Segoe UI', Helvetica, Arial, sans-serif",
      fontSize: "14px"
    }
  });

  mermaid.run({
    querySelector: "pre code.language-mermaid"
  });

  /* Horizontal centering – reliable */
  requestAnimationFrame(() => {
    document.querySelectorAll('svg[id^="mermaid-"]').forEach(svg => {
      svg.style.display = "block";
      svg.style.margin = "2rem auto";
      svg.style.maxWidth = "100%";
    });
  });
</script>
{% endif %}
-->


```mermaid
flowchart TD
    Dev[Developer] -->|PR| GitHub[GitHub Repo]

    GitHub --> PRChecks[PR Workflows]
    PRChecks -->|Lint| Lint[Lint Workflow]
    PRChecks -->|Title| PRTitle[PR Title Check]

    Lint --> Pass1[Pass]
    PRTitle --> Pass2[Pass]

    Pass1 --> Merge[Merge to main]
    Pass2 --> Merge

    Merge --> ReleaseTrigger[Push to main]

    ReleaseTrigger --> Caller[Repo Release Workflow]
    Caller --> Reusable[Org Reusable Release Workflow]

    Reusable --> Semantic[semantic-release]
    Semantic --> Tag[Git Tag]
    Semantic --> GHRelease[GitHub Release]
```