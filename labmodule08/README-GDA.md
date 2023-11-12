# Gateway Device Application (Connected Devices)

## Lab Module 08

Be sure to implement all the PIOT-GDA-* issues (requirements) listed at [PIOT-INF-08-001 - Lab Module 08](https://github.com/orgs/programming-the-iot/projects/1#column-10488501).

### Description

NOTE: Include two full paragraphs describing your implementation approach by answering the questions listed below.

What does your implementation do? 

The Gateway Device Application's (GDA) CoAP server implementation serves as a crucial component in the IoT architecture, facilitating communication with Constrained Device Applications (CDAs) through the Constrained Application Protocol (CoAP). The server supports two main functionalities: First, it manages incoming SensorData and SystemPerformanceData updates from CDAs, validating and processing the received JSON-formatted data. Second, it enables CDAs to retrieve ActuatorData by responding to "Get" requests. The resource handlers, such as UpdateSystemPerformanceResourceHandler and GetActuatorCommandResourceHandler, ensure the proper handling of incoming data and the provision of actuation commands. The implementation adheres to CoAP's principles, maintaining observability for efficient data updates and ensuring a secure communication channel between the GDA and CDAs.

How does your implementation work?

The CoAP server in the GDA operates by creating resource handlers tailored for specific data interactions. When CDAs send SensorData or SystemPerformanceData updates, the corresponding Update resource handlers validate and process the incoming data, forwarding it to the DeviceDataManager. This manager, serving as the orchestrator, decides whether to further process the data, validate it through the ActuatorAdapterManager, or log it based on application-specific logic. Conversely, when CDAs request ActuatorData, the GetActuatorCommandResourceHandler responds with the requested data. The integration of these resource handlers establishes a seamless communication link, allowing the GDA to manage and coordinate data flows within the IoT ecosystem.

### Code Repository and Branch

NOTE: Be sure to include the branch (e.g. https://github.com/programming-the-iot/python-components/tree/alpha001).

URL: 

### UML Design Diagram(s)

NOTE: Include one or more UML designs representing your solution. It's expected each
diagram you provide will look similar to, but not the same as, its counterpart in the
book [Programming the IoT](https://learning.oreilly.com/library/view/programming-the-internet/9781492081401/).

![image](https://github.com/JadEletry/book-exercise-docs/assets/71851213/491d2dff-1715-4f41-b16c-510122e59740)

### Unit Tests Executed

NOTE: TA's will execute your unit tests. You only need to list each test case below
(e.g. ConfigUtilTest, DataUtilTest, etc). Be sure to include all previous tests, too,
since you need to ensure you haven't introduced regressions.

PIOT-CFG-08-001: Install and configure the CoAP Java library for your platform - Unit Tests - Client
![image](https://github.com/JadEletry/book-exercise-docs/assets/71851213/f0ee4700-a86b-432c-b560-d5b0dfcf453c)<br>

PIOT-CFG-08-001: Install and configure the CoAP Java library for your platform - Unit Tests - Server
![image](https://github.com/JadEletry/book-exercise-docs/assets/71851213/c3d54827-0aa7-4345-8ba0-19c1925576f3)


### Integration Tests Executed

NOTE: TA's will execute most of your integration tests using their own environment, with
some exceptions (such as your cloud connectivity tests). In such cases, they'll review
your code to ensure it's correct. As for the tests you execute, you only need to list each
test case below (e.g. SensorSimAdapterManagerTest, DeviceDataManagerTest, etc.)

PIOT-GDA-08-004 - Integration Test
![image](https://github.com/JadEletry/book-exercise-docs/assets/71851213/92ba3552-c6a7-41cb-baf0-695d3162db61)<br>
![image](https://github.com/JadEletry/book-exercise-docs/assets/71851213/4dd279b3-69ab-4694-bd9b-47e3d023bb98)


EOF.
