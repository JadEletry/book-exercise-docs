# Gateway Device Application (Connected Devices)

## Lab Module 02

Be sure to implement all the PIOT-GDA-* issues (requirements) listed at [PIOT-INF-02-001 - Lab Module 02](https://github.com/orgs/programming-the-iot/projects/1#column-9974938).

### Description

NOTE: Include two full paragraphs describing your implementation approach by answering the questions listed below.

What does your implementation do? 

The GDA implementation in this section utilizes the java language to create an IoT system containing the same
components included in our CDA, however this time we include anadditional metric -the SystemDiskUtilTask component to 
read and generate disk telemtry. 

How does your implementation work?

Similar to the CDA, the GDA implementation works by editing the pre-existing SystemPerformanceManager class
and provide it with its necessary components to actually collect the telemtry data. We start by adding the
start/stop methods then create a telemetry value template method. We're able to retrieve system CPU Util by 
using the java management interface. To gather and assess its own system performance at regular intervals
we can leverage the java language by using polling systems which are built into Java's SDK. 

### Code Repository and Branch

NOTE: Be sure to include the branch (e.g. https://github.com/programming-the-iot/python-components/tree/alpha001).
![image](https://github.com/JadEletry/book-exercise-docs/assets/71851213/d6c4bcba-c348-48ef-888d-101813fcfafb)

URL: https://github.com/ShahzabeM/GDA-Java

### UML Design Diagram(s)

NOTE: Include one or more UML designs representing your solution. It's expected each
diagram you provide will look similar to, but not the same as, its counterpart in the
book [Programming the IoT](https://learning.oreilly.com/library/view/programming-the-internet/9781492081401/).

![image](https://github.com/JadEletry/book-exercise-docs/assets/71851213/ebca867e-81c8-4e8f-9206-ada902381609)


### Unit Tests Executed

NOTE: TA's will execute your unit tests. You only need to list each test case below
(e.g. ConfigUtilTest, DataUtilTest, etc). Be sure to include all previous tests, too,
since you need to ensure you haven't introduced regressions.

ConfigUtilTests: 

GDA - 001 ConfigUtilTest Unit Test
![image](https://github.com/JadEletry/book-exercise-docs/assets/71851213/45721c5e-dc3f-4235-9fd9-f785048dfb69)


### Integration Tests Executed

NOTE: TA's will execute most of your integration tests using their own environment, with
some exceptions (such as your cloud connectivity tests). In such cases, they'll review
your code to ensure it's correct. As for the tests you execute, you only need to list each
test case below (e.g. SensorSimAdapterManagerTest, DeviceDataManagerTest, etc.)

GDA-App Test:

GDA - 001 Integration
![image](https://github.com/JadEletry/book-exercise-docs/assets/71851213/e40693f1-baab-445e-a649-a5c30aa3bb41)

GDA - 002 Integration Test for System Performane Manager Test
![image](https://github.com/JadEletry/book-exercise-docs/assets/71851213/62e98af7-ba03-4daf-a54e-d1a29c77f132)

GDA - 003 : Test for GatewaYDeviceAppTest
![image](https://github.com/JadEletry/book-exercise-docs/assets/71851213/ecd81905-383e-4139-ba3a-e4068471c527)

GDA - 005 Integration Test for SystemCpuUtil
![image](https://github.com/JadEletry/book-exercise-docs/assets/71851213/c92d8973-933e-46f7-8380-78d95c55373e)

GDA - 006 INtegration Test for SystemMemUtil
![image](https://github.com/JadEletry/book-exercise-docs/assets/71851213/bd6be850-3114-4861-bd3b-af3006f87e05)

GDA 007 - Integration Test
![image](https://github.com/JadEletry/book-exercise-docs/assets/71851213/b907f4ef-c6d5-468d-8136-ca992b88f638)


EOF.
