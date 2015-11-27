# where-is-module

This is a bash script that takes a module name as an argument and searches the current and
sub-directories for what javascript files that module is required in and what line in those 
files the corresponding reference name is called in each file.

On the command line:
```
$where-is-module modulename
```

Or add this `whereis` key/value pair to your `package.json` scripts objects:
```
"scripts": {
    "whereis": "where-is-module"
}
```

Then run:
```
$npm run whereis my-fun-module
```

Outputs:
```
./index.js
     6  var funstuff = require('my-fun-module')
    17      results = funstuff('one', 'two')
```

### install

Copy the `./bin/where-is-module` program to your computer, make it executable, and be sure the
installation directory is in your $PATH.

### license

MIT
