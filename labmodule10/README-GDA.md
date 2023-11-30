# Gateway Device Application (Connected Devices)

## Lab Module 10

Be sure to implement all the PIOT-GDA-* issues (requirements) listed at [PIOT-INF-10-001 - Lab Module 10](https://github.com/orgs/programming-the-iot/projects/1#column-10488510).

### Description

NOTE: Include two full paragraphs describing your implementation approach by answering the questions listed below.

What does your implementation do? 

The Gateway Device App (GDA) implementation focuses on establishing secure communication and handling data interpretation between devices within an IoT infrastructure. It enables the GDA to securely send messages, including actuation commands, to the Constrained Device App (CDA) by employing Transport Layer Security (TLS) for MQTT communication. The GDA's implementation also involves interpreting incoming data from the CDA, processing it, and potentially triggering responses or taking further actions based on the received information.


How does your implementation work?

The GDA's implementation primarily revolves around ensuring secure communication by implementing TLS encryption for MQTT connections. It establishes a secure channel to transmit messages to the CDA by subscribing to specific topics, allowing the GDA to send ActuatorData commands securely. Upon receiving messages from the CDA, the system employs logic to interpret and process the ActuatorData content. This includes decoding the incoming data, transforming it into actionable insights, and potentially initiating appropriate actions or relaying relevant information to other components within the GDA.

### Code Repository and Branch

NOTE: Be sure to include the branch (e.g. https://github.com/programming-the-iot/python-components/tree/alpha001).

URL: https://github.com/ShahzabeM/GDA-Java/tree/labmodule10

### UML Design Diagram(s)

NOTE: Include one or more UML designs representing your solution. It's expected each
diagram you provide will look similar to, but not the same as, its counterpart in the
book [Programming the IoT](https://learning.oreilly.com/library/view/programming-the-internet/9781492081401/).

![image](https://github.com/JadEletry/book-exercise-docs/assets/71851213/7775f0b2-a152-4d36-985b-61c2261def0a)

### Unit Tests Executed

NOTE: TA's will execute your unit tests. You only need to list each test case below
(e.g. ConfigUtilTest, DataUtilTest, etc). Be sure to include all previous tests, too,
since you need to ensure you haven't introduced regressions.


### Integration Tests Executed

NOTE: TA's will execute most of your integration tests using their own environment, with
some exceptions (such as your cloud connectivity tests). In such cases, they'll review
your code to ensure it's correct. As for the tests you execute, you only need to list each
test case below (e.g. SensorSimAdapterManagerTest, DeviceDataManagerTest, etc.)

GDA -  PIOT-INT-10-001: MqttClientPerformanceTest - testConnectAndDisconnect() 
```
Nov 28, 2023 21:13:55 programmingtheiot.gda.connection.MqttClientConnector initCredentialConnectionParameters INFO: Checking if credentials file exists and is loadable...
Nov 28, 2023 21:13:55 programmingtheiot.common.ConfigUtil getCredentials
WARNING: Credential file non-existent: ./cred/PiotMqttCred.props. Ignoring.
Nov 28, 2023 21:13:55 programmingtheiot.gda.connection.MqttClientConnector initCredentialConnectionParameters WARNING: No credentials are set.
Nov 28, 2023 21:13:55 programmingtheiot.gda.connection.MqttClientConnector initClientParameters
INFO: Using URL for broker conn: tcp://127.0.0.1:1883
Nov 28, 2023 21:13:55 programmingtheiot.gda.connection.MqttClientConnector connectClient
INFO: MQTT client connecting to broker: tcp://127.0.0.1:1883
Nov 28, 2023 21:13:55 programmingtheiot.gda.connection.MqttClientConnector connectComplete
INFO: connectComplete method called. Client has successfully connected.
Nov 28, 2023 21:13:55 programmingtheiot.gda.connection.MqttClientConnector disconnectClient
INFO: Disconnecting MQTT client from broker: tcp://127.0.0.1:1883
Nov 28, 2023 21:13:55 programmingtheiot.part03. integration.connection.MqttClient PerformanceTest testConnectAndDisconnect INFO: Connect and Disconnect [1]: 451 ms
```
GDA -  PIOT-INT-10-001: MqttClientPerformanceTest -  testPublishQoS0()
```
Nov 28, 2023 21:19:55 programmingtheiot.gda.connection.MqttClientConnector initCredentialConnectionParameters INFO: Checking if credentials file exists and is loadable...
Nov 28, 2023 21:19:55 programmingtheiot.common.ConfigUtil getCredentials
WARNING: Credential file non-existent: ./cred/PiotMqttCred.props. Ignoring.
Nov 28, 2023 21:19:55 programmingtheiot.gda.connection.MqttClientConnector initCredentialConnectionParameters WARNING: No credentials are set.
Nov 28, 2023 21:19:55 programmingtheiot.gda.connection.MqttClientConnector initClientParameters
INFO: Using URL for broker conn: tcp://127.0.0.1:1883
Nov 28, 2023 21:19:55 programmingtheiot.gda.connection.MqttClientConnector connectClient
INFO: MQTT client connecting to broker: tcp://127.0.0.1:1883
Nov 28, 2023 21:19:55 programmingtheiot.gda.connection.MqttClientConnector connectComplete
INFO: connectComplete method called. Client has successfully connected.
Nov 28, 2023 21:19:55 programmingtheiot.gda.connection.MqttClientConnector disconnectClient
INFO: Disconnecting MQTT client from broker: tcp://127.0.0.1:1883
Nov 28, 2023 21:19:55 programmingtheiot.part03. integration.connection.MqttClientPerformanceTest execTestPublish
INFO: \n\tTesting Publish: QoS = 0 | msgs = 10000 | payload size = 212 | start = 1.70112448E9 | end = 1.70112448E9 | elapsed = 9.16
```
GDA -  PIOT-INT-10-001: MqttClientPerformanceTest -   testPublishQoS1()
```
Nov 28, 2023 21:23:05 programmingtheiot.gda.connection.MqttClientConnector initCredentialConnectionParameters INFO: Checking if credentials file exists and is loadable...
Nov 28, 2023 21:23:05 programmingtheiot.common.ConfigUtil getCredentials
WARNING: Credential file non-existent: ./cred/PiotMqttCred.props. Ignoring.
Nov 28, 2023 21:23:05 programmingtheiot.gda.connection.MqttClientConnector initCredentialConnectionParameters WARNING: No credentials are set.
Nov 28, 2023 21:23:05 programmingtheiot.gda.connection.MqttClientConnector initClientParameters
INFO: Using URL for broker conn: tcp://127.0.0.1:1883
Nov 28, 2023 21:23:05 programmingtheiot.gda.connection.MqttClientConnector connectClient
INFO: MQTT client connecting to broker: tcp://127.0.0.1:1883
Nov 28, 2023 21:23:05 programmingtheiot.gda.connection.MqttClientConnector connectComplete
INFO: connectComplete method called. Client has successfully connected.
Nov 28, 2023 21:23:05 programmingtheiot.gda.connection.MqttClientConnector disconnectClient
INFO: Disconnecting MQTT client from broker: tcp://127.0.0.1:1883
Nov 28, 2023 21:23:05 programmingtheiot.part03. integration.connection.MqttClientPerformanceTest execTestPublish
INFO: \n\tTesting Publish: QoS = 1 | msgs = 10000 | payload size = 212 | start = 1.70112461E9 | end = 1.70112461E9 | elapsed = 17.751
```
GDA -  PIOT-INT-10-001: MqttClientPerformanceTest -   testPublishQoS2()
```
Nov 28, 2023 21:27:19 programmingtheiot.gda.connection.MqttClientConnector initCredentialConnectionParameters INFO: Checking if credentials file exists and is loadable...
Nov 28, 2023 21:27:19 programmingtheiot.common.ConfigUtil getCredentials
WARNING: Credential file non-existent: ./cred/PiotMqttCred.props. Ignoring.
Nov 28, 2023 21:27:19 programmingtheiot.gda.connection.MqttClientConnector initCredentialConnectionParameters WARNING: No credentials are set.
Nov 28, 2023 21:27:19 programmingtheiot.gda.connection.MqttClientConnector initClientParameters
INFO: Using URL for broker conn: tcp://127.0.0.1:1883
Nov 28, 2023 21:27:19 programmingtheiot.gda.connection.MqttClientConnector connectClient
INFO: MQTT client connecting to broker: tcp://127.0.0.1:1883
Nov 28, 2023 21:27:19 programmingtheiot.gda.connection.MqttClientConnector connectComplete
INFO: connectComplete method called. Client has successfully connected.
Nov 28, 2023 21:27:19 programmingtheiot.gda.connection.MqttClientConnector disconnectClient
INFO: Disconnecting MQTT client from broker: tcp://127.0.0.1:1883
Nov 28, 2023 21:27:19 programmingtheiot.part03. integration.connection.MqttClientPerformanceTest execTestPublish
INFO: \n\tTesting Publish: QoS = 2 | msgs = 10000 | payload size = 212 | start = 1.70112461E9 | end = 1.70112461E9 | elapsed = 34.452
```
PIOT-GDA-10-001: MqttClientConnectorTest
```
Nov 28, 2023 21:34:26 programmingtheiot.gda.connection.MqttClientConnector initCredentialConnectionParameters INFO: Checking if credentials file exists and is loadable...
Nov 28, 2023 21:34:26 programmingtheiot.common.ConfigUtil getCredentials
WARNING: Credential file non-existent: ./cred/PiotMqttCred.props. Ignoring.
Nov 28, 2023 21:34:26 programmingtheiot.gda.connection.MqttClientConnector initCredentialConnectionParameters WARNING: No credentials are set.
Nov 28, 2023 21:34:26 programmingtheiot.gda.connection.MqttClientConnector initClientParameters
INFO: Using URL for broker conn: tcp://127.0.0.1:1883
Nov 28, 2023 21:34:26 programmingtheiot.gda.connection.MqttClientConnector connectClient
INFO: MQTT client connecting to broker: tcp://127.0.0.1:1883
Nov 28, 2023 21:34:26 programmingtheiot.gda.connection.MqttClientConnector connectComplete INFO: connectComplete method called. Client has successfully connected.
Nov 28, 2023 21:34:26 programmingtheiot.gda.connection.MqttClientConnector connectClient WARNING: MQTT client already connected to broker: tcp://127.0.0.1:1883
Nov 28, 2023 21:34:26 programmingtheiot.gda.connection.MqttClientConnector disconnectClient INFO: Disconnecting MQTT client from broker: tcp://127.0.0.1:1883
Nov 28, 2023 21:34:26 programmingtheiot.gda.connection.MqttClientConnector disconnectClient WARNING: MQTT client not connected to broker: tcp://127.0.0.1:1883
```
PIOT-GDA-10-002: MqttClientConnectorTest - testConnectAndDisconnect()
```
INFO: MQTT client connecting to broker: tcp://127.0.0.1:1883
Nov 28, 2023 21:36:22 programmingtheiot.gda.connection.MqttClientConnector connectClient SEVERE: Failed to connect MQTT client to broker: tcp://127.0.0.1:1883
Connect already in progress (32110)
at org.eclipse.paho.client.mqttv3.MqttAsyncClient.connect(MqttAsyncClient.java:602)
at org.eclipse.paho.client.mqttv3.MqttAsyncClient.connect(MqttAsyncClient.java:584)
at programmingtheiot.gda.connection.MqttClientConnector.connectClient (MqttClientConnector.java:128)
at programmingtheiot.part03.integration.connection.MqttClientConnectorTest.testConnectAndDisconnect (MqttClientConnectorTest.java:77)
at java.base/jdk.internal.reflect.NativeMethodAccessorImpl.invoke0(Native Method)
at java.base/jdk.internal.reflect.NativeMethodAccessorImpl.invoke(NativeMethodAccessorImpl.java:77)
at
java.base/jdk.internal.reflect.DelegatingMethodAccessorImpl.invoke(DelegatingMethodAccessorImpl.java:43)
at java.base/java.lang.reflect.Method.invoke(Method.java:568)
at
org.junit.runners.model. FrameworkMethod$1.runReflectiveCall (FrameworkMethod.java:59) at org.junit.internal.runners.model.ReflectiveCallable.run(ReflectiveCallable.java:12)
at org.junit.runners.model. FrameworkMethod.invokeExplosively (FrameworkMethod.java:56)
at org.junit.internal.runners.statements. InvokeMethod.evaluate(InvokeMethod.java:17) at org.junit.internal.runners.statements. RunBefores.evaluate(RunBefores.java:26) at org.junit.internal.runners.statements. RunAfters.evaluate(RunAfters.java:27)
at
org.junit.runners. ParentRunner$3.evaluate(ParentRunner.java:306)
at org.junit.runners. BlockJUnit4ClassRunner$1.evaluate(BlockJUnit4ClassRunner.java:100) at org.junit.runners. ParentRunner.runLeaf (ParentRunner.java:366)
at org.junit.runners. BlockJUnit4ClassRunner.runChild (BlockJUnit4ClassRunner.java:103) at org.junit.runners. BlockJUnit4ClassRunner.runChild (BlockJUnit4ClassRunner.java:63) at org.junit.runners. ParentRunner$4.run(ParentRunner.java:331)
at org.junit.runners. ParentRunner$1.schedule (ParentRunner.java:79) at org.junit.runners. ParentRunner.runChildren (ParentRunner.java:329) at org.junit.runners. ParentRunner.access$100 (ParentRunner.java:66) at org.junit.runners. ParentRunner$2.evaluate(ParentRunner.java:293) at org.junit.runners. ParentRunner$3.evaluate(ParentRunner.java:306) at org.junit.runners. ParentRunner.run(ParentRunner.java:413)
at org.eclipse.jdt.internal.junit4.runner.JUnit4TestReference.run(JUnit4TestReference.java:93) at org.eclipse.jdt.internal.junit.runner. TestExecution.run(TestExecution.java:40)
at org.eclipse.jdt.internal.junit.runner. RemoteTestRunner.runTests (RemoteTestRunner.java:529) at org.eclipse.jdt.internal.junit.runner. RemoteTestRunner.runTests (RemoteTestRunner.java:756) at org.eclipse.jdt.internal.junit.runner.RemoteTestRunner.run(RemoteTestRunner.java:452) at org.eclipse.jdt.internal.junit.runner.RemoteTestRunner.main(RemoteTestRunner.java:210)
Nov 28, 2023 21:36:22 programmingtheiot.gda.connection.MqttClientConnector connectComplete INFO: MQTT connection successful (is reconnect = false). Broker: tcp://127.0.0.1:1883
Nov 28, 2023 21:36:22 programmingtheiot.gda.connection.MqttClientConnector disconnectClient INFO: Disconnecting MQTT client from broker: tcp://127.0.0.1:1883
Nov 28, 2023 21:36:22 programmingtheiot.gda.connection.MqttClientConnector disconnectClient WARNING: MQTT client not connected to broker: tcp://127.0.0.1:1883
```
PIOT-GDA-10-002: MqttClientConnectorTest - testActuatorCommandResponseSubscription()
```
Nov 28, 2023 21:38:02 programmingtheiot.gda.connection.MqttClientConnector initCredentialConnectionParameters INFO: Checking if credentials file exists and is loadable...
Nov 28, 2023 21:38:02 programming theiot.common.ConfigUtil getCredentials
WARNING: Credential file non-existent: ./cred/PiotMqttCred.props. Ignoring.
Nov 28, 2023 21:38:02 programmingtheiot.gda.connection.MqttClientConnector initCredentialConnectionParameters WARNING: No credentials are set.
Nov 28, 2023 21:38:02 programmingtheiot.gda.connection.MqttClientConnector initClientParameters
INFO: Using URL for broker conn: tcp://127.0.0.1:1883
Nov 28, 2023 21:38:02 programmingtheiot.gda.connection.MqttClientConnector connectClient
INFO: MQTT client connecting to broker: tcp://127.0.0.1:1883
Nov 28, 2023 21:38:02 programmingtheiot.gda.connection.MqttClientConnector connectComplete INFO: MQTT connection successful (is reconnect = false). Broker: tcp://127.0.0.1:1883
Nov 28, 2023 21:38:02 programmingtheiot.gda.connection.MqttClientConnector messageArrived INFO: messageArrived method called. a message has arrived
Nov 28, 2023 21:38:02 programmingtheiot.gda.connection.MqttClientConnector disconnectClient INFO: Disconnecting MQTT client from broker: tcp://127.0.0.1:1883
```
PIOT-GDA-10-003: DeviceDataManagerSimpleCdaActuationTest
```
Nov 28, 2023 21:41:51 programmingtheiot.gda.connection.MqttClientConnector initCredentialConnectionParameters INFO: Checking if credentials file exists and is loadable...
Nov 28, 2023 21:41:51 programmingtheiot.common.ConfigUtil getCredentials
WARNING: Credential file non-existent: ./cred/PiotMqttCred.props. Ignoring.
Nov 28, 2023 21:41:51 programmingtheiot.gda.connection.MqttClientConnector initCredentialConnectionParameters WARNING: No credentials are set.
Nov 28, 2023 21:41:51 programmingtheiot.gda.connection.MqttClientConnector initClientParameters
INFO: Using URL for broker conn: tcp://127.0.0.1:1883
Nov 28, 2023 21:41:51 programmingtheiot.gda.app.DeviceDataManager handleHumiditySensorAnalysis
INFO: Humidity exceptional value reached. Sending actuation event to CDA: name=HumidifierActuator, typeID=1002, timestamp=2023-11-28T00:41:51.2186871497, statusCode=0, hasError=false, locationID=constra Nov 28, 2023 21:41:51 programmingtheiot.gda.app.DeviceDataManager sendActuatorCommandtoCda
WARNING: Failed to publish ActuatorData humidifier command from GDA to CDA: 1
Nov 28, 2023 21:41:51 programmingtheiot.gda.app.DeviceDataManager handleHumiditySensorAnalysis
INFO: Humidity nominal value reached. Sending OFF actuation event to CDA: name=HumidifierActuator, typeID=1002, timestamp=2023-11-28T00:41:51.2832407612, statusCode=0, hasError=false, locationID=constra Nov 28, 2023 21:41:51 programmingtheiot.gda.app.DeviceDataManager sendActuatorCommandtoCda WARNING: Failed to publish ActuatorData humidifier command from GDA to CDA: 0
```
PIOT-INT-10-003: CDA + GDA Running
```
Nov 28, 2023 21:44:35 programmingtheiot.gda.connection.MqttClientConnector connectionLost INFO: connectionLost method called. Client has successfully disconnected.
Nov 28, 2023 21:44:35 programmingtheiot.gda.connection.MqttClientConnector connectComplete INFO: MQTT connection successful (is reconnect = true). Broker: tcp://127.0.0.1:1883 Nov 28, 2023 21:44:36 programmingtheiot.gda.connection.MqttClientConnector connectionLost INFO: connectionLost method called. Client has successfully disconnected.
Nov 28, 2023 21:44:36 programmingtheiot.gda.connection.MqttClientConnector connectComplete INFO: MQTT connection successful (is reconnect = true). Broker: tcp://127.0.0.1:1883 Nov 28, 2023 21:44:37 programmingtheiot.gda.connection.MqttClientConnector connectionLost INFO: connectionLost method called. Client has successfully disconnected.
Nov 28, 2023 21:44:37 programmingtheiot.gda.connection.MqttClientConnector connectComplete INFO: MQTT connection successful (is reconnect = true). Broker: tcp://127.0.0.1:1883 Nov 28, 2023 21:44:38 programmingtheiot.gda.connection.MqttClientConnector connectionLost INFO: connectionLost method called. Client has successfully disconnected.
Nov 28, 2023 21:44:38 programmingtheiot.gda.connection.MqttClientConnector connectComplete INFO: MQTT connection successful (is reconnect = true). Broker: tcp://127.0.0.1:1883 Nov 28, 2023 21:44:39 programmingtheiot.gda.connection.MqttClientConnector connectionLost INFO: connectionLost method called. Client has successfully disconnected.
Nov 28, 2023 21:44:39 programmingtheiot.gda.connection.MqttClientConnector connectComplete INFO: MQTT connection successful (is reconnect = true). Broker: tcp://127.0.0.1:1883 Nov 28, 2023 21:44:40 programmingtheiot.gda.connection.MqttClientConnector connectionLost INFO: connectionLost method called. Client has successfully disconnected.
Nov 28, 2023 21:44:40 programmingtheiot.gda.connection.MqttClientConnector connectComplete INFO: MQTT connection successful (is reconnect = true). Broker: tcp://127.0.0.1:1883 Nov 28, 2023 21:44:41 programmingtheiot.gda.connection.MqttClientConnector connectionLost INFO: connectionLost method called. Client has successfully disconnected.
Nov 28, 2023 21:44:41 programmingtheiot.gda.connection.MqttClientConnector connectComplete INFO: MQTT connection successful (is reconnect = true). Broker: tcp://127.0.0.1:1883 Nov 28, 2023 21:44:42 programmingtheiot.gda.connection.MqttClientConnector connectionLost INFO: connectionLost method called. Client has successfully disconnected.
Nov 28, 2023 21:44:42 programmingtheiot.gda.connection.MqttClientConnector disconnectClient WARNING: MQTT client not connected to broker: tcp://127.0.0.1:1883
Nov 28, 2023 21:44:42 programmingtheiot.gda.connection.MqttClientConnector unsubscribeFromTopic INFO: Successfully unsubscribed from topic: PIOT/GatewayDevice/Mgmt StatusMsg
Nov 28, 2023 21:44:42 programmingtheiot.gda.connection.MqttClientConnector unsubscribeFromTopic INFO: Successfully unsubscribed from topic: PIOT/ConstrainedDevice/ActuatorResponse
Nov 28, 2023 21:44:42 programmingtheiot.gda.connection.MqttClientConnector unsubscribeFromTopic
INFO: Successfully unsubscribed from topic: PIOT/ConstrainedDevice/SensorMsg
Nov 28, 2023 21:44:42 programmingtheiot.gda.connection.MqttClientConnector unsubscribeFromTopic
INFO: Successfully unsubscribed from topic: PIOT/ConstrainedDevice/SystemPerfMsg
Nov 28, 2023 21:44:42 programmingtheiot.gda.connection.MqttClientConnector disconnectClient
INFO: Disconnecting MQTT client from broker: tcp://127.0.0.1:1883
Nov 28, 2023 21:44:42 programmingtheiot.gda.app.DeviceDataManager stopManager
INFO: Successfully disconnected MQTT client from broker.
```
PIOT-INT-10-004: CDA + GDA with TLS
```
Nov 28, 2023 21:49:45 programmingtheiot.gda.connection.MqttClientConnector connectComplete INFO: MQTT connection successful (is reconnect = true). Broker: ssl://127.0.0.1:8883 Nov 28, 2023 21:49:47 programmingtheiot.gda.connection.MqttClientConnector connectionLost INFO: connectionLost method called. Client has successfully disconnected.
Nov 28, 2023 21:49:47 programmingtheiot.gda.connection.MqttClientConnector connectComplete INFO: MQTT connection successful (is reconnect = true). Broker: ss1://127.0.0.1:8883 Nov 28, 2023 21:49:48 programmingtheiot.gda.connection.MqttClientConnector connectionLost INFO: connectionLost method called. Client has successfully disconnected.
Nov 28, 2023 21:49:48 programmingtheiot.gda.connection.MqttClientConnector connectComplete INFO: MQTT connection successful (is reconnect = true). Broker: ss1://127.0.0.1:8883 Nov 28, 2023 21:49:49 programmingtheiot.gda.connection.MqttClientConnector connectionLost INFO: connectionLost method called. Client has successfully disconnected.
Nov 28, 2023 21:49:49 programmingtheiot.gda.connection.MqttClientConnector connectComplete INFO: MQTT connection successful (is reconnect = true). Broker: ssl://127.0.0.1:8883 Nov 28, 2023 21:49:51 programmingtheiot.gda.connection.MqttClientConnector connectionLost INFO: connectionLost method called. Client has successfully disconnected.
Nov 28, 2023 21:49:51 programmingtheiot.gda.connection.MqttClientConnector connectComplete INFO: MQTT connection successful (is reconnect = true). Broker: ss1://127.0.0.1:8883 Nov 28, 2023 21:49:52 programmingtheiot.gda.connection.MqttClientConnector connectionLost INFO: connectionLost method called. Client has successfully disconnected.
Nov 28, 2023 21:49:52 programmingtheiot.gda.connection.MqttClientConnector connectComplete INFO: MQTT connection successful (is reconnect = true). Broker: ss1://127.0.0.1:8883 Nov 28, 2023 21:49:53 programmingtheiot.gda.connection.MqttClientConnector connectionLost INFO: connectionLost method called. Client has successfully disconnected.
Nov 28, 2023 21:49:53 programmingtheiot.gda.connection.MqttClientConnector connectComplete INFO: MQTT connection successful (is reconnect = true). Broker: ssl://127.0.0.1:8883 Nov 28, 2023 21:49:55 programmingtheiot.gda.connection.MqttClientConnector connectionLost INFO: connectionLost method called. Client has successfully disconnected.
Nov 28, 2023 21:49:55 programmingtheiot.gda.connection.MqttClientConnector connectComplete INFO: MQTT connection successful (is reconnect = true). Broker: ss1://127.0.0.1:8883 Nov 28, 2023 21:49:56 programmingtheiot.gda.connection.MqttClientConnector connectionLost INFO: connectionLost method called. Client has successfully disconnected.
Nov 28, 2023 21:49:56 programmingtheiot.gda.connection.MqttClientConnector connectComplete INFO: MQTT connection successful (is reconnect = true). Broker: ssl://127.0.0.1:8883 Nov 28, 2023 21:49:57 programmingtheiot.gda.connection.MqttClientConnector connectionLost INFO: connectionLost method called. Client has successfully disconnected.
Nov 28, 2023 21:49:57 programmingtheiot.gda.connection.MqttClientConnector connectComplete INFO: MQTT connection successful (is reconnect = true). Broker: ss1://127.0.0.1:8883 Nov 28, 2023 21:49:59 programmingtheiot.gda.connection.MqttClientConnector connectionLost INFO: connectionLost method called. Client has successfully disconnected.
Nov 28, 2023 21:49:59 programmingtheiot.gda.connection.MqttClientConnector connectComplete INFO: MQTT connection successful (is reconnect = true). Broker: ssl://127.0.0.1:8883
Nov 28, 2023 21:49:59 programmingtheiot.gda.connection.MqttClientConnector disconnectClient INFO: Disconnecting MQTT client from broker: ssl://127.0.0.1:8883
```


EOF.
