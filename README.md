# Basic Hands-on (21-24)

1. Create a Pod named **`webapp-pod`** with the image **`nginx:1.19`** and label it with **`app=webapp`**
2. Expose the Pod **`webapp-pod`** on port 80 using a Service named **`webapp-service`** and expose it internally within the cluster.
3. Scale the Pod **`webapp-pod`** to 3 replicas using a Deployment named **`webapp-deployment`**.
4. Update the image of the Deployment **`webapp-deployment`** to **`nginx:1.21`** and verify the rollout status.
5. Roll back the Deployment **`webapp-deployment`** to the previous version and ensure all replicas are running the previous image.
6. Create a ConfigMap named **`app-config`** with the key-value pair **`app.color=blue`** and use it to set an environment variable in the Pod **`webapp-pod`**.
7. Create a Secret named **`db-credentials`** with the data **`username=admin`** and **`password=secret`** and use it as environment variables in the Pod **`webapp-pod`**.
8. Create a Namespace named **`webapp-namespace`** and create the Pod **`webapp-pod`** and Service **`webapp-service`** within that namespace.
9. Get the logs of the Pod **`webapp-pod`** and save them to a file named **`webapp-logs.txt`**.
10. Create a PersistentVolume named **`data-pv`** with a storage capacity of 1Gi, hostPath as the storage type, and the path as **`/data`**.
11. Create a PersistentVolumeClaim named **`data-pvc`** requesting a storage capacity of 500Mi and use it to mount the volume in the Pod **`webapp-pod`** at the path **`/data`**.  **CHECK**
12. Create a readiness probe for the Pod **`webapp-pod`** that performs an HTTP GET request on the path **`/health`** and port 80.
13. Create a liveness probe for the Pod **`webapp-pod`** that performs an HTTP GET request on the path **`/`** and port 80.
14. ~~Create a Job named **`backup-job`** that runs the command **`pg_dump`** on a PostgreSQL database container.~~
15. ~~Create a CronJob named **`cleanup-cronjob`** that runs a cleanup script every day at 2:00 AM.~~
16. ***Create a Horizontal Pod Autoscaler for the Deployment `webapp-deployment` that targets an average CPU usage of 50% and a minimum of 2 replicas. (Still Beta version)***
17. Create a NetworkPolicy that allows incoming connections to the Pod **`webapp-pod`** only from Pods within the same Namespace with the label **`app=webapp-client`**.
18. Create a ResourceQuota named **`webapp-quota`** for the Namespace **`webapp-namespace`** that limits the total number of Pods to 5, total memory to 2Gi, and total CPU to 2.
19. Create a LimitRange named **`webapp-limits`** for the Namespace **`webapp-namespace`** that sets the default memory limit for Containers to 500Mi and the CPU limit to 200m.
20. ~~Create a PodDisruptionBudget named **`webapp-pdb`** for the Deployment **`webapp-deployment`** that allows at most 1 unavailable Pod at a time.~~ (out of scope)
21. ~~Create a PodSecurityPolicy named **`webapp-psp`** that requires Pods to run with a non-root user and drop the capabilities **`SYS_ADMIN`** and **`SYS_RAWIO`**.~~ **(Out of exam scope)**
22. Create an Ingress named **`webapp-ingress`** that routes traffic to the Service **`webapp-service`** on the path **`/webapp`**.
23. Attach a PersistentVolume to the Pod **`webapp-pod`** using a PersistentVolumeClaim and mount it at the path **`/data`**.
24. Create a ServiceAccount named **`webapp-service-account`** and assign it to the Pod **`webapp-pod`**.
25. Update the imagePullPolicy of the Deployment **`webapp-deployment`** to **`Always`** to ensure the latest image is always pulled.
26. Label the Pod **`webapp-pod`** with the key-value pair **`environment=production`** and verify the label using **`kubectl`**.
27. Delete the Service **`webapp-service`** and ensure the associated Pods are not affected.
28. ~~Create a Namespace named **`monitoring-namespace`** and create a Prometheus instance within that namespace.~~ **(Out of exam scope)**
29. ~~Create a ServiceMonitor that monitors the Pods with the label **`app=webapp`** and scrapes the **`/metrics`** endpoint.~~ **(Out of exam scope)**
30. Export the resources of the **`webapp-namespace`** and save them to a file named **`webapp-resources.yaml`**.
