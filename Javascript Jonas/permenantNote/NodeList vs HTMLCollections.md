# Explanation

- html collection updated automatically not like nodelist

```js

const nodeLinks = document.querySelectorAll('a');//nodelist

console.log(nodeLinks);

const htmlCollectionLinks = document.getElementsByTagName('a');// html collection

console.log(htmlCollectionLinks);
```
