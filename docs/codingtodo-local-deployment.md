# Codingtodo Local Deployment Notes

Date: 2026-05-07

This fork is used by the `codingtodo` workspace to evaluate and customize Vibe Kanban.

## Fork

- Upstream: `https://github.com/BloopAI/vibe-kanban`
- Fork: `https://github.com/nanyumeng/vibe-kanban`
- Working branch: `codex/local-deploy`
- Base commit: `4deb7ec`

## Local Deployment Used

The current machine does not have Rust/Cargo installed, so the verified local deployment uses the official prebuilt `npx vibe-kanban` binary instead of source compilation.

Verified URL:

```text
http://127.0.0.1:3210
```

Verified result:

```text
HTTP/1.1 200 OK
```

The wrapper scripts live one directory above this repository in the `codingtodo` workspace:

```text
../scripts/start-vibe-kanban.sh
../scripts/status-vibe-kanban.sh
../scripts/stop-vibe-kanban.sh
```

## Source Development

Install the Rust toolchain before running the source development server:

```bash
cargo install cargo-watch
cargo install sqlx-cli
pnpm i
pnpm run dev
```

## License

Vibe Kanban is licensed under Apache License 2.0. Commercial use, modification, and redistribution are allowed subject to the license obligations.

## Operational Caveat

The original company behind Vibe Kanban announced shutdown on 2026-04-10. Treat this fork as a self-maintained codebase and avoid depending on upstream hosted services.

