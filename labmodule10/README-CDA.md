# Constrained Device Application (Connected Devices)

## Lab Module 10

Be sure to implement all the PIOT-CDA-* issues (requirements) listed at [PIOT-INF-10-001 - Lab Module 10](https://github.com/orgs/programming-the-iot/projects/1#column-10488510).

### Description

NOTE: Include two full paragraphs describing your implementation approach by answering the questions listed below.

What does your implementation do? 

How does your implementation work?

### Code Repository and Branch

NOTE: Be sure to include the branch (e.g. https://github.com/programming-the-iot/python-components/tree/alpha001).

URL: 

### UML Design Diagram(s)

NOTE: Include one or more UML designs representing your solution. It's expected each
diagram you provide will look similar to, but not the same as, its counterpart in the
book [Programming the IoT](https://learning.oreilly.com/library/view/programming-the-internet/9781492081401/).


### Unit Tests Executed

NOTE: TA's will execute your unit tests. You only need to list each test case below
(e.g. ConfigUtilTest, DataUtilTest, etc). Be sure to include all previous tests, too,
since you need to ensure you haven't introduced regressions.

### Integration Tests Executed

NOTE: TA's will execute most of your integration tests using their own environment, with
some exceptions (such as your cloud connectivity tests). In such cases, they'll review
your code to ensure it's correct. As for the tests you execute, you only need to list each
test case below (e.g. SensorSimAdapterManagerTest, DeviceDataManagerTest, etc.)

PIOT-INT-10-001: estConnectAndDisconnect(), testPublishQoS0(), testPublishQoS1(), testPublishQoS2()
```
2023-11-28 18:47:08,709: ConfigUtil: INFO: Loading config: /home/zabe/programmingtheiot/python-components/config/PiotConfig.props
2023-11-28 18:47:08,710: ConfigUtil: DEBUG:Config: ['Mqtt.GatewayService', 'Coap. GatewayService', 'ConstrainedDevice']
2023-11-28 18:47:08,710: ConfigUtil:INFO:Created instance of ConfigUtil: <programmingtheiot.common.ConfigUtil.ConfigUtil object at 0x7f389c1801d0>
2023-11-28 18:47:08,710:MqttClientConnector: INFO: MQTT Client ID: CDAMqttClientPerformanceTest001
2023-11-28 18:47:08,711: MqttClientConnector: INFO: 2023-11-28 18:47:08,711: MqttClientConnector: INFO: 2023-11-28 18:47:88,711: MqttClientConnector: INFO:
MQTT Broker Host: 127.0.0.1 MQTT Broker Port: 1883 MQTT Keep Alive: 60
MQTT Client ID:
CDAMqttClientPerformanceTest001
2023-11-28 18:47:08,711: MqttClientConnector: INFO: MQTT client connecting to broker at host: 127.0.0.1 2023-11-28 18:47:08,716:MqttClientConnector: INFO:Disconnecting MQTT client from broker: 127.0.0.1 2023-11-28 18:47:09,719:MqttClientPerformanceTest: INFO: Connect and Disconnect: 1008.503043 ms .2023-11-28 18:47:09,720: MqttClientConnector: INFO: 2023-11-28 18:47:09,720: MqttClientConnector: INFO: 2023-11-28 18:47:09,720: MqttClientConnector: INFO: 2023-11-28 18:47:09,720: MqttClientConnector: INFO:
MQTT Broker Host: 127.0.0.1 MQTT Broker Port: 1883 MQTT Keep Alive: 60
2023-11-28 18:47:09,720: MqttClientConnector: INFO: MQTT client connecting to broker at host: 127.0.0.1 2023-11-28 18:47:09,721:DataUtil: INFO:Created DataUtil instance.
2023-11-28 18:47:12,755:MqttClientConnector: INFO: Disconnecting MQTT client from broker: 127.0.0.1
2023-11-28 18:47:13,756:MqttClientPerformanceTest:INFO:
Testing Publish: QoS = 0 | msgs = 10000 | payload size = 264 | start = 1701125229721883.0 | end = 1701125232755647.5 | elapsed = 3.033764502 .2023-11-28 18:47:13,757:MqttClientConnector: INFO: MQTT Client ID: CDAMqttClientPerformanceTest001
2023-11-28 18:47:13,757: MqttClientConnector: INFO: 2023-11-28 18:47:13,757:MqttClientConnector: INFO:
2023-11-28 18:47:13,757:MqttClientConnector: INFO: MQTT Broker Host: 127.0.0.1
MQTT Broker Port: 1883 MQTT Keep Alive: 60
2023-11-28 18:47:13,757:MqttClientConnector: INFO: MQTT client connecting to broker at host: 127.0.0.1
2023-11-28 18:47:13,758:DataUtil:INFO:Created DataUtil instance.
2023-11-28 18:47:18, 139: MqttClientConnector: INFO: Disconnecting MQTT client from broker: 127.0.0.1 2023-11-28 18:47:19, 139: MqttClientPerformanceTest:INFO:
Testing Publish: QoS = 1 | msgs = 10000 | payload size = 264 | start = 1701125233759100.0 | end = 1701125238139843.0 | elapsed = 4.379942972 2023-11-28 18:47:19,140:MqttClientConnector: INFO: MQTT Client ID: CDAMqttClientPerformanceTest001 2023-11-28 18:47:19, 140: MqttClientConnector: INFO: 2023-11-28 18:47:19, 140:MqttClientConnector: INFO:
2023-11-28 18:47:19,140: MqttClientConnector: INFO:
MQTT Broker Host: 127.0.0.1
MQTT Broker Port: 1883 MQTT Keep Alive: 60
2023-11-28 18:47:19,140: MqttClientConnector: INFO: MQTT client connecting to broker at host: 127.0.0.1 2023-11-28 18:47:19,141:DataUtil:INFO:Created DataUtil instance.
2023-11-28 18:47:25, 167: MqttClientConnector: INFO: Disconnecting MQTT client from broker: 127.0.0.1
2023-11-28 18:47:26,169: MqttClientPerformanceTest: INFO:
Testing Publish: QoS = 2 | msgs = 10000 | payload size = 264 | start = 1701125239141879.8 | end = 1701125245167484.0 | elapsed = 6.0256843319999995
Ran 4 tests in 17.460s
OK
```
PIOT-CDA-10-001: MqttClientConnectorTest
```
<terminated> MqttClientConnectorTest.py [unittest] [/home/zabe/programmingtheiot/.venv/bin/python] 0.00s Debugger warning: It seems that frozen modules are being used, which may
0.00s make the debugger miss breakpoints. Please pass -Xfrozen_modules-off
0.00s
to python to disable frozen modules.
0.00s - Note: Debugging will proceed. Set PYDEVD_DISABLE_FILE_VALIDATION=1 to disable this validation.
Finding files... done.
Importing test modules ... done.
2023-11-28 19:54:41, 458:MqttClientConnectorTest: INFO: Testing MqttClientConnector class...
2023-11-28 19:54:41, 460: ConfigUtil: INFO: Loading config: /home/zabe/programmingtheiot/python-components/config/PiotConfig.props
2023-11-28 19:54:41,462: ConfigUtil: DEBUG:Config: ['Mqtt.GatewayService', 'Coap. GatewayService', 'ConstrainedDevice']
2023-11-28 19:54:41, 463: ConfigUtil: INFO: Created instance of ConfigUtil: <programmingtheiot.common.ConfigUtil.ConfigUtil object at 0x7f763aa09a10> 2023-11-28 19:54:41,463: MqttClientConnector: INFO: MQTT Client ID: MqttclientTest
2023-11-28 19:54:41, 463: MqttClientConnector: INFO: 2023-11-28 19:54:41, 463: MqttClientConnector: INFO:
2023-11-28 19:54:41, 463: MqttClientConnector: INFO:
MQTT Broker Host: 127.0.0.1
MQTT Broker Port: 1883 MQTT Keep Alive: 60
2023-11-28 19:54:41,464:MqttClientConnector: INFO: MQTT client connecting to broker at host: 127.0.0.1 2023-11-28 19:55:46,467: MqttClientConnector: INFO:Disconnecting MQTT client from broker: 127.0.0.1
Ran 8 tests in 65.050s
OK (skipped=7)
```
PIIOT-CDA-10-002: DeviceDatamanagerCallbackTest
```
<terminated> DeviceDataManagerCallbackTest.py [/home/zabe/programmingtheiot/.venv/bin/python]
2023-11-28 20:03:40, 405: DeviceDataManagerCallbackTest: INFO: Testing DeviceDataManager class...
2023-11-28 20:03:40, 405: ConfigUtil: INFO: Loading config: /home/zabe/programmingtheiot/python-components/config/PiotConfig.props 2023-11-28 20:03:40, 406: ConfigUtil: DEBUG:Config: ['Mqtt. GatewayService', 'Coap. GatewayService', 'ConstrainedDevice']
2023-11-28 20:03:40, 407: ConfigUtil: INFO:Created instance of ConfigUtil: <programmingtheiot.common.ConfigUtil.ConfigUtil object at 0x7f0ae1188b10> 2023-11-28 20:03:40, 407:MqttClientConnector: INFO: MQTT Client ID: DeviceDataMQTT
2023-11-28 20:03:40,407:MqttClientConnector: INFO: 2023-11-28 20:03:40,407:MqttClientConnector: INFO: 2023-11-28 20:03:40,407:MqttClientConnector: INFO:
MQTT Broker Host: 127.0.0.1 MQTT Broker Port: 1883
MQTT Keep Alive: 60
2023-11-28 20:03:40,407: DeviceDataManager: INFO: Starting DeviceDataManager...
2023-11-28 20:03:40,407: MqttClientConnector: INFO: MQTT client connecting to broker at host: 127.0.0.1
2023-11-28 20:03:40,412: DeviceDataManager: INFO:Started DeviceDataManager.
2023-11-28 20:03:40,414: MqttClientConnector: INFO: [Callback] Connected to MQTT broker. Result code: 0
2023-11-28 20:03:40,415:MqttClientConnector: INFO: MQTT client subscribed: <paho.mqtt.client.Client object at 0x7f0ae0b66110> 2023-11-28 20:03:40,416:MqttClientConnector: INFO: MQTT client subscribed: <paho.mqtt.client.Client object at 0x7f0ae0b66110>
2023-11-28 20:03:50,413: DeviceDataManager: INFO:Stopping DeviceDataManager...
2023-11-28 20:03:50,414: MqttClientConnector: INFO: Disconnecting MQTT client from broker: 127.0.0.1 2023-11-28 20:03:50,414: DeviceDataManager: INFO: Stopped DeviceDataManager.
Ran 1 test in 10.010s
OK
```
PIOT-CDA-10-003: MqttClientConnectorTest
```
<terminated> MqttClientConnectorTest.py [/home/zabe/programmingthelot/.venv/bin/python]
2023-11-28 20:20:07,080:MqttClientConnectorTest: INFO: Testing MqttClientConnector class...
2023-11-28 20:20:07,080: ConfigUtil: INFO: Loading config: /home/zabe/programmingtheiot/python-components/config/PiotConfig.props 2023-11-28 20:20:07,080: ConfigUtil: DEBUG:Config: ['Mqtt. GatewayService', 'Coap. GatewayService', 'ConstrainedDevice']
2023-11-28 20:20:07,081: ConfigUtil: INFO:Created instance of ConfigUtil: <programmingtheiot.common.ConfigUtil.ConfigUtil object at 0x7f1e18981490> 2023-11-28 20:20:07,081: MqttClientConnector: INFO: MQTT Client ID: MqttclientTest 2023-11-28 20:20:07,081: MqttClientConnector: INFO: 2023-11-28 20:20:07,081: MqttClientConnector: INFO:
2023-11-28 20:20:07,081: MqttClientConnector: INFO:
MQTT Broker Host: 127.0.0.1
MQTT Broker Port: 1883
MQTT Keep Alive: 60
ssssss2023-11-28 20:20:07,082: DataUtil: INFO:Created DataUtil instance.
2023-11-28 20:20:07,082: MqttClientConnector: INFO: MQTT client connecting to broker at host: 127.0.0.1
2023-11-28 20:20:07,088: MqttClientConnector: INFO: [Callback] Connected to MQTT broker. Result code: 0
2023-11-28 20:20:07,092: MqttClientConnector: INFO: MQTT client subscribed: <paho.mqtt.client.Client object at 0x7f1e18969450>
2023-11-28 20:20:12,092: MqttClientConnector: INFO: [Callback] Actuator command message received. Topic: PIOT/ConstrainedDevice/ActuatorCmd. 2023-11-28 20:20:12,092: DataUtil: INFO:Created DataUtil instance.
2023-11-28 20:20:12,092: DefaultDataMessageListener: INFO: Actuator Command Msg: 0
2023-11-28 20:21:12,091: MqttClientConnector: INFO: Disconnecting MQTT client from broker: 127.0.0.1
Ran 8 tests in 65.043s
OK (skipped=7)
```
PIOT-CDA-10-004: DeviceDataManagerIntegrationTest
```
<terminated> DeviceDataManagerIntegrationTest.py [/home/zabe/programmingthelot/.venv/bin/python] 2023-11-28 20:26:40,923: DeviceDataManagerIntegrationTest: INFO: Testing DeviceDataManager class...
2023-11-28 20:26:40,926: ConfigUtil: INFO: Loading config: /home/zabe/programmingtheiot/python-components/config/PiotConfig.props 2023-11-28 20:26:40,927: ConfigUtil: DEBUG:Config: ['Mqtt. GatewayService', 'Coap. GatewayService', 'ConstrainedDevice'] 2023-11-28 20:26:40,927: ConfigUtil: INFO: Created instance of ConfigUtil: 2023-11-28 20:26:40,930: MqttClientConnector: INFO: 2023-11-28 20:26:40,930: MqttClientConnector: INFO:
2023-11-28 20:26:40,930: MqttClientConnector: INFO: 2023-11-28 20:26:40,930: MqttClientConnector: INFO:
<programmingtheiot.common.ConfigUtil.ConfigUtil object at 0x7f66dbbf67d0>
MQTT Client ID: DeviceDataMQTT MQTT Broker Host: 127.0.0.1 MQTT Broker Port: 1883
MQTT Keep Alive: 60
2023-11-28 20:26:40,930: DeviceDataManager: INFO: Starting DeviceDataManager...
2023-11-28 20:26:40,931: MqttClientConnector: INFO:MQTT client connecting to broker at host: 127.0.0.1 2023-11-28 20:26:40,947:MqttClientConnector: INFO: [Callback] Connected to MQTT broker. Result code: 0
2023-11-28 20:26:40,951: MqttClientConnector: INFO: MQTT client subscribed: <paho.mqtt.client.Client object at 0x7f66dbb06fd0> 2023-11-28 20:26:40, 954: DeviceDataManager: INFO:Started DeviceDataManager.
2023-11-28 20:26:40,955: MqttClientConnector: INFO: MQTT client subscribed: <paho.mqtt.client.Client object at 0x7f66dbb06fd0> 2023-11-28 20:27:55,954: DeviceDataManager: INFO: Stopping DeviceDataManager...
2023-11-28 20:27:55,955: MqttClientConnector: INFO: Disconnecting MQTT client from broker: 127.0.0.1 2023-11-28 20:27:55,958: DeviceDataManager: INFO: Stopped DeviceDataManager.
Ran 1 test in 15.036s
OK
```
PIOT-INT-10-003: Running CDA and GDA Together
```
<terminated> DeviceDataManagerIntegrationTest.py [/home/zabe/programmingthelot/.venv/bin/python] 2023-11-28 20:31:55,739: DeviceDataManagerIntegrationTest: INFO: Testing DeviceDataManager class...
2023-11-28 20:31:55,739: ConfigUtil: INFO: Loading config: /home/zabe/programmingtheiot/python-components/config/PiotConfig.props 2023-11-28 20:31:55,739: ConfigUtil: DEBUG:Config: ['Mqtt. GatewayService', 'Coap. GatewayService', 'ConstrainedDevice']
2023-11-28 20:31:55,739: ConfigUtil: INFO:Created instance of ConfigUtil: <programmingtheiot.common.ConfigUtil.ConfigUtil object at 0x7f5db2343b90> 2023-11-28 20:31:55,739:MqttClientConnector: INFO: MQTT Client ID: DeviceDataMQTT
2023-11-28 20:31:55,740:MqttClientConnector: INFO: 2023-11-28 20:31:55,740:MqttClientConnector: INFO: 2023-11-28 20:31:55,740:MqttClientConnector: INFO:
MQTT Broker Host: 127.0.0.1
MQTT Broker Port: 1883 MQTT Keep Alive: 60
2023-11-28 20:31:55,740: DeviceDataManager: INFO:Starting DeviceDataManager...
2023-11-28 20:31:55,740:MqttClientConnector: INFO: MQTT client connecting to broker at host: 127.0.0.1 2023-11-28 20:31:55,746: DeviceDataManager: INFO:Started DeviceDataManager.
2023-11-28 20:31:55,746:MqttClientConnector: INFO: [Callback] Connected to MQTT broker. Result code:
2023-11-28 20:31:55,748:MqttClientConnector: INFO: MQTT client subscribed: <paho.mqtt.client.Client object at 0x7f5db29ee9d0> 2023-11-28 20:31:55,748:MqttClientConnector: INFO: MQTT client subscribed: <paho.mqtt.client.Client object at 0x7f5db29ee9d0> 2023-11-28 20:33:35,746: DeviceDataManager: INFO: Stopping DeviceDataManager...
2023-11-28 20:33:35,747: MqttClientConnector: INFO: Disconnecting MQTT client from broker: 127.0.0.1 2023-11-28 20:33:35,747: DeviceDataManager: INFO: Stopped DeviceDataManager.
Ran 1 test in 100.009s
OK
```
PIOT-INT-10-004; CDA + GDA and TLS
```
<terminated> DeviceDataManagerIntegrationTest.py [/home/zabe/programmingthelot/.venv/bin/python] 2023-11-28 20:43:14,378: DeviceDataManagerIntegrationTest: INFO: Testing DeviceDataManager class...
2023-11-28 20:43:14,378: ConfigUtil: INFO: Loading config: /home/zabe/programmingtheiot/python-components/config/PiotConfig.props 2023-11-28 20:43:14,381: ConfigUtil: DEBUG:Config: ['Mqtt. GatewayService', 'Coap.GatewayService', 'ConstrainedDevice']
2023-11-28 20:43:14,381: ConfigUtil: INFO:Created instance of ConfigUtil: <programmingtheiot.common.ConfigUtil.ConfigUtil object at 0x7fd2fd87f190> 2023-11-28 20:43:14,381:MqttClientConnector: INFO: MQTT Client ID: DeviceDataMQTT
MQTT Broker Host: 127.0.0.1
MQTT Broker Port: 1883 MQTT Keep Alive: 60
2023-11-28 20:43:14,381:MqttClientConnector: INFO: 2023-11-28 20:43:14,381:MqttClientConnector: INFO: 2023-11-28 20:43:14,381:MqttClientConnector: INFO: 2023-11-28 20:43:14,381: DeviceDataManager: INFO:Starting DeviceDataManager...
2023-11-28 20:43:14,381:MqttClientConnector: INFO: Enabling TLS encryption...
/home/zabe/programmingtheiot/.venv/lib/python3.11/site-packages/paho/mqtt/client.py:792: DeprecationWarning: ssl.PROTOCOL_TLSv1_2 is deprecated
context = ssl.SSLContext(tls_version)
2023-11-28 20:43:14,389: MqttClientConnector: INFO: MQTT client connecting to broker at host: 127.0.0.1
2023-11-28 20:43:14,402: DeviceDataManager: INFO: Started DeviceDataManager.
2023-11-28 20:43:14,409: MqttClientConnector: INFO: [Callback] Connected to MQTT broker. Result code: 0
2023-11-28 20:43:14,410:MqttClientConnector: INFO: MQTT client subscribed: <paho.mqtt.client.Client object at 0x7fd2fceacb90> 2023-11-28 20:43:14,410:MqttClientConnector: INFO: MQTT client subscribed: <paho.mqtt.client.Client object at 0x7fd2fceacb90> 2023-11-28 20:44:54,405: DeviceDataManager: INFO: Stopping DeviceDataManager...
2023-11-28 20:44:54,405: MqttClientConnector: INFO:Disconnecting MQTT client from broker: 127.0.0.1 2023-11-28 20:44:54,405: DeviceDataManager: INFO:Stopped DeviceDataManager.
Ran 1 test in 100.028s
OK
```
EOF.
