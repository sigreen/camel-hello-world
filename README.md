# Camel Log QuickStart

This quickstart shows a simple Apache Camel application that logs a message to the server log every 5th second.

This example is implemented using solely the XML DSL (there is no Java code). The source code is provided in the following XML file `src/main/resources/OSGI-INF/blueprint/camel-log.xml`.

This example uses a timer to trigger every 5th second, and then writes a message to the server log.

The goals karaf:assembly and karaf:archive MUST be called to create the custom karaf assembly as shown in the command below -

    mvn clean install karaf:assembly karaf:archive

# Running on OpenShift v3

You can run this application on OpenShift using the Source 2 Image builders like this:

   `oc new-app --strategy=source fabric8/s2i-karaf:1.1.5~https://github.com/<YOUR-REPO>/camel-hello-world`
