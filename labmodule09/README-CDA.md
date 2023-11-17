# Constrained Device Application (Connected Devices)

## Lab Module 09

Be sure to implement all the PIOT-CDA-* issues (requirements) listed at [PIOT-INF-09-001 - Lab Module 09](https://github.com/orgs/programming-the-iot/projects/1#column-10488503).

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

![image](https://github.com/JadEletry/book-exercise-docs/assets/71851213/ea374343-f645-4afa-8cf8-b4e2f8aba15c)

### Unit Tests Executed

NOTE: TA's will execute your unit tests. You only need to list each test case below
(e.g. ConfigUtilTest, DataUtilTest, etc). Be sure to include all previous tests, too,
since you need to ensure you haven't introduced regressions.

### Integration Tests Executed

NOTE: TA's will execute most of your integration tests using their own environment, with
some exceptions (such as your cloud connectivity tests). In such cases, they'll review
your code to ensure it's correct. As for the tests you execute, you only need to list each
test case below (e.g. SensorSimAdapterManagerTest, DeviceDataManagerTest, etc.)

PIOT-CDA-09-002: Add GET functionality to CoapClientConnector - Discovery Test - Test Case<br>
![image](https://github.com/JadEletry/book-exercise-docs/assets/71851213/70d51213-ba85-4e71-ba3c-e0f276f97abc)

PIOT-CDA-09-002: Add GET functionality to CoapClientConnector - GET Actuator Command Test - Test Case
![image](https://github.com/JadEletry/book-exercise-docs/assets/71851213/7efe3ffd-634d-4283-8d31-71f004138302)

PIOT-CDA-09-004: Add POST functionality to CoapClientConnector -Test Cases for POST
```txt
2023-11-17 16:29:57,393:CoapClientConnectorTest:INFO:Testing CoapClientConnector class...
2023-11-17 16:29:57,393:ConfigUtil:INFO:Loading config: ../../../../../../../config/PiotConfig.props
2023-11-17 16:29:57,394:ConfigUtil:INFO:Created instance of ConfigUtil: <programmingtheiot.common.ConfigUtil.ConfigUtil object at 0x7f80972ec790>
2023-11-17 16:29:57,394:CoapClientConnector:INFO:	Host:Port: localhost:5683
2023-11-17 16:29:57,398:CoapClientConnector:INFO:Client created. Will invoke resources at: coap://localhost:5683/
ssss2023-11-17 16:29:57,398:CoapClientConnector:INFO:Issuing GET with path: PIOT/ConstrainedDevice/ActuatorCmd
2023-11-17 16:29:57,398:messagelayer:INFO:send_request - From None, To ('127.0.0.1', 5683), None-None, GET-4d7b, [Uri-Path: PIOT, Uri-Path: ConstrainedDevice, Uri-Path: ActuatorCmd, ] No payload
2023-11-17 16:29:57,398:coap:INFO:send_datagram - From None, To ('127.0.0.1', 5683), CON-54980, GET-4d7b, [Uri-Path: PIOT, Uri-Path: ConstrainedDevice, Uri-Path: ActuatorCmd, ] No payload
/home/zabe/programmingtheiot/piotvenv/lib/python3.11/site-packages/coapthon/client/coap.py:250: DeprecationWarning: isSet() is deprecated, use is_set() instead
  while not self.stopped.isSet():
/home/zabe/programmingtheiot/piotvenv/lib/python3.11/site-packages/coapthon/client/coap.py:218: DeprecationWarning: isSet() is deprecated, use is_set() instead
  and not transaction.retransmit_stop.isSet():
2023-11-17 16:29:57,470:messagelayer:INFO:receive_empty - From ('127.0.0.1', 5683), To None, ACK-54980, EMPTY-None, [] No payload
2023-11-17 16:29:57,485:coap:INFO:receive_datagram - From ('127.0.0.1', 5683), To None, CON-55243, CONTENT-4d7b, [Content-Type: 0, ] No payload
2023-11-17 16:29:57,490:messagelayer:INFO:receive_response - From ('127.0.0.1', 5683), To None, CON-55243, CONTENT-4d7b, [Content-Type: 0, ] No payload
2023-11-17 16:29:57,490:messagelayer:INFO:send_empty - From None, To None, ACK-None, EMPTY-None, [] No payload
2023-11-17 16:29:57,494:coap:INFO:send_datagram - From None, To ('127.0.0.1', 5683), ACK-55243, EMPTY-4d7b, [] No payload
2023-11-17 16:30:00,486:coap:INFO:receive_datagram - From ('127.0.0.1', 5683), To None, CON-55243, CONTENT-4d7b, [Content-Type: 0, ] No payload
2023-11-17 16:30:00,492:messagelayer:INFO:receive_response - From ('127.0.0.1', 5683), To None, CON-55243, CONTENT-4d7b, [Content-Type: 0, ] No payload
2023-11-17 16:30:00,492:messagelayer:INFO:send_empty - From None, To None, ACK-None, EMPTY-None, [] No payload
2023-11-17 16:30:00,492:coap:INFO:send_datagram - From None, To ('127.0.0.1', 5683), ACK-55243, EMPTY-4d7b, [] No payload
2023-11-17 16:30:05,515:CoapClientConnector:WARNING:GET response invalid. Ignoring.
.2023-11-17 16:30:05,515:CoapClientConnector:INFO:Issuing GET with path: PIOT/ConstrainedDevice/ActuatorCmd
2023-11-17 16:30:05,515:messagelayer:INFO:send_request - From None, To ('127.0.0.1', 5683), NON-None, GET-b340, [Uri-Path: PIOT, Uri-Path: ConstrainedDevice, Uri-Path: ActuatorCmd, ] No payload
2023-11-17 16:30:05,515:coap:INFO:send_datagram - From None, To ('127.0.0.1', 5683), NON-54981, GET-b340, [Uri-Path: PIOT, Uri-Path: ConstrainedDevice, Uri-Path: ActuatorCmd, ] No payload
2023-11-17 16:30:05,521:coap:INFO:receive_datagram - From ('127.0.0.1', 5683), To None, NON-55244, CONTENT-b340, [Content-Type: 0, ] No payload
2023-11-17 16:30:05,521:messagelayer:INFO:receive_response - From ('127.0.0.1', 5683), To None, NON-55244, CONTENT-b340, [Content-Type: 0, ] No payload
2023-11-17 16:30:05,522:CoapClientConnector:INFO:GET response received.
2023-11-17 16:30:05,522:CoapClientConnector:INFO:ActuatorData received: None
2023-11-17 16:30:05,522:DataUtil:INFO:Created DataUtil instance.
2023-11-17 16:30:05,522:DataUtil:WARNING:JSON data is empty or null. Returning null.
.ss2023-11-17 16:30:05,523:DataUtil:INFO:Created DataUtil instance.
2023-11-17 16:30:05,523:CoapClientConnector:INFO:Issuing PUT with path: PIOT/ConstrainedDevice/SensorMsg
.2023-11-17 16:30:05,523:messagelayer:INFO:send_request - From None, To ('127.0.0.1', 5683), None-None, PUT-3e4b, [Uri-Path: PIOT, Uri-Path: ConstrainedDevice, Uri-Path: SensorMsg, ] {
    "timeStamp": "...264 bytes
2023-11-17 16:30:05,524:DataUtil:INFO:Created DataUtil instance.
2023-11-17 16:30:05,524:CoapClientConnector:INFO:Issuing PUT with path: PIOT/ConstrainedDevice/SensorMsg
2023-11-17 16:30:05,524:coap:INFO:send_datagram - From None, To ('127.0.0.1', 5683), CON-54982, PUT-3e4b, [Uri-Path: PIOT, Uri-Path: ConstrainedDevice, Uri-Path: SensorMsg, ] {
    "timeStamp": "...264 bytes
2023-11-17 16:30:05,525:messagelayer:INFO:send_request - From None, To ('127.0.0.1', 5683), NON-None, PUT-bb65, [Uri-Path: PIOT, Uri-Path: ConstrainedDevice, Uri-Path: SensorMsg, ] {
    "timeStamp": "...264 bytes
2023-11-17 16:30:05,526:coap:INFO:send_datagram - From None, To ('127.0.0.1', 5683), NON-54983, PUT-bb65, [Uri-Path: PIOT, Uri-Path: ConstrainedDevice, Uri-Path: SensorMsg, ] {
    "timeStamp": "...264 bytes
/home/zabe/programmingtheiot/piotvenv/lib/python3.11/site-packages/coapthon/client/helperclient.py:62: DeprecationWarning: isSet() is deprecated, use is_set() instead
  while not self.protocol.stopped.isSet():
2023-11-17 16:30:05,537:messagelayer:INFO:receive_empty - From ('127.0.0.1', 5683), To None, ACK-54982, EMPTY-None, [] No payload
.
----------------------------------------------------------------------
Ran 10 tests in 8.146s

OK (skipped=6)
2023-11-17 16:30:05,769:coap:INFO:receive_datagram - From ('127.0.0.1', 5683), To None, CON-55246, CHANGED-3e4b, [Content-Type: 0, ] Update system perf d...50 bytes
2023-11-17 16:30:05,769:messagelayer:INFO:receive_response - From ('127.0.0.1', 5683), To None, CON-55246, CHANGED-3e4b, [Content-Type: 0, ] Update system perf d...50 bytes
2023-11-17 16:30:05,769:messagelayer:INFO:send_empty - From None, To None, ACK-None, EMPTY-None, [] No payload
2023-11-17 16:30:05,769:coap:INFO:send_datagram - From None, To ('127.0.0.1', 5683), ACK-55246, EMPTY-3e4b, [] No payload
2023-11-17 16:30:05,769:coap:INFO:receive_datagram - From ('127.0.0.1', 5683), To None, NON-55245, CHANGED-bb65, [Content-Type: 0, ] Update system perf d...50 bytes
2023-11-17 16:30:05,769:messagelayer:INFO:receive_response - From ('127.0.0.1', 5683), To None, NON-55245, CHANGED-bb65, [Content-Type: 0, ] Update system perf d...50 bytes
2023-11-17 16:30:05,779:CoapClientConnector:INFO:PUT response received: Update system perf data request handled: SensorMsg
2023-11-17 16:30:05,779:CoapClientConnector:INFO:PUT response received: Update system perf data request handled: SensorMsg
2023-11-17 16:30:06,421:coap:INFO:receive_datagram - From ('127.0.0.1', 5683), To None, CON-55243, CONTENT-4d7b, [Content-Type: 0, ] No payload
2023-11-17 16:30:06,421:messagelayer:INFO:receive_response - From ('127.0.0.1', 5683), To None, CON-55243, CONTENT-4d7b, [Content-Type: 0, ] No payload
2023-11-17 16:30:06,421:messagelayer:INFO:send_empty - From None, To None, ACK-None, EMPTY-None, [] No payload
2023-11-17 16:30:06,421:coap:INFO:send_datagram - From None, To ('127.0.0.1', 5683), ACK-55243, EMPTY-4d7b, [] No payload
2023-11-17 16:30:06,431:CoapClientConnector:INFO:PUT response received: None
2023-11-17 16:30:07,889:coap:INFO:receive_datagram - From ('127.0.0.1', 5683), To None, CON-55246, CHANGED-3e4b, [Content-Type: 0, ] Update system perf d...50 bytes
2023-11-17 16:30:07,889:messagelayer:INFO:receive_response - From ('127.0.0.1', 5683), To None, CON-55246, CHANGED-3e4b, [Content-Type: 0, ] Update system perf d...50 bytes
2023-11-17 16:30:07,889:messagelayer:INFO:send_empty - From None, To None, ACK-None, EMPTY-None, [] No payload
2023-11-17 16:30:07,889:coap:INFO:send_datagram - From None, To ('127.0.0.1', 5683), ACK-55246, EMPTY-3e4b, [] No payload
2023-11-17 16:30:07,891:CoapClientConnector:INFO:PUT response received: Update system perf data request handled: SensorMsg
2023-11-17 16:30:12,031:coap:INFO:receive_datagram - From ('127.0.0.1', 5683), To None, CON-55246, CHANGED-3e4b, [Content-Type: 0, ] Update system perf d...50 bytes
2023-11-17 16:30:12,031:messagelayer:INFO:receive_response - From ('127.0.0.1', 5683), To None, CON-55246, CHANGED-3e4b, [Content-Type: 0, ] Update system perf d...50 bytes
2023-11-17 16:30:12,031:messagelayer:INFO:send_empty - From None, To None, ACK-None, EMPTY-None, [] No payload
2023-11-17 16:30:12,031:coap:INFO:send_datagram - From None, To ('127.0.0.1', 5683), ACK-55246, EMPTY-3e4b, [] No payload
2023-11-17 16:30:12,034:CoapClientConnector:INFO:PUT response received: Update system perf data request handled: SensorMsg
2023-11-17 16:30:18,159:coap:INFO:receive_datagram - From ('127.0.0.1', 5683), To None, CON-55243, CONTENT-4d7b, [Content-Type: 0, ] No payload
2023-11-17 16:30:18,159:messagelayer:INFO:receive_response - From ('127.0.0.1', 5683), To None, CON-55243, CONTENT-4d7b, [Content-Type: 0, ] No payload
2023-11-17 16:30:18,159:messagelayer:INFO:send_empty - From None, To None, ACK-None, EMPTY-None, [] No payload
2023-11-17 16:30:18,159:coap:INFO:send_datagram - From None, To ('127.0.0.1', 5683), ACK-55243, EMPTY-4d7b, [] No payload
2023-11-17 16:30:18,162:CoapClientConnector:INFO:PUT response received: None
2023-11-17 16:30:20,334:coap:INFO:receive_datagram - From ('127.0.0.1', 5683), To None, CON-55246, CHANGED-3e4b, [Content-Type: 0, ] Update system perf d...50 bytes
2023-11-17 16:30:20,335:messagelayer:INFO:receive_response - From ('127.0.0.1', 5683), To None, CON-55246, CHANGED-3e4b, [Content-Type: 0, ] Update system perf d...50 bytes
2023-11-17 16:30:20,335:messagelayer:INFO:send_empty - From None, To None, ACK-None, EMPTY-None, [] No payload
2023-11-17 16:30:20,335:coap:INFO:send_datagram - From None, To ('127.0.0.1', 5683), ACK-55246, EMPTY-3e4b, [] No payload
2023-11-17 16:30:20,336:CoapClientConnector:INFO:PUT response received: Update system perf data request handled: SensorMsg
2023-11-17 16:30:36,889:coap:INFO:receive_datagram - From ('127.0.0.1', 5683), To None, CON-55246, CHANGED-3e4b, [Content-Type: 0, ] Update system perf d...50 bytes
2023-11-17 16:30:36,889:messagelayer:INFO:receive_response - From ('127.0.0.1', 5683), To None, CON-55246, CHANGED-3e4b, [Content-Type: 0, ] Update system perf d...50 bytes
2023-11-17 16:30:36,889:messagelayer:INFO:send_empty - From None, To None, ACK-None, EMPTY-None, [] No payload
2023-11-17 16:30:36,889:coap:INFO:send_datagram - From None, To ('127.0.0.1', 5683), ACK-55246, EMPTY-3e4b, [] No payload
2023-11-17 16:30:36,891:CoapClientConnector:INFO:PUT response received: Update system perf data request handled: SensorMsg
2023-11-17 16:30:41,611:coap:INFO:receive_datagram - From ('127.0.0.1', 5683), To None, CON-55243, CONTENT-4d7b, [Content-Type: 0, ] No payload
2023-11-17 16:30:41,611:messagelayer:INFO:receive_response - From ('127.0.0.1', 5683), To None, CON-55243, CONTENT-4d7b, [Content-Type: 0, ] No payload
2023-11-17 16:30:41,611:messagelayer:INFO:send_empty - From None, To None, ACK-None, EMPTY-None, [] No payload
2023-11-17 16:30:41,611:coap:INFO:send_datagram - From None, To ('127.0.0.1', 5683), ACK-55243, EMPTY-4d7b, [] No payload
2023-11-17 16:30:41,613:CoapClientConnector:INFO:PUT response received: None
```

PIOT-CDA-09-005: Add DELETE functionality to CoapClientConnector - Test Case for DELETE
```txt
2023-11-17 16:41:33,170:CoapClientConnectorTest:INFO:Testing CoapClientConnector class...
2023-11-17 16:41:33,170:ConfigUtil:INFO:Loading config: ../../../../../../../config/PiotConfig.props
2023-11-17 16:41:33,171:ConfigUtil:INFO:Created instance of ConfigUtil: <programmingtheiot.common.ConfigUtil.ConfigUtil object at 0x7fa9e4bbdd10>
2023-11-17 16:41:33,171:CoapClientConnector:INFO:	Host:Port: localhost:5683
2023-11-17 16:41:33,177:CoapClientConnector:INFO:Client created. Will invoke resources at: coap://localhost:5683/
ss2023-11-17 16:41:33,177:CoapClientConnector:INFO:Issuing DELETE with path: PIOT/ConstrainedDevice/SensorMsg
2023-11-17 16:41:33,187:messagelayer:INFO:send_request - From None, To ('127.0.0.1', 5683), None-None, DELETE-281f, [Uri-Path: PIOT, Uri-Path: ConstrainedDevice, Uri-Path: SensorMsg, ] No payload
.2023-11-17 16:41:33,188:coap:INFO:send_datagram - From None, To ('127.0.0.1', 5683), CON-41876, DELETE-281f, [Uri-Path: PIOT, Uri-Path: ConstrainedDevice, Uri-Path: SensorMsg, ] No payload
2023-11-17 16:41:33,188:CoapClientConnector:INFO:Issuing DELETE with path: PIOT/ConstrainedDevice/SensorMsg
2023-11-17 16:41:33,190:messagelayer:INFO:send_request - From None, To ('127.0.0.1', 5683), NON-None, DELETE-5b44, [Uri-Path: PIOT, Uri-Path: ConstrainedDevice, Uri-Path: SensorMsg, ] No payload
2023-11-17 16:41:33,190:coap:INFO:send_datagram - From None, To ('127.0.0.1', 5683), NON-41877, DELETE-5b44, [Uri-Path: PIOT, Uri-Path: ConstrainedDevice, Uri-Path: SensorMsg, ] No payload
.ssssss
----------------------------------------------------------------------
Ran 10 tests in 0.026s

OK (skipped=8)
2023-11-17 16:41:33,292:coap:INFO:receive_datagram - From ('127.0.0.1', 5683), To None, NON-19184, METHOD_NOT_ALLOWED-5b44, [] No payload
2023-11-17 16:41:33,292:messagelayer:INFO:receive_response - From ('127.0.0.1', 5683), To None, NON-19184, METHOD_NOT_ALLOWED-5b44, [] No payload
2023-11-17 16:41:33,312:CoapClientConnector:INFO:DELETE response received: None
2023-11-17 16:41:33,314:coap:INFO:receive_datagram - From ('127.0.0.1', 5683), To None, ACK-41876, METHOD_NOT_ALLOWED-281f, [] No payload
2023-11-17 16:41:33,314:messagelayer:INFO:receive_response - From ('127.0.0.1', 5683), To None, ACK-41876, METHOD_NOT_ALLOWED-281f, [] No payload
2023-11-17 16:41:33,347:CoapClientConnector:INFO:DELETE response received: None
```

PIOT-CDA-09-006: Add OBSERVE functionality to CoapClientConnector - Test Case Observe
```txt
2023-11-17 17:06:13,694:CoapClientConnectorTest:INFO:Testing CoapClientConnector class...
2023-11-17 17:06:13,694:ConfigUtil:INFO:Loading config: ../../../../../../../config/PiotConfig.props
2023-11-17 17:06:13,696:ConfigUtil:INFO:Created instance of ConfigUtil: <programmingtheiot.common.ConfigUtil.ConfigUtil object at 0x7f99ddcb3810>
2023-11-17 17:06:13,696:CoapClientConnector:INFO:	Host:Port: localhost:5683
2023-11-17 17:06:13,706:CoapClientConnector:INFO:Client created. Will invoke resources at: coap://localhost:5683/
2023-11-17 17:06:13,710:messagelayer:INFO:send_request - From None, To ('127.0.0.1', 5683), None-None, GET-None, [Uri-Path: PIOT, Uri-Path: ConstrainedDevice, Uri-Path: ActuatorCmd, Observe: 0, ] No payload
2023-11-17 17:06:13,710:coap:INFO:send_datagram - From None, To ('127.0.0.1', 5683), CON-61815, GET-None, [Uri-Path: PIOT, Uri-Path: ConstrainedDevice, Uri-Path: ActuatorCmd, Observe: 0, ] No payload
/home/zabe/programmingtheiot/piotvenv/lib/python3.11/site-packages/coapthon/client/coap.py:250: DeprecationWarning: isSet() is deprecated, use is_set() instead
  while not self.stopped.isSet():
/home/zabe/programmingtheiot/piotvenv/lib/python3.11/site-packages/coapthon/client/coap.py:218: DeprecationWarning: isSet() is deprecated, use is_set() instead
  and not transaction.retransmit_stop.isSet():
/home/zabe/programmingtheiot/piotvenv/lib/python3.11/site-packages/coapthon/client/helperclient.py:62: DeprecationWarning: isSet() is deprecated, use is_set() instead
  while not self.protocol.stopped.isSet():
2023-11-17 17:06:13,765:messagelayer:INFO:receive_empty - From ('127.0.0.1', 5683), To None, ACK-61815, EMPTY-None, [] No payload
2023-11-17 17:06:13,790:coap:INFO:receive_datagram - From ('127.0.0.1', 5683), To None, CON-32431, CONTENT-None, [Observe: 0, Content-Type: 0, ] No payload
2023-11-17 17:06:13,791:messagelayer:INFO:receive_response - From ('127.0.0.1', 5683), To None, CON-32431, CONTENT-None, [Observe: 0, Content-Type: 0, ] No payload
2023-11-17 17:06:13,791:messagelayer:INFO:send_empty - From None, To None, ACK-None, EMPTY-None, [] No payload
2023-11-17 17:06:13,791:coap:INFO:send_datagram - From None, To ('127.0.0.1', 5683), ACK-32431, EMPTY-None, [] No payload
2023-11-17 17:06:13,791:messagelayer:INFO:send_empty - From None, To None, ACK-None, EMPTY-None, [] No payload
2023-11-17 17:06:13,791:coap:INFO:send_datagram - From None, To ('127.0.0.1', 5683), ACK-32431, EMPTY-None, [] No payload
2023-11-17 17:06:13,847:CoapClientConnector:INFO:Received actuator command response to resource PIOT/ConstrainedDevice/ActuatorCmd: None
2023-11-17 17:06:43,720:CoapClientConnector:INFO:Canceling observe for resource PIOT/ConstrainedDevice/ActuatorCmd.
2023-11-17 17:06:43,720:messagelayer:INFO:send_empty - From None, To ('127.0.0.1', 5683), RST-32431, EMPTY-None, [] No payload
2023-11-17 17:06:43,720:coap:INFO:send_datagram - From None, To ('127.0.0.1', 5683), RST-32431, EMPTY-None, [] No payload
2023-11-17 17:06:43,768:CoapClientConnector:INFO:Canceled observe for resource PIOT/ConstrainedDevice/ActuatorCmd.
.s2023-11-17 17:06:43,803:CoapClientConnector:INFO:Issuing DELETE with path: PIOT/ConstrainedDevice/SensorMsg
.2023-11-17 17:06:43,803:messagelayer:INFO:send_request - From None, To ('127.0.0.1', 5683), None-None, DELETE-eb3d, [Uri-Path: PIOT, Uri-Path: ConstrainedDevice, Uri-Path: SensorMsg, ] No payload
2023-11-17 17:06:43,804:CoapClientConnector:INFO:Issuing DELETE with path: PIOT/ConstrainedDevice/SensorMsg
2023-11-17 17:06:43,804:coap:INFO:send_datagram - From None, To ('127.0.0.1', 5683), CON-61816, DELETE-eb3d, [Uri-Path: PIOT, Uri-Path: ConstrainedDevice, Uri-Path: SensorMsg, ] No payload
.ssssss2023-11-17 17:06:43,804:messagelayer:INFO:send_request - From None, To ('127.0.0.1', 5683), NON-None, DELETE-93be, [Uri-Path: PIOT, Uri-Path: ConstrainedDevice, Uri-Path: SensorMsg, ] No payload

----------------------------------------------------------------------
Ran 10 tests in 30.121s

OK (skipped=7)
2023-11-17 17:06:43,815:coap:INFO:send_datagram - From None, To ('127.0.0.1', 5683), NON-61817, DELETE-93be, [Uri-Path: PIOT, Uri-Path: ConstrainedDevice, Uri-Path: SensorMsg, ] No payload
2023-11-17 17:06:46,163:coap:INFO:send_datagram - From None, To ('127.0.0.1', 5683), CON-61816, DELETE-eb3d, [Uri-Path: PIOT, Uri-Path: ConstrainedDevice, Uri-Path: SensorMsg, ] No payload
2023-11-17 17:06:50,845:coap:INFO:send_datagram - From None, To ('127.0.0.1', 5683), CON-61816, DELETE-eb3d, [Uri-Path: PIOT, Uri-Path: ConstrainedDevice, Uri-Path: SensorMsg, ] No payload
2023-11-17 17:07:00,205:coap:INFO:send_datagram - From None, To ('127.0.0.1', 5683), CON-61816, DELETE-eb3d, [Uri-Path: PIOT, Uri-Path: ConstrainedDevice, Uri-Path: SensorMsg, ] No payload
2023-11-17 17:07:56,347:coap:WARNING:Give up on message From None, To ('127.0.0.1', 5683), CON-61816, DELETE-eb3d, [Uri-Path: PIOT, Uri-Path: ConstrainedDevice, Uri-Path: SensorMsg, ] No payload
```
EOF.
