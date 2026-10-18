# dev-env-artifacts

Self-contained Windows x64 packages for the **本地开发环境管理面板** (dev-env-manager).
Every package includes its runtime; target machines do not need Node, Java, VC++ Redist or msys2.

## Catalog

- Fast mirror (recommended in China): `https://cdn.jsdelivr.net/gh/mokesss/dev-env-artifacts@main/manifest.json`
- GitHub Releases: `https://github.com/mokesss/dev-env-artifacts/releases/download/catalog/manifest.json`
- Asset base (China mirror): `https://gh-proxy.com/https://github.com/mokesss/dev-env-artifacts/releases/download`
- Asset base (GitHub direct): `https://github.com/mokesss/dev-env-artifacts/releases/download`

The panel's Download Center accepts the Catalog URL and assetBase above. Public repositories do not need a token.

## Packages

| Package | Version | Notes |
|---|---|---|
| panel | 1.0.0 | Node SEA single exe + web/dist + start-panel.vbs |
| nginx | 1.28.3 | official Windows build |
| mysql | 8.4.11 | app-local MSVCP140 / VCRUNTIME140 / VCRUNTIME140_1 |
| redis | 8.10.2 | bundled msys2 runtime |
| xxl-job | 3.5.0 | jpackage runtime + db/tables_xxl_job.sql |
| nacos | 3.2.4 | jpackage runtime |
| rocketmq | 5.5.1 | three jpackage runtimes; mqadmin java.exe for JSON messages |

## Integrity

Each release asset has a SHA-256 in `manifest.json`; the panel verifies it before extraction.
Downloads support HTTP Range resume. Installation keeps a `.bak-<timestamp>` backup and rolls back on failure.