START
Basic
Front: Describe the `lookup` function. What does it do, what arguments does it have, which of them are optional? What does it return, how to work with the result? How does it work, and what are its limitations?
Back: 
The `lookup` function looks up resources in a running cluster.  
  
The arguments of the function are **apiVersion**, **kind**, **namespace** and **name**, all **string**s. The **name** and **namespace** arguments are optional. The function returns a resource (a dictionary) or a list. If no resources are found, it returns an empty object.  
  
When the function returns an object, you can navigate it to extract specific values:  

```go
(lookup "v1" "Namespace" "" "mynamespace").metadata.annotations

```

When `lookup` returns a list of objects, you can access it via the `items` field:  

```go
{{ range $index, $service := (lookup "v1" "Service" "mynamespace" "").items }}
    {{/* do something with each service */}}
{{ end }}
```

The function uses Helm's existing Kubernetes connection configuration to query Kubernetes. The template processing will fail in case of any API errors.  
  
Helm is not supposed to contact the Kubernetes API Server during a `helm template` or a `helm install|upgrade|delete|rollback --dry-run`, so the `lookup` function will return an empty list (i.e. dict) in such a case.  
  
Source: [https://helm.sh/docs/chart_template_guide/functions_and_pipelines/#using-the-lookup-function](https://helm.sh/docs/chart_template_guide/functions_and_pipelines/#using-the-lookup-function)
<!--ID: 1745135900089-->
END
