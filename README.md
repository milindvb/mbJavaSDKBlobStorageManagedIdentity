to run this code

clone
In pom.xml:
Update values of resource group and appname (search "changeThis" in the file to find the update spots)

In /src/main/java/com/example/springboot/HelloController.java  :
Update mystorage1 to your storage account name
String endpoint = String.format(Locale.ROOT, "https://%s.blob.core.windows.net", "myteststorage1");


mvn clean package -DskipTests

to deploy

mvn azure-webapp:deploy

In webapp, enable System Assigned Managed identity

In storage account
Add Roles following roles for Storage account:
Contributor
Storage Blob Data Contributor
Storage Queue Data Contributor

Access your app in browser and check the output
