# pizza-apiserver
An aggregated custom API server example.

## General workflow

* Get the `CustomServerOption` for the API server via the underlying `RecommendedOption` [here](https://github.com/HanFa/pizza-apiserver/blob/d86c41ae03db733440a9fcd9da6fddd262619661/pkg/cmd/server/start.go#L46)
* Start the API Server [here](https://github.com/programming-kubernetes/pizza-apiserver/blob/d86c41ae03db733440a9fcd9da6fddd262619661/pkg/cmd/server/start.go#L129), which is wrapped in a blocking cobra `Run` command
  * API installation with `rest.Storage` for pizzas and toppings
  * Register a post-start hook `start-pizza-apiserver-informers` to notify them when the HTTPS server is up and listening
  * Run the API server
* 

