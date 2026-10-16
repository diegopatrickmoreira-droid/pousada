<!-- LOVABLE:BEGIN -->
> [!IMPORTANT]
> This project is connected to [Lovable](https://lovable.dev). Avoid rewriting
> published git history — force pushing, or rebasing/amending/squashing commits
> that are already pushed — as it rewrites history on Lovable's side and the
> user will likely lose their project history.
>
> Commits you push to the connected branch sync back to Lovable and show up in
> the editor, so keep the branch in a working state.
<!-- LOVABLE:END -->

- Keep this hospitality website on the index route with hash-anchor navigation; the requested experience is a single page.
- Keep official contact and accommodation values in the browser-safe pousada module and test reservation destinations; all reservation links must share one source of truth.
- Use uploaded media through asset JSON pointers and preserve the official logo colors; optimized images stay external to source.
- Use semantic CSS tokens and shared Button variants for hospitality controls; keep visual styling centralized.
- Render the location through Google Maps Embed using the public managed browser key and the supplied address; never expose server connector credentials.
