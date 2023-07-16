## Detailed step-by-step instructions for setting up MongoDB and Mongo Express on Minikube:

1. Start Minikube:
    
    ```
    minikube start
    
    ```
    
2. Save the `deployment.yaml` file and apply the MongoDB deployment and service YAML using the following command:
    
    ```
    kubectl apply -f deployment.yaml
    ```
    
3. Verify that the MongoDB deployment and service are running:
    
    ```
    kubectl get deployments
    kubectl get services
    ```
    
    Ensure that both the MongoDB deployment and service have the status "Running."
    
4. Save the `mongo-express.yaml` file and apply the Mongo Express deployment and service YAML using the following command:
    
    ```
    kubectl apply -f mongo-express.yaml
    ```
    
5. Verify that the Mongo Express deployment and service are running:
    
    ```
    kubectl get deployments
    kubectl get services
    ```
    
    Ensure that both the Mongo Express deployment and service have the status "Running."
    
6. Get the Minikube IP address:
    
    ```
    minikube ip
    ```
    
    Take note of the IP address returned by this command.
    
7. Determine the assigned port for the Mongo Express service:
    
    ```
    kubectl get service mongo-express
    ```
    
    Note the port number under the "PORT(S)" column for the "mongo-express" service.
    
8. Access the Mongo Express UI using Minikube's IP and assigned port:
    
    ```
    <Minikube IP>:<assigned port>
    ```
    
    Replace `<Minikube IP>` with the IP address obtained in step 8, and `<assigned port>` with the port number obtained in step 6.
    
    Open the resulting URL in your default browser, and you should see the Mongo Express UI.
    

That's it! You have successfully set up MongoDB and Mongo Express on Minikube, and you can now use the Mongo Express UI to interact with your MongoDB deployment.