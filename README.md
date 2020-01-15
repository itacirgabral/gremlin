# Gremlin

## [air-routes.graphml](https://github.com/krlawrence/graph/tree/master/sample-data)

```bash
git clone https://github.com/itacirgabral/gremlin
cd gremlin
docker run -v $(pwd)/data:/opt/gremlin/data  --rm -it cruftlab/gremlin-console
```

```groove
conf = new BaseConfiguration()
conf.setProperty("gremlin.tinkergraph.vertexIdManager","LONG")
conf.setProperty("gremlin.tinkergraph.edgeIdManager","LONG")
conf.setProperty("gremlin.tinkergraph.vertexPropertyIdManager","LONG");[]
graph = TinkerGraph.open(conf)
graph.io(graphml()).readGraph('data/air-routes.graphml')
g=graph.traversal()
:set max-iteration 1000
```