# Any.do API (unofficial)
This API allows to list and add tasks and also get auth token

## Installation
```bash
npm install anydo-api
```
## Example
```js
const Api = require('anydo-api');

const api = new Api('your_email', 'your_password');

api.addTask({title: 'from api'})
    .then(() => api.sync())
    .then(res => {
        console.log(res.models.task.items.map(t => t.title))
    });
```

## CLI
[Any.DO CLI](https://github.com/davoam/anydo-cli)
