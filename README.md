# This App Service example will download a file from Azure blob storage using System Assigned Managed Identity and Azure blob storage Java SDK.
**To run this code**


# Clone and update files


## In pom.xml:

Update values of resource group and appname (search &quot;changeThis&quot; in the file to find the update spots)


## In /src/main/java/com/example/springboot/HelloController.java :

Update mystorage1 to your storage account name

String endpoint = String.format(Locale.ROOT, &quot;https://%s.blob.core.windows.net&quot;, &quot;myteststorage1&quot;);

mvn clean package -DskipTests


# Deploy webapp

mvn azure-webapp:deploy


# In webapp, enable System Assigned Managed identity


# In storage account

Add Roles following roles for Storage account:

Contributor

Storage Blob Data Contributor

Storage Queue Data Contributor

# Access your app in browser and check the output
