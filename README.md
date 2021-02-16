# alicia-website

## Installation

1. install git and npm
2. git clone the repo
3. run `npm install`
## ? 4. run `npm install netlify-cli -g`
4. to log into netlify, run `login`
5. to start development mode, type `npm run netlify-dev` in the terminal

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

### Dev Tools
Use [VS Code](https://code.visualstudio.com/download)

.editorconfig will tell VSCode the project's settings.

### LFS setup (large media)

[Netlify Large Media Setup](https://docs.netlify.com/large-media/setup/)

You will need to install git lfs by following the steps on this page, this is how netlify is going to host your pictures/audio/videos

Before you use Cloudinary, you can directly transform and re-scale images by using the [Nellify LFS Transform Images](https://docs.netlify.com/large-media/transform-images/) functionality

For audio files, just use the [<audio></audio>](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/audio) HTML5 tag, its supported by all browsers

### Styling and Responsive Design

To make the site mobile-compatible and also look good, use [Bootstrap-Vue](https://bootstrap-vue.org/docs/components), its already installed and all of the components are globally available.

Reading on how bootstrap-vue handles layout: https://bootstrap-vue.org/docs/components/layout
A

I recommend creating [single file components](https://vuejs.org/v2/guide/single-file-components.html) in the /componets/ folder, they will automatically be registered and available your main page.

### Favicon creation

You will want to create a favicon (the icon that appears in the browser tab) for your site.

I recommend https://favicon.io/, then put the file in the /static/ folder with the name "favicon.ico", the static site generator will handle the rest.