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

# kubernetes_service
Key  | Type | Required  | Description | Default
------------- | ------------- | ------------- | ------------- | -------------
metadata | map  | true | Standard service's metadata.  | none 
spec  | map  | true  | Defines the behavior of a service.  | none
spec.port  | map  | true  | The list of ports that are exposed by this service.  | none
spec.container  | map  | false  | List of containers belonging to the pod.   | none

# kubernetes_pod
Key  | Type | Required  | Description | Default
------------- | ------------- | ------------- | ------------- | -------------
metadata | map  | true | Standard pod's metadata.  | none 
spec  | map  | true | Spec of the pod owned by the cluster  | none
spec.container  | map  | false | List of containers belonging to the pod.  | none
spec.container.env  | map  | false  | Block of string name and value pairs to set in the container's environment.  | none
spec.container.port  | map  | false  | Block(s) of ports to expose on the container. Exposing a port here gives the system additional information about the network connections a container uses, but is primarily informational. Not specifying a port here DOES NOT prevent that port from being exposed. Any port which is listening on the default "0.0.0.0" address inside a container will be accessible from the network.  | none
container.liveness_probe  | map  | false  | Periodic probe of container liveness.  | none
liveness_probe.http_get  | map  | false  | Specifies the http request to perform.  | none
liveness_probe.http_get.http_header  | map  | false  | Scheme to use for connecting to the host.  | none
spec.dns_config  | map  | false  | Specifies the DNS parameters of a pod.  | none
spec.dns_config.option  | map  | false  | A list of DNS resolver options specified as blocks with name/value pairs. This will be merged with the base options generated from DNSPolicy. Duplicated entries will be removed. Resolution options given in Options will override those that appear in the base DNSPolicy.  | none

# kubernetes_secret
Key  | Type | Required  | Description | Default
------------- | ------------- | ------------- | ------------- | -------------
metadata | map  | true | Standard secret's metadata.  | none 
data  | map  | false | A map of the secret data.  | none
type  | map  | false  | The secret type.  | none

# kubernetes_config_map
Key  | Type | Required  | Description | Default
------------- | ------------- | ------------- | ------------- | -------------
metadata | map  | true | Standard config map's metadata. | none 
data  | map  | false  | Data contains the configuration data.  | none
binary_data  | map  | false  | BinaryData contains the binary data.  | none

# kubernetes_job
Key  | Type | Required  | Description | Default
------------- | ------------- | ------------- | ------------- | -------------
metadata | map  | true | Standard resource's metadata.  | none 
spec  | map  | true  | Specification of the desired behavior of a job.  | none
spec.template  | map  | false  | Describes the pod that will be created when executing a job.  | none
spec.template.metadata  | map  | true  | Standard  metadata.  | none
spec.container  | map  | false  | List of containers belonging to the pod.  | none

# kubernetes_cron_job
Key  | Type | Required  | Description | Default
------------- | ------------- | ------------- | ------------- | -------------
metadata | map  | true | Standard resource's metadata.  | none 
spec  | map  | true  | Spec defines the behavior of a CronJob.  | none
spec.job_template  | map  | true  | Specifies the job that will be created when executing a CronJob.  | none
spec.job_template.metadata  | map  | true  | Standard object's metadata of the jobs created from this template.  | none
spec.job_template.spec  | map  | true  |  Specification of the desired behavior of the job.  | none
spec.container  | map  | false  | List of containers belonging to the pod. | none

# kubernetes_horizontal_pod_autoscaler
Key  | Type | Required  | Description | Default
------------- | ------------- | ------------- | ------------- | -------------
metadata | map  | true | Standard horizontal pod autoscaler's metadata.  | none 
spec  | map  | true  | Behaviour of the autoscaler.  | none
spec.scale_target_ref  | map  | true  | Reference to scaled resource. e.g. Replication Controller  | none
spec.metric  | map  | false  | A metric on which to scale.  | none
spec.metric.external  | map  | false  | A global metric that is not associated with any Kubernetes object.  | none
spec.metric.selector  | map  | false  | The label selector for the given metric  | none
spec.external.target  | map  | true  | The target for the given metric.  | none

# kubernetes_service_account
Key  | Type | Required  | Description | Default
------------- | ------------- | ------------- | ------------- | -------------
metadata | map  | true | Standard service account's metadata.  | none 
secret  | map  | false  | A list of secrets allowed to be used by pods running using this Service Account.  | none
secret.metadata  | map  | true  | Standard metadata. | none

# kubernetes_stateful_set
Key  | Type | Required  | Description | Default
------------- | ------------- | ------------- | ------------- | -------------
metadata | map  | true | Standard Kubernetes object metadata.  | none 





