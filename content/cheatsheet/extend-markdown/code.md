---
layout: cheats/item
headline: code
---

Code in Remark can be either `inlineCode` (single back-ticks in markdown) or a block `code` (fenced with three back-ticks in markdown).

```js
const visit = require( 'unist-util-visit' );

const attacher = () => {
  const transformer = ( tree, file ) => {
    visit( tree, 'inlineCode', node => {
      // transform the node here
    } );

    visit( tree, 'code', node => {
      // transform the node here
      let language = node.lang;
    } );
  };

  return transformer;
};
```
