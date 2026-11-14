# Clothing Store

Clothing Store is a responsive storefront demo built with HTML, Sass, and vanilla JavaScript. It includes a home page for promotions and new arrivals, a product catalog, and dedicated About and Contact pages.

| Page | Contents |
| --- | --- |
| [Home](index.html) | Promotional banners, featured products, and new arrivals |
| [Shop](shop.html) | Product cards with photos, prices, and ratings |
| [About](about.html) | Store information and service highlights |
| [Contact](contact.html) | Contact details and a sample message form |

The catalog uses static product data. Cart, checkout, and message delivery are outside the scope of the demo.

## Run locally

Install Python 3, then run these commands from a terminal:

```sh
git clone https://github.com/graymuck/Clothing-store.git
cd Clothing-store
python -m http.server 8000
```

Open [http://localhost:8000](http://localhost:8000). Serve the project from its root so the Shop page can load its root-relative JavaScript paths. The compiled CSS is included, so previewing the site does not require a build.

## Project structure

| Path | Purpose |
| --- | --- |
| `*.html` | The four storefront pages |
| [`assets/SASS/`](assets/SASS/) | Page styles, shared layouts, and responsive mixins |
| [`assets/Css/`](assets/Css/) | Compiled CSS plus Normalize.css and Font Awesome styles |
| [`assets/Js/app.js`](assets/Js/app.js) | Mobile navigation toggle |
| [`assets/images/`](assets/images/) | Product photos and promotional artwork |
| [`assets/webfonts/`](assets/webfonts/) | Bundled Font Awesome fonts |

## Rebuild styles

With Node.js and npm installed, run this command from the project root after editing the Sass source:

```sh
npx sass --no-source-map assets/SASS/pages/home/main.scss:assets/Css/main.css assets/SASS/pages/shop/shop.scss:assets/Css/shop.css assets/SASS/pages/about/about.scss:assets/Css/about.css assets/SASS/pages/contact/contact.scss:assets/Css/contact.css
```
