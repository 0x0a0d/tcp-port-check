# tcp-port-check

NodeJS tcp open port check

## Author

0x0a0d

## Usage

```javascript
const TCPPortCheck = require('tcp-port-check')

let checker = new TCPPortCheck({
    timeout: 3000,
    getBanner: 512
})

checker
    .check('127.0.0.1', 9050)
    .check('127.0.0.1', 6942)
    .on('done', (ip, port, result) => {
        console.log(ip, port, result)
    })
```
