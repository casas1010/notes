
** select device
command+shit+p
select device

** rebuild file
flutter clean
flutter pub get


** data types
const: internal value that cannot change when you write and when the code runs (compile and run time)
final: internal value that cannot be changed at run time
late: eventhough it has no value, it will have a value when it will be used. ex:I will be ready later
ex:1

void test(List<String>? names) {
  final int lenght;
  if (names != null) {
    lenght = names.length;
  }
}

** diff time values
compile: package this up so that i can run it later. its the packaging 
compile time:
run time: 


** functions
-function syntaxt:
returnType functionName(param1,arg2){
}

ex1:
String getFullName(String firstName, String lastName) {
  //return firstName + ' ' + lastName;
  return '$firstName $lastName';
}

- returnType can be void: means it does not return anything


** hot reload
saving code, looks for changes, and executes only those changes. it will execute everything in its path


** operators
-prefix:
-infix:
-sufix:


** list


** Sets
list of unique thins
ensures data is not duplicated!
ex:
final names = {1, 2, 3}; // works
final names = {1, 2, 3,3}; // breaks


**Maps   :: same as obs in javascript
- hold key value pairs
- keys need to be unique


** Sound Null-safety in dart
-null is the absence of a value
-syntax:
dataType? dataName = varValue;

-ex:
 String? name = null;   // this means that name can sometimes be null eventhough its type is String


** Cherry picking non-null values
- returns the first value after null
ex1:
const String? firstName = null;
const String? middleName = null;
const String? lastName = '3';

const FirstNoneNullValue = firstName ?? middleName ?? lastName;
print(FirstNoneNullValue); // 3

ex:2
const String? firstName = null;
const String? middleName = '2';
const String? lastName = '3';

const FirstNoneNullValue = firstName ?? middleName ?? lastName;
print(FirstNoneNullValue); // 2


** null-aware assignment operator
- pick a value that aint null (i think)
-
ex:
void test(String? firstName, String? middleName, String? lastName) {
  String? name = firstName;
  name ??= middleName;
  name ??= lastName;
  print(name);
}
test(null, 'middleName', 'lastName'); // middleName
test(null, null, 'lastName');         // lastName


** Conditional invocation
- acess properties of null obj
ex:
void test(List<String>? names) {
  final length = names?.length ?? 0;
}


** Enumerators
- named list of related items
- kinda like a string
- name starts with captital letter

ex:
enum PersonProperties { firstName, lastName, age }

void test() {
  print(PersonProperties.firstName);         // PersonProperties.firstName
  print(PersonProperties.firstName.name);    // firstName
}

** classes
- starts with upper case
- obj are created from classes
- blue print

** Objects
- obj is an instance of a class


** Inheritance and subclassing
- user key word extends
- allows u to recycle methods and props

** abstract classes
- class that cant be instantiated
- used as a utility class, to borrow functions
ex:
abstract class Person {
  final String name;
  final int age;

  Person(this.name, this.age);

  void run() {
    print('Running');
  }

  void breathe() {
    print('Breathing');
  }
}


** factory constructors
- can return instances that are not of the same class
ex:
class Cat {
  final String name;

  Cat(this.name);

  factory Cat.fluffBall() {
    return Cat('Fluf Ball');
  }
}

**Custom Operator

@override


** Extensions
- adding logic to existing classes


** Future
- async classes, kinda
* Async: does not return imediatly
- sync: does return imediatly
- await: waits until future function returns, kinda


** Streams
- contious data going
- future data that never ends


** Generators
- list of things that get calculated on the go
-uses sync*



** create flutter project
flutter create --org domain appName



** what is in a flutter file?

-analysis_options.yaml: contains syntax rules
-pubspec.yaml: info about tool, kinda like a config file. icons, version nm, dependencies


** BuildContext


** Scaffold
- basic component
- allows status bar




** Init state and dispose
- used by stateful widgets


** Navigating
Navigator.of(context).pushNamedAndRemoveUntil('ROUTE_NAME' (route) => false):
- routes and replaces

Navigator.of(context).pushNamed('ROUTE_NAME');
- routes without replacing


Navigator.of(contex).pop();
- pop view off