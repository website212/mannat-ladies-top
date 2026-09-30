# Mannat Ladies Top — GitHub Pages Website

A premium, responsive women's fashion boutique website built with only HTML5, CSS3 and vanilla JavaScript. No backend is required.

## 1. Upload the project to GitHub Pages

Keep this structure:

```text
/
├── index.html
├── style.css
├── script.js
├── README.md
└── images/
    ├── logo.png
    ├── hero/
    │   └── hero.jpg
    ├── categories/
    ├── banners/
    ├── products/
    ├── gallery/
    └── store/
```

On GitHub:
1. Create/open your repository.
2. Upload `index.html`, `style.css`, `script.js`, `README.md`, and the complete `images` folder.
3. Go to **Settings → Pages**.
4. Under **Build and deployment**, choose **Deploy from a branch**.
5. Select the branch containing these files and the `/ (root)` folder.
6. Save. GitHub will provide the website URL.

## 2. Where to put the logo

Put the shop logo here:

```text
images/logo.png
```

The same logo is used in the navbar, footer, favicon and browser metadata.

## 3. Hero image

Put the main fashion image here:

```text
images/hero/hero.jpg
```

Recommended: a high-quality vertical or landscape fashion image. The site automatically shows a clean placeholder if the file is missing.

## 4. Category images

Put one image in each location:

```text
images/categories/tops.jpg
images/categories/jeans.jpg
images/categories/sarees.jpg
images/categories/one-piece.jpg
images/categories/two-piece.jpg
images/categories/three-piece.jpg
images/categories/party-wear.jpg
```

These appear in the "Shop by Category" cards.

## 5. Large category banner images

Put one banner image in each location:

```text
images/banners/tops-banner.jpg
images/banners/jeans-banner.jpg
images/banners/sarees-banner.jpg
images/banners/one-piece-banner.jpg
images/banners/two-piece-banner.jpg
images/banners/three-piece-banner.jpg
images/banners/party-wear-banner.jpg
```

These appear at the top of each detailed collection.

## 6. Product photos — easiest part

Product photos are controlled from **one section near the top of `script.js`** called:

```js
const PRODUCTS = { ... };
```

Example:

```js
tops: [
  {src:"images/products/tops/top-01.jpg", badge:"Trending", type:"Tops"},
  {src:"images/products/tops/top-02.jpg", badge:"New", type:"Tops"}
]
```

To add a new Tops photo:

1. Upload the image into:
   `images/products/tops/`
2. Give it a name such as:
   `top-05.jpg`
3. Add one line to the `tops` array:

```js
{src:"images/products/tops/top-05.jpg", badge:"New", type:"Tops"}
```

Do the same for:

```text
images/products/jeans/
images/products/sarees/
images/products/one-piece/
images/products/two-piece/
images/products/three-piece/
images/products/party-wear/
```

You do **not** need to edit the HTML for each new product.

## 7. Gallery photos

Put gallery images here:

```text
images/gallery/gallery-01.jpg
images/gallery/gallery-02.jpg
images/gallery/gallery-03.jpg
images/gallery/gallery-04.jpg
images/gallery/gallery-05.jpg
images/gallery/gallery-06.jpg
```

The filenames can be changed, but if you change them, update the `GALLERY` array in `script.js`.

## 8. Store photo

Put the shop/store image here:

```text
images/store/store.jpg
```

## 9. Important image rules

- Use `.jpg`, `.jpeg`, `.png`, or `.webp`.
- Keep filenames simple: lowercase letters, numbers and hyphens.
- Avoid spaces in filenames.
- If an expected image is missing, the website shows an elegant "Add your photo here" placeholder instead of a broken-image icon.
- Product cards do not display prices anywhere.

## 10. Business links already configured

Phone:
`tel:9834041020`

Google Maps destination:
Tuljai Chowk, Bhaya Nagar, Datta Nagar, Beed, Maharashtra 431122

Instagram:
`https://www.instagram.com/mannat_fashion_girls_top?stkn=MWRzdWNzbWFwMXM2Ng==`

## 11. Editing product badges

Each product can use:

```text
New
Trending
Popular
```

Example:

```js
{src:"images/products/tops/top-05.jpg", badge:"Popular", type:"Tops"}
```

## 12. Design/technical notes

- No backend.
- No database.
- GitHub Pages compatible.
- Vanilla JavaScript only.
- Product images use lazy loading.
- Lightbox supports mouse/touch-friendly controls and desktop keyboard arrows.
- Scroll reveal uses Intersection Observer.
- `prefers-reduced-motion` is respected.
- Responsive layouts are designed for Android phones, tablets and desktop screens.
- No WhatsApp button.
- No product prices.
