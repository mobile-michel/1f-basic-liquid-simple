# Basic template with Eleventy, Liquid & Simple CSS framework
[01-basic-liquid-simple](https://github.com/mobile-michel/01-basic-liquid-simple)

## Folder structure
- pages in /src
- layouts in /_layouts
- includes in /_includes
- Json files in /_data
- Simple CSS in /assets/css
- images in /assets/images

## Page layout
- _layouts/base.liquid
- _includes/header.liquid
- _includes/footer.liquid

## Primary navigation
- add tags in frontmatter: primary

## Package.json scripts
- "start": "npx @11ty/eleventy --serve",
- "build": "eleventy",
- "debug": "DEBUG=* eleventy"

## Dependencies
- "@11ty/eleventy": "^2.0.1"

## eleventy.config.js
```
module.exports = function (eleventyConfig) {
    eleventyConfig.addPassthroughCopy("src/assets"); // Scss, JS, and images files
    return {
        dir: {
            input: "src", // Set the source for 11ty to the /src directory
            output: "_site", // This is the default
            includes: "_includes", // All UI partials
            layouts: "_layouts" // Base page layouts
        },
        templateFormats: ["html", "md", "liquid"]
    };
};
```
