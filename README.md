# ASR submission for GARD evaluation (January 2022)

This repo contains the code and scenarios for the evaluation.

## How to run in Docker

### First, install Docker app in your host machine, and run it

### Setting up API token to download the repo

Enter [GitHub Token settins](https://github.com/settings/tokens) and add a token with the access to private repos.
Set `ARMORY_GITHUB_TOKEN` env var with the token's value.

```bash
$  export ARMORY_GITHUB_TOKEN=...
```

### Installing armory

```bash
$ pip install armory-testbed==0.15.3
```

### Obtaining models

Models used are in
```
/export/b17/janto/gard/armory/saved_models
```

Copy the models in your host machine in
```
~/.armory/saved_models
```

### Running scenarios

```bash
# Run the full evaluation.
$ armory run scenarios/JHUM_k2_defended_denoiser_bpda_pgd.json
# Or just check quickly that it works okay.
$ armory run --check scenarios/JHUM_k2_defended_denoiser_bpda_pgd.json
```
