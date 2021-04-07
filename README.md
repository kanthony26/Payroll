import java.util.Scanner;

public class Payroll {

//set variable field
private String name;
private int idNumber;
private double hourlyRate;
private int hoursWorked;
private double grossPay;

//set accessors
public String getName()
{
return name;
}

public int getIdNumber()
{
return idNumber;
}

public double getHourlyRate()
{
return hourlyRate;
}

public int getHoursWorked()
{
return hoursWorked;
}

public double getGrossPay()
{
return hoursWorked * hourlyRate;
}

//set mutators
public void setName( String nameGiven)
{
name = nameGiven;
}

public void setIdNumber(int idNumberGiven)
{
idNumber = idNumberGiven;
}

public void setHourlyRate(double rateGiven)
{
hourlyRate = rateGiven;
}

public void setHoursWorked(int hoursGiven)
{
hoursWorked = hoursGiven;
}

//set constructor
public Payroll(String nameGiven, int idNumberGiven, double rateGiven, int hoursGiven)
{
name = nameGiven;
idNumber = idNumberGiven;
hourlyRate = rateGiven;
hoursWorked = hoursGiven;
}

//create user entry
public static void main(String[] args)
{
//get input variable
double userGrossPay;
String userEmplName;
int userIdNum;
double userRate;
int userHours;

//create new scanner object
Scanner scanner = new Scanner(System.in);

//get input from user
System.out.print("Enter employee's name:");
userEmplName = scanner.nextLine();

System.out.print("Enter employee's ID number:");
userIdNum = scanner.nextInt();

System.out.print("Enter hourly rate:");
userRate = scanner.nextDouble();

System.out.print("Enter number of hours worked:");
userHours = scanner.nextInt();

//create the object
Payroll payroll1 = new Payroll(userEmplName, userIdNum, userRate, userHours);

//Set the info
payroll1.setName(userEmplName);
payroll1.setIdNumber(userIdNum);
payroll1.setHourlyRate(userRate);
payroll1.setHoursWorked(userHours);

//Print entry and gross pay
System.out.printf(userEmplName + ", employee number " + userIdNum + ", made $%.2f in gross pay.\n", payroll1.getGrossPay());

}
}

