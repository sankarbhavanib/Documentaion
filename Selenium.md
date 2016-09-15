##Learning

http://www.seleniumhq.org/docs/

http://testng.org/doc/index.html

We are going to use http://www.mortgagecalculator.org/ for our testing 

To learn https://www.youtube.com/watch?v=3BeK5aH2y3Q&list=PL2DAF7B30B4063C7A

##Interview 

https://www.youtube.com/watch?v=YWdAh3gTc6c

http://www.softwaretestinghelp.com/selenium-interview-questions-answers/

https://bitbucket.org/
sankarbhavanib/standard short one
======================
mobile 

http://appium.io/
Phyton 


rest
http://www.mastertheboss.com/jboss-frameworks/resteasy/resteasy-client-api-tutorial
http://www.vogella.com/tutorials/REST/article.html
http://www.vogella.com/tutorials/GoogleAppEngineJava/article.html

 
java 

what is the difference between compare / cooperative  (what-is-the-difference-between-compare-and-compareto)
exceptions are two types. For details of checked and unchecked exceptions 

try -catch - finally 


what is difference between string builder / string buffer , which one you prefer 

what is null pointer exceptiosn ? how to resolve it ?  how do general  exceptions you get ? and how do you handle them 


Types if selenium exceptions (https://selenium.googlecode.com/git/docs/api/java/org/openqa/selenium/support/ui/ExpectedConditions.html) for further  informationrmaion  
	1.	Exception
	2.	NullPointerException 
	3.	NoSuchElementException :There are three common causes for this exception:
	⁃	The locator that you are using to find the element is incorrect
	⁃	Something has gone wrong and the element has not been rendered
	⁃	You tried to find the element before it was rendered
	4.	NoSuchFrameException
	5.	NoSuchWindowException : String currentWindowHandle = driver.getWindowHandle();
	6.	ElementNotVisibleException
	7.	StaleElementReferenceException : AJAX or JavaScript-heavy websites
	8.	InvalidElementStateException
	9.	UnsupportedCommandException
	10.UnreachableBrowserException  : browser that you are trying to use has not been installed or nor not installed in the default location 
	11.SessionNotFoundException  :   browser crashed or you quit the driver instance inadvertently 

Wait functions
Thread.sleep(5000);
Object.wait()
Timeouts() object  in selenium has 3 built in features (Global variables) 
	•	The page load timeout  : driver.manage().timeouts().pageLoadTimeout(15, TimeUnit.SECONDS);
	•	The script timeout
	•	The implicit wait timeout : driver.manage().timeouts().implicitlyWait(15, TimeUnit.SECONDS);








couple of scenario questions 

how do you write the logic , on each open bracket has corresponding closing bracket 
how do you write the logic to find uniques words on string / letter 

what are classes ? methods ? interfaces ? abstract class , what is implementation ?
 
selenium 
/Users/bbheemanadham/Google Drive/Learning/Java Learning/rest/mastering-selenium-testng


Selenium 2 Testing Tools: Beginner's Guide, David Burns.
AJAX Methods 
	•	waitForAlertNotPresent
	•	waitForAlertPresent
	•	waitForElementPresent
	•	waitForElementNotPresent
	•	waitForTextPresent
	•	waitForTextNotPresent
	•	waitForPageToLoad
	•	waitForFrameToLoad”
Locators 
	•	Locate elements by ID
	•	Locate elements by Name
	•	Locate elements by Link
	•	Locate elements by XPath
				By byXpath = By.xpath("//input[(@id='id_Start') and (@class = 'blabla')]")
				List<WebElement> elements = driver.findElements(byXpath);

	•	Locate elements by CSS
	•	Locate elements by DOM


Firebug: https://addons.mozilla.org/firefox/addon/firebug
Firebug has become the defacto tool for web developers as it allows developers to find elements on the page by using the find functionality.It has a JavaScript REPL. REPL stands for Read-Eval-Print-Loop or interactive shell that allows you to run JavaScript without having to create an entire page.
Firefinder: https://addons.mozilla.org/firefox/addon/firefinder-for-firebug
Excerpt From: “Selenium 2 Testing Tools Beginner's Guide.” iBooks. y good tool for testing out XPath and CSS on the page. It will highlight all elements on the page that match the selector to your element location.


how to work on Chrome and IE 
“On Linux and Mac OS X do: export PATH=$PATH:/path/to/chromedriver.
On Windows do: set PATH=$PATH;\path\to\chromedriver.

mastering-selenium-webdriver
***
if you add  below configarable  variable on pom.xml ,
	<properties>
		<!-- Configurable variables -->
		<threads>1</threads>
	</properties>
 you can use in from  command line as follows  mvn clean install -Dthreads=2
***
Question ? : when i execute mvn clean install why my all tests are not running 
Answer :  by default Maven will use “maven-surefire-plugin” to run files that have test at the start or end of their name ( class name) 
what is the difference  between “maven-surefire-plugin” and “maven-failsafe-plugin”
http://selenium-python.readthedocs.org

make sure the read the wait statemets from selenium  and compare how paypal made it easy in se-lien / bluefin 

how to find elements ( Xpath / DOM reader   other options 

reports , what kind of reports you use and how to do it 
testNG

why i am not able to see web driver interface ? or Jar file called web driver 

http://career.guru99.com/top-30-selenium-interview-questions-answers/
http://www.softwaretestinghelp.com/selenium-interview-questions-answers/


java.lang.IllegalStateException: The path to the driver executable must be set by the webdriver.chrome.driver system property; for more information, see http://code.google.com/p/selenium/wiki/ChromeDriver. The latest version can be downloaded from http://code.google.com/p/chromedriver/downloads/list




