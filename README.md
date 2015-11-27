# where-is-module

This is a bash script that takes a module name as an argument and searches the current and
sub-directories for what files that module is required in and where in those files the 
corresponding reference name is called in each file.

On the command line:
```
$whereismodule modulename
```

Or add this to your `package.json` scripts objects:
```
whereis: "whereismodule"
```

Then run:
```
$npm run whereis path
```

Outputs:
```
./index.js
     6  var path = require('path')
    17      this.st = ecstatic(path.join(__dirname, 'public'))
./lib/router.js
     3  var path = require('path')
```

### install

Copy the `./bin/where-is-module` program to your computer, make it executable, and be sure the
installation directory is in your $PATH.

### license

MIT
