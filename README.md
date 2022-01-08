# buildx-image-to-ghcr
Build images by buildx and push them to ghcr.io


### Example:


```yaml
  build-and-publish:
    runs-on: ubuntu-latest
      - name: Build and Publish Image
        uses: xczpw/buildx-image-to-ghcr@main
        with:
          github-token: ${{ secrets.TOKEN }}
          image-name: my_image
          image-tag: v1
          dockerfile: Dockerfile
          build-context: .
          build-platform: linux/amd64,linux/386,linux/arm64,linux/arm/v7,linux/arm/v6,linux/arm/v8
```
