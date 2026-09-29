# AGENTS.md
A [Slidev](https://sli.dev) presentation (Slidev 53 + Vue 3).


## Structure and good practices
- Keeps files organized by topic or by single slides. Each slide/groups of slides shoudl be under `slides` folder
- Try to stick to markdown syntax as much as possible. If a more involved Vue component is needed then ask befure creating one. In general all slides should contain not much html and should be easily human readable
- Use css root variables as much as possible; avoid using colors directly so that the whole presentation could be themed tweking the main colors in the style.css file

## Slidev auto-loading (do not import these)

- `style.css` — global styles, auto-loaded. Design tokens live in `:root` / `html.dark` (`--c-*`, `--slidev-theme-primary`). Helper classes: `.box`, `.badge` (+ `.badge-accent`, `.badge-round`), `.eyebrow`. Indented with tabs.
- `components/*.vue` — usable in slides with no import (e.g. `<Badge round>vs</Badge>`, `<Counter />`).
- `global-bottom.vue` — footer rendered on every slide (author + `page / total`).
- `snippets/` — code-import snippets.

## Directives
- NEVER run chromium with shell to test; use chrome-devtools and attach to `http://localhost:3030`. The instance will be already running
- NEVER run shell tools like ls, grep and so on. You can use your integrated tools for that
- Try to stick to default markdown syntax as much as possible. Limit html and if something complicated is needed prompt the user before implementing it

##  tools
You should use mcp/builtin tools/plugins whenever possible, resorting to shell only when something that is not achievable with said tools is needed

### Mcp
- slidev: registers a `slidev` MCP server at `http://localhost:3030/__mcp`.
- code-graph: use to index and navigate codebase
- chrome-devtools: use to interact with the browser (e.g. read console logs). The application slides will be already running in `http://localhost:3030`. If thats not the case please let me know before proceeding
