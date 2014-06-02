#tw5-jsxgraph-widget

JSXGraph Widget for TiddlyWiki5

#Usage

In your tiddler use the ```jsxgraph``` widget like this:

```
<$jsxgraph width="600px" height="400px" id="aJSXGraph">
var brd = JXG.JSXGraph.initBoard('aJSXGraph',
           {axis:true,originX: 250, originY: 250, unitX: 50, unitY: 25});
...
</$jsxgraph>
```

Check the demo at [$:/plugins/kpe/jsxgraph/jsxgraph.demo.tid]($:/plugins/kpe/jsxgraph/jsxgraph.demo.tid).

