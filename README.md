# m.normalize
Custom Normalize File for M projects under MIT License

#### Add m.normalize to your project
If you already have [npm](https://www.npmjs.com/) run:
```sh
npm install https://github.com/flkt-crnpio/m.normalize.git
```
___

### Customization

You need had installed [sass](https://sass-lang.com/install)

#### Understand the files
Under `_vars.scss` have a few list of vars to set general style.

There is two special vars for convert all tags in to classes `$m-prefix-each` and add a prefix `$m-prefix`, if you left set `$m-prefix` to `null` all styles will be affect directly to html tags, and if `$m-prefix-each` is set to `false` it only create one main class that will be normalize all tags inside.

The `_normalize.scss` is the main and only file that have all rules.

You can see how all tags are formatted on `index.html` file, which use the `normalize.css` uncompressed file to load styles.


#### Rebuild your custom normalize file

Change variables on `_vars.scss` file or rules on `_normalize.scss`.
Run sass watch to get updated files and keep an eye on changes
```sh
sass --watch _normalize.scss:normalize.css --style expanded
```

Open and refresh `index.html` file to see your changes reflected.
```sh
open index.html
```

Once finish editing those files, get the compressed min file.
```sh
sass _normalize.scss:normalize.min.css --style compressed
```
___

### Tested and working
* Brave
* Chrome
* Firefox
* Opera
* Safari

### Known Issues

`[type="search"]`

It's not possible to set styles on inputs type search without hide the input first, so, it's working as textfield losing his properties... sorry. But you can apply the functionality with javascript, right?!
