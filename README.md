# kubernetes_deployment
Key  | Type | Required  | Description | Default
------------- | ------------- | ------------- | ------------- | -------------
metadata | map  | true | Standard deployment's metadata.  | none 
spec  | map  | true  |  Defines the specification of the desired behavior of the deployment.  | none
spec.selector | map | false | A label query over pods that should match the Replicas count. | none
spec.template  | map  | true  | Describes the pod that will be created if insufficient replicas are detected.  | none   
spec.template.metadata  | map  | true  | Standard  metadata.  | none
spec.template.container  | map  | false  | List of containers belonging to the pod.   | none
spec.container.resources  | map  | false  | Compute Resources required by this container.  | none
spec.resources.limits  | map  | false  | Describes the maximum amount of compute resources allowed.   | none
spec.resources.requests  | map  | false  | Describes the minimum amount of compute resources required.  | none  
container.liveness_probe   | map  | false  | Periodic probe of container liveness.  | none
liveness_probe.http_get  | map  | false  | Specifies the http request to perform.  | none
liveness_probe.http_get.http_header  | map  | false  | Scheme to use for connecting to the host.  | none
liveness_probe.initial_delay_seconds  | string  | false  | Number of seconds after the container has started before liveness probes are initiated.  | none
liveness_probe.period_seconds  | string  | false  | How often (in seconds) to perform the probe  | 30s
