# n8n-builds

Prebuilt `n8n` npm installs (ubuntu-24.04 x64, Node 24.18.0) for servers too small to run
`npm install -g n8n` (it needs >1 GB RAM). Built nightly by `.github/workflows/build.yml`.

orcvm1 (auto.velinaai.in) installs them with `~/n8n-autoupdate.sh`: download → unpack next to the
running version → back up the DB → swap the `lib/node_modules/n8n` symlink → restart → health check,
rolling the symlink and DB back if it fails.
