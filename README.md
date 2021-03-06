# gatsby-wordpress-theme-libre

A Gatsby theme plugin for creating blogs from headless WordPress CMS.

Turn your WordPress blog into a lightning fast static website. This Gatsby theme is a frontend replacement of the WordPress engine featuring the standard Libre 2 skin and functionality. All content is sourced from a headless WordPress CMS.

## Demo

Play with the [Demo](https://gatsby-wordpress-libre.netlify.com/) to get a first impression.

## Features

- WordPress Libre 2 skin
- SEO optimized
- Fully responsive
- Composable and extensible


## Getting Started

1. Install this starter by running

   ```bash
   gatsby new wp-starter https://github.com/armada-inc/gatsby-wordpress-libre-starter
   ```

2. Change directory

   ```bash
   cd wp-starter
   ```

3. Run

   ```bash
   gatsby develop
   ```

   and visit your site at `http://localhost:8000`.

## 🧐 What's inside?

A quick look at the top-level files and directories you'll see in a Gatsby project.

    .
    ├── node_modules
    ├── static
    ├── .gitignore
    ├── gatsby-config.js
    ├── yarn.lock
    ├── package.json
    ├── siteConfig.js
    ├── .wordpress-config.json
    └── README.md

1.  **`/node_modules`**: This directory contains all of the modules of code that your project depends on (npm packages) are automatically installed.

2.  **`/static`**: This directory will contain all of the static files required by theme such as `favicon`, `logo` and `robot.txt`.

3.  **`.gitignore`**: This file tells git which files it should not track / not maintain a version history for.

4.  **`gatsby-config.js`**: This is the main configuration file for a Gatsby site. This is where you can specify information about your site (metadata) like the site title and description, which Gatsby plugins you’d like to include, etc. (Check out the [config docs](https://www.gatsbyjs.org/docs/gatsby-config/) for more detail).

5.  **`yarn.lock`** (See `yarn.lock` below, first). This is an automatically generated file based on the exact versions of your npm dependencies that were installed for your project. **(You won’t change this file directly).**

6.  **`siteConfig`**: A config file for your website, which includes things like website url, title, Background color, theme color etc.

8.  **`.wordpress-config.json`**: A config file containing config required to fetch data from wordpress such as url and content keys etc.

9.  **`README.md`**: A text file containing useful reference information about your project.

## Configure

```js
//siteConfig.js
module.exports = {
  siteUrl: "http://localhost:9000", // Site domain. Do not include a trailing slash!

  postsPerPage: 2, // Number of posts shown on paginated pages (changes this requires sometimes to delete the cache)

  siteTitleMeta: "Wordpress Gatsby Starter", // This allows an alternative site title for meta data for pages.
  siteDescriptionMeta:
    "A starter template to build amazing static websites with Wordpress and Gatsby", // This allows an alternative site description for meta data for pages.

  shareImageWidth: 1000, // Change to the width of your default share image
  shareImageHeight: 523, // Change to the height of your default share image

  shortTitle: "Wordpress", // Used for App manifest e.g. Mobile Home Screen
  siteIcon: "favicon.png", // Logo in /static dir used for SEO, RSS, and App manifest
  backgroundColor: "#e9e9e9", // Used for Offline Manifest
  themeColor: "#15171A" // Used for Offline Manifest
};
```

In the configuration shown above, the most important fields to be changed are `siteUrl`, `siteTitleMeta` and `siteDescriptionMeta`. Update at least those to fit your needs.

## WordPress Content configuration

```bash
    {
        "baseUrl": "yourwordpressblog.com",
        "protocol": "https",
        "hostingWPCOM": false,
        "useACF": true,
        "includedRoutes": [
            "**/categories",
            "**/posts",
            "**/pages",
            "**/media",
            "**/tags",
            "**/taxonomies",
            "**/users"
        ]
    }
```

In the configuration shown above, the most important fields to be changed are `baseUrl` and `hostingWPCOM` . Update those with your configuration. example shown above works great for self hosted wordpress.

If your blog is hosted on wordpress.com you will have to add few extra keys for reference check out [wordpress-source-docs](https://www.gatsbyjs.org/packages/gatsby-source-wordpress/).

## Deploy

```bash
    gatsby build
```

After completion of the build process your static site can be found in the `public/` folder. Copy those files over to your webserver.

# Copyright & License

Copyright (c) 2020 Armada Intelligence Inc - Released under the [MIT license](LICENSE).
