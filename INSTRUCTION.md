Use the following instructions below:

1. All instructions:
    - how to deploy daemonset.yml and cronjob.yml to the cluster:
        kubectl apply -f .infrastructure/daemonset.yml
        kubectl apply -f .infrastructure/cronjob.yml
        

    - how to validate the solution (Logs for the daemonset and cronjob should be present)
        kubectl apply -f .infrastructure/todoapp-pod.yml
        kubectl apply -f .infrastructure/clusterIp.yml

        kubectl logs test-daemon-set-7czf4 -n mateapp
        kubectl logs test-cronjob-29820696-dtgls -n mateapp

        Log information for daemonset you can find in /logs/daemonset.log and for cronjob in /logs/cronjob.log.