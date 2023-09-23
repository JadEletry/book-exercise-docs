# Constrained Device Application (Connected Devices)

## Lab Module 02

Be sure to implement all the PIOT-CDA-* issues (requirements) listed at [PIOT-INF-02-001 - Lab Module 02](https://github.com/orgs/programming-the-iot/projects/1#column-9974938).

### Description

NOTE: Include two full paragraphs describing your implementation approach by answering the questions listed below.

What does your implementation do? 

We've expanded on the previous implementation to create an IoT edge tier environment which utilizes python
to collect data through two different performance task components. One component being for the system cpu and
the other being for the system's memory. 

How does your implementation work?

The CDA application in this implemenation works by creating an instance called SystemPerformanceManager which is 
self-explanataory in its usage. We use this component to manage the two main telemetry data collection components within 
the function called SystemCpuUtilTask and SystemMemUtilTask which run as asynchronous threads. We're able to do this
by importing the psutil library. We want to be able to separate and manage our key functions so we use the 
BaseSystemUtilTask class to do this. 

### Code Repository and Branch

NOTE: Be sure to include the branch (e.g. https://github.com/programming-the-iot/python-components/tree/alpha001).

URL: 

### UML Design Diagram(s)

NOTE: Include one or more UML designs representing your solution. It's expected each
diagram you provide will look similar to, but not the same as, its counterpart in the
book [Programming the IoT](https://learning.oreilly.com/library/view/programming-the-internet/9781492081401/).

![image](https://github.com/JadEletry/book-exercise-docs/assets/71851213/f2f3531b-04ea-498c-baf6-61e9a90c8f4b)


### Unit Tests Executed

NOTE: TA's will execute your unit tests. You only need to list each test case below
(e.g. ConfigUtilTest, DataUtilTest, etc). Be sure to include all previous tests, too,
since you need to ensure you haven't introduced regressions.

ConfigUtilTests:

CDA 001 - Py UNIT TEST
![image](https://github.com/JadEletry/book-exercise-docs/assets/71851213/c65051f1-ef32-4e97-b33f-2043415c73ea)

### Integration Tests Executed

NOTE: TA's will execute most of your integration tests using their own environment, with
some exceptions (such as your cloud connectivity tests). In such cases, they'll review
your code to ensure it's correct. As for the tests you execute, you only need to list each
test case below (e.g. SensorSimAdapterManagerTest, DeviceDataManagerTest, etc.)

CDA-App Tests:

CDA 001 - Integration test of ConstrainedDeviceAppTest.py
![image](https://github.com/JadEletry/book-exercise-docs/assets/71851213/6888061c-66e5-47e2-84ba-651154c1dc4a)

CDA 002 - Integration test of SystemPerformanceManagerTest
![image](https://github.com/JadEletry/book-exercise-docs/assets/71851213/eda2627e-e69c-4209-adcd-52dda16573cb)

CDA 003 - Integration test of ConstrainedDeviceAppTest
![image](https://github.com/JadEletry/book-exercise-docs/assets/71851213/f42b6bb7-5d7b-4be2-9acb-9651f0da0027)

CDA 005 - test should pass
![image](https://github.com/JadEletry/book-exercise-docs/assets/71851213/53aa7faf-a4f0-4fd8-a975-1300c0bac884)

CDA 006 - test should pass
![image](https://github.com/JadEletry/book-exercise-docs/assets/71851213/abce5ff2-86c0-43aa-ac14-c8cf78ed2af9)

CDA - 007 Integration test of system performana manager,  for connecting the cpuUtilTask and memUtilTask to the PerformanceManager

![image](https://github.com/JadEletry/book-exercise-docs/assets/71851213/38d0cd7a-3e5a-4b56-977d-7c853c4c7c1b)

EOF.
