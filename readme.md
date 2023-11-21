# VMware Tanzu GemFire @Cacheable REST Demo

VMware Tanzu GemFire is a distributed, in-memory, key-value store that performs read and write operations at blazingly fast speeds. It offers highly available parallel message queues, continuous availability, and an event-driven architecture you can scale dynamically, with no downtime. As your data size requirements increase to support high-performance, real-time apps, Tanzu GemFire can scale linearly with ease.

VMware Tanzu GemFire for Kubernetes brings the power of GemFire to Kubernetes.    Tanzu GemFire for Kubernetes enables users create, update, scale and manage GemFire with ease.

## How to run

1. Install GemFire - https://docs.vmware.com/en/VMware-GemFire/10.0/gf/getting_started-installation-install_intro.html
2. From the scripts directory run [`./start_gemfire.sh`](scripts/start_gemfire.sh)
3. From the project directory build and run the spring boot application [`./gradlew bootRun`](build.gradle)
4. Call the rest service with a location and see the performance differance between the two calls.  
   * `curl http://localhost:8080/search?location=94111`
   * That will give a query for all the bikes in the San Francisco area that are affected.
5. To shutdown GemFire from the scripts directory run [`./shutdown_gemfire.sh`](scripts/shutdown_gemfire.sh)