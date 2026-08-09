# LLM Wiki Agent Instructions

This repository is an Obsidian-first, LLM-maintained knowledge base. Treat its Markdown like a codebase: inspect the existing structure, make small coherent edits, keep links healthy, and record material changes.

## Start Here

1. Read `WIKI.md` for the wiki's topic, purpose, audience, source policy, and exclusions.
2. Read `index.md` before answering questions or deciding where knowledge belongs.
3. If `WIKI.md` has `status: unconfigured`, configure the wiki before ingesting sources.

## Layers

- `raw/` contains source material and is immutable evidence. Do not rewrite source body text.
- `raw/processed/` contains sources that have already been ingested.
- `raw/assets/` and `raw/images/` contain source attachments.
- `wiki/` is the LLM-maintained compiled knowledge layer.
- `index.md` is the content catalog.
- `templates/` contains Obsidian templates; it is not wiki content.

## Global Conventions

- Follow the profile and source policy in `WIKI.md`.
- Use Obsidian links such as `[[Page Name]]` internally and Markdown links only for external URLs.
- Give generated pages frontmatter with at least `type`, `created`, `updated`, `status`, and relevant `tags`.
- Put a short summary near the top, followed by evidence, connections, open questions, and sources when relevant.
- Cross-link usefully. Add reciprocal links when two pages are natural navigation partners.
- Mark uncertainty explicitly. Preserve meaningful source conflicts instead of smoothing them away.
- Never invent source-backed facts. Distinguish sourced claims, synthesis, and inference.
- Use today's local date unless a source provides a more specific date.
- Keep generated images in an `images/` folder beside the relevant subject pages. Keep source images under `raw/images/`.

## Wiki Structure

- Organize durable knowledge by subject rather than only by page type.
- Reuse an existing subject folder before creating a near-duplicate.
- Create a subject folder when a durable cluster emerges, especially when three or more related pages would otherwise be scattered.
- Give each subject folder a short overview page with `type: subject` unless a suitable overview already exists.
- Mixed page types are allowed within subject folders. Use frontmatter types such as `source-summary`, `concept`, `entity`, `tool`, `workflow`, `synthesis`, `comparison`, or `question`.
- Store standalone source summaries under `wiki/sources/`; use source-family subfolders for recurring feeds.
- Avoid large retroactive reorganizations during normal ingestion. When moving a page, update its links and index entry in the same change.

## Ingest Workflow

1. Read `WIKI.md` and `index.md`.
2. Find unprocessed source files directly under `raw/`, excluding `processed/`, `assets/`, and `images/`.
3. Read each source and extract the material required by the wiki profile.
4. Choose or create the subject path before writing generated pages.
5. Create or update a source summary and the relevant durable wiki pages.
6. Preserve source provenance and link generated claims back to source summaries.
7. Update `index.md` for every created, moved, or materially changed page.
8. Move successfully processed source files into `raw/processed/` without rewriting their body text. Move referenced attachments with them or preserve valid links.

## Query Workflow

1. Read `WIKI.md` and `index.md`.
2. Search `wiki/`, then read the most relevant pages and their linked sources.
3. Answer from the compiled wiki when possible and cite the relevant local pages or sources.
4. Identify uncertainty, missing evidence, and conflicting sources explicitly.
5. Only create durable synthesis when the user asks to preserve it. If files change, update `index.md`.

## Lint Workflow

1. Check for broken links, orphan pages, duplicate concepts, missing backlinks, stale claims, unresolved contradictions, missing source summaries, and invalid frontmatter.
2. Fix low-risk structural issues directly.
3. Surface larger editorial choices to the user.

## Git And Obsidian

- The repository root is the Obsidian vault root.
- Portable `.obsidian` configuration is versioned; workspace/session state is ignored.
- Obsidian Git performs automatic pull, commit, and push. Do not change its synchronization settings unless the user asks.
- Never commit credentials, cookies, tokens, or `.env` files.
