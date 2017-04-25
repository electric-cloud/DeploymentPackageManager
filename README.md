Manifest files in the SampleManifests can be used to create Deployment package. Once you create the Deployment Package you can use the 'createApplicationFromDeploymentPackage' API to create an Electric Flow deploy application based on the manifest definition included with the package.

Currently we support the following Application Servers from the Deployment package 
1. JBOSS
2. Tomcat
3. WebSphere
4. WebLogic
5. IIS

Sample API usage from CLI
ectool createApplicationFromDeploymentPackage org.ec hello 1.0 hellopackage.zip --retrieveToFolder /tmp

API assumes you have already uploaded your package to the Flow application repository flowing the GAV ( Group-artifactKey-version ) naming convention as described in Deployment package manager documentation.

DSL used by the the package manager is defaulted from the Service Catalog Item that is referenced by the server property
Administration -> ec_selfservice -> defaultPackageManagerCatalogItem -> "Deployment Package Manager"
