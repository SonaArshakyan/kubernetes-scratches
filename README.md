# kubernetes-scratches

This is very basic deployment of two application : mongo db and mongo express.

1 MongoDB Deployment: We'll deploy MongoDB as a Kubernetes Deployment. This ensures that the MongoDB pod can be scaled and managed easily. The MongoDB pod will only be accessible internally within the Kubernetes cluster. We'll create an internal Service to allow communication between other components in the cluster and MongoDB.

2 Secret for Sensitive Data: We'll create a Kubernetes Secret to store sensitive data such as usernames and passwords. This Secret will be used to securely provide authentication credentials to MongoDB and MongoDB Express.

3 Mongo Express Deployment: MongoDB Express will be deployed as a separate pod in the cluster. To enable external access, we'll create a Service of type LoadBalancer or NodePort for MongoDB Express. This allows external requests to reach MongoDB Express while ensuring that MongoDB remains isolated internally.

4 ConfigMap for External Configuration: We'll create a ConfigMap to store external configuration data, such as connection strings or environment variables. This ConfigMap will be mounted as a volume in the MongoDB Express pod, allowing MongoDB Express to access external configuration settings.per

