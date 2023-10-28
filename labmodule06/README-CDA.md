# Constrained Device Application (Connected Devices)

## Lab Module 06

Be sure to implement all the PIOT-CDA-* issues (requirements) listed at [PIOT-INF-06-001 - Lab Module 06](https://github.com/orgs/programming-the-iot/projects/1#column-10488434).

### Description

NOTE: Include two full paragraphs describing your implementation approach by answering the questions listed below.

What does your implementation do?

The implementation introduces a pivotal MQTT integration layer into the Constrained Device Application (CDA), allowing for efficient, topic-based communication with MQTT brokers. The CDA seamlessly adopts the roles of both MQTT publisher and subscriber, facilitating the exchange of data and updates through MQTT topics. Connection management, Quality of Service (QoS) mechanisms, and custom callback functions work in tandem to ensure robust communication. Rigorous integration testing verifies the implementation's reliability, with a scalable and extensible architecture poised to adapt to evolving IoT requirements. In addition, comprehensive error handling safeguards against potential network disruptions and authentication challenges, resulting in a technically sound and versatile solution for diverse IoT applications.


How does your implementation work?

This implementation operates by leveraging the MQTT (Message Queuing Telemetry Transport) protocol to enable efficient and reliable communication within the Constrained Device Application (CDA). It first establishes a connection with an MQTT broker, specifying the broker's address and port. The CDA can act as both a publisher and subscriber by sending data to specific MQTT topics and receiving updates through topic-level subscriptions. Custom callback functions are employed to handle connection events, including successful connections and message reception. The Quality of Service (QoS) settings are employed to fine-tune the message delivery guarantees, offering the flexibility to adapt to various application requirements. This implementation relies on topic-based messaging to categorize and route data effectively. Rigorous integration tests validate its performance and reliability. The architecture is designed to be scalable and extensible, accommodating the addition of more MQTT topics and support for additional devices. Robust error handling ensures graceful management of potential issues, including network disruptions and authentication errors, resulting in a technically sound and versatile solution for IoT applications.



### Code Repository and Branch

NOTE: Be sure to include the branch (e.g. https://github.com/programming-the-iot/python-components/tree/alpha001).

URL: hhttps://github.com/ShahzabeM/CDA-Python/tree/labmodule06

### UML Design Diagram(s)

NOTE: Include one or more UML designs representing your solution. It's expected each
diagram you provide will look similar to, but not the same as, its counterpart in the
book [Programming the IoT](https://learning.oreilly.com/library/view/programming-the-internet/9781492081401/).

![image](https://github.com/JadEletry/book-exercise-docs/assets/71851213/0c43ef3b-6aeb-4718-8079-267621831839)


### Unit Tests Executed

NOTE: TA's will execute your unit tests. You only need to list each test case below
(e.g. ConfigUtilTest, DataUtilTest, etc). Be sure to include all previous tests, too,
since you need to ensure you haven't introduced regressions.


### Integration Tests Executed

NOTE: TA's will execute most of your integration tests using their own environment, with
some exceptions (such as your cloud connectivity tests). In such cases, they'll review
your code to ensure it's correct. As for the tests you execute, you only need to list each
test case below (e.g. SensorSimAdapterManagerTest, DeviceDataManagerTest, etc.)

PIOT-CDA-06-001: Create / edit module MqttClientConnector #19 - Integration Test<br>
![image](https://github.com/JadEletry/book-exercise-docs/assets/71851213/35a89e15-9106-4ec3-898d-924e7f7c774a)

PIOT-CDA-06-002 - Create the callback infrastructure for the MqttClientConnector #18 - IntegrationTest-MqttClientConnectorTest<br>
![image](https://github.com/JadEletry/book-exercise-docs/assets/71851213/a0703619-a169-4a93-bc3a-46847a9da3f1)

PIOT-CDA-06-003: Create the publish and subscribe methods for MqttClientConnector - IntegrationTest - testConnectAndCDAManagementStatusPubSub() in MqttClientConnectorTest<br>
![image](https://github.com/JadEletry/book-exercise-docs/assets/71851213/1aaf5d58-3947-41a6-82e3-bf9a0b83fed9)





EOF.
