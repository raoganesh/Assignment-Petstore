# Assignment-Petstore
Petstore-Assignment
Testing Assignment
Date: 18/03/2018
Time: 10:00 AM
Prepared By: Ganesh Rao
Project under Test: Online Pet Store
Sprint: 01 – Week 1
 
Test Scenarios Identified Based on User Scenarios:
01:  Test to verify system display the current date- Ref US01
02: Test to verify Adding New Pet into the system-Ref US03
03: Test to verify List of Available Pets in the system-Ref US02
04: Test to edit details of Existing Pets in the system-Ref US04
 
Assumptions:
1. Browser Considered for Test: Internet Explorer 11.0
2. Software Tools Used: Eclipse, Selenium Web Driver (Free Open Source tools)
3. SQL Server Databases
4. Operating System: Windows 7
 
Development Team Assumptions & Responsibilities:
1. Code Delivery via Appropriate Configuration Management Tools (  eg : TFS, IBM Clear case)
2. Test URL’s
3. Release Information’s or  Special Instructions
4. Unit  Test Results
 
Test Data Requirements: Test Team to create appropriate test data required for relevant testing
 
Test Execution Procedure:
01. Download and Install Eclipse Application to System under Test
02. Download and Install Selenium Web driver files.
Test Scripting: 01:  Test to verify system display the current date- Ref US01
Manual Test Case Development:
S/N
Description
Test Data
Expected Result
Actual Result
1
Invoke IE Explorer
     
IE should be invoked
 
2
Enter the Pet store ULR in the IE explorer address bas
URL:           ”https://www.petstore.com”
Pet Store URL should be entered
 
3.
Verify the Pet store Portal successfully launched and loaded
URL:           ”https://www.petstore.com”
Pet store Portal should be successfully launched
 
4.
Verify the system current date is displayed in the pet store portal
Date :
Time :
Pet store Portal should display the current system date and time.
 
 
 
 
 
 
 
Automation Test Case Development: Test to verify system display the current date- Ref US01
import java.util.concurrent.TimeUnit;
import org.openqa.selenium.*;
import org.openqa.selenium.InternetExplorer.InternetExplorerDriver;
public class uiAutomation
 
{
public static void main(String[] args)
{
 
WebDriver driver = new InternetExplorerDriver();
 
driver.manage ().timeouts ().implicitlyWait (10, TimeUnit.SECONDS);
 
// Launch website
 
driver.navigate ().to ("http://www.petstore.com /");
 
// Maximize the browser
 
driver.manage().window().maximize();
 
//get current date time with Date()
 
Date date = new Date();
 
// Now format the date
 
String date1= dateFormat.format(date);
 
// Print the Date
System.out.println(date1);
 
}
 
}
 
 
 
 
Test Scripting: 01:  Test to verify Adding New Pet into the system-Ref US03
Manual Test Case Development:
S/N
Description
Test Data
Expected Result
Actual Result
1
Invoke IE  Explorer
     
IE should be invoked
 
2
Enter the Pet store ULR in the IE explorer address bas
URL:           ”https://www.petstore.com””
Pet Store URL should be entered
 
3.
Verify the Pet store Portal successfully launched and loaded
URL:           ”https://www.petstore.com”
Pet store Portal should be successfully launched
 
4.
Select Create New Pet tab
 
Create new Pet Tab should be selected
 
5.
Verify Create New Pet tab has two fields
Name :
Status:
Create New Pet tab should have two fields for Creating pet information.
 
6.
Select the Name field and Enter the Pet Name in the Name filed
Name : “TEST”
Given Name should be entered in the Name field.
 
7.
Press SHIFT + Tab keys
Status : “’Active”
Focus should now be set on Status field
 
8.
Press Create button on the Create  Pet tab
Status : “’Active”
New Pet should be created and saved in DB with status set to active.
 
 
Automation Test Case Development: Test to verify Adding New Pet into the system-Ref US03
import java.util.concurrent.TimeUnit;
import org.openqa.selenium.*;
import org.openqa.selenium.InternetExplorer.InternetExplorerDriver;
public class uiAutomation
 
{
public static void main(String[] args)
{
 
WebDriver driver = new InternetExplorerDriver();
 
driver.manage ().timeouts ().implicitlyWait (10, TimeUnit.SECONDS);
 
// Launch website
 
driver.navigate ().to ("http://www.petstore.com /");
 
// Maximize the browser
 
driver.manage().window().maximize();
 
 
// Click on Create New Pet Tab
driver.findElement(By.xpath(".//*[@id='Create Net Pet']/div[4]/div[3]/a")).click();
 
 
// Click Name Field
driver.findElement(By.xpath(".//*[@id='Name']/div[4]/div[3]/a")).click();
 
 
// Enter value TEST in the Name Field
driver.findElement(By.id("Name")).sendKeys("Test");
 
// Enter value Active in the Status Field
driver.findElement(By.id("Status")).sendKeys("Active");
 
// Click Create  Button
driver.findElement(By.xpath(".//*[@id='create']/table/tbody
/tr/td[2]/input")).click();
 
// Get the Result Text based on its xpath
String result =
driver.findElement(By.xpath(".//*[@id='content']/p[2]/span/font/b")
)
.getText();
//Print a Log In message to the screen
System.out.println(" The Result is " + result);
//Close the Browser.
driver.close();
}
} ​ ​
 
 
 
Summary: Please find above assignment done in good faith with my industry knowledge. My expertise comes in Functional Testing and am building my Automation skills in parallel. I have only delivered the assignments of 2 user scenarios and similar approach will be applied in development of other user scenarios as will and this is just the testimony of how I intend approach to solutions for the given problem.
 
 
 
 
 
 
