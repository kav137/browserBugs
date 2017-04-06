# Browser bugs
Just a list of issues that aren't obvious or easily googlable

  - MS Edge: when you set an SVG as background there is a bug with scaling - background-size property would be ignored. Workaround: specify the second parameter for background-size even if you have a shape of square. E.g.:
```sh
background-size: 1rem 1rem;
```
  - IE: if you have a list of SVG sprites and some symbols have <defs> block inside you have to pull this block out from <symbol>. Otherwise things like gradients or clipPaths wouldn't work 
