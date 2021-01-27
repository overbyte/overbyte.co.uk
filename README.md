# overbyte.co.uk

## Requirements

This project requires the following environment variables to access Storyblok
CMS API:
* SB_TOKEN
* SB_CV

For local testing, these should be stored in a `.env` file in the root of the
project and not committed to GIT.

These can be found at https://app.storyblok.com/#!/me/spaces/103220/edit?tab=api
and on the most recent publish json in Storyblok

## Build Setup

```bash
# install dependencies
$ npm install

# serve with hot reload at localhost:3000
$ npm run dev

# build for production and launch server
$ npm run build
$ npm run start

# generate static project
$ npm run generate
```

For detailed explanation on how things work, check out [Nuxt.js docs](https://nuxtjs.org).
