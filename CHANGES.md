## 2.9.10.28

- updated dependencies, latest `conman` release supports setting `doc` meta for generated functions
 
## 2.9.10.27

- ClojureScript cleanup

## 2.9.10.25

- added [lein-test-refresh](https://github.com/jakemcc/lein-test-refresh) to default dev plugins

## 2.9.10.24

- fixed bootstrap styling for navbar

## 2.9.10.23

- added `^{:on-reload :noop}` for HTTP/nREPL server states

## 2.9.10.21

- fixed regression with loading exteranl logging configuration

## 2.9.10.19

- enables the Figwheel REPL via this [PR](https://github.com/luminus-framework/luminus-template/pull/213), it's now possible to start and stop the figwheel compiler from the `user` namespace by running `start-fw` and `stop-fw` respectively. The ClojureScript REPL is start by running `cljs`. 

## 2.9.10.18

- fixed a regression in the `+war` profile

## 2.9.10.16

- added a default validation `cljc` namespace

## 2.9.10.15

- switched to use [profile-dependent target path to avoid cross-profile contamination](https://github.com/luminus-framework/luminus-template/pull/210)

## 2.9.10.6

- switched to using [cprop](https://github.com/tolitius/cprop) as the default configuration system
- updated to use [mount](https://github.com/tolitius/mount) for manging HTTP/nREPL server lifecycle
- removed init/destroy functions from handler unless using +war profile
- war profile defaults to putting the core namespace in the dev source path
- war profile sets up mock JNDI in the core namespace
- war profile puts HTTP server dependency under the dev profile
 
## 2.9.9.7

- switched from using Yesql to [HugSQL](http://www.hugsql.org/), see documentation for syntactic differences for SQL queries
- as a result of moving to HugSQL, [conman](https://github.com/luminus-framework/conman) no longer requires an atom to hold the connection 

## 2.9.9.2

- updated to use a single `src` source path. The sources are found under `src/clj`, `src/cljc`, and `src/cljs` respectively.
- updated to latest compojure-api, see [official changelog](https://github.com/metosin/compojure-api/blob/master/CHANGELOG.md) for the syntactic changes
- updated to use cljs-ajax interceptors to provide default `Accept` and `x-csrf-token` headers
- updated to automatically generate ClojureScript test scaffolding when the `+cljs` flag is used 

## 2.9.9.0

- added font awesome to the template

## 2.9.8.99

- switched to Bootstrap 4
- factored out logging to a plugin, allows for future alternate logging implementations, e.g: Timbre

## 2.9.8.96

- default HTTP port for production is now found in `prod/env/config.edn`

## 2.9.8.94

- switched to using [luminus/config](https://github.com/luminus-framework/config) instead of environ
- dev profile now provides a `user` namespace

## 2.9.8.93

- switched to Clojure 1.8

## 2.9.8.92

- split out log config to dev/prod profiles

## 2.9.8.85

- moved out HTTP/nREPL servers into plugins

## 2.9.8.79
 
- switched to using log4j as the default logger