# TB3 Workspace

This repository collects multiple Solana challenge projects and related example work for Q1 2026 Accelerator.

## Main directories

- `week1/` — Week 1 challenges workspace
- `week2/` — Week 2 challenges workspace
- `week3/` — Week 3 challenges workspace

Each week folder contains one or more independent project folders (some are git submodules).

## Submodules

Several project folders are tracked as git submodules. To initialize or update submodules after cloning this repo run:

```bash
git submodule sync
git submodule update --init --recursive
```

To add or change submodules locally:

```bash
git submodule add <repo-url> <path>
git add .gitmodules
git commit -m "Add submodule <path>"
git push origin HEAD
```

If you change `.gitmodules`, run `git submodule sync` in downstream clones to pick up the new mapping.

## Quick start

From the repository root:

1. Initialize submodules as shown above.
2. Enter a project folder under `week1/`, `week2/` or `week3/`.
3. Install dependencies and run the project's tests. Typical commands:

```bash
cd week2/tuktuk-gpt-oracle
npm install
anchor build
anchor test
```

Adjust the path and commands per project — many projects include `Anchor.toml`, `Cargo.toml`, and a `tests/` folder.

## Notes

- Verify your Solana CLI is pointed at the desired cluster (localnet, devnet): `solana config set --url <RPC_URL>`
- Ensure your Anchor provider wallet is funded on the cluster you use for tests.
- To untrack a directory that is already committed, use `git rm -r --cached <path>` (keeps files locally).

If you'd like, I can add a short per-week index listing each project and its remote URL.
