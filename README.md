# Browser bugs
Just a list of issues that aren't obvious or easily googlable

  - MS Edge (38.14393): there is a bug with scaling when you set an SVG as element's background: background-size property would be ignored. Workaround: specify the second parameter for background-size even if you have a shape of square. E.g.:
```sh
background-size: 1rem 1rem;
```

  - IE 11: if you have a list of SVG sprites and some symbols have <defs> block inside you have to pull this block out from <symbol>. Otherwise things like gradients or clipPaths wouldn't work. Also do not use 'display: none' for block with sprites
  
  
  - MS Edge (38.14393): MutationObserver don't recognize changes of element in case you change element's style using .cssText property
