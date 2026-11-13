This repo contains the templates of configs for iotube prod. They may be used directly, but feel free to update the parameters as you want.

## Layout

- `witness/<route>.yaml`: one witness config per route (for example
  `witness/bsc-to-iotex.yaml`). Operator values are not edited in these files:
  they are read from the environment (`.env`), as `${VAR}` in the file
  (RPC endpoint, start height) or directly by the witness (signing key, relayer
  address, sign policy). See `witness-service/README.md` in
  [ioTube](https://github.com/iotubeproject/ioTube) for the install bundle
  that uses them.
- `witness-config-*.yaml`: the original per-chain config and secret files, used
  by `start_witness.sh` setups. Kept unchanged for existing deployments.
- `relayer-config-*.yaml`: relayer configs.
