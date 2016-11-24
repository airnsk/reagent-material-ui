# Reagent Material UI
[![Clojars Project](https://img.shields.io/clojars/v/reagent-material-ui.svg)](https://clojars.org/reagent-material-ui)

A reagent wrapper for [Material UI](http://www.material-ui.com/#/) components.

Thanks to the maintainers of [reagent-material](https://github.com/tuhlmann/reagent-material), which I basically copied and turned into a package. Thanks also to [om-material-ui](https://github.com/taylorSando/om-material-ui) for providing the build process for the material ui javascript.

## Usage

Just add `[reagent-material-ui "0.2.3"]` to your `project.clj`, then require the components like so:

```clojure
(ns your-project.example
    (:require [reagent-material-ui.core :refer [AppBar Card]]))
```
#### Important note
`cljsjs/material-ui` comes with its own `cljsjs/react`. This is because it currently has to
 be built with . Read more [here](http://www.material-ui.com/#/get-started/installation). This won't be needed in a future.
 Important is to put `react` into `exclusions` in `project.clj` for libraries, which include it.
 For example:

 ```
    [reagent "0.6.0" :exclusions [cljsjs/react]]
    [devcards "0.2.1-7" :exclusions [cljsjs/react]]
 ```


You can then use the Material UI components as you would normal reagent components. See the [Material UI docs](http://www.material-ui.com/#/components/app-bar) for more info about the different components.
