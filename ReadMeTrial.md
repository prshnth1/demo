# Apache Beam an Introduction
### _Reading an Object[Employee Entity ] and writing a CSV file_

### Steps

- Create a pipeline
- Generate Employees List 
- Converts the list of Employees to a PCollecton Object.
- Convert the PCollection Object of Employee Type to String
  - Create a MapElements Object which takes in Employee and converts it to a String
  - Using the newly created MapElement Object create a PCollection Object of String Type
- Write the PCollection result to a file
- Run the pipeline
- Item 1
- Item 2
  - Sub Item 1
  - Sub Item 2


### 1) Create a Pipeline
    Pipeline pipeline = Pipeline.create();
    

### 2) Generate Employees List  

```sh

//Generate Employees Method

static List<EmployeeEntity> generateEmployees() {
		EmployeeEntity employee1 = new EmployeeEntity("1", "Mayank");
		EmployeeEntity employee2 = new EmployeeEntity("2", "Awadhes");
		EmployeeEntity employee3 = new EmployeeEntity("3", "Prashanth");
		EmployeeEntity employee4 = new EmployeeEntity("4", "Taimur");
		List<EmployeeEntity> employeeList = new ArrayList<EmployeeEntity>();
		employeeList.add(employee1);
		employeeList.add(employee2);
		employeeList.add(employee3);
		employeeList.add(employee4);
		return employeeList;
	}
	
// Gets employees	
List<EmployeeEntity> employeeList = generateEmployees();
	

```
We have use **Create.of(employeeList)**. Create<T> takes a collection of elements of type T known when the pipeline is constructed and returns a PCollection<T> containing the elements.

### 4) Converts the list of Employees to a PCollecton Object.

```sh


	

```

### 3) Running Pipeline 

```sh
pipeline.run();
```
## Plugins



Reference documents:
    [ApacheBeam][ApacheBeam]



[//]: # (These are reference links used in the body of this note and get stripped out when the markdown processor does its job. There is no need to format nicely because it shouldn't be seen. - http://stackoverflow.com/questions/4823468/store-comments-in-markdown-syntax)

   [ApacheBeam]: <https://beam.apache.org/documentation/programming-guide/>
   [Create.of]: <https://beam.apache.org/releases/javadoc/2.4.0/org/apache/beam/sdk/transforms/Create.html/>
