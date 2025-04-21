START
Basic
Front: 
How to view the build problems and failing tests for a particular project?
What is a "flaky test" in TeamCity terminology?
How to view flaky tests, what information is available there? 
How to check out in which build the test initially failed and when was it fixed?
Back: 
Go to the **Project Home** page and select the **Problems** tab. It shows the tests and build problems as separate tabs, with the ability to filter by **All** or **Failed** tests, **Muted** or **Not muted**, **Investigated** or **Not investigated**.

Flaky test label is based on the following heuristics:
- high flip rate: a **flip** is a change between OK and Failure; **flip rate** is the ratio of such "flips" to the invocation count per agent per build configuration or over a certain time period (7 days by default); if a test constantly fails, it has a flip rate of 0; if it flips each time, it has the flip rate close to 100%;
- if a test flipped in a new build with no changes;
- if the same test was invoked multiple times during the build and had different outcomes (within the same build configuration).

Flaky tests can be viewed on the **Flaky tests** tab of the **Project Home** page. It displays the number of failures, the flip rate and the reasons for qualifying the test as flaky.

If you go to the **Tests** tab of a build and check out the failing test, it might have several tabs, **Current failure**, **First failure** and **Already fixed**. 

The **Already fixed** tab shows the first build where this failed test was successful and which was run after the build with the initial test failure (**after** meaning either on newer changes, or on the same changes but after the failed one, history builds not considered).

The **First failure** tab shows the first failure of this test going back in time (with regards to changes as detected by TeamCity) until the first successful run is found within the same build configuration, skipping the builds where this test wasn't run.

Tests are considered the same when they have the same name. If there are several tests with the same name within the build, TeamCity also counts and considers the order number of the test. All invocations of the same test within a single build count as one.

See: https://www.jetbrains.com/help/teamcity/viewing-tests-and-configuration-problems.html
<!--ID: 1745135900081-->
END
