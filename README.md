# gha-docker

## Usage

```yaml
# ...

jobs:
  build-and-publish-image:
    runs-on: "ubuntu-latest"
    permissions:
      contents: "read"
      packages: "write"
    steps:
      - uses: "actions/checkout@v4"
      - uses: "c032/gha-docker@main"
        with:
          image-name: "${{ github.repository }}"
          registry-username: "${{ github.actor }}"
          registry-password: "${{ secrets.GITHUB_TOKEN }}"
```

## License

MPL 2.0.
