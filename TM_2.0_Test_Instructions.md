

TM 2.0 Test Instructions
========================

Nav: [DSDP/TM](./TM "DSDP/TM") | [DSDP/TM/Testing](./Testing "DSDP/TM/Testing") | [TM 2.0 Testing](./TM_2.0_Testing "TM 2.0 Testing") | TM 2.0 Test Instructions | [TM 2.0 Known Issues and Workarounds](./TM_2.0_Known_Issues_and_Workarounds "TM 2.0 Known Issues and Workarounds") | [TM Manual Test Plan](./TM_Manual_Test_Plan "TM Manual Test Plan")

* * *

Contents
--------

*   [1 Latest News](#Latest-News)
*   [2 Test Procedure](#Test-Procedure)
    *   [2.1 Step 1: Download Prerequisites](#Step-1:-Download-Prerequisites)
    *   [2.2 Step 2: Install TM / RSE](#Step-2:-Install-TM-.2F-RSE)
    *   [2.3 Step 3: Record your Test Environment](#Step-3:-Record-your-Test-Environment)
    *   [2.4 Step 4: Prepare for Bug Reports](#Step-4:-Prepare-for-Bug-Reports)
    *   [2.5 Step 5: Basic Sanity Check](#Step-5:-Basic-Sanity-Check)
    *   [2.6 Step 6: Do your special test assignment](#Step-6:-Do-your-special-test-assignment)
*   [3 Final Comments](#Final-Comments)
    *   [3.1 Comments for testing round 1](#Comments-for-testing-round-1)
    *   [3.2 Comments](#Comments)

Latest News
-----------

*   **See [TM 2.0 Known Issues and Workarounds](./TM_2.0_Known_Issues_and_Workarounds "TM 2.0 Known Issues and Workarounds") now** for other known bugs and how to avoid them.

Test Procedure
--------------

### Step 1: Download Prerequisites

RSE has been compiled against the Europa (Eclipse 3.3) milestones.

*   [Eclipse 3.3 Platform Downloads](http://download.eclipse.org/eclipse/downloads/) \- use the "SDK" or the "Platform" bundle, just as you like
*   **Optional** \- Remote CDT Launcher only:
    *   Get CDT from the Europa Staging Update Site
*   **Optional** \- Experimental Discovery only:
    *   Get EMF from the Europa Staging Update Site
*   **Optional** \- Serial Terminal only
    *   Get Sun Javacomm according to the instructions in the serial terminal readme.txt

The minimum installation is to get Eclipse-platform-3.3Mx, and then install RSE-runtime-core from the update site. To do something useful, you'll also need your choice of either FTP, or SSH, or the examples (one or more of them)

### Step 2: Install TM / RSE

*   The [TM download page](http://download.eclipse.org/dsdp/tm/downloads/) has all packages, mirrored to at least 18 mirrors.
    *   The simplest is to download and install the SDK, it has all components to test
    *   If you dont want programmer examples or ISV docs, you can also pick the runtime packages
    *   For testing dstore, you'll need one of the rseserver-* packages.
*   If you prefer installing from the update site, please use [http://download.eclipse.org/dsdp/tm/testUpdates](http://download.eclipse.org/dsdp/tm/testUpdates) (at least 15 mirrors)
    *   You know how to do it: Help > Software updates > Find and Install > New Remote Site
    *   Pick the SDK, or the runtime just as you like
    *   When testing dstore: the Dstore server packages (rseserver-*) must be obtained from the TM download page.

### Step 3: Record your Test Environment

As the first step after installation, please record your exact test environment, to ensure we get good bugzilla reports:

*   In Eclipse, choose **Help > About Eclipse SDK**, press **Configuration Details**
*   **Copy & Paste the configuration into an empty text file**, we might need such exact information later when working on bug reports.
*   The most interesting lines in this file are (line numbers and contents vary on your platform, of course):
    *   Line 7: eclipse.buildId=M20060629-1905
    *   Line 47: java.runtime.version=1.5.0_07-b03
    *   Line 77: os.name=Windows XP
    *   Line 78: os.version=5.1

On the target side, the following commands are helpful to find out exact system versions (you dont need to issue all of these commands right now):

*   **cat /etc/*-release**  
    Red Hat Enterprise Linux WS release 4 (Nahant Update 3)
*   **uname -a**  
    Linux parser.takefive.co.at 2.6.9-34.EL #1 Fri Feb 24 16:44:51 EST 2006 i686 athlon i386 GNU/Linux
*   **java -version**  
    Java HotSpot(TM) Client VM (build 1.4.2_12-b03, mixed mode)

If your test setup changed, please update your entry in the [RSE 1.0 Testing round 2](./RSE_1.0_Testing_round_2 "RSE 1.0 Testing round 2") table, and update your bugzilla bug entry template (see below). We'd like to ensure that we get good coverage by asking people to use many different OS and JVM flavors.

### Step 4: Prepare for Bug Reports

*   Click [this link to check](https://bugs.eclipse.org/bugs/enter_bug.cgi?product=Target%20Management) if you are already logged in to Bugzilla.  
    If you get a bug entry form, you are logged in already; you can proceed with the next step. Otherwise, Log in or create an account.
*   **Click [this link to get a sample bug entry template](https://bugs.eclipse.org/bugs/enter_bug.cgi?product=Target%20Management&version=2.0&component=RSE&rep_platform=PC&op_sys=Windows%20XP&priority=P3&bug_severity=normal&bug_status=NEW&assigned_to=dsdp.tm.rse-inbox%40eclipse.org&qa_contact=martin.oberhuber%40windriver.com&cc=&bug_file_loc=http%3A%2F%2F&short_desc=&comment=%0D%0A-----------Enter%20bugs%20above%20this%20line-----------%0D%0ARSE%202.0M4%20Testing%0D%0Ainstallation%20%3A%20eclipse-platform-3.2.1%20%28M20060921-0945%29%2C%20cdt-3.1.1%2C%20emf-2.1.1%0D%0ARSE%20install%20%20%3A%20update-site%20RSE-runtime-all%20%2B%20discovery%20%2B%20efs%0D%0Ajava.runtime%20%3A%20Sun%201.5.0_08-b03%0D%0Aos.name%3A%20%20%20%20%20%3A%20Windows%20XP%205.1%2C%20Service%20Pack%202%0D%0A------------------------------------------------%0D%0Asystemtype%20%20%20%3A%20Unix-ssh%20%28dstore-processes%29%0D%0Atargetos%20%20%20%20%20%3A%20SUSE%20LINUX%2010.1%20%28i586%29%0D%0Atargetuname%20%20%3A%20Linux%20osgiliath%202.6.16.21-0.21-default%20%231%20Tue%20Aug%2029%2016%3A42%3A05%20UTC%202006%20i686%20athlon%20i386%20GNU%2FLinux%0D%0Atargetvm%20%20%20%20%20%3A%20Sun%20Java%20HotSpot%28TM%29%20Client%20VM%20%28build%201.5.0_07-b03%2C%20mixed%20mode%2C%20sharing%29%0D%0A------------------------------------------------%0D%0A&commentprivacy=0&keywords=&dependson=&blocked=&maketemplate=Remember%20values%20as%20bookmarkable%20template&form_name=enter_bug)**
*   **Edit** the "Platform", "OS" and "Description" fields to match **YOUR** setup. The goal is to get YOUR personal customized bug entry template that you'll use to make your reports easily, while conveying all information about your system. When done, press the **Remember values as bookmarkable entry** button.
*   In Firefox or Internet Explorer, I like to move this bookmark into the Toolbar; that way I can file a new proper bug report with a single button click.

You are ready to go now! - Check the [RSE 2.0 Known Issues and Workarounds](./RSE_2.0_Known_Issues_and_Workarounds "RSE 2.0 Known Issues and Workarounds") page once more to ensure you don't duplicate the most obvious known issues. Then, go ahead and file all bugs, glitches or enhancement requests or suggestions in Bugzilla right away. Thanks to your bookmark this will be really fast and easy to do. You may also record bugs against a bad website, unclear testing instructions, bad documentation etc -- file bugs as bugs can ;-)

Also, dont lose time searching for bugs - just file them, it's quick and easy to do.

### Step 5: Basic Sanity Check

All testers, regardless of their main test signup, are encouraged to do a 30-minute sanity check of the most common actions in RSE. **Please do explore RSE on your own a little bit, with your own assigned configuration - the steps below are just for example what _could_ be done.** This is the "exploratory" part of testing: it will help us understand how much the online docs and getting started helps, and thus improve the out-of-box experience. **Dont invest more than 30 minutes for this sanity check. Its more important to cover the coordinated test matrix right now.** As an example only, here is the sanity check I'm doing:

*   Download and extract into H:\\RSETest\\2.0M4
    *   eclipse-platform-3.3M4, org.eclipse.cdt-sdk-4.0M4, RSE-runtime-core, RSE-runtime-dstore, RSE-runtime-remotecdt
*   Dbl click eclipse, workspace = H:\\RSETest\\2.0M4\\workspace
*   Open Perspective Remote System Explorer
*   New Connection, Linux, Next; Dstore, Launcher params, Server-Launcher=Rexec; Finish
*   Expand My Home/RSETest/2.0M4 ; New Filter, Next, name="Test2.0M4"
*   Select the new filter, Show in table, create new folder "test"
*   Select the test folder, Rightclick > launch shell
*   In shell, enter: cd ../te<ctrl+space>
*   enter: ps -> check icons for output
*   _The following works with dstore only:_
    *   enter: cat
    *   Open Processes > My Processes, find "cat" process and kill it
    *   From Windows Explorer, Drag&Drop a ZIP archive into the remote test folder
    *   In RSE tree, browse into the ZIP archive; dbl click on a text file
    *   Copy & paste the text file out of the archive
    *   Select the folder above the text file, right-click > Search
*   With the connections still connected, quit & restart RSE (should reconnect)

### Step 6: Do your special test assignment

Detailed instructions are currently being written. Please check back here later, and have fun exploring RSE on your own in the meantime.

See the [TM Manual Test Plan](./TM_Manual_Test_Plan "TM Manual Test Plan")

Final Comments
--------------

Please edit this page, and leave your comments here. It will help us understand who's actually read up to here and understands how to edit a Wiki :-) - and it will help us improve future testing efforts.

*   Did you like the format of this test?
*   Did you have any difficulties?
*   What could we improve?

### Comments for testing round 1

See [RSE 1.0 Test Instructions#Comments for testing round 1](./RSE_1.0_Test_Instructions#Comments_for_testing_round_1 "RSE 1.0 Test Instructions")

### Comments


(Migrated from [https://wiki.eclipse.org//TM_2.0_Test_Instructions](https://wiki.eclipse.org//TM_2.0_Test_Instructions))