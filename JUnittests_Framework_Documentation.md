

DSDP/TM/JUnittests Framework Documentation
==========================================

< [DSDP](/DSDP "DSDP")‎ | [TM](/DSDP/TM "DSDP/TM")

Contents
--------

*   [1 Hitch-Hacker's Guide to Using and Writing DSDP-TM (aka RSE) JUnit tests](#Hitch-Hacker.27s-Guide-to-Using-and-Writing-DSDP-TM-.28aka-RSE.29-JUnit-tests)
*   [2 Using the DSDP-TM JUnit tests](#Using-the-DSDP-TM-JUnit-tests)
    *   [2.1 Launching the DSDP-TM JUnit tests as JUnit Plug-in Test](#Launching-the-DSDP-TM-JUnit-tests-as-JUnit-Plug-in-Test)
    *   [2.2 Launching the DSDP-TM JUnit tests from within the currently running Eclipse instance](#Launching-the-DSDP-TM-JUnit-tests-from-within-the-currently-running-Eclipse-instance)
*   [3 Writing DSDP-TM JUnit tests](#Writing-DSDP-TM-JUnit-tests)
    *   [3.1 Where to put a new test suite or test case?](#Where-to-put-a-new-test-suite-or-test-case.3F)
    *   [3.2 Which base class should a test case inherit from?](#Which-base-class-should-a-test-case-inherit-from.3F)
    *   [3.3 Dynamic single test enablement](#Dynamic-single-test-enablement)
    *   [3.4 _RSECoreTestCase_ features in detail](#RSECoreTestCase-features-in-detail)
        *   [3.4.1 Test Properties Management](#Test-Properties-Management)
        *   [3.4.2 Views and Perspective Management](#Views-and-Perspective-Management)
        *   [3.4.3 Test Data Location Management](#Test-Data-Location-Management)
        *   [3.4.4 Test Failure Log Collection Management](#Test-Failure-Log-Collection-Management)
        *   [3.4.5 Waiting for Results (RSEWaitAndDispatchUtil)](#Waiting-for-Results-.28RSEWaitAndDispatchUtil.29)
    *   [3.5 _RSEBaseConnectionTestCase_ features in detail](#RSEBaseConnectionTestCase-features-in-detail)
        *   [3.5.1 The Connection Manager](#The-Connection-Manager)
        *   [3.5.2 The Default Local System Connection](#The-Default-Local-System-Connection)

Hitch-Hacker's Guide to Using and Writing DSDP-TM (aka RSE) JUnit tests
-----------------------------------------------------------------------

This page is giving a introduction to the usage of the DSDP-TM JUnit tests framework as well as providing _How To's_ and short descriptions of the features available in the framework for JUnit test developers.

**Note:** The page is under on-going maintenance and will be updated if the framework is changed or extended!

Using the DSDP-TM JUnit tests
-----------------------------

Using means running the test cases either within a _target platform_ Eclipse or within the _currently executing_ Eclipse instance. There is basically only one question to distiguish between the two use cases:

_Do you only **use** RSE within your currently running Eclipse environment for remote system connectivity or do you **develop** plugin(s) based on RSE and/or using RSE API?_

*   If you answer _I develop plugin(s) using RSE API and/or I contribute/plan to contribute actively to RSE._ **-\> see section [2.1](#Launching-the-DSDP-TM-JUnit-tests-as-JUnit-Plug-in-Test)**
*   If you answer _I only use RSE within my running Eclipse for accessing remote systems._ **-\> see section [2.2](#Launching-the-DSDP-TM-JUnit-tests-from-within-the-currently-running-Eclipse-instance)**
*   If you cannot answer the above question clearly (because you may simple fall in both user groups at the same time), you may choose the use case with can serve your needs most efficiently.

### Launching the DSDP-TM JUnit tests as JUnit Plug-in Test

**Precondition:** Both JDT and PDE needs to be installed and activated.

1.  Open the Eclipse Launch Configuration Dialog in Run mode (Run -> Run...).
2.  Expand the "_JUnit Plug-in test_" category if not expanded anyway.
3.  Select the pre-configured launch configuration named "_RSE Combined Test Suite_".
4.  Choose "_Duplicate_" either from the context menu or from the tree toolbar.
5.  Change the launch configuration name of the duplicate to identify your test suites launch configuration.
6.  If your test suite is in another project than "_org.eclipse.rse.tests_", click now on the "_Browse..._" right after the "_Project_" entry field and select the project which contains your test suite.
7.  Click on the "_Select..._" button right after the "_Test class_" and choose your test suite or test case to run.
8.  Switch to the "_Main_" tab and check all settings to be as you want them. Usely you can leave them with their defaults.
9.  Switch to the "_Arguments_" tab and check all settings to be as you want them. Usely you can leave them with their defaults.
10.  Switch to the "_Environment_" tab if you require to set a specific environment to enable your test suite to run.
11.  **Switch to the "_Common_" tab and change the "_Save as_" setting to "_Local file_".**
12.  Click on the "_Run_" button to execute the launch configuration.

The _JUnit_ view will open, near to the _Problems_ view, to show the progress, successes and failures in executing the single test cases. Inspect the failures within the failure trace part for analysing why a test case might have failed. You have real great navigation possibilities and comparisation support from there.

In case that the _JUnit_ view is not opened automatically, you can open the view via _Window -> Show View -> Other ... -> Java -> JUnit_.

### Launching the DSDP-TM JUnit tests from within the currently running Eclipse instance

**Precondition:** The plugin _org.eclipse.rse.tests.framework_ must be installed and activated.

1.  Switch to the "_Remote System Explorer_" perspective.
2.  Open the "_Test Suites_" view via _Window -> Show View -> Other ... -> RSE Testing -> Test Suites_.
3.  Select your test suite (or all test suites if you want to run them all) and choose "_Run_" from the context menu.

Progress and results of the single running test cases are presented in the result pane of the view. Copy the content of the result pane and send it to the contact how have asked you to run a specific test suite (or all) within your running Eclipse instance.

Please note that the "_Test Suites_" view executes the test suites by default in a random Eclipse worker thread. You may enforce the test suite execution to the SWT UI thread by unselecting the green button in the view toolbar. However this will not have any effect either way for test suites or test cases how **require** to run in worker threads to succeed. As these test suites or test cases can (and should) flag the desire to run in worker threads and the test framework can (and will) asure that this desire is fulfilled on runtime, the green button may not show an noticable effect.

If you are using this way to launch the test cases for RSE development, you must carefully indentify the output part belonging to the failed test case and copy the failure stack trace from there to you RSE development environments _Java Stack Trace Console_. As you loose any comfort of easy navigation and result comparisation this way, for RSE developers it is gently advised to follow section [2.1](#Launching-the-DSDP-TM-JUnit-tests-as-JUnit-Plug-in-Test).

Writing DSDP-TM JUnit tests
---------------------------

### Where to put a new test suite or test case?

*   If you write test suites and test cases to test RSE components or parts, add the test suites and test cases to the _org.eclipse.rse.tests_ plug-in.
*   If you write test suites and test cases for your own implementation based on RSE and the RSE tests framework, create your own tests plug-in which depends on RSE and RSE tests framework plug-ins.
*   If you want to add a new test case, always check if you can extend an existing test suite before creating a new one.
*   If you have a set of test cases, probably linked to an specific RSE component or part, create a new test suite if there is not already one for the same RSE component or part.
*   If creating a new test suite
    *   Follow the package naming scheme of the existing test suites and test cases.
    *   Each package must start with the prefix _org.eclipse.rse.tests_.
    *   Place interfaces and implementations designated for use only in specific test case(s) in _internal_ packages.
    *   **Always** use the following template to create your own test suite and **change only** the _<YOUR ...>_ markers!

   <YOUR COPYRIGHT HEADER>
   package <YOUR PACKAGE DECLARATION>;

   import junit.framework.Test;
   import junit.framework.TestSuite;

   import org.eclipse.rse.tests.framework.DelegatingTestSuiteHolder;

   <YOUR TEST SUITE COMMENT HEADER>
   public class <YOUR TEST SUITE NAME> extends DelegatingTestSuiteHolder {

	/\*\*
	 \* Standard Java application main method. Allows to launch the test
	 \* suite from outside as part of nightly runs, headless runs or other.
	 \* <p><b>Note:</b> Use only <code>junit.textui.TestRunner</code> here as
	 \* it is explicitly supposed to output the test output to the shell the
	 \* test suite has been launched from.
	 \* <p>
	 \* @param args The standard Java application command line parameters passed in.
	 */
	public static void main(String\[\] args) {
		junit.textui.TestRunner.run(suite());
	}

	/\*\*
	 \* Combine all test into a suite and returns the test suite instance.
	 \* <p>
	 \* <b>Note: This method must be always called <i><code>suite</code></i> ! Otherwise
	 \* the JUnit plug-in test launcher will fail to detect this class!</b>
	 \* <p>
	 \* @return The test suite instance.
	 */
	public static Test suite() {
		TestSuite suite = new TestSuite("<YOUR TEST SUITE HUMAN READABLE NAME>"); //$NON-NLS-1$
		// add the single test suites to the overall one here.
		suite.addTestSuite(<YOUR TEST CASE IMPLEMENTATION CLASS NAME>.class);
		
		return suite;
	}
	
	/\* (non-Javadoc)
	 \* @see org.eclipse.rse.tests.framework.AbstractTestSuiteHolder#getTestSuite()
	 */
	public TestSuite getTestSuite() {
		return (TestSuite)RSEConnectionTestSuite.suite();
	}
   }
   

### Which base class should a test case inherit from?

That is quite simple. _Do you write test cases which requires the existance of a valid connection to a remote system?_

*   If **Yes**: Inherit from _RSEBaseConnectionTestCase_.
*   If **No**: Inherit from _RSECoreTestCase_.

### Dynamic single test enablement

It has been proved more than useful to introduce the possiblity to enable and disable single tests via configuration. This basically prevents administrator to disable failing tests by commenting out the corresponding test method within a test case. Furthermore, it enables users, having access only to the binary class files, and JUnit test developers to temporarly disable single tests of one or more test cases and/or test suites in order to focus on a specific limited set of tests. To satisfy this desire, a **certain style** of writing single test methods **is required**.

**Test method template:**

a)
   ...
   public class MyTestCase extends RSEBaseConnectionTestCase {
      ...
      public void testMyFunctionality() {
         // Call isTestCaseEnabled with the test id and return immediatelly if the
         // call should return false!
         if (!RSETestsPlugin.isTestCaseEnabled("MyTestCase.testMyFunctionality") return; //$NON-NLS-1$
         ...
      }
      ...
   }

b)
   Add the test id to the RSETestsResources.properties file and adjust the default (true == enabled, false == disabled).

   ...
   RSEConnectionTestCase.testConnect=true
   RSEConnectionTestCase.testResolveFilterString=true

   MyTestCase.testMyFunctionality=true
   ...

Single tests can be enabled/disabled by

*   *   Adjusting the test enabled state within _RSETestsResources.properties_ file or
    *   Specifying _-D<test id>=<true|false>_.

If _-D<test id>_ is explicitly provided, it overrides all other settings. If neither _-D<test id>_ provided nor the test id is defined within _RSETestsResources.properties_, the test is _enabled by default_.

**Related methods:**

   \* RSETestsPlugin.isTestCaseEnabled(String)

   See the corresponding javadoc for details on these method.
   

### _RSECoreTestCase_ features in detail

#### Test Properties Management

The RSE JUnit test framework provides the possibility to set and test for test case wide properties. The framework itself uses the test properties to control global test case behavior like the perspective to switch to before a test case runs or if and which view might be maximized to eliminate other view redraws for performance sensitive test cases. You can choose to manipulate the standard RSE JUnit test framework properties or you may add your own properties controlling specific behaviour of your own test framework base classes. The framework initialize the test properties once at the time the test case is instanciated. Most of the global framework properties are controlling _setUp()_ and/or _tearDown()_ behavior, but you may use the test properties management framework for controlling the behavior of your test or framework methods besides these two core JUnit test framework methods.

**Related methods:**

   \* initializeProperties()
   \* setProperty(String, boolean)
   \* setProperty(String, String)
   \* isProperty(String, boolean)
   \* initializeProperties()
   \* isProperty(String, String)
   \* getProperty(String)

   See the corresponding javadoc for details on these methods.

**Related interfaces:**

  \* 

    IRSECoreTestCaseProperties

 \- Defines static constants identifying the RSE JUnit test framework global properties

**Global properties:**

*   _PROP\_SWITCH\_TO_PERSPECTIVE_
    *   Default perspective id. This perspective will be activated, if not active anyway, within the tests _setUp()_ method. Default value is _org.eclipse.rse.ui.view.SystemPerspective_.
*   _PROP\_MAXIMIZE\_REMOTE\_SYSTEMS\_VIEW_
    *   Maximize the _Remote Systems_ view within the tests _setUp()_ method? Default value is _false_.
*   _PROP\_FORCE\_BACKGROUND_EXECUTION_
    *   Enforce the execution of the test within a non SWT display (UI) thread? Default value is _false_.
*   _PROP\_PERFORMANCE\_TIMING\_INCLUDE\_SETUP_TEARDOWN_
    *   Print the test performance timing information including the time consumed from _setUp()_ and _tearDown()_? Default value is _false_.

#### Views and Perspective Management

The RSE JUnit test framework provides convenience methods to find, show and hide views. You may use these methods to manipulate certain view attributes like toggle the zoom state of views. The framework itself uses these methods to switch to the default perspective and maximize the _Remote Systems_ view, if configured.

**Related methods:**

   \* findView(String, String)
   \* showView(String, String)
   \* hideView(String, String)

   See the corresponding javadoc for details on these methods.

**Related interfaces:**

  \* 

    IRSEViews

 \- Defines static constants for all RSE related view id's.

#### Test Data Location Management

Single tests may require to store and access whatever kind of data file(s) to test certain RSE functionality. The test framework provides access to a centralized test data location. **Any** test data accessed from any of the single tests, have to be stored relative to '**org.eclipse.rse.tests/test.data'**. Create a senseful named subdirectory there, identifying the test suite, test case or single test which is accessing this specific test data. If the test data is _host operating system_ specific, place the test data in subdirectories named the host operating system specific id (see _Platform.getOS()_ for details).

**Related methods:**

   \* getTestDataLocation(String, boolean)

   See the corresponding javadoc for details on these method.

#### Test Failure Log Collection Management

In many cases, if a single test if failing, it is not enough to see the _assert_ which caused the failure, to analyse and understand _why_ the tested attribute or object does not have the expected value. Connections and communication to and from remote systems may easely fail by any unpredictable external event causing either the remote system or any of the involved communication tools (probably external processes) to fail. As these tools may log not necessarly to the Eclipse error log, especially if external processes are involved, it is essential to get access and collect all possible existing logs in case of a test failure. The collected logs may explicitly include information dynamically dumped to a temporary file at the time the test log collector delegate is called. The default RSE JUnit test framework test failure log collector is collecting the Eclipse error log and the current set of Java system properties at the time of the failure. Write and register your own test log collector delegate if you have to collect other files and information in case of a test failure. You may register the delegate either globally for collecting the information on all test failures or only for your specific test cases.

_All logs are collected into a ZIP archive named RSEUnittestFailureLogs_<test name>.zip. The ZIP archive is located within the org.eclipse.rse.tests plugin state location (<workspace_loc>/.metadata/.plugins/org.eclipse.rse.tests). It needs to be cleared how we can get access to these log files for the nightly running tests._

**Related methods:**

   \* collectTestLogs(Test)
   \* RSETestsPlugin.addDelegate(IRSETestLogCollectorDelegate)
   \* RSETestsPlugin.removeDelegate(IRSETestLogCollectorDelegate)
   \* RSETestsPlugin.getTestLogCollectorDelegates()
   \* IRSETestLogCollectorDelegate.getAbsoluteLogFileLocations()
   \* IRSETestLogCollectorDelegate.dispose()

   See the corresponding javadoc for details on these method.

**Related interfaces:**

  \* 

    IRSETestLogCollectorDelegate

 \- RSE Test log collector delegate public API.

#### Waiting for Results (RSEWaitAndDispatchUtil)

As by the multi-threaded nature of Eclipse and Java, it is not guaranteed that all API calls, events and other possible activities are executed synchronously or are finished or even started at the moment the API call returns. A lot of activities, important for test cases to wait for, Eclipse or other API implementors can decide to initiate and execute asynchronously via the very powerful Eclipse Jobs framework. It is _absolutly essential_ for successfully writing complex (up to very complex) _functionality_ JUnit test cases to hold the execution of the current thread time out based and/or interrupt condition based _without preventing the SWT UI events from dispatching_! The _RSEWaitAndDispatchUtil_ is providing methods and interfaces to deal with these requirements.

**Related methods:**

   \* RSEWaitAndDispatchUtil.isDispatchThread()
   \* RSEWaitAndDispatchUtil.waitAndDispatch(long)
   \* RSEWaitAndDispatchUtil.waitAndDispatch(long, IInterruptCondition)
   \* IInterruptCondition.isTrue()
   \* IInterruptCondition.dispose()

   See the corresponding javadoc for details on these method.

**Related interfaces:**

  \* 

    IInterruptCondition

 \- Wait and dispatch interrupt condition public API.

### _RSEBaseConnectionTestCase_ features in detail

#### The Connection Manager

The RSE connection manager is providing and encapsulating all functionality related to finding, creating, removing or manipulating RSE connections and sub systems.

**Related methods:**

   \* getConnectionManager()
   \* IRSEConnectionManager.loadConnectionProperties(IPath, boolean)
   \* IRSEConnectionManager.loadConnectionProperties(Properties, boolean)
   \* IRSEConnectionManager.removeConnection(String, String)
   \* IRSEConnectionManager.findOrCreateConnection(IRSEConnectionProperties)
   \* IRSEConnectionManager.getFileSubSystem(IHost, String)
   \* IRSEConnectionManager.getShellSubSystem(IHost)
   \* IRSEConnectionManager.getTestSubSystem(IHost)
   \* IRSEConnectionProperties.getProperty(String)
   \* IRSEConnectionProperties.setProperty(String, String)

   See the corresponding javadoc for details on these method.

**Related interfaces:**

  \* 

    IRSEConnectionManager

 \- RSE connection manager plugin API.
  \* 

    IRSEConnectionProperties

 \- Defines static constants for accessing the single connection properties and related public API.

**RSE Connection Properties:**

*   _ATTR_NAME_
    *   The connection name. _Required_.
*   _ATTR\_PROFILE\_NAME_
    *   The profile name to store the connection to. _Optional_.
*   _ATTR\_SYSTEM\_TYPE_
    *   The system type of the connection. _Required_.
*   _ATTR_ADDRESS_
    *   The remote system IP address or DNS name. _Required_
*   _ATTR_USERID_
    *   The user id to use for connecting to the remote system. _Optional_.
*   _ATTR_PASSWORD_
    *   The password to use for connecting to the remote system. _Optional_.

_If a connection property is not specified, default values are assumed. The default values are loaded from org.eclipse.rse.tests/test.data/connectionDefault.properties. The load of the default connection properties can be suppressed if necessary._

#### The Default Local System Connection

The RSE JUnit test framework provides convenience access to the default available and always connected "_Local_" connection (system type == "_Local_"). You **should prefer** to use this connection for any test requiring a valid connection but does not test any remote system specific functionality.

**Related methods:**

   \* getLocalSystemConnection()

   See the corresponding javadoc for details on these method.


(Migrated from [https://wiki.eclipse.org/DSDP/TM/JUnittests_Framework_Documentation](https://wiki.eclipse.org/DSDP/TM/JUnittests_Framework_Documentation))