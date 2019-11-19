# kubernetesserviceswithistio
istio service example

this is basic example of istio service mesh entire arch build on gcloud.
special do not use googel istio ,build the istio control pane on your own , 
requirements:

PS D:\kubernetes\istioControlPane\servicediscovery> kubectl get namespaces -L istio-injection
NAME              STATUS   AGE   ISTIO-INJECTION
default           Active   35h   enabled
istio-system      Active   35h
kube-node-lease   Active   35h
kube-public       Active   35h
kube-system       Active   35h

istio injection should be enabled for the namespace you are running or creating virtual service or gateway.

hellovirtualservice.yaml
hellowroldgateway.yaml

these two files conatins the code for istio enablement please go through them
gateway service actualy defines the port it will open for external traffic and virtualgateway workd like nginx proxy and it will route traffic  to the acual service.
it supports canary will add them after some time.
