# Constrained Device Application (Connected Devices)

## Lab Module 03

Be sure to implement all the PIOT-CDA-* issues (requirements) listed at [PIOT-INF-03-001 - Lab Module 03](https://github.com/orgs/programming-the-iot/projects/1#column-10488379).

### Description

NOTE: Include two full paragraphs describing your implementation approach by answering the questions listed below.

![image](https://github.com/JadEletry/book-exercise-docs/assets/71851213/617e776a-1b46-48fd-9926-d89697a3112f)


What does your implementation do? 

Module 3's implementation focuses on adding functionality to our CDA so that we can measure and model the data it generates 
as a part of a simple sensor and actuator simulation environment. So the CDA incorporates logical components to produce 
sensing and actuation capabilities. 

How does your implementation work?

The CDA application works in this implementation by using a sensor data generator class named SensorDataGenerator which relies on NumPy 
packages to generate a series of float values with a given range over a period of time. The given values then provide sufficient variety to 
trigger actuation events which are configured within the settings file 'PiotConfig.props'. Our generator class implements 6 different 
methods to generate values for temperature, pressure, humidity, and any other float-based range which then returns an instance of 
the SensorDataSet class containing the float value entries and timestamp.

### Code Repository and Branch

NOTE: Be sure to include the branch (e.g. https://github.com/programming-the-iot/python-components/tree/alpha001).

URL: https://github.com/ShahzabeM/CDA-Python

### UML Design Diagram(s)

NOTE: Include one or more UML designs representing your solution. It's expected each
diagram you provide will look similar to, but not the same as, its counterpart in the
book [Programming the IoT](https://learning.oreilly.com/library/view/programming-the-internet/9781492081401/).

![image](https://github.com/JadEletry/book-exercise-docs/assets/71851213/133c1535-98dc-4729-818c-94be1b4193d5)


### Unit Tests Executed

NOTE: TA's will execute your unit tests. You only need to list each test case below
(e.g. ConfigUtilTest, DataUtilTest, etc). Be sure to include all previous tests, too,
since you need to ensure you haven't introduced regressions.

CDA-03-001: Actuator Test <br>
![image](https://github.com/JadEletry/book-exercise-docs/assets/71851213/930729d9-73ee-4ad2-a694-78db04ec9772)

CDA-03-001: SensorDataTest <br>
![image](https://github.com/JadEletry/book-exercise-docs/assets/71851213/bd0334ed-941a-4818-bfed-37329a2c7fca)

CDA-03-001: SensorDataTestCDA-03-001: SystemPerformanceDataTest <br>
![image](https://github.com/JadEletry/book-exercise-docs/assets/71851213/902a93f3-6036-44dc-b113-0b860c6e9f22)

CDA-03-003: HumidtySensorSimTaskTest <br>
![image](https://github.com/JadEletry/book-exercise-docs/assets/71851213/b6682b68-e6ed-4e97-bd53-bea10efa9709)

CDA-03-003: PressureSensorSimTaskTest <br>
![image](https://github.com/JadEletry/book-exercise-docs/assets/71851213/b8a1a0c3-1e68-42c9-9de3-a7a4a2910699)

CDA-03-003: TemperatureSensorSimTaskTest <br>
![image](https://github.com/JadEletry/book-exercise-docs/assets/71851213/3f487917-ecb6-48e2-beba-39157abd9f3c)

CDA-03-005: HvacActuatorSimTaskTest <br>
![image](https://github.com/JadEletry/book-exercise-docs/assets/71851213/9f9bf9e5-3e14-4c88-bf71-7aee27e2f00e)

CDA-03-005:HumidifierActuatorSimTaskTest <br>
![image](https://github.com/JadEletry/book-exercise-docs/assets/71851213/dea2ad92-6864-43c1-8630-2abb3cadb7ff)

CDA-03-006: SensorAdapterMangerTest <br>
![image](https://github.com/JadEletry/book-exercise-docs/assets/71851213/368e69ea-5720-45ec-833e-ab3dc9bb8dbf)

CDA-03-007: ActuatorAdpaterManagerTest <br>
![image](https://github.com/JadEletry/book-exercise-docs/assets/71851213/ca48f49d-7b93-49eb-b59e-cd0359b85941)

CDA-03-008: DeviceDataManager  <br>
![image](https://github.com/JadEletry/book-exercise-docs/assets/71851213/7e4e4eb6-9e07-4638-a713-4867eca82a37)

### Integration Tests Executed

NOTE: TA's will execute most of your integration tests using their own environment, with
some exceptions (such as your cloud connectivity tests). In such cases, they'll review
your code to ensure it's correct. As for the tests you execute, you only need to list each
test case below (e.g. SensorSimAdapterManagerTest, DeviceDataManagerTest, etc.)

CDA-03-009: Integraion Test for Constrained Device App <br>
![image](https://github.com/JadEletry/book-exercise-docs/assets/71851213/cb9004dc-5348-4e79-957e-fa340c427031)


EOF.
