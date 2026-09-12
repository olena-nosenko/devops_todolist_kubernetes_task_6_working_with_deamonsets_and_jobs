Use the following instructions below:

Prerequisites

* Kubernetes cluster
* Existing todoapp deployment (todoapp-pod.yml)
* Existing ClusterIP service for todoapp (clusterIp.yml)
* Namespace `mateapp`

1. All instructions:
    - how to deploy daemonset.yml and cronjob.yml to the cluster:
        kubectl apply -f .infrastructure/daemonset.yml
        kubectl apply -f .infrastructure/cronjob.yml
        

    - how to validate the solution (Logs for the daemonset and cronjob should be present)
        kubectl get pods -n mateapp
        kubectl logs <daemonset-pod-name> -n mateapp

        kubectl get cronjob -n mateapp
        kubectl get jobs -n mateapp
        kubectl logs job/<job-pod-name> -n mateapp
        
        Log information for daemonset you can find in /logs/daemonset.txt and for cronjob in /logs/cronjob.txt.