# Contributing

We work in the following manner:

## Git Workflow

Every feature should be developed in a seperate branch. Once the feature is ready for review, a merge request is made, so that any other team members can give feedback on the code. When one or more team members approved the changes, the merge request can be merged and will be automatically deployed.

## Features

### HTML

Every feature should have its own CSS and JavaScript files. The base structure of the feature should be defined in [`./docs/index.html`](./docs/index.html). 

### CSS

The styles for the feature should go in a `./docs/assets/css/feature.css` file and imported in the [`./docs/assets/main.css`](./docs/assets/main.css) file in the following manner:

```css
@import url("./feature.css");
```

### JavaScript

JavaScript logic should go in a `./docs/assets/js/feature.js` file and be imported in the [`./docs/main.js`](./docs/main.js) file. To import the logic, first its path must be defined in [`./docs/index.html`](./docs/index.html):

```html
<script type="importmap">
  {
    "imports": {
      // other imports are also defined here
      "feature": "/WAFS-team-rocket/assets/js/feature.js"
    }
  }
</script>
```

Then, the file can be used in [`./docs/main.js`](./docs/main.js) in the following way:

```js
import { setSomeFeature } from "feature";

setSomeFeature(data)
```
