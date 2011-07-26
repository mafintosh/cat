# cat

cat takes an scheme based url and reads it's endpoint. it's available through npm

	npm install cat
	
currently supported protocols are `file`, `http` and `https`.

it's easy to use

```js
var cat = require('cat');

// you can read files 
cat('myfile.txt', console.log);             // reads the file as utf-8 and returns it output
cat('file://myfile.txt', console.log);      // same as above

// or http / https urls
cat('http://google.com', console.log);      // cat also follows any redirects
cat('https://github.com', console.log);     // and cat read https
cat('http://fail.google.com', console.log); // if a status code != 2xx is received it will 
                                            // call the callback with an error.

```