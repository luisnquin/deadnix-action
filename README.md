# deadnix-action

Automatically creates pull requests to remove unused code in `.nix`
files

## Usage

Create a `.github/workflows/deadnix.yml` file:

```yaml
on: [push]

name: Dead code analysis

jobs:
  deadnix:
    name: Deadnix
      runs-on: ubuntu-latest
        steps:
          - uses: actions/checkout@v2
          - uses: cachix/install-nix-action@v16
          - uses: cachix/cachix-action@v10
            with:
            name: deadnix
          - uses:
            astro/deadnix-action@main
```on: [push]

`git add`, `git commit`, `git push`, be happy.
