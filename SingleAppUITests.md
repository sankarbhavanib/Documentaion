
Step1 : add following  to gradle.properties  under  defaultConfig

```
testInstrumentationRunner 'android.support.test.runner.AndroidJUnitRunner'
```
Step2 : add following  to gradle.properties  unde dependencycs 
```
 //new tests
    androidTestCompile 'com.android.support:support-annotations:23.2.0'
    androidTestCompile 'com.android.support.test:runner:0.4.1'
    androidTestCompile 'com.android.support.test:rules:0.4.1'
    androidTestCompile 'com.android.support.test.espresso:espresso-core:2.2.1'
    androidTestCompile 'com.github.lkorth:device-automator:master-SNAPSHOT'
  ```
step 2: create tests under App/Src/androidTest/java/com.paypal.teat

```
package com.paypal.test;

import android.support.test.espresso.action.ViewActions;
import android.support.test.rule.ActivityTestRule;
import android.support.test.runner.AndroidJUnit4;

import com.lukekorth.deviceautomator.AutomatorAction;
import com.paypal.android.sdk.onetouch.sample.MainOtcSampleAppActivity;
import com.paypal.android.sdk.onetouch.sample.R;

import org.junit.Rule;
import org.junit.Test;
import org.junit.runner.RunWith;

import static android.support.test.espresso.Espresso.onView;
import static android.support.test.espresso.action.ViewActions.closeSoftKeyboard;
import static android.support.test.espresso.action.ViewActions.scrollTo;
import static android.support.test.espresso.assertion.ViewAssertions.matches;
import static android.support.test.espresso.matcher.ViewMatchers.withId;
import static android.support.test.espresso.matcher.ViewMatchers.withText;
import static com.lukekorth.deviceautomator.AutomatorAction.setText;
import static com.lukekorth.deviceautomator.DeviceAutomator.onDevice;
import static com.lukekorth.deviceautomator.UiObjectMatcher.withContentDescription;

@RunWith(AndroidJUnit4.class)
public class OTCBrowserTest {

    @Rule
    public ActivityTestRule<MainOtcSampleAppActivity> mActivityRule = new ActivityTestRule<>(
            MainOtcSampleAppActivity.class);

    @Test(timeout = 60000)
    public void BrowserConsent() throws InterruptedException {
        TestHelper.selectSpinner(R.id.server_spinner, "mock");
        onView(withId(R.id.consentButton)).perform(scrollTo());
        onView(withId(R.id.addressScopeCheckBox)).perform(ViewActions.click());
        onView(withId(R.id.walletSecurityCheckSwitch)).perform(ViewActions.click());
        onView(withId(R.id.consentButton)).perform(scrollTo(),ViewActions.click());
        onDevice(withContentDescription("Email")).perform(AutomatorAction.click(), setText("test@paypal.com"));
        onDevice().pressTab().typeText("password");
        closeSoftKeyboard();
        onDevice(withContentDescription("Log In")).perform(AutomatorAction.click());
        onDevice(withContentDescription("Log In")).perform(AutomatorAction.click());
        onDevice(withContentDescription("Agree")).perform(AutomatorAction.click());
        onView(withId(R.id.textViewResultStatus)).perform(scrollTo());
        onView(withId(R.id.textViewResultStatus)).check(matches(withText("CONSENT success")));

    }



}```
