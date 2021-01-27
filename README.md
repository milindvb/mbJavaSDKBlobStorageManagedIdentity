**To run this code**

1.
# Clone and update files

  1.
## In pom.xml:

Update values of resource group and appname (search &quot;changeThis&quot; in the file to find the update spots)

  1.
## In /src/main/java/com/example/springboot/HelloController.java :

Update mystorage1 to your storage account name

String endpoint = String.format(Locale.ROOT, &quot;https://%s.blob.core.windows.net&quot;, &quot;myteststorage1&quot;);

mvn clean package -DskipTests

1.
# Deploy webapp

mvn azure-webapp:deploy

1.
# In webapp, enable System Assigned Managed identity

1.
# In storage account

Add Roles following roles for Storage account:

Contributor

Storage Blob Data Contributor

Storage Queue Data Contributor

Access your app in browser and check the output
