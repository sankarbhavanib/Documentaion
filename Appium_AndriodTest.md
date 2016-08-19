# Source 
http://appium.io/

# Pom.xml

<project xmlns="http://maven.apache.org/POM/4.0.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
	xsi:schemaLocation="http://maven.apache.org/POM/4.0.0 http://maven.apache.org/xsd/maven-4.0.0.xsd">
	<modelVersion>4.0.0</modelVersion>
	<groupId>com.mobile</groupId>
	<artifactId>com.mobile</artifactId>
	<version>0.0.1-SNAPSHOT</version>
	<!-- https://mvnrepository.com/artifact/io.appium/java-client -->
	<dependencies>
		<dependency>
			<groupId>io.appium</groupId>
			<artifactId>java-client</artifactId>
			<version>3.3.0</version>
		</dependency>
		<dependency>
			<groupId>org.seleniumhq.selenium</groupId>
			<artifactId>selenium-java</artifactId>
			<version>2.53.1</version>
		</dependency>
	</dependencies>
</project>


# Sample Test 

package com.mobile;

import static org.junit.Assert.*;

import java.io.File;
import java.net.MalformedURLException;
import java.net.URL;
import java.util.List;

import org.junit.Test;
import org.openqa.selenium.By;
import org.openqa.selenium.WebElement;
import org.openqa.selenium.remote.DesiredCapabilities;

import io.appium.java_client.android.AndroidDriver;
import io.appium.java_client.remote.MobileCapabilityType;
import io.appium.java_client.remote.MobilePlatform;

public class DesiredCapabulities {

	@Test
	public void test() throws MalformedURLException {
		File appDir = new File("src");
		File app = new File (appDir,"app-demo-debug.apk");
		
		DesiredCapabilities desiredCapabulities = new DesiredCapabilities();
		desiredCapabulities.setCapability(MobileCapabilityType.PLATFORM_NAME, MobilePlatform.ANDROID);
		desiredCapabulities.setCapability(MobileCapabilityType.DEVICE_NAME, "Android Emulator");
		desiredCapabulities.setCapability(MobileCapabilityType.PLATFORM_VERSION, "6.0");
		desiredCapabulities.setCapability(MobileCapabilityType.NEW_COMMAND_TIMEOUT, "100");
		desiredCapabulities.setCapability(MobileCapabilityType.APP, app.getAbsolutePath());
		
		AndroidDriver androidDriver = new AndroidDriver(new URL("http://127.0.0.1:4723/wd/hub"), desiredCapabulities);
		androidDriver.findElementById("com.paypal.android.sdk.onetouch.demo:id/refreshWalletStatusButton").click();
		
		// this is just refarence code . when you have more then one element with same naem , you get all to List<WebElement>
//		int s=androidDriver.findElements(By.className("android.widget.EditText")).size();
//		System.out.println(s);
//		List<WebElement> a = androidDriver.findElements(By.className("android.widget.EditText"));
//		a.get(0).sendKeys("Appium");
//		a.get(1).sendKeys("Mobile");
//		a.get(2).sendKeys("appium@training");
//		a.get(3).sendKeys("password");
//		androidDriver.findElementById("com.bt.bms:id/action_icon").click();
		
		// sample set code 2 to move item with display test "scrollTo"
		
//		driver.scrollTo("Preference").click();
//		List <WebElement>b=driver.findElements(By.id("android:id/text1"));
//		System.out.println(b.get(8).getText());
//		
		//mobile Guestures swipe , zoom and .. 
//		
//		MobileElement abc=(MobileElement)driver.findElement(By.className("android.widget.CheckedTextView"));
//		abc.swipe(SwipeElementDirection.UP, 6000);
//		abc.zoom();
//		
		//t0 tap action 
		
		//TouchAction t=new TouchAction(driver);
		//t.tap(abc.get(2)).perform();
		//TouchAction t1=new TouchAction(driver).longPress(el);
		
		
		
		//driver.installApp("");
		//driver.closeApp();
		
		//driver.currentActivity();
		//driver.context(name)
		//driver.zoom(el);
		
	//	driver.findElementById("com.calculator:id/EditText01").sendKeys("50");
	//	driver.findElementById("com.calculator:id/EditText02").sendKeys("50");
		
		//to find the element for UIselector 
	//	driver.findElementByAndroidUIAutomator("new UiSelector().text(\"Multiply\")").click();
	//	System.out.println(driver.findElementById("com.calculator:id/TextView01").getText());
		
		
		//driver.sendKeyEvent(AndroidKeyCode.HOME);
	}

}

