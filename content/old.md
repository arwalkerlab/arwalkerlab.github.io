#Wiki

<nav id="Table of Contents"><ul></ul></nav>

{{if and (gt .WordCount 100 ) (.Params.toc) }}

<main>
  <header>
    <h1>{{.Title}}</h1>
  </header>
  <aside>
    {{ .TableOfContents }}
  </aside>
</main>

{{end}}
