Use the following instructions below:

1. All instructions:
    - how to deploy daemonset.yml and cronjob.yml to the cluster:
        kubectl apply -f .infrastructure/daemonset.yml
        kubectl apply -f .infrastructure/cronjob.yml
        

    - how to validate the solution (Logs for the daemonset and cronjob should be present)
        kubectl apply -f .infrastructure/todoapp-pod.yml
        kubectl apply -f .infrastructure/clusterIp.yml

        kubectl get daemonset -n mateapp
        kubectl logs daemonset/test-daemon-set -n mateapp

        kubectl get job -n mateapp
        kubectl logs job/test-cronjob-29820696-dtgls -n mateapp
        
        Log information for daemonset you can find in /logs/daemonset.txt and for cronjob in /logs/cronjob.txt.