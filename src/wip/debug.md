# debug

``` clojure
(ns-unalias *ns* 'http)
(ns-unmap *ns* ‘func)
```

Reload!!!
(require '[hello] :reload-all)

C-u C-M-x


# client

* http-debug-raw // request / response
* http-debug-normal // params / body {is-pretty}


# server

* http-debug-raw // request / response
* http-debug-normal // params / body {is-pretty}

## Ref

- <https://github.com/clojure/tools.namespace>
- <https://github.com/clojure-emacs/cider/blob/master/doc/debugging.md>
