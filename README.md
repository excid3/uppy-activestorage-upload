# uppy-activestorage-upload

<img src="https://uppy.io/images/logos/uppy-dog-head-arrow.svg" width="120" alt="Uppy logo: a superman puppy in a pink suit" align="right">

The ActiveStorage Upload plugin handles Ruby on Rails ActiveStorage direct uploads with Uppy.

## Example

Add this line to your HEAD tag.
```erb
<%= tag.meta name: "direct-upload-url", content: rails_direct_uploads_path %>
```

Then use `ActiveStorageUpload` as an Uppy plugin in your Javascript pack with Webpacker.

```js
const Uppy = require('@uppy/core')
const ActiveStorageUpload = require('@excid3/uppy-activestorage-upload')

const uppy = Uppy()
uppy.use(ActiveStorageUpload, {
  directUploadUrl: document.querySelector("meta[name='direct-upload-url']").getAttribute("content")
})
```

## Installation

```bash
yarn add https://github.com/excid3/uppy-activestorage-upload
or
npm install https://github.com/excid3/uppy-activestorage-upload --save
```

We recommend installing from npm and then using a module bundler such as [Webpack](http://webpack.github.io/), [Browserify](http://browserify.org/) or [Rollup.js](http://rollupjs.org/).

## License

[The MIT License](./LICENSE).
