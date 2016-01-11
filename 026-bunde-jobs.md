## bundle install --jobs

`bundle` умеет скачивать и устанавливать гемы параллельно:

```shell
bundle install --jobs 4
```

Из [документации](http://bundler.io/v1.11/man/bundle-install.1.html):

> --jobs=[&lt;number&gt;]  
> The maximum number of parallel download and install jobs. The default is 1.
