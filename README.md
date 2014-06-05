#[tw5-jsxgraph-widget](https://kpe.github.io/tw5-jsxgraph-widget/)

A [JSXGraph](http://jsxgraph.uni-bayreuth.de/) Widget for [TiddlyWiki5](tiddlywiki.com).

#[Usage](https://kpe.github.io/tw5-jsxgraph-widget/)

In your tiddler use the ```jsxgraph``` widget like this:

```
<$jsxgraph width="600px" height="400px">
var brd = JXG.JSXGraph.initBoard('ignored',
           {axis:true,originX: 250, originY: 250, unitX: 50, unitY: 25});
...
</$jsxgraph>
```

Note that the first argument to ```initBoard()``` will be ignored (and set internally by the widget).

Check the demo at [$:/plugins/kpe/jsxgraph/jsxgraph.demo.tid](https://kpe.github.io/tw5-jsxgraph-widget/).

## Dev notes
When updating [jsxgraphcore.js](https://raw.githubusercontent.com/jsxgraph/jsxgraph/master/distrib/jsxgraphcore.js)
consider, that the distribution of [JSXGraph](https://github.com/jsxgraph/jsxgraph) uses 
requirejs through almond, and it somehow does not load properly in node's CommonJS.
 
As a workaround replace the

```js
    require("../build/core.deps.js")}();
```
at the end of the last line with:

```js
    module.exports = require("../build/core.deps.js")}();
```
