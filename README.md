# spring-actuator

1. Spring Boot Actuator Module
<br/>Spring boot’s module Actuator allows you to monitor and manage application usages in production environment, without coding and configuration for any of them. 
This monitoring and management information is exposed via REST like endpoint URLs.

2. Important Actuator Endpoints
<br/>Most applications exposes endpoints via HTTP, where the ID of the endpoint along with a prefix of /actuator is mapped to a URL. 
For example, by default, the health endpoint is mapped to /actuator/health.
By default, only /health and /info are exposed via Web APIs. Rest are exposed via JMX. Use management.endpoints.web.exposure.include=* to expose all endpoints through the Web APIs.

#####application.properties
#####management.endpoints.web.exposure.include=*
 
#####To expose only selected endpoints
#####management.endpoints.jmx.exposure.include=health,info,env,beans
<br/>

ENDPOINT --> USAGE
<br/>/auditevents --> Returns all auto-configuration candidates and the reason why they ‘were’ or ‘were not’ applied.
<br/>/beans --> Returns a complete list of all the Spring beans in your application.
<br/>/mappings --> Displays a collated list of all @RequestMapping paths..
<br/>/env --> Returns list of properties in current environment
<br/>/health --> Returns application health information.
<br/>/caches --> It exposes available caches.
<br/>/conditions --> Shows the conditions that were evaluated on configuration and auto-configuration.
<br/>/configprops --> It displays a collated list of all @ConfigurationProperties.
<br/>/integrationgraph --> It shows the Spring Integration graph. Requires a dependency on spring-integration-core.
<br/>/loggers --> The configuration of loggers in the application..
<br/>/scheduledtasks --> Displays the scheduled tasks in the application.
<br/>/sessions --> Returns trace logs (by default the last 100 HTTP requests). Requires an HttpTraceRepository bean.
<br/>/httptrace --> It allows retrieval and deletion of user sessions from a Spring Session-backed session store. Requires a Servlet-based web application using Spring Session.
<br/>/shutdown --> Lets the application be gracefully shutdown. Disabled by default.
<br/>/threaddump --> It performs a thread dump.
<br/>/metrics --> It shows several useful metrics information like JVM memory used, system CPU usage, open files, and much more.
<br/>/heapdump --> Returns an hprof heap dump file.
<br/>/logfile --> Returns the contents of the logfile if logging.file.name or logging.file.path properties have been set.