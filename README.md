# Task 5: Simple Application Deployment with Helm

## File Structure

- 
- Chart-wp/Chart.yaml —  YAML file containing information about the chart
- Chart-wp/values.yaml — The default configuration values for this chart
- Chart-wp/templates/  - A directory of templates that, when combined with values,


## Objective

In this task, you will create a Helm chart for a simple application and deploy it on your Kubernetes (K8s) cluster.

## Steps

1. **Create Helm Chart**

   - Create a Helm chart for your application.

2. **Deploy the Application**

   - Deploy the WordPress application using the Helm chart.

   ```bash
   helm install my-wp ./Chart-wp --set wp.image=wordpress:6.2.1-apache --set namespace=wp --set mysql.pass=$MYSQL_PASS -n wp  --create-namespace
   ```
     
     - 
   
   - Ensure the application is accessible from the internet.

3. **Store Artifacts in Git**

   - Store the WordPress application and Helm chart in a new git repository.

4. **Verify the Application**

   - Verify that the application is running and accessible.

   ```bash
   kubectl get all -n wp
   ```

