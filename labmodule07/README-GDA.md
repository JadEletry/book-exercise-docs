# Gateway Device Application (Connected Devices)

## Lab Module 07

Be sure to implement all the PIOT-GDA-* issues (requirements) listed at [PIOT-INF-07-001 - Lab Module 07](https://github.com/orgs/programming-the-iot/projects/1#column-10488499).

### Description

NOTE: Include two full paragraphs describing your implementation approach by answering the questions listed below.

What does your implementation do? 

The implementation described in the provided text facilitates the integration of the MQTT protocol into the Gateway Device Application (GDA) of an IoT system. It accomplishes this by employing the Eclipse Paho MQTT client library and Java programming language. The implementation encompasses features such as connecting to MQTT brokers, subscribing and unsubscribing from MQTT topics, publishing messages, and handling incoming messages. It leverages protocol-specific Quality of Service (QoS) levels to ensure message delivery reliability. This implementation works by instantiating and configuring MQTT client connectors and orchestrating their start and stop procedures as part of the GDA's functionality. Key actions include initializing client connectors, subscribing to relevant MQTT topics, and processing incoming MQTT messages, further strengthening the GDA's ability to interact seamlessly with MQTT-enabled devices and services.

How does your implementation work?

The MQTT implementation operates within the GDA to support essential IoT communication functions, ensuring that sensor data, system performance data, and actuator command responses are exchanged effectively. It provides a systematic approach to manage MQTT connections, effectively subscribing to topics of interest and responding to incoming MQTT messages, thereby enabling the GDA to take informed actions based on the received MQTT data. The use of callback interfaces and QoS levels enhances message handling and delivery reliability, contributing to a robust and reliable MQTT integration in the GDA's ecosystem

### Code Repository and Branch

NOTE: Be sure to include the branch (e.g. https://github.com/programming-the-iot/python-components/tree/alpha001).

URL: https://github.com/ShahzabeM/GDA-Java/tree/labmodule07

### UML Design Diagram(s)

NOTE: Include one or more UML designs representing your solution. It's expected each
diagram you provide will look similar to, but not the same as, its counterpart in the
book [Programming the IoT](https://learning.oreilly.com/library/view/programming-the-internet/9781492081401/).

![image](https://github.com/JadEletry/book-exercise-docs/assets/71851213/1faa377e-4e67-4cb8-b5ba-c9571e784bb0)

### Unit Tests Executed

NOTE: TA's will execute your unit tests. You only need to list each test case below
(e.g. ConfigUtilTest, DataUtilTest, etc). Be sure to include all previous tests, too,
since you need to ensure you haven't introduced regressions.

### Integration Tests Executed

NOTE: TA's will execute most of your integration tests using their own environment, with
some exceptions (such as your cloud connectivity tests). In such cases, they'll review
your code to ensure it's correct. As for the tests you execute, you only need to list each
test case below (e.g. SensorSimAdapterManagerTest, DeviceDataManagerTest, etc.)

PIOT-GDA-07-001: Create / edit module MqttClientConnector - Integration Test for testConnectAndDisconnect()<br>
![image](https://github.com/JadEletry/book-exercise-docs/assets/71851213/b66c8039-4030-4f24-9b6a-e8874cc9180e)

PIOT-GDA-07-002: Create the callback infrastructure for MqttClientConnector -  Integration Test for testConnectAndDisconnect()<br>
![image](https://github.com/JadEletry/book-exercise-docs/assets/71851213/26ccf8d5-9cc3-43be-b979-4b235dc67239)

PIOT-GDA-07-003: Create the publish and subscribe methods for MqttClientConnector - Integration Test for testPublishAndSubscribe()<br>
![image](https://github.com/JadEletry/book-exercise-docs/assets/71851213/c7be1b95-ec4a-493b-b4d8-780f1e857818)

EOF.
