# Constrained Device Application (Connected Devices)

## Lab Module 08

Be sure to implement all the PIOT-CDA-* issues (requirements) listed at [PIOT-INF-08-001 - Lab Module 08](https://github.com/orgs/programming-the-iot/projects/1#column-10488501).

### Description

NOTE: Include two full paragraphs describing your implementation approach by answering the questions listed below.

What does your implementation do? 

The Constrained Device Application's (CDA) CoAP server implementation facilitates communication with the Gateway Device Application (GDA) using the Constrained Application Protocol (CoAP). Specifically, it supports two main functionalities: First, the server handles incoming ActuatorData updates sent by the GDA, validating and processing the received JSON-formatted data. Second, it provides access to SensorData and SystemPerformanceData through "Get" requests initiated by the GDA. The server's resource handlers, such as UpdateActuatorResourceHandler, ensure the proper validation and handling of incoming ActuatorData, while the "Get" handlers, like GetTelemetryResourceHandler and GetSystemPerformanceResourceHandler, enable the GDA to retrieve telemetry and system performance data. The implementation also supports observability, allowing the GDA to receive updates when new data is available. This CoAP server establishes a crucial link between the GDA and CDA for seamless data exchange in IoT applications.

How does your implementation work?

The CoAP server in the CDA functions by creating resource handlers for different types of data interactions. When the GDA sends ActuatorData updates, the UpdateActuatorResourceHandler processes the incoming data, ensuring its validity, and then passes it to the DeviceDataManager. This data manager, acting as the orchestrator, decides whether to further process the actuation data or log it based on additional validation. On the other hand, when the GDA requests SensorData or SystemPerformanceData, the corresponding "Get" resource handlers respond with the requested data. These handlers are linked to the DeviceDataManager, allowing the manager to notify the GDA when new telemetry or system performance data is available. Overall, the CDA's CoAP server establishes a bidirectional communication channel, enabling coordinated interactions between the GDA and CDA components in the IoT ecosystem.

### Code Repository and Branch

NOTE: Be sure to include the branch (e.g. https://github.com/programming-the-iot/python-components/tree/alpha001).

URL: https://github.com/ShahzabeM/CDA-Python

### UML Design Diagram(s)

NOTE: Include one or more UML designs representing your solution. It's expected each
diagram you provide will look similar to, but not the same as, its counterpart in the
book [Programming the IoT](https://learning.oreilly.com/library/view/programming-the-internet/9781492081401/).

![image](https://github.com/JadEletry/book-exercise-docs/assets/71851213/cf3b672a-ff0a-487b-ad6c-08e2378d7d46)

### Unit Tests Executed

NOTE: TA's will execute your unit tests. You only need to list each test case below
(e.g. ConfigUtilTest, DataUtilTest, etc). Be sure to include all previous tests, too,
since you need to ensure you haven't introduced regressions.


### Integration Tests Executed

NOTE: TA's will execute most of your integration tests using their own environment, with
some exceptions (such as your cloud connectivity tests). In such cases, they'll review
your code to ensure it's correct. As for the tests you execute, you only need to list each
test case below (e.g. SensorSimAdapterManagerTest, DeviceDataManagerTest, etc.)

PIOT-CDA-08-004 - Integration Test
![image](https://github.com/JadEletry/book-exercise-docs/assets/71851213/4651a12e-4d16-48a5-bf07-e619c4281a35)


EOF.
