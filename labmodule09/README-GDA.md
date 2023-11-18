# Gateway Device Application (Connected Devices)

## Lab Module 09

Be sure to implement all the PIOT-CDA-* issues (requirements) listed at [PIOT-INF-09-001 - Lab Module 09](https://github.com/orgs/programming-the-iot/projects/1#column-10488503).

### Description

NOTE: Include two full paragraphs describing your implementation approach by answering the questions listed below.

What does your implementation do? 

Our Gateway Device Application (GDA) implementation incorporates a CoAP (Constrained Application Protocol) client, enhancing the device's capability to interact with servers using CoAP messaging. This client primarily facilitates GET, PUT, and OBSERVE requests, enabling the device to retrieve, send, and monitor data from diverse sources. Notably, the client supports CONFIRMABLE (CON) and NON-CONFIRMABLE (NON) messages, ensuring reliable and efficient communication between the GDA and servers. Moreover, it manages payload encoding and decoding intricacies, crucial for interpreting messages exchanged with external servers.

How does your implementation work?

Within the Gateway Device Application, the CoAP client initiates communication channels with servers using CoAP messages. For a GET request, it constructs a request message and awaits the server's response, interpreting the received data for local processing. When executing a PUT request, the client crafts and dispatches data to designated servers, conforming to CoAP standards. Additionally, it supports OBSERVE functionality, enabling continual monitoring of specific resources and handling subsequent updates received from servers. Throughout these interactions, the client meticulously handles various message types, maintaining data integrity and ensuring efficient communication between the device and external servers.

### Code Repository and Branch

NOTE: Be sure to include the branch (e.g. https://github.com/programming-the-iot/python-components/tree/alpha001).

URL: https://github.com/ShahzabeM/GDA-Java/tree/labmodule09

### UML Design Diagram(s)

NOTE: Include one or more UML designs representing your solution. It's expected each
diagram you provide will look similar to, but not the same as, its counterpart in the
book [Programming the IoT](https://learning.oreilly.com/library/view/programming-the-internet/9781492081401/).

![image](https://github.com/JadEletry/book-exercise-docs/assets/71851213/5ba3aaa3-9c06-4ec1-acd5-4518d4da15df)


### Unit Tests Executed

NOTE: TA's will execute your unit tests. You only need to list each test case below
(e.g. ConfigUtilTest, DataUtilTest, etc). Be sure to include all previous tests, too,
since you need to ensure you haven't introduced regressions.

### Integration Tests Executed

NOTE: TA's will execute most of your integration tests using their own environment, with
some exceptions (such as your cloud connectivity tests). In such cases, they'll review
your code to ensure it's correct. As for the tests you execute, you only need to list each
test case below (e.g. SensorSimAdapterManagerTest, DeviceDataManagerTest, etc.)

GDA-09-004 - CoapClientConnectorTest - Integration Test for GET
```txt
19:52:04.829 [main] INFO org.eclipse.californium.elements.config.Configuration - defaults added COAP.
19:52:04.834 [main] INFO org.eclipse.californium.elements.config.Configuration - defaults added SYS.
19:52:04.838 [main] INFO org.eclipse.californium.elements.config.Configuration - defaults added UDP.
Nov 17, 2023 7:52:04 PM programmingtheiot.gda.connection.CoapClientConnector initClient
INFO: Created client connection to server / resource: coap://localhost:5683
Nov 17, 2023 7:52:05 PM programmingtheiot.gda.connection.CoapClientConnector <init>
INFO: Using URL for server conn: coap://localhost:5683
19:52:05.086 [main] DEBUG org.eclipse.californium.elements.util.NetworkInterfacesUtil - Found broadcast address /10.0.2.255 - enp0s3.
19:52:05.111 [main] INFO org.eclipse.californium.elements.config.Configuration - loading properties from file /home/zabe/programmingtheiot/java-components/Californium3.properties
19:52:05.127 [main] INFO org.eclipse.californium.core.network.RandomTokenGenerator - using tokens of 8 bytes in length
19:52:05.183 [main] DEBUG org.eclipse.californium.core.network.InMemoryMessageExchangeStore - coap using TokenProvider org.eclipse.californium.core.network.RandomTokenGenerator
19:52:05.188 [main] INFO org.eclipse.californium.ban - Started.
19:52:05.189 [main] INFO org.eclipse.californium.core.network.CoapEndpoint - coap CoapEndpoint uses udp context
19:52:05.197 [main] INFO org.eclipse.californium.core.network.stack.BlockwiseLayer - coap BlockwiseLayer uses MAX_MESSAGE_SIZE=1024, PREFERRED_BLOCK_SIZE=512, BLOCKWISE_STATUS_LIFETIME=300000, MAX_RESOURCE_BODY_SIZE=8192, BLOCKWISE_STRICT_BLOCK2_OPTION=false
19:52:05.203 [main] INFO org.eclipse.californium.core.network.CoapEndpoint - coap Endpoint [coap://0.0.0.0:0] requires an executor to start, using default single-threaded daemon executor
19:52:05.230 [main] DEBUG org.eclipse.californium.core.network.CoapEndpoint - coap Starting endpoint at coap://0.0.0.0:0
19:52:05.232 [main] DEBUG org.eclipse.californium.core.network.InMemoryMessageExchangeStore - coap no MessageIdProvider set, using default org.eclipse.californium.core.network.InMemoryMessageIdProvider
19:52:05.236 [main] INFO org.eclipse.californium.elements.UDPConnector - UDPConnector starts up 2 sender threads and 2 receiver threads
19:52:05.245 [UDP-Receiver-0.0.0.0/0.0.0.0:0[0]] DEBUG org.eclipse.californium.elements.UDPConnector - Starting network stage thread [UDP-Receiver-0.0.0.0/0.0.0.0:0[0]]
19:52:05.246 [UDP-Receiver-0.0.0.0/0.0.0.0:0[1]] DEBUG org.eclipse.californium.elements.UDPConnector - Starting network stage thread [UDP-Receiver-0.0.0.0/0.0.0.0:0[1]]
19:52:05.248 [UDP-Sender-0.0.0.0/0.0.0.0:0[0]] DEBUG org.eclipse.californium.elements.UDPConnector - Starting network stage thread [UDP-Sender-0.0.0.0/0.0.0.0:0[0]]
19:52:05.287 [main] INFO org.eclipse.californium.elements.UDPConnector - UDPConnector listening on /[0:0:0:0:0:0:0:0]:60608, recv buf = 106496, send buf = 106496, recv packet size = 2048
19:52:05.287 [UDP-Sender-0.0.0.0/0.0.0.0:0[1]] DEBUG org.eclipse.californium.elements.UDPConnector - Starting network stage thread [UDP-Sender-0.0.0.0/0.0.0.0:0[1]]
19:52:05.288 [main] INFO org.eclipse.californium.core.network.CoapEndpoint - coap Started endpoint at coap://[0:0:0:0:0:0:0:0]:60608
19:52:05.289 [main] INFO org.eclipse.californium.core.network.EndpointManager - created implicit endpoint coap://[0:0:0:0:0:0:0:0]:60608 for coap
19:52:05.334 [:CoapEndpoint-UDP-0.0.0.0:0#1] DEBUG org.eclipse.californium.core.network.stack.ReliabilityLayer - Exchange[L1, localhost:5683] send request
19:52:05.334 [:CoapEndpoint-UDP-0.0.0.0:0#1] DEBUG org.eclipse.californium.core.network.stack.ReliabilityLayer - Exchange[L1, localhost:5683] prepare retransmission for CON-GET    MID=   -1, Token=null, OptionSet={"Uri-Host":"localhost", "Uri-Path":["PIOT","GatewayDevice","MgmtStatusMsg"]}, <empty data>
19:52:05.337 [:CoapEndpoint-UDP-0.0.0.0:0#1] DEBUG org.eclipse.californium.core.network.InMemoryMessageExchangeStore - coap Exchange[L1, localhost:5683] added with generated mid KeyMID[localhost/127.0.0.1:5683-54317], CON-GET    MID=54317, Token=null, OptionSet={"Uri-Host":"localhost", "Uri-Path":["PIOT","GatewayDevice","MgmtStatusMsg"]}, <empty data>
19:52:05.338 [:CoapEndpoint-UDP-0.0.0.0:0#1] DEBUG org.eclipse.californium.core.network.InMemoryMessageExchangeStore - coap Exchange[L1, localhost:5683] added with generated token KeyToken[localhost/127.0.0.1:5683-282FF8EFF0279363], CON-GET    MID=54317, Token=282FF8EFF0279363, OptionSet={"Uri-Host":"localhost", "Uri-Path":["PIOT","GatewayDevice","MgmtStatusMsg"]}, <empty data>
19:52:05.339 [:CoapEndpoint-UDP-0.0.0.0:0#1] DEBUG org.eclipse.californium.core.network.UdpMatcher - tracking open request [KeyMID[localhost/127.0.0.1:5683-54317], KeyToken[localhost/127.0.0.1:5683-282FF8EFF0279363]]
19:52:05.343 [UDP-Sender-0.0.0.0/0.0.0.0:0[0]] DEBUG org.eclipse.californium.elements.UDPConnector - UDPConnector (Thread[UDP-Sender-0.0.0.0/0.0.0.0:0[0],5,Californium/Elements]) sent 57 bytes to localhost/127.0.0.1:5683
19:52:05.421 [UDP-Receiver-0.0.0.0/0.0.0.0:0[0]] DEBUG org.eclipse.californium.elements.UDPConnector - UDPConnector ([0:0:0:0:0:0:0:0]:60608) received 12 bytes from 127.0.0.1:5683
19:52:05.486 [:CoapEndpoint-UDP-0.0.0.0:0#1] DEBUG org.eclipse.californium.core.network.stack.BlockwiseLayer - coap  received error ACK-4.04   MID=54317, Token=282FF8EFF0279363, OptionSet={}, <empty data>:
19:52:05.487 [:CoapEndpoint-UDP-0.0.0.0:0#1] DEBUG org.eclipse.californium.core.network.Exchange - Exchange[L1, localhost:5683, complete]!
19:52:05.488 [:CoapEndpoint-UDP-0.0.0.0:0#1] DEBUG org.eclipse.californium.core.network.InMemoryMessageExchangeStore - coap removing Exchange[L1, localhost:5683, complete] for token KeyToken[localhost/127.0.0.1:5683-282FF8EFF0279363]
19:52:05.488 [:CoapEndpoint-UDP-0.0.0.0:0#1] DEBUG org.eclipse.californium.core.network.InMemoryMessageExchangeStore - coap removing Exchange[L1, localhost:5683, complete] for MID KeyMID[localhost/127.0.0.1:5683-54317]
19:52:05.489 [:CoapEndpoint-UDP-0.0.0.0:0#1] DEBUG org.eclipse.californium.core.network.Exchange - local Exchange[L1, localhost:5683, complete] completed CON-GET    MID=54317, Token=282FF8EFF0279363, OptionSet={"Uri-Host":"localhost", "Uri-Path":["PIOT","GatewayDevice","MgmtStatusMsg"]}, acked <empty data>!
Nov 17, 2023 7:52:05 PM programmingtheiot.gda.connection.CoapClientConnector sendGetRequest
INFO: Handling GET. Response: false - {} - 4.04 - 
Nov 17, 2023 7:52:05 PM programmingtheiot.gda.connection.CoapClientConnector initClient
INFO: Created client connection to server / resource: coap://localhost:5683
Nov 17, 2023 7:52:05 PM programmingtheiot.gda.connection.CoapClientConnector <init>
INFO: Using URL for server conn: coap://localhost:5683
19:52:05.520 [:CoapEndpoint-UDP-0.0.0.0:0#1] DEBUG org.eclipse.californium.core.network.stack.ReliabilityLayer - Exchange[L2, localhost:5683] send request
19:52:05.526 [:CoapEndpoint-UDP-0.0.0.0:0#1] DEBUG org.eclipse.californium.core.network.InMemoryMessageExchangeStore - coap Exchange[L2, localhost:5683] added with generated mid KeyMID[localhost/127.0.0.1:5683-54318], NON-GET    MID=54318, Token=null, OptionSet={"Uri-Host":"localhost", "Uri-Path":["PIOT","GatewayDevice","MgmtStatusMsg"]}, <empty data>
19:52:05.552 [:CoapEndpoint-UDP-0.0.0.0:0#1] DEBUG org.eclipse.californium.core.network.InMemoryMessageExchangeStore - coap Exchange[L2, localhost:5683] added with generated token KeyToken[localhost/127.0.0.1:5683-08CFFCF555491598], NON-GET    MID=54318, Token=08CFFCF555491598, OptionSet={"Uri-Host":"localhost", "Uri-Path":["PIOT","GatewayDevice","MgmtStatusMsg"]}, <empty data>
19:52:05.552 [:CoapEndpoint-UDP-0.0.0.0:0#1] DEBUG org.eclipse.californium.core.network.UdpMatcher - tracking open request [KeyMID[localhost/127.0.0.1:5683-54318], KeyToken[localhost/127.0.0.1:5683-08CFFCF555491598]]
19:52:05.552 [UDP-Sender-0.0.0.0/0.0.0.0:0[1]] DEBUG org.eclipse.californium.elements.UDPConnector - UDPConnector (Thread[UDP-Sender-0.0.0.0/0.0.0.0:0[1],5,Californium/Elements]) sent 57 bytes to localhost/127.0.0.1:5683
19:52:05.577 [UDP-Receiver-0.0.0.0/0.0.0.0:0[1]] DEBUG org.eclipse.californium.elements.UDPConnector - UDPConnector ([0:0:0:0:0:0:0:0]:60608) received 12 bytes from 127.0.0.1:5683
19:52:05.578 [:CoapEndpoint-UDP-0.0.0.0:0#1] DEBUG org.eclipse.californium.core.network.deduplication.SweepDeduplicator - add exchange for KeyMID[127.0.0.1:5683-21386]
19:52:05.578 [:CoapEndpoint-UDP-0.0.0.0:0#1] DEBUG org.eclipse.californium.core.network.stack.BlockwiseLayer - coap  received error NON-4.04   MID=21386, Token=08CFFCF555491598, OptionSet={}, <empty data>:
19:52:05.578 [:CoapEndpoint-UDP-0.0.0.0:0#1] DEBUG org.eclipse.californium.core.network.Exchange - Exchange[L2, localhost:5683, complete]!
19:52:05.578 [:CoapEndpoint-UDP-0.0.0.0:0#1] DEBUG org.eclipse.californium.core.network.InMemoryMessageExchangeStore - coap removing Exchange[L2, localhost:5683, complete] for token KeyToken[localhost/127.0.0.1:5683-08CFFCF555491598]
19:52:05.578 [:CoapEndpoint-UDP-0.0.0.0:0#1] DEBUG org.eclipse.californium.core.network.InMemoryMessageExchangeStore - coap removing Exchange[L2, localhost:5683, complete] for MID KeyMID[localhost/127.0.0.1:5683-54318]
19:52:05.578 [:CoapEndpoint-UDP-0.0.0.0:0#1] DEBUG org.eclipse.californium.core.network.Exchange - local Exchange[L2, localhost:5683, complete] completed NON-GET    MID=54318, Token=08CFFCF555491598, OptionSet={"Uri-Host":"localhost", "Uri-Path":["PIOT","GatewayDevice","MgmtStatusMsg"]}, acked <empty data>!
Nov 17, 2023 7:52:05 PM programmingtheiot.gda.connection.CoapClientConnector sendGetRequest
INFO: Handling GET. Response: false - {} - 4.04 -
```
GDA-09-005 - CoapClientConnectorTest - Integration Test for PUT
```txt
19:56:28.428 [main] INFO org.eclipse.californium.elements.config.Configuration - defaults added COAP.
19:56:28.433 [main] INFO org.eclipse.californium.elements.config.Configuration - defaults added SYS.
19:56:28.435 [main] INFO org.eclipse.californium.elements.config.Configuration - defaults added UDP.
Nov 17, 2023 7:56:28 PM programmingtheiot.gda.connection.CoapClientConnector initClient
INFO: Created client connection to server / resource: coap://localhost:5683
Nov 17, 2023 7:56:28 PM programmingtheiot.gda.connection.CoapClientConnector <init>
INFO: Using URL for server conn: coap://localhost:5683
19:56:28.844 [main] DEBUG org.eclipse.californium.elements.util.NetworkInterfacesUtil - Found broadcast address /10.0.2.255 - enp0s3.
19:56:28.852 [main] INFO org.eclipse.californium.elements.config.Configuration - loading properties from file /home/zabe/programmingtheiot/java-components/Californium3.properties
19:56:28.884 [main] INFO org.eclipse.californium.core.network.RandomTokenGenerator - using tokens of 8 bytes in length
19:56:28.890 [main] DEBUG org.eclipse.californium.core.network.InMemoryMessageExchangeStore - coap using TokenProvider org.eclipse.californium.core.network.RandomTokenGenerator
19:56:28.979 [main] INFO org.eclipse.californium.ban - Started.
19:56:28.981 [main] INFO org.eclipse.californium.core.network.CoapEndpoint - coap CoapEndpoint uses udp context
19:56:28.992 [main] INFO org.eclipse.californium.core.network.stack.BlockwiseLayer - coap BlockwiseLayer uses MAX_MESSAGE_SIZE=1024, PREFERRED_BLOCK_SIZE=512, BLOCKWISE_STATUS_LIFETIME=300000, MAX_RESOURCE_BODY_SIZE=8192, BLOCKWISE_STRICT_BLOCK2_OPTION=false
19:56:29.000 [main] INFO org.eclipse.californium.core.network.CoapEndpoint - coap Endpoint [coap://0.0.0.0:0] requires an executor to start, using default single-threaded daemon executor
19:56:29.006 [main] DEBUG org.eclipse.californium.core.network.CoapEndpoint - coap Starting endpoint at coap://0.0.0.0:0
19:56:29.011 [main] DEBUG org.eclipse.californium.core.network.InMemoryMessageExchangeStore - coap no MessageIdProvider set, using default org.eclipse.californium.core.network.InMemoryMessageIdProvider
19:56:29.020 [main] INFO org.eclipse.californium.elements.UDPConnector - UDPConnector starts up 2 sender threads and 2 receiver threads
19:56:29.025 [UDP-Receiver-0.0.0.0/0.0.0.0:0[0]] DEBUG org.eclipse.californium.elements.UDPConnector - Starting network stage thread [UDP-Receiver-0.0.0.0/0.0.0.0:0[0]]
19:56:29.027 [UDP-Receiver-0.0.0.0/0.0.0.0:0[1]] DEBUG org.eclipse.californium.elements.UDPConnector - Starting network stage thread [UDP-Receiver-0.0.0.0/0.0.0.0:0[1]]
19:56:29.028 [main] INFO org.eclipse.californium.elements.UDPConnector - UDPConnector listening on /[0:0:0:0:0:0:0:0]:46159, recv buf = 106496, send buf = 106496, recv packet size = 2048
19:56:29.029 [UDP-Sender-0.0.0.0/0.0.0.0:0[0]] DEBUG org.eclipse.californium.elements.UDPConnector - Starting network stage thread [UDP-Sender-0.0.0.0/0.0.0.0:0[0]]
19:56:29.029 [UDP-Sender-0.0.0.0/0.0.0.0:0[1]] DEBUG org.eclipse.californium.elements.UDPConnector - Starting network stage thread [UDP-Sender-0.0.0.0/0.0.0.0:0[1]]
19:56:29.031 [main] INFO org.eclipse.californium.core.network.CoapEndpoint - coap Started endpoint at coap://[0:0:0:0:0:0:0:0]:46159
19:56:29.032 [main] INFO org.eclipse.californium.core.network.EndpointManager - created implicit endpoint coap://[0:0:0:0:0:0:0:0]:46159 for coap
19:56:29.052 [:CoapEndpoint-UDP-0.0.0.0:0#1] DEBUG org.eclipse.californium.core.network.stack.ReliabilityLayer - Exchange[L1, localhost:5683] send request
19:56:29.052 [:CoapEndpoint-UDP-0.0.0.0:0#1] DEBUG org.eclipse.californium.core.network.stack.ReliabilityLayer - Exchange[L1, localhost:5683] prepare retransmission for CON-PUT    MID=   -1, Token=null, OptionSet={"Uri-Host":"localhost", "Uri-Path":["PIOT","GatewayDevice","MgmtStatusMsg"], "Content-Format":"text/plain"}, "{"name":"Not Set","timeStamp":"2".. 200 bytes
19:56:29.074 [:CoapEndpoint-UDP-0.0.0.0:0#1] DEBUG org.eclipse.californium.core.network.InMemoryMessageExchangeStore - coap Exchange[L1, localhost:5683] added with generated mid KeyMID[localhost/127.0.0.1:5683-33957], CON-PUT    MID=33957, Token=null, OptionSet={"Uri-Host":"localhost", "Uri-Path":["PIOT","GatewayDevice","MgmtStatusMsg"], "Content-Format":"text/plain"}, "{"name":"Not Set","timeStamp":"2".. 200 bytes
19:56:29.078 [:CoapEndpoint-UDP-0.0.0.0:0#1] DEBUG org.eclipse.californium.core.network.InMemoryMessageExchangeStore - coap Exchange[L1, localhost:5683] added with generated token KeyToken[localhost/127.0.0.1:5683-F0C8FF7545BF1D39], CON-PUT    MID=33957, Token=F0C8FF7545BF1D39, OptionSet={"Uri-Host":"localhost", "Uri-Path":["PIOT","GatewayDevice","MgmtStatusMsg"], "Content-Format":"text/plain"}, "{"name":"Not Set","timeStamp":"2".. 200 bytes
19:56:29.079 [:CoapEndpoint-UDP-0.0.0.0:0#1] DEBUG org.eclipse.californium.core.network.UdpMatcher - tracking open request [KeyMID[localhost/127.0.0.1:5683-33957], KeyToken[localhost/127.0.0.1:5683-F0C8FF7545BF1D39]]
19:56:29.102 [UDP-Sender-0.0.0.0/0.0.0.0:0[0]] DEBUG org.eclipse.californium.elements.UDPConnector - UDPConnector (Thread[UDP-Sender-0.0.0.0/0.0.0.0:0[0],5,Californium/Elements]) sent 259 bytes to localhost/127.0.0.1:5683
19:56:29.157 [UDP-Receiver-0.0.0.0/0.0.0.0:0[0]] DEBUG org.eclipse.californium.elements.UDPConnector - UDPConnector ([0:0:0:0:0:0:0:0]:46159) received 12 bytes from 127.0.0.1:5683
19:56:29.167 [:CoapEndpoint-UDP-0.0.0.0:0#1] DEBUG org.eclipse.californium.core.network.stack.BlockwiseLayer - coap  received error ACK-4.04   MID=33957, Token=F0C8FF7545BF1D39, OptionSet={}, <empty data>:
19:56:29.168 [:CoapEndpoint-UDP-0.0.0.0:0#1] DEBUG org.eclipse.californium.core.network.Exchange - Exchange[L1, localhost:5683, complete]!
19:56:29.168 [:CoapEndpoint-UDP-0.0.0.0:0#1] DEBUG org.eclipse.californium.core.network.InMemoryMessageExchangeStore - coap removing Exchange[L1, localhost:5683, complete] for token KeyToken[localhost/127.0.0.1:5683-F0C8FF7545BF1D39]
19:56:29.168 [:CoapEndpoint-UDP-0.0.0.0:0#1] DEBUG org.eclipse.californium.core.network.InMemoryMessageExchangeStore - coap removing Exchange[L1, localhost:5683, complete] for MID KeyMID[localhost/127.0.0.1:5683-33957]
19:56:29.168 [:CoapEndpoint-UDP-0.0.0.0:0#1] DEBUG org.eclipse.californium.core.network.Exchange - local Exchange[L1, localhost:5683, complete] completed CON-PUT    MID=33957, Token=F0C8FF7545BF1D39, OptionSet={"Uri-Host":"localhost", "Uri-Path":["PIOT","GatewayDevice","MgmtStatusMsg"], "Content-Format":"text/plain"}, acked "{"name":"Not Set","timeStamp":"2".. 200 bytes!
Nov 17, 2023 7:56:29 PM programmingtheiot.gda.connection.CoapClientConnector sendPutRequest
INFO: Handling PUT. Response: false - {} - 4.04 - 
Nov 17, 2023 7:56:29 PM programmingtheiot.gda.connection.CoapClientConnector initClient
INFO: Created client connection to server / resource: coap://localhost:5683
Nov 17, 2023 7:56:29 PM programmingtheiot.gda.connection.CoapClientConnector <init>
INFO: Using URL for server conn: coap://localhost:5683
19:56:29.245 [:CoapEndpoint-UDP-0.0.0.0:0#1] DEBUG org.eclipse.californium.core.network.stack.ReliabilityLayer - Exchange[L2, localhost:5683] send request
19:56:29.261 [:CoapEndpoint-UDP-0.0.0.0:0#1] DEBUG org.eclipse.californium.core.network.InMemoryMessageExchangeStore - coap Exchange[L2, localhost:5683] added with generated mid KeyMID[localhost/127.0.0.1:5683-33958], NON-PUT    MID=33958, Token=null, OptionSet={"Uri-Host":"localhost", "Uri-Path":["PIOT","GatewayDevice","MgmtStatusMsg"], "Content-Format":"text/plain"}, "{"name":"Not Set","timeStamp":"2".. 200 bytes
19:56:29.262 [:CoapEndpoint-UDP-0.0.0.0:0#1] DEBUG org.eclipse.californium.core.network.InMemoryMessageExchangeStore - coap Exchange[L2, localhost:5683] added with generated token KeyToken[localhost/127.0.0.1:5683-A050ACC70D4CB84F], NON-PUT    MID=33958, Token=A050ACC70D4CB84F, OptionSet={"Uri-Host":"localhost", "Uri-Path":["PIOT","GatewayDevice","MgmtStatusMsg"], "Content-Format":"text/plain"}, "{"name":"Not Set","timeStamp":"2".. 200 bytes
19:56:29.263 [:CoapEndpoint-UDP-0.0.0.0:0#1] DEBUG org.eclipse.californium.core.network.UdpMatcher - tracking open request [KeyMID[localhost/127.0.0.1:5683-33958], KeyToken[localhost/127.0.0.1:5683-A050ACC70D4CB84F]]
19:56:29.263 [UDP-Sender-0.0.0.0/0.0.0.0:0[1]] DEBUG org.eclipse.californium.elements.UDPConnector - UDPConnector (Thread[UDP-Sender-0.0.0.0/0.0.0.0:0[1],5,Californium/Elements]) sent 259 bytes to localhost/127.0.0.1:5683
19:56:29.274 [UDP-Receiver-0.0.0.0/0.0.0.0:0[1]] DEBUG org.eclipse.californium.elements.UDPConnector - UDPConnector ([0:0:0:0:0:0:0:0]:46159) received 12 bytes from 127.0.0.1:5683
19:56:29.275 [:CoapEndpoint-UDP-0.0.0.0:0#1] DEBUG org.eclipse.californium.core.network.deduplication.SweepDeduplicator - add exchange for KeyMID[127.0.0.1:5683-9305]
19:56:29.276 [:CoapEndpoint-UDP-0.0.0.0:0#1] DEBUG org.eclipse.californium.core.network.stack.BlockwiseLayer - coap  received error NON-4.04   MID= 9305, Token=A050ACC70D4CB84F, OptionSet={}, <empty data>:
19:56:29.276 [:CoapEndpoint-UDP-0.0.0.0:0#1] DEBUG org.eclipse.californium.core.network.Exchange - Exchange[L2, localhost:5683, complete]!
19:56:29.276 [:CoapEndpoint-UDP-0.0.0.0:0#1] DEBUG org.eclipse.californium.core.network.InMemoryMessageExchangeStore - coap removing Exchange[L2, localhost:5683, complete] for token KeyToken[localhost/127.0.0.1:5683-A050ACC70D4CB84F]
19:56:29.276 [:CoapEndpoint-UDP-0.0.0.0:0#1] DEBUG org.eclipse.californium.core.network.InMemoryMessageExchangeStore - coap removing Exchange[L2, localhost:5683, complete] for MID KeyMID[localhost/127.0.0.1:5683-33958]
19:56:29.276 [:CoapEndpoint-UDP-0.0.0.0:0#1] DEBUG org.eclipse.californium.core.network.Exchange - local Exchange[L2, localhost:5683, complete] completed NON-PUT    MID=33958, Token=A050ACC70D4CB84F, OptionSet={"Uri-Host":"localhost", "Uri-Path":["PIOT","GatewayDevice","MgmtStatusMsg"], "Content-Format":"text/plain"}, acked "{"name":"Not Set","timeStamp":"2".. 200 bytes!
Nov 17, 2023 7:56:29 PM programmingtheiot.gda.connection.CoapClientConnector sendPutRequest
INFO: Handling PUT. Response: false - {} - 4.04 - 
```
GDA-09-006 - CoapClientConnectorTest - Integration Test for POST
```txt
19:58:08.145 [main] INFO org.eclipse.californium.elements.config.Configuration - defaults added COAP.
19:58:08.150 [main] INFO org.eclipse.californium.elements.config.Configuration - defaults added SYS.
19:58:08.151 [main] INFO org.eclipse.californium.elements.config.Configuration - defaults added UDP.
Nov 17, 2023 7:58:08 PM programmingtheiot.gda.connection.CoapClientConnector initClient
INFO: Created client connection to server / resource: coap://localhost:5683
Nov 17, 2023 7:58:08 PM programmingtheiot.gda.connection.CoapClientConnector <init>
INFO: Using URL for server conn: coap://localhost:5683
19:58:08.717 [main] DEBUG org.eclipse.californium.elements.util.NetworkInterfacesUtil - Found broadcast address /10.0.2.255 - enp0s3.
19:58:08.734 [main] INFO org.eclipse.californium.elements.config.Configuration - loading properties from file /home/zabe/programmingtheiot/java-components/Californium3.properties
19:58:08.739 [main] INFO org.eclipse.californium.core.network.RandomTokenGenerator - using tokens of 8 bytes in length
19:58:08.889 [main] DEBUG org.eclipse.californium.core.network.InMemoryMessageExchangeStore - coap using TokenProvider org.eclipse.californium.core.network.RandomTokenGenerator
19:58:08.922 [main] INFO org.eclipse.californium.ban - Started.
19:58:08.925 [main] INFO org.eclipse.californium.core.network.CoapEndpoint - coap CoapEndpoint uses udp context
19:58:08.951 [main] INFO org.eclipse.californium.core.network.stack.BlockwiseLayer - coap BlockwiseLayer uses MAX_MESSAGE_SIZE=1024, PREFERRED_BLOCK_SIZE=512, BLOCKWISE_STATUS_LIFETIME=300000, MAX_RESOURCE_BODY_SIZE=8192, BLOCKWISE_STRICT_BLOCK2_OPTION=false
19:58:08.960 [main] INFO org.eclipse.californium.core.network.CoapEndpoint - coap Endpoint [coap://0.0.0.0:0] requires an executor to start, using default single-threaded daemon executor
19:58:08.972 [main] DEBUG org.eclipse.californium.core.network.CoapEndpoint - coap Starting endpoint at coap://0.0.0.0:0
19:58:08.981 [main] DEBUG org.eclipse.californium.core.network.InMemoryMessageExchangeStore - coap no MessageIdProvider set, using default org.eclipse.californium.core.network.InMemoryMessageIdProvider
19:58:09.006 [main] INFO org.eclipse.californium.elements.UDPConnector - UDPConnector starts up 2 sender threads and 2 receiver threads
19:58:09.074 [UDP-Receiver-0.0.0.0/0.0.0.0:0[0]] DEBUG org.eclipse.californium.elements.UDPConnector - Starting network stage thread [UDP-Receiver-0.0.0.0/0.0.0.0:0[0]]
19:58:09.075 [UDP-Receiver-0.0.0.0/0.0.0.0:0[1]] DEBUG org.eclipse.californium.elements.UDPConnector - Starting network stage thread [UDP-Receiver-0.0.0.0/0.0.0.0:0[1]]
19:58:09.076 [UDP-Sender-0.0.0.0/0.0.0.0:0[0]] DEBUG org.eclipse.californium.elements.UDPConnector - Starting network stage thread [UDP-Sender-0.0.0.0/0.0.0.0:0[0]]
19:58:09.079 [main] INFO org.eclipse.californium.elements.UDPConnector - UDPConnector listening on /[0:0:0:0:0:0:0:0]:33138, recv buf = 106496, send buf = 106496, recv packet size = 2048
19:58:09.080 [main] INFO org.eclipse.californium.core.network.CoapEndpoint - coap Started endpoint at coap://[0:0:0:0:0:0:0:0]:33138
19:58:09.081 [main] INFO org.eclipse.californium.core.network.EndpointManager - created implicit endpoint coap://[0:0:0:0:0:0:0:0]:33138 for coap
19:58:09.086 [UDP-Sender-0.0.0.0/0.0.0.0:0[1]] DEBUG org.eclipse.californium.elements.UDPConnector - Starting network stage thread [UDP-Sender-0.0.0.0/0.0.0.0:0[1]]
19:58:09.087 [:CoapEndpoint-UDP-0.0.0.0:0#1] DEBUG org.eclipse.californium.core.network.stack.ReliabilityLayer - Exchange[L1, localhost:5683] send request
19:58:09.087 [:CoapEndpoint-UDP-0.0.0.0:0#1] DEBUG org.eclipse.californium.core.network.stack.ReliabilityLayer - Exchange[L1, localhost:5683] prepare retransmission for CON-POST   MID=   -1, Token=null, OptionSet={"Uri-Host":"localhost", "Uri-Path":["PIOT","GatewayDevice","MgmtStatusMsg"], "Content-Format":"text/plain"}, "{"name":"Not Set","timeStamp":"2".. 200 bytes
19:58:09.096 [:CoapEndpoint-UDP-0.0.0.0:0#1] DEBUG org.eclipse.californium.core.network.InMemoryMessageExchangeStore - coap Exchange[L1, localhost:5683] added with generated mid KeyMID[localhost/127.0.0.1:5683-20428], CON-POST   MID=20428, Token=null, OptionSet={"Uri-Host":"localhost", "Uri-Path":["PIOT","GatewayDevice","MgmtStatusMsg"], "Content-Format":"text/plain"}, "{"name":"Not Set","timeStamp":"2".. 200 bytes
19:58:09.097 [:CoapEndpoint-UDP-0.0.0.0:0#1] DEBUG org.eclipse.californium.core.network.InMemoryMessageExchangeStore - coap Exchange[L1, localhost:5683] added with generated token KeyToken[localhost/127.0.0.1:5683-2012CFB3C08E2DA2], CON-POST   MID=20428, Token=2012CFB3C08E2DA2, OptionSet={"Uri-Host":"localhost", "Uri-Path":["PIOT","GatewayDevice","MgmtStatusMsg"], "Content-Format":"text/plain"}, "{"name":"Not Set","timeStamp":"2".. 200 bytes
19:58:09.098 [:CoapEndpoint-UDP-0.0.0.0:0#1] DEBUG org.eclipse.californium.core.network.UdpMatcher - tracking open request [KeyMID[localhost/127.0.0.1:5683-20428], KeyToken[localhost/127.0.0.1:5683-2012CFB3C08E2DA2]]
19:58:09.124 [UDP-Sender-0.0.0.0/0.0.0.0:0[0]] DEBUG org.eclipse.californium.elements.UDPConnector - UDPConnector (Thread[UDP-Sender-0.0.0.0/0.0.0.0:0[0],5,Californium/Elements]) sent 259 bytes to localhost/127.0.0.1:5683
19:58:09.203 [UDP-Receiver-0.0.0.0/0.0.0.0:0[0]] DEBUG org.eclipse.californium.elements.UDPConnector - UDPConnector ([0:0:0:0:0:0:0:0]:33138) received 12 bytes from 127.0.0.1:5683
19:58:09.286 [:CoapEndpoint-UDP-0.0.0.0:0#1] DEBUG org.eclipse.californium.core.network.stack.BlockwiseLayer - coap  received error ACK-4.04   MID=20428, Token=2012CFB3C08E2DA2, OptionSet={}, <empty data>:
19:58:09.287 [:CoapEndpoint-UDP-0.0.0.0:0#1] DEBUG org.eclipse.californium.core.network.Exchange - Exchange[L1, localhost:5683, complete]!
19:58:09.288 [:CoapEndpoint-UDP-0.0.0.0:0#1] DEBUG org.eclipse.californium.core.network.InMemoryMessageExchangeStore - coap removing Exchange[L1, localhost:5683, complete] for token KeyToken[localhost/127.0.0.1:5683-2012CFB3C08E2DA2]
19:58:09.289 [:CoapEndpoint-UDP-0.0.0.0:0#1] DEBUG org.eclipse.californium.core.network.InMemoryMessageExchangeStore - coap removing Exchange[L1, localhost:5683, complete] for MID KeyMID[localhost/127.0.0.1:5683-20428]
19:58:09.289 [:CoapEndpoint-UDP-0.0.0.0:0#1] DEBUG org.eclipse.californium.core.network.Exchange - local Exchange[L1, localhost:5683, complete] completed CON-POST   MID=20428, Token=2012CFB3C08E2DA2, OptionSet={"Uri-Host":"localhost", "Uri-Path":["PIOT","GatewayDevice","MgmtStatusMsg"], "Content-Format":"text/plain"}, acked "{"name":"Not Set","timeStamp":"2".. 200 bytes!
Nov 17, 2023 7:58:09 PM programmingtheiot.gda.connection.CoapClientConnector sendPostRequest
INFO: Handling POST. Response: false - {} - 4.04 - 
Nov 17, 2023 7:58:09 PM programmingtheiot.gda.connection.CoapClientConnector initClient
INFO: Created client connection to server / resource: coap://localhost:5683
Nov 17, 2023 7:58:09 PM programmingtheiot.gda.connection.CoapClientConnector <init>
INFO: Using URL for server conn: coap://localhost:5683
19:58:09.316 [:CoapEndpoint-UDP-0.0.0.0:0#1] DEBUG org.eclipse.californium.core.network.stack.ReliabilityLayer - Exchange[L2, localhost:5683] send request
19:58:09.316 [:CoapEndpoint-UDP-0.0.0.0:0#1] DEBUG org.eclipse.californium.core.network.InMemoryMessageExchangeStore - coap Exchange[L2, localhost:5683] added with generated mid KeyMID[localhost/127.0.0.1:5683-20429], NON-POST   MID=20429, Token=null, OptionSet={"Uri-Host":"localhost", "Uri-Path":["PIOT","GatewayDevice","MgmtStatusMsg"], "Content-Format":"text/plain"}, "{"name":"Not Set","timeStamp":"2".. 200 bytes
19:58:09.316 [:CoapEndpoint-UDP-0.0.0.0:0#1] DEBUG org.eclipse.californium.core.network.InMemoryMessageExchangeStore - coap Exchange[L2, localhost:5683] added with generated token KeyToken[localhost/127.0.0.1:5683-E06144B70A70E104], NON-POST   MID=20429, Token=E06144B70A70E104, OptionSet={"Uri-Host":"localhost", "Uri-Path":["PIOT","GatewayDevice","MgmtStatusMsg"], "Content-Format":"text/plain"}, "{"name":"Not Set","timeStamp":"2".. 200 bytes
19:58:09.317 [:CoapEndpoint-UDP-0.0.0.0:0#1] DEBUG org.eclipse.californium.core.network.UdpMatcher - tracking open request [KeyMID[localhost/127.0.0.1:5683-20429], KeyToken[localhost/127.0.0.1:5683-E06144B70A70E104]]
19:58:09.317 [UDP-Sender-0.0.0.0/0.0.0.0:0[1]] DEBUG org.eclipse.californium.elements.UDPConnector - UDPConnector (Thread[UDP-Sender-0.0.0.0/0.0.0.0:0[1],5,Californium/Elements]) sent 259 bytes to localhost/127.0.0.1:5683
19:58:09.340 [UDP-Receiver-0.0.0.0/0.0.0.0:0[1]] DEBUG org.eclipse.californium.elements.UDPConnector - UDPConnector ([0:0:0:0:0:0:0:0]:33138) received 12 bytes from 127.0.0.1:5683
19:58:09.341 [:CoapEndpoint-UDP-0.0.0.0:0#1] DEBUG org.eclipse.californium.core.network.deduplication.SweepDeduplicator - add exchange for KeyMID[127.0.0.1:5683-63629]
19:58:09.341 [:CoapEndpoint-UDP-0.0.0.0:0#1] DEBUG org.eclipse.californium.core.network.stack.BlockwiseLayer - coap  received error NON-4.04   MID=63629, Token=E06144B70A70E104, OptionSet={}, <empty data>:
19:58:09.341 [:CoapEndpoint-UDP-0.0.0.0:0#1] DEBUG org.eclipse.californium.core.network.Exchange - Exchange[L2, localhost:5683, complete]!
19:58:09.341 [:CoapEndpoint-UDP-0.0.0.0:0#1] DEBUG org.eclipse.californium.core.network.InMemoryMessageExchangeStore - coap removing Exchange[L2, localhost:5683, complete] for token KeyToken[localhost/127.0.0.1:5683-E06144B70A70E104]
19:58:09.342 [:CoapEndpoint-UDP-0.0.0.0:0#1] DEBUG org.eclipse.californium.core.network.InMemoryMessageExchangeStore - coap removing Exchange[L2, localhost:5683, complete] for MID KeyMID[localhost/127.0.0.1:5683-20429]
19:58:09.342 [:CoapEndpoint-UDP-0.0.0.0:0#1] DEBUG org.eclipse.californium.core.network.Exchange - local Exchange[L2, localhost:5683, complete] completed NON-POST   MID=20429, Token=E06144B70A70E104, OptionSet={"Uri-Host":"localhost", "Uri-Path":["PIOT","GatewayDevice","MgmtStatusMsg"], "Content-Format":"text/plain"}, acked "{"name":"Not Set","timeStamp":"2".. 200 bytes!
Nov 17, 2023 7:58:09 PM programmingtheiot.gda.connection.CoapClientConnector sendPostRequest
INFO: Handling POST. Response: false - {} - 4.04 -
```
GDA-09-007 - CoapClientConnectorTest - Integration Test for DELETE
```txt
20:01:55.849 [main] INFO org.eclipse.californium.elements.config.Configuration - defaults added COAP.
20:01:55.857 [main] INFO org.eclipse.californium.elements.config.Configuration - defaults added SYS.
20:01:55.859 [main] INFO org.eclipse.californium.elements.config.Configuration - defaults added UDP.
Nov 17, 2023 8:01:56 PM programmingtheiot.gda.connection.CoapClientConnector initClient
INFO: Created client connection to server / resource: coap://localhost:5683
Nov 17, 2023 8:01:56 PM programmingtheiot.gda.connection.CoapClientConnector <init>
INFO: Using URL for server conn: coap://localhost:5683
20:01:56.626 [main] DEBUG org.eclipse.californium.elements.util.NetworkInterfacesUtil - Found broadcast address /10.0.2.255 - enp0s3.
20:01:56.638 [main] INFO org.eclipse.californium.elements.config.Configuration - loading properties from file /home/zabe/programmingtheiot/java-components/Californium3.properties
20:01:56.643 [main] INFO org.eclipse.californium.core.network.RandomTokenGenerator - using tokens of 8 bytes in length
20:01:56.655 [main] DEBUG org.eclipse.californium.core.network.InMemoryMessageExchangeStore - coap using TokenProvider org.eclipse.californium.core.network.RandomTokenGenerator
20:01:56.711 [main] INFO org.eclipse.californium.ban - Started.
20:01:56.715 [main] INFO org.eclipse.californium.core.network.CoapEndpoint - coap CoapEndpoint uses udp context
20:01:56.748 [main] INFO org.eclipse.californium.core.network.stack.BlockwiseLayer - coap BlockwiseLayer uses MAX_MESSAGE_SIZE=1024, PREFERRED_BLOCK_SIZE=512, BLOCKWISE_STATUS_LIFETIME=300000, MAX_RESOURCE_BODY_SIZE=8192, BLOCKWISE_STRICT_BLOCK2_OPTION=false
20:01:56.777 [main] INFO org.eclipse.californium.core.network.CoapEndpoint - coap Endpoint [coap://0.0.0.0:0] requires an executor to start, using default single-threaded daemon executor
20:01:56.796 [main] DEBUG org.eclipse.californium.core.network.CoapEndpoint - coap Starting endpoint at coap://0.0.0.0:0
20:01:56.813 [main] DEBUG org.eclipse.californium.core.network.InMemoryMessageExchangeStore - coap no MessageIdProvider set, using default org.eclipse.californium.core.network.InMemoryMessageIdProvider
20:01:56.827 [main] INFO org.eclipse.californium.elements.UDPConnector - UDPConnector starts up 2 sender threads and 2 receiver threads
20:01:56.830 [UDP-Receiver-0.0.0.0/0.0.0.0:0[0]] DEBUG org.eclipse.californium.elements.UDPConnector - Starting network stage thread [UDP-Receiver-0.0.0.0/0.0.0.0:0[0]]
20:01:56.831 [UDP-Receiver-0.0.0.0/0.0.0.0:0[1]] DEBUG org.eclipse.californium.elements.UDPConnector - Starting network stage thread [UDP-Receiver-0.0.0.0/0.0.0.0:0[1]]
20:01:56.833 [UDP-Sender-0.0.0.0/0.0.0.0:0[0]] DEBUG org.eclipse.californium.elements.UDPConnector - Starting network stage thread [UDP-Sender-0.0.0.0/0.0.0.0:0[0]]
20:01:56.833 [main] INFO org.eclipse.californium.elements.UDPConnector - UDPConnector listening on /[0:0:0:0:0:0:0:0]:55104, recv buf = 106496, send buf = 106496, recv packet size = 2048
20:01:56.842 [UDP-Sender-0.0.0.0/0.0.0.0:0[1]] DEBUG org.eclipse.californium.elements.UDPConnector - Starting network stage thread [UDP-Sender-0.0.0.0/0.0.0.0:0[1]]
20:01:56.853 [main] INFO org.eclipse.californium.core.network.CoapEndpoint - coap Started endpoint at coap://[0:0:0:0:0:0:0:0]:55104
20:01:56.853 [main] INFO org.eclipse.californium.core.network.EndpointManager - created implicit endpoint coap://[0:0:0:0:0:0:0:0]:55104 for coap
20:01:56.889 [:CoapEndpoint-UDP-0.0.0.0:0#1] DEBUG org.eclipse.californium.core.network.stack.ReliabilityLayer - Exchange[L1, localhost:5683] send request
20:01:56.892 [:CoapEndpoint-UDP-0.0.0.0:0#1] DEBUG org.eclipse.californium.core.network.stack.ReliabilityLayer - Exchange[L1, localhost:5683] prepare retransmission for CON-DELETE MID=   -1, Token=null, OptionSet={"Uri-Host":"localhost", "Uri-Path":["PIOT","GatewayDevice","MgmtStatusCmd"]}, <empty data>
20:01:56.910 [:CoapEndpoint-UDP-0.0.0.0:0#1] DEBUG org.eclipse.californium.core.network.InMemoryMessageExchangeStore - coap Exchange[L1, localhost:5683] added with generated mid KeyMID[localhost/127.0.0.1:5683-37762], CON-DELETE MID=37762, Token=null, OptionSet={"Uri-Host":"localhost", "Uri-Path":["PIOT","GatewayDevice","MgmtStatusCmd"]}, <empty data>
20:01:56.916 [:CoapEndpoint-UDP-0.0.0.0:0#1] DEBUG org.eclipse.californium.core.network.InMemoryMessageExchangeStore - coap Exchange[L1, localhost:5683] added with generated token KeyToken[localhost/127.0.0.1:5683-8405C606A35E7DBF], CON-DELETE MID=37762, Token=8405C606A35E7DBF, OptionSet={"Uri-Host":"localhost", "Uri-Path":["PIOT","GatewayDevice","MgmtStatusCmd"]}, <empty data>
20:01:56.916 [:CoapEndpoint-UDP-0.0.0.0:0#1] DEBUG org.eclipse.californium.core.network.UdpMatcher - tracking open request [KeyMID[localhost/127.0.0.1:5683-37762], KeyToken[localhost/127.0.0.1:5683-8405C606A35E7DBF]]
20:01:56.985 [UDP-Sender-0.0.0.0/0.0.0.0:0[0]] DEBUG org.eclipse.californium.elements.UDPConnector - UDPConnector (Thread[UDP-Sender-0.0.0.0/0.0.0.0:0[0],5,Californium/Elements]) sent 57 bytes to localhost/127.0.0.1:5683
20:01:57.075 [UDP-Receiver-0.0.0.0/0.0.0.0:0[0]] DEBUG org.eclipse.californium.elements.UDPConnector - UDPConnector ([0:0:0:0:0:0:0:0]:55104) received 12 bytes from 127.0.0.1:5683
Nov 17, 2023 8:01:57 PM programmingtheiot.gda.connection.CoapClientConnector sendDeleteRequest
INFO: Handling DELETE. Response: false - {} - 4.04 - 
Nov 17, 2023 8:01:57 PM programmingtheiot.gda.connection.CoapClientConnector initClient
INFO: Created client connection to server / resource: coap://localhost:5683
Nov 17, 2023 8:01:57 PM programmingtheiot.gda.connection.CoapClientConnector <init>
INFO: Using URL for server conn: coap://localhost:5683
20:01:57.202 [:CoapEndpoint-UDP-0.0.0.0:0#1] DEBUG org.eclipse.californium.core.network.stack.BlockwiseLayer - coap  received error ACK-4.04   MID=37762, Token=8405C606A35E7DBF, OptionSet={}, <empty data>:
20:01:57.202 [:CoapEndpoint-UDP-0.0.0.0:0#1] DEBUG org.eclipse.californium.core.network.Exchange - Exchange[L1, localhost:5683, complete]!
20:01:57.202 [:CoapEndpoint-UDP-0.0.0.0:0#1] DEBUG org.eclipse.californium.core.network.InMemoryMessageExchangeStore - coap removing Exchange[L1, localhost:5683, complete] for token KeyToken[localhost/127.0.0.1:5683-8405C606A35E7DBF]
20:01:57.203 [:CoapEndpoint-UDP-0.0.0.0:0#1] DEBUG org.eclipse.californium.core.network.InMemoryMessageExchangeStore - coap removing Exchange[L1, localhost:5683, complete] for MID KeyMID[localhost/127.0.0.1:5683-37762]
20:01:57.203 [:CoapEndpoint-UDP-0.0.0.0:0#1] DEBUG org.eclipse.californium.core.network.Exchange - local Exchange[L1, localhost:5683, complete] completed CON-DELETE MID=37762, Token=8405C606A35E7DBF, OptionSet={"Uri-Host":"localhost", "Uri-Path":["PIOT","GatewayDevice","MgmtStatusCmd"]}, acked <empty data>!
20:01:57.216 [:CoapEndpoint-UDP-0.0.0.0:0#1] DEBUG org.eclipse.californium.core.network.stack.ReliabilityLayer - Exchange[L2, localhost:5683] send request
20:01:57.216 [:CoapEndpoint-UDP-0.0.0.0:0#1] DEBUG org.eclipse.californium.core.network.InMemoryMessageExchangeStore - coap Exchange[L2, localhost:5683] added with generated mid KeyMID[localhost/127.0.0.1:5683-37763], NON-DELETE MID=37763, Token=null, OptionSet={"Uri-Host":"localhost", "Uri-Path":["PIOT","GatewayDevice","MgmtStatusCmd"]}, <empty data>
20:01:57.216 [:CoapEndpoint-UDP-0.0.0.0:0#1] DEBUG org.eclipse.californium.core.network.InMemoryMessageExchangeStore - coap Exchange[L2, localhost:5683] added with generated token KeyToken[localhost/127.0.0.1:5683-F8B59CAC7675CE95], NON-DELETE MID=37763, Token=F8B59CAC7675CE95, OptionSet={"Uri-Host":"localhost", "Uri-Path":["PIOT","GatewayDevice","MgmtStatusCmd"]}, <empty data>
20:01:57.216 [:CoapEndpoint-UDP-0.0.0.0:0#1] DEBUG org.eclipse.californium.core.network.UdpMatcher - tracking open request [KeyMID[localhost/127.0.0.1:5683-37763], KeyToken[localhost/127.0.0.1:5683-F8B59CAC7675CE95]]
20:01:57.225 [UDP-Sender-0.0.0.0/0.0.0.0:0[1]] DEBUG org.eclipse.californium.elements.UDPConnector - UDPConnector (Thread[UDP-Sender-0.0.0.0/0.0.0.0:0[1],5,Californium/Elements]) sent 57 bytes to localhost/127.0.0.1:5683
20:01:57.233 [UDP-Receiver-0.0.0.0/0.0.0.0:0[1]] DEBUG org.eclipse.californium.elements.UDPConnector - UDPConnector ([0:0:0:0:0:0:0:0]:55104) received 12 bytes from 127.0.0.1:5683
20:01:57.237 [:CoapEndpoint-UDP-0.0.0.0:0#1] DEBUG org.eclipse.californium.core.network.deduplication.SweepDeduplicator - add exchange for KeyMID[127.0.0.1:5683-54040]
20:01:57.238 [:CoapEndpoint-UDP-0.0.0.0:0#1] DEBUG org.eclipse.californium.core.network.stack.BlockwiseLayer - coap  received error NON-4.04   MID=54040, Token=F8B59CAC7675CE95, OptionSet={}, <empty data>:
20:01:57.239 [:CoapEndpoint-UDP-0.0.0.0:0#1] DEBUG org.eclipse.californium.core.network.Exchange - Exchange[L2, localhost:5683, complete]!
20:01:57.239 [:CoapEndpoint-UDP-0.0.0.0:0#1] DEBUG org.eclipse.californium.core.network.InMemoryMessageExchangeStore - coap removing Exchange[L2, localhost:5683, complete] for token KeyToken[localhost/127.0.0.1:5683-F8B59CAC7675CE95]
20:01:57.239 [:CoapEndpoint-UDP-0.0.0.0:0#1] DEBUG org.eclipse.californium.core.network.InMemoryMessageExchangeStore - coap removing Exchange[L2, localhost:5683, complete] for MID KeyMID[localhost/127.0.0.1:5683-37763]
20:01:57.239 [:CoapEndpoint-UDP-0.0.0.0:0#1] DEBUG org.eclipse.californium.core.network.Exchange - local Exchange[L2, localhost:5683, complete] completed NON-DELETE MID=37763, Token=F8B59CAC7675CE95, OptionSet={"Uri-Host":"localhost", "Uri-Path":["PIOT","GatewayDevice","MgmtStatusCmd"]}, acked <empty data>!
Nov 17, 2023 8:01:57 PM programmingtheiot.gda.connection.CoapClientConnector sendDeleteRequest
INFO: Handling DELETE. Response: false - {} - 4.04 -
```
GDA-09-008 - CoapClientConnectorTest - Integration Test for OBSERVE
```txt
20:07:21.182 [main] INFO org.eclipse.californium.elements.config.Configuration - defaults added COAP.
20:07:21.188 [main] INFO org.eclipse.californium.elements.config.Configuration - defaults added SYS.
20:07:21.189 [main] INFO org.eclipse.californium.elements.config.Configuration - defaults added UDP.
Nov 17, 2023 8:07:21 PM programmingtheiot.gda.connection.CoapClientConnector initClient
INFO: Created client connection to server / resource: coap://localhost:5683
Nov 17, 2023 8:07:21 PM programmingtheiot.gda.connection.CoapClientConnector <init>
INFO: Using URL for server conn: coap://localhost:5683
Nov 17, 2023 8:07:21 PM programmingtheiot.gda.connection.CoapClientConnector startObserver
INFO: Observing resource [START]: coap://localhost:5683/PIOT/GatewayDevice/MgmtStatusCmd
20:07:21.524 [main] DEBUG org.eclipse.californium.elements.util.NetworkInterfacesUtil - Found broadcast address /10.0.2.255 - enp0s3.
20:07:21.528 [main] INFO org.eclipse.californium.elements.config.Configuration - loading properties from file /home/zabe/programmingtheiot/java-components/Californium3.properties
20:07:21.532 [main] INFO org.eclipse.californium.core.network.RandomTokenGenerator - using tokens of 8 bytes in length
20:07:21.536 [main] DEBUG org.eclipse.californium.core.network.InMemoryMessageExchangeStore - coap using TokenProvider org.eclipse.californium.core.network.RandomTokenGenerator
20:07:21.541 [main] INFO org.eclipse.californium.ban - Started.
20:07:21.542 [main] INFO org.eclipse.californium.core.network.CoapEndpoint - coap CoapEndpoint uses udp context
20:07:21.610 [main] INFO org.eclipse.californium.core.network.stack.BlockwiseLayer - coap BlockwiseLayer uses MAX_MESSAGE_SIZE=1024, PREFERRED_BLOCK_SIZE=512, BLOCKWISE_STATUS_LIFETIME=300000, MAX_RESOURCE_BODY_SIZE=8192, BLOCKWISE_STRICT_BLOCK2_OPTION=false
20:07:21.660 [main] INFO org.eclipse.californium.core.network.CoapEndpoint - coap Endpoint [coap://0.0.0.0:0] requires an executor to start, using default single-threaded daemon executor
20:07:21.685 [main] DEBUG org.eclipse.californium.core.network.CoapEndpoint - coap Starting endpoint at coap://0.0.0.0:0
20:07:21.687 [main] DEBUG org.eclipse.californium.core.network.InMemoryMessageExchangeStore - coap no MessageIdProvider set, using default org.eclipse.californium.core.network.InMemoryMessageIdProvider
20:07:21.693 [main] INFO org.eclipse.californium.elements.UDPConnector - UDPConnector starts up 2 sender threads and 2 receiver threads
20:07:21.701 [UDP-Receiver-0.0.0.0/0.0.0.0:0[0]] DEBUG org.eclipse.californium.elements.UDPConnector - Starting network stage thread [UDP-Receiver-0.0.0.0/0.0.0.0:0[0]]
20:07:21.719 [UDP-Receiver-0.0.0.0/0.0.0.0:0[1]] DEBUG org.eclipse.californium.elements.UDPConnector - Starting network stage thread [UDP-Receiver-0.0.0.0/0.0.0.0:0[1]]
20:07:21.724 [main] INFO org.eclipse.californium.elements.UDPConnector - UDPConnector listening on /[0:0:0:0:0:0:0:0]:37164, recv buf = 106496, send buf = 106496, recv packet size = 2048
20:07:21.725 [UDP-Sender-0.0.0.0/0.0.0.0:0[0]] DEBUG org.eclipse.californium.elements.UDPConnector - Starting network stage thread [UDP-Sender-0.0.0.0/0.0.0.0:0[0]]
20:07:21.726 [main] INFO org.eclipse.californium.core.network.CoapEndpoint - coap Started endpoint at coap://[0:0:0:0:0:0:0:0]:37164
20:07:21.726 [main] INFO org.eclipse.californium.core.network.EndpointManager - created implicit endpoint coap://[0:0:0:0:0:0:0:0]:37164 for coap
20:07:21.743 [UDP-Sender-0.0.0.0/0.0.0.0:0[1]] DEBUG org.eclipse.californium.elements.UDPConnector - Starting network stage thread [UDP-Sender-0.0.0.0/0.0.0.0:0[1]]
20:07:21.843 [:CoapEndpoint-UDP-0.0.0.0:0#1] DEBUG org.eclipse.californium.core.network.stack.ReliabilityLayer - Exchange[L1, localhost:5683] send request
20:07:21.843 [:CoapEndpoint-UDP-0.0.0.0:0#1] DEBUG org.eclipse.californium.core.network.stack.ReliabilityLayer - Exchange[L1, localhost:5683] prepare retransmission for CON-GET    MID=   -1, Token=null, OptionSet={"Uri-Host":"localhost", "Observe":0, "Uri-Path":["PIOT","GatewayDevice","MgmtStatusCmd"]}, <empty data>
20:07:21.846 [:CoapEndpoint-UDP-0.0.0.0:0#1] DEBUG org.eclipse.californium.core.network.BaseMatcher - registering observe request CON-GET    MID=40986, Token=null, OptionSet={"Uri-Host":"localhost", "Observe":0, "Uri-Path":["PIOT","GatewayDevice","MgmtStatusCmd"]}, <empty data>
20:07:21.848 [:CoapEndpoint-UDP-0.0.0.0:0#1] DEBUG org.eclipse.californium.core.observe.InMemoryObservationStore - added observation for Token=DB9A97F758467560
20:07:21.849 [:CoapEndpoint-UDP-0.0.0.0:0#1] DEBUG org.eclipse.californium.core.network.InMemoryMessageExchangeStore - coap Exchange[L1, localhost:5683] added with KeyMID[localhost/127.0.0.1:5683-40986], CON-GET    MID=40986, Token=DB9A97F758467560, OptionSet={"Uri-Host":"localhost", "Observe":0, "Uri-Path":["PIOT","GatewayDevice","MgmtStatusCmd"]}, <empty data>
20:07:21.851 [:CoapEndpoint-UDP-0.0.0.0:0#1] DEBUG org.eclipse.californium.core.network.InMemoryMessageExchangeStore - coap Exchange[L1, localhost:5683] added with token KeyToken[DB9A97F758467560], CON-GET    MID=40986, Token=DB9A97F758467560, OptionSet={"Uri-Host":"localhost", "Observe":0, "Uri-Path":["PIOT","GatewayDevice","MgmtStatusCmd"]}, <empty data>
20:07:21.851 [:CoapEndpoint-UDP-0.0.0.0:0#1] DEBUG org.eclipse.californium.core.network.UdpMatcher - tracking open request [KeyMID[localhost/127.0.0.1:5683-40986], KeyToken[DB9A97F758467560]]
20:07:21.869 [UDP-Sender-0.0.0.0/0.0.0.0:0[0]] DEBUG org.eclipse.californium.elements.UDPConnector - UDPConnector (Thread[UDP-Sender-0.0.0.0/0.0.0.0:0[0],5,Californium/Elements]) sent 58 bytes to localhost/127.0.0.1:5683
```

```txt
[main] INFO org.eclipse.californium.elements.config.Configuration - defaults added COAP.
[main] INFO org.eclipse.californium.elements.config.Configuration - defaults added SYS.
[main] INFO org.eclipse.californium.elements.config.Configuration - defaults added UDP.
Nov 17, 2023 8:00:21 PM programmingtheiot.gda.connection.CoapClientConnector initClient
INFO: Created client connection to server / resource: coap://localhost:5683
Nov 17, 2023 8:00:21 PM programmingtheiot.gda.connection.CoapClientConnector <init>
INFO: Using URL for server conn: coap://localhost:5683
[main] INFO org.eclipse.californium.elements.config.Configuration - loading properties from file loading properties from file /home/zabe/programmingtheiot/java-components/Californium3.properties
[main] INFO org.eclipse.californium.core.network.RandomTokenGenerator - using tokens of 8 bytes in length
[main] INFO org.eclipse.californium.ban - Started.
[main] INFO org.eclipse.californium.core.network.CoapEndpoint - coap CoapEndpoint uses udp context
[main] INFO org.eclipse.californium.core.network.stack.BlockwiseLayer - coap BlockwiseLayer uses MAX_MESSAGE_SIZE=1024, PREFERRED_BLOCK_SIZE=512, BLOCKWISE_STATUS_LIFETIME=300000, MAX_RESOURCE_BODY_SIZE=8192, BLOCKWISE_STRICT_BLOCK2_OPTION=false
[main] INFO org.eclipse.californium.core.network.CoapEndpoint - coap Endpoint [coap://0.0.0.0:0] requires an executor to start, using default single-threaded daemon executor
[main] INFO org.eclipse.californium.elements.UDPConnector - UDPConnector starts up 2 sender threads and 2 receiver threads
[main] INFO org.eclipse.californium.elements.UDPConnector - UDPConnector listening on /[0:0:0:0:0:0:0:0]:63230, recv buf = 65536, send buf = 65536, recv packet size = 2048
[main] INFO org.eclipse.californium.core.network.CoapEndpoint - coap Started endpoint at coap://[0:0:0:0:0:0:0:0]:63230
[main] INFO org.eclipse.californium.core.network.EndpointManager - created implicit endpoint coap://[0:0:0:0:0:0:0:0]:63230 for coap
Nov 17, 2023 8:00:21 PM programmingtheiot.gda.connection.CoapClientConnector sendDiscoveryRequest
INFO:  --> URI: /PIOT. Attributes: org.eclipse.californium.core.server.resources.ResourceAttributes@7a6d7e92
NoNov 17, 2023 8:00:21 PM programmingtheiot.gda.connection.CoapClientConnector sendDiscoveryRequest
INFO:  --> URI: /PIOT/ConstrainedDevice. Attributes: org.eclipse.californium.core.server.resources.ResourceAttributes@aba625
Nov 17, 2023 8:00:21 PM programmingtheiot.gda.connection.CoapClientConnector sendDiscoveryRequest
INFO:  --> URI: /PIOT/ConstrainedDevice/ActuatorCmd. Attributes: org.eclipse.californium.core.server.resources.ResourceAttributes@97e93f1
Nov 17, 2023 8:00:21 PM programmingtheiot.gda.connection.CoapClientConnector sendDiscoveryRequest
INFO:  --> URI: /PIOT/ConstrainedDevice/SensorMsg. Attributes: org.eclipse.californium.core.server.resources.ResourceAttributes@5a5a729f
Nov 17, 2023 8:00:21 PM programmingtheiot.gda.connection.CoapClientConnector sendDiscoveryRequest
INFO:  --> URI: /PIOT/ConstrainedDevice/SystemPerfMsg. Attributes: org.eclipse.californium.core.server.resources.ResourceAttributes@4b520ea8
```
EOF.
