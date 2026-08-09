# LLM Wiki

This private repository is an Obsidian vault and an LLM-maintained knowledge base.

## First use

1. Open this repository folder as a vault in Obsidian.
2. Allow the bundled community plugin when Obsidian asks. Obsidian Git is already installed, enabled, and configured for automatic synchronization every ten minutes.
3. Ask your preferred file-editing AI agent: `Read AGENTS.md and WIKI.md. Configure this wiki for <topic> before ingesting sources.`
4. Review the resulting `WIKI.md` profile.
5. Add evidence to `raw/` and ask the agent to ingest it according to `AGENTS.md`.

## Structure

- `WIKI.md` defines the subject, audience, source policy, and output expectations.
- `raw/` contains immutable evidence waiting to be processed.
- `raw/processed/` contains evidence already ingested.
- `raw/assets/` and `raw/images/` contain source attachments.
- `wiki/` contains generated and maintained knowledge pages.
- `index.md` is the catalog to read before browsing or answering questions.
- `templates/` contains Obsidian note templates.

Use Obsidian links such as `[[Page Name]]` for internal navigation and normal Markdown links for external sources.

## Obsidian Git credential helper

The bundled `obsidian_askpass.sh` belongs to the upstream Obsidian Git plugin. It bridges Git credential prompts to the plugin when Git is running inside Obsidian without an interactive terminal. The plugin invokes it automatically when needed; you do not run it yourself.
