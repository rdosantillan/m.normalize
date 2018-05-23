# m.normalize #

Custom Normalize File for M projects under MIT License


## To add this file to your project ##
If you already have [npm](https://www.npmjs.com/) simply run

```sh
npm install https://github.com/flkt-crnpio/m.normalize.git
```

And load the normalize.min.css from your node_modules/m.normalize/ folder like
```sh
<link rel="stylesheet" href="node_modules/m.normalize/normalize.min.css">
```


## What this project need if you want to edit ##

You only need had installed [sass](https://sass-lang.com/install)


## Organization files about project ##

Under `_vars.scss` have a few list of vars to set general style. There is a special var for add a prefix to each tag `$m-prefix` but if you left set on `null` all styles will be affect directly to html tags.

The `_normalize.scss` is the main and only file that have all rules.

You can see how all tags are formatted on `index.html` file, which use the `normalize.css` uncompressed file to load styles.



## Edit and Rebuild your custom normalize file ##

If you change some variables on `_vars.scss` file or rule on `_normalize.scss`, you can run
```sh
sass --watch _normalize.scss:normalize.css --style expanded
```

and open `index.html` file to see your changes reflected.

Once finish editing those files, you need to run the line below, in order to get the compressed min file.
```sh
sass _normalize.scss:normalize.min.css --style compressed
```



## Tested and working on ##
* Brave
* Chrome
* Firefox
* Opera
* Safari



## Known Issues ##

#### `[type="search"]` ####

It's not possible to set styles on inputs type search without hide the input first, so, it's working as textfield losing his properties... sorry. But you can apply the functionality with javascript, right?!
