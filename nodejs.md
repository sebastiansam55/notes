## Test HTTPS certificate
Used for testing if the SSL certificates are in the correct format for node to understand.

```
const https = require('https');
const fs = require('fs');

const options = {
  key: fs.readFileSync('./ssl/server.key'),
  cert: fs.readFileSync('./ssl/server.crt')
};

https.createServer(options, function (req, res) {
  res.writeHead(200);
  res.end("hello world\n");
}).listen(800);
```

## Manually generate password hash for use with formio
```
const bcrypt = require('bcrypt');
const { Console } = require('console');

function genPassword(text){
    bcrypt.genSalt(10, function(err, salt) {

        bcrypt.hash(text, salt, function(error, hash) {

            console.log(hash);
        });
    });
}

genPassword(process.argv[2])
```