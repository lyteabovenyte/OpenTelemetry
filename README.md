##### OpenTelemetry using Go
###### In this example of using OpenTelemetry for ingesting, transforming, and exporting logs, we will use docker-compose to set up an environment that will simulate a Kubernetes host, with logs stored under /var/logs/pods/*/*/*.log. The OTel Collector will act as an agent running on the host. The logs will be ingested from the files in the log path, routed to appropriate operators in the filelog receiver, parsed per their particular format, have parsed attributes standardized, and then exported to STDOUT through the logging exporter.

###### *Logging* directory:
- The docker-compose.yml file contains the service definition where we will run the OTel Collector and mount the collector configuration and log files directory, varlogpods, to simulate the collector running on a Kubernetes host.
