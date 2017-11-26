# gatsby-plugin-segment
A feature-rich, lightweight Gatsby plugin to easily add [Segment JS snippet](https://segment.com/docs/sources/website/analytics.js/quickstart/) to your site.

## Features
Packed with features:
- use multiple write keys (one for prod env, another optional one for dev)
- disable page view tracking just in case you want to add that manually
- super lightweight
- up to date (Segment snippet 4.0.0)

## Install 
- `$ yarn add gatsby-plugin-segment`
- or `$ npm install --save gatsby-plugin-segment`

## How to use

In your gatsby-config.js file:
```javascript
plugins: [
    {
        resolve: `gatsby-plugin-segment`,
        options: {
            // your segment write key for your production environment
            // when process.env.NODE_ENV === 'production'
            // required; non-empty string
            prodKey: `SEGMENT_PRODUCTION_WRITE_KEY`,

            // if you have a development env for your segment account, paste that key here
            // when process.env.NODE_ENV === 'development'
            // optional; non-empty string
            devKey: `SEGMENT_DEV_WRITE_KEY`,

            // whether you want to include analytics.page()
            // optional; boolean that defaults to true
            // if false, then don't forget to manually add it to your codebase manually!
            trackPage: true
        }
    }
]
```
