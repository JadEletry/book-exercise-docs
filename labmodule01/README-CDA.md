# Constrained Device Application (Connected Devices)

## Lab Module 01

Be sure to implement all the PIOT-CDA-* issues (requirements) listed at [PIOT-INF-01-001 - Lab Module 01](https://github.com/orgs/programming-the-iot/projects/1#column-9974937).

### Description

NOTE: Include two full paragraphs describing your implementation approach by answering the questions listed below.

What does your implementation do? 

The implementation for the CDA device creates an environment for pydev to run in order to
initialize the device. In doing so, we can approve the environment's ability to run securely.

How does your implementation work?

The implementation works by utilizing the python language within the CDA environement to pull data
from the github repository, the data being excuted is tested within Eclipse and then pushed back into the 
repository.


### Code Repository and Branch

![image](https://github.com/JadEletry/book-exercise-docs/assets/71851213/7df27f88-bc8c-4c30-8157-82b8465a1aa4)


NOTE: Be sure to include the branch (e.g. https://github.com/programming-the-iot/python-components/tree/alpha001).

URL: https://github.com/ShahzabeM/CDA-Python.git

### UML Design Diagram(s)

NOTE: Include one or more UML designs representing your solution. It's expected each
diagram you provide will look similar to, but not the same as, its counterpart in the
book [Programming the IoT](https://learning.oreilly.com/library/view/programming-the-internet/9781492081401/).

![image](https://github.com/JadEletry/book-exercise-docs/assets/71851213/dd10ce58-a6d8-42e8-8d8d-49401a82b288)


### Unit Tests Executed

NOTE: TA's will execute your unit tests. You only need to list each test case below
(e.g. ConfigUtilTest, DataUtilTest, etc). Be sure to include all previous tests, too,
since you need to ensure you haven't introduced regressions.

ConfigUtilTest: 

![image](https://github.com/JadEletry/book-exercise-docs/assets/71851213/d38dac1e-7177-4e05-88be-df7f230a4048)



### Integration Tests Executed

NOTE: TA's will execute most of your integration tests using their own environment, with
some exceptions (such as your cloud connectivity tests). In such cases, they'll review
your code to ensure it's correct. As for the tests you execute, you only need to list each
test case below (e.g. SensorSimAdapterManagerTest, DeviceDataManagerTest, etc.)

CDA-AppTest:

![image](https://github.com/JadEletry/book-exercise-docs/assets/71851213/cc68313f-ab6f-443a-a167-1b5f8333dc46)


EOF.
