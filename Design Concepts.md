# Design Concepts

##### Identify the number of containers created in the red pod.
  ```kubectl describe pod```

##### Identify the name of the containers running in the blue pod.

##### Create a multi-container pod with 2 containers.

Use the spec given below.

If the pod goes into the crashloopbackoff then add the command sleep 1000 in the lemon container.

##### We have deployed an application logging stack in the elastic-stack namespace. Inspect it.


##### Before proceeding with the next set of questions, please wait for all the pods in the elastic-stack namespace to be ready. This can take a few minutes.

Once the pod is in a ready state, inspect the Kibana UI using the link above your terminal. There shouldn't be any logs for now.


##### We will configure a sidecar container for the application to send logs to Elastic Search.

NOTE: It can take a couple of minutes for the Kibana UI to be ready after the Kibana pod is ready.

You can inspect the Kibana logs by running:

```kubectl -n elastic-stack logs kibana```

Inspect the app pod and identify the number of containers in it.


It is deployed in the elastic-stack namespace.

##### The application outputs logs to the file /log/app.log. View the logs and try to identify the user having issues with Login.


Inspect the log file inside the pod.


##### Edit the pod to add a sidecar container to send logs to Elastic Search. Mount the log volume to the sidecar container.

Only add a new container. Do not modify anything else. Use the spec provided below.




Note: State persistence concepts are discussed in detail later in this course. For now please make use of the below documentation link for updating the concerning pod.



https://kubernetes.io/docs/tasks/access-application-cluster/communicate-containers-same-pod-shared-volume/


##### Inspect the Kibana UI. You should now see logs appearing in the Discover section.


You might have to wait for a couple of minutes for the logs to populate. You might have to create an index pattern to list the logs. If not sure check this video: https://bit.ly/2EXYdHf
