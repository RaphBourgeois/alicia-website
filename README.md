# alicia-website

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



## Tony's notes

### LFS setup (large media)

[Netlify Large Media Setup](https://docs.netlify.com/large-media/setup/)

You will need to install git lfs by following the steps on this page, this is how netlify is going to host your pictures/audio/videos

Before you use Cloudinary, you can directly transform and re-scale images by using the [Nellify LFS Transform Images](https://docs.netlify.com/large-media/transform-images/) functionality