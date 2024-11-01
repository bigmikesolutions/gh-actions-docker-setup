# gh-actions-docker-setup
GitHub Action to set up Docker CE on Linux (Debian, Ubuntu) allowing you to use Docker in subsequent steps.

## Inputs

### `docker_version`

*Optional* The version of Docker to install. Defaults to `latest`.

## Example Usage

```yaml
jobs:
  build:
    runs-on: ubuntu-latest
    steps:
      - name: Checkout code
        uses: actions/checkout@v2

      - name: Install Docker
        uses: bigmikesolutions/gh-actions-docker-setup@v1
        with:
          docker_version: "20.10.7"  # Optional: specify a version