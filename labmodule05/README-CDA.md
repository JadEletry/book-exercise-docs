# Constrained Device Application (Connected Devices)

## Lab Module 05

Be sure to implement all the PIOT-CDA-* issues (requirements) listed at [PIOT-INF-05-001 - Lab Module 05](https://github.com/orgs/programming-the-iot/projects/1#column-10488421).

### Description

NOTE: Include two full paragraphs describing your implementation approach by answering the questions listed below.

What does your implementation do? 

Module 5's CDA implementation extends the telemtry data generated from the simulated sensors previous implementations 
to have the data usable by other devices. In other, words, we're trying to send objects written in python over to our GDA, 
which are written in java. 

How does your implementation work?

The implementation works by integrating data translation within the project so that the generated data being used by the CDA
is converted/comprehended so that the GDA can process the information. We use the _DeviceDataManager_ class to orchestrate
information flow within the application, and then use a new component - _DataUtil_ as a centralized data translation utility
for converting the CDA's data container objects into a format in which the GDA can read. 

### Code Repository and Branch

NOTE: Be sure to include the branch (e.g. https://github.com/programming-the-iot/python-components/tree/alpha001).

URL: 

### UML Design Diagram(s)

NOTE: Include one or more UML designs representing your solution. It's expected each
diagram you provide will look similar to, but not the same as, its counterpart in the
book [Programming the IoT](https://learning.oreilly.com/library/view/programming-the-internet/9781492081401/).

![image](https://github.com/JadEletry/book-exercise-docs/assets/71851213/08fd8c96-c146-411b-896e-af5db3d485a8)

### Unit Tests Executed

NOTE: TA's will execute your unit tests. You only need to list each test case below
(e.g. ConfigUtilTest, DataUtilTest, etc). Be sure to include all previous tests, too,
since you need to ensure you haven't introduced regressions.


### Integration Tests Executed

NOTE: TA's will execute most of your integration tests using their own environment, with
some exceptions (such as your cloud connectivity tests). In such cases, they'll review
your code to ensure it's correct. As for the tests you execute, you only need to list each
test case below (e.g. SensorSimAdapterManagerTest, DeviceDataManagerTest, etc.)

PIOT-CDA-05-001: Part01 Integration Test for SystemPerformanceManagerTest<br>
![image](https://github.com/JadEletry/book-exercise-docs/assets/71851213/5de76576-ce95-4858-82ad-1e5a4f684610)

EOF.
