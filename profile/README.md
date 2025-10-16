# DotAISlash

**DotAISlash** is home to **VERSA** – the *Vendor-neutral Extensible Repo Spec for Agents*. We maintain a portable `.ai/` folder standard, the CodeVibe design system, and tooling that lets IDEs, CLIs, and hosted copilots load the same project context without bespoke adapters.

## What we ship

| Area | Repos | Status |
| --- | --- | --- |
| Core specification | [`dotaislash-spec`](https://github.com/dotAIslash/dotaislash-spec) | drafting VERSA 1.0 |
| Schemas & validation | [`dotaislash-schemas`](https://github.com/dotAIslash/dotaislash-schemas) | scaffolded |
| Reference CLI | [`dotaislash-cli`](https://github.com/dotAIslash/dotaislash-cli) | scaffolded |
| Examples | [`dotaislash-examples`](https://github.com/dotAIslash/dotaislash-examples) | scaffolded |
| Conformance | [`dotaislash-conformance`](https://github.com/dotAIslash/dotaislash-conformance) | scaffolded |
| Landing site & design system | [`dotaislash.github.io`](https://dotaislash.github.io/) | live Next.js site |
| Community | [Org discussions](https://github.com/orgs/dotAIslash/discussions) · [Spec issues](https://github.com/dotAIslash/dotaislash-spec/issues) | forming |

## VERSA at a glance

- **Eight categories**: Rules · Prompts · Agents · Memory · Knowledge · Tools · Settings · Permissions
- **File types**: JSON for structure, Markdown for human guidance with `ai:meta` JSON preambles
- **Merge contract**: `settings.json` → profile overlays → user overrides (keys flagged `user_overridable`) → runtime flags
- **Security**: deny → ask → allow policy, secret bindings via env/keychain, redaction hints for retrieval
- **Interop**: Mirrors AGENTS.md, CLAUDE.md, GEMINI.md, and Cursor project rules so existing tools can adopt with minimal mapping

## Design system – CodeVibe

We use the [CodeVibe design system](https://dotaislash.github.io/design/codevibe/) to present VERSA: gradient-driven, AAA-compliant, Tailwind-native. All palettes, radii, and animations are published for direct reuse in dashboards, docs, and spec viewers.

## Get involved

1. ⭐ Star the repos that matter to you
2. 📄 Watch [`dotaislash-spec`](https://github.com/dotAIslash/dotaislash-spec) for specification updates
3. 💬 Join discussions or propose ideas in [org discussions](https://github.com/orgs/dotAIslash/discussions)
4. 📝 File proposals or feedback in [dotaislash-spec issues](https://github.com/dotAIslash/dotaislash-spec/issues)

> One folder, many runtimes. Build the interoperable future of agentic coding with VERSA.
