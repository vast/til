## Задавать переменные окружения в шебанге

```javascript
#!/usr/bin/env NODE_PATH=foo/app nodejs

require('models/foo'); // require('foo/app/models/foo')
```
