# cleanCode

## **Variables**
### Use meaningful and pronounceable variable names
**Bad codes:**
**Bad:**
```java
String yyyymmdstr = new SimpleDateFormat("YYYY/MM/DD").format(new Date());
// address
private String getDiZhi();
//pwd
private void modifyPassword(String password1 ,String password2)
```

**Good:**
```java
String currentDate = new SimpleDateFormat("YYYY/MM/DD").format(new Date());

private String getAddress();
private void modifyPassword(String oldPassowrd,String newPassword)
```

### Use the same vocabulary for the same type of variable

**Bad codes:**
```java
getUserInfo();
getClientData();
getCustomerRecord();
```

**Good:**
```java
getUser();
```

### Don't add unneeded context
If your class/object name tells you something, don't repeat that in your
variable name.

**Bad:**
```java
class Car {
  public String carMake = "Honda";
  public String carModel = "Accord";
  public String carColor = "Blue";
}

void paintCar(Car car) {
  car.carColor = "Red";
}
```

**Good:**
```java
class Car {
  public String make = "Honda";
  public String model = "Accord";
  public String color = "Blue";
}

void paintCar(Car car) {
  car.color = "Red";
}
```