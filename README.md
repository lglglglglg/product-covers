# Product Covers

HTTPS-hosted product cover images for storefront listings.

## Public page

Open the gallery page at:

`https://lglglglglg.github.io/product-covers/`

Every card has a button that copies its own storefront-ready HTTPS image URL.

## Structure and ordering

```text
index.html             # Gallery page
images/
  manifest.json         # Cover metadata and display order
  macOS-store-download.png
  xiaoshuo-download.png
```

All cover files live in `images/`; do not place them at the repository root. The gallery sorts by `sortOrder` in `images/manifest.json`, from largest to smallest, so a newly added cover appears first.

## Add a new cover

1. Put the image in `images/` using a stable lowercase English filename, such as `product-003.png` or `brand-banner.svg`.
2. Add an item to `images/manifest.json`, using the next larger `sortOrder` value.
3. Push the change. GitHub Pages will update the gallery and its copyable link.

For a wide SVG banner, add `"display": "banner"` to its item so the gallery shows the entire image rather than cropping it to 16:9.

Do not rename or overwrite a file after its URL has been used in a product listing.

## Direct links

- Page image URL pattern: `https://lglglglglg.github.io/product-covers/images/<filename>`
- Raw GitHub URL pattern: `https://raw.githubusercontent.com/lglglglglg/product-covers/main/images/<filename>`
