VisuTest
========

VisuTest is a tool intended for the purpose of adding some semantic intelligence to your unit-tests.


The first use, at this point, is to enable fully-automated unit-tests for UX features. For example, test that when the user selects X, the UI shows a text-field that says Y. This tool would not require any special instrumentation of the target code. The UI is run, actually shows on the screen and a snapshot taken (automatically), and the image is then analyzed for it's content. This can test, for example, whether Y is shown clearly and not occluded by some other widget nor clipped by the edges, and that the font in use does show the intended text.


Another intended feature for unit-testing, is semantic message checking. Ie, in some cases you may not care about the exact wording and punctuation of your error-message, but you do want you confirm that one is shown to the user and that it is grammatically and semantically correct. The only way to do this is for your test-system to understand the intent of the message -- in the same sense as you'd expect a human user to understand what to look for. Hence the A.I. nature of this test.


For example: You want your UI to show a message that says "There are 2 errors found within your file." 


So you create a unit-test that checks for this text. Then a dev changes it to say "two errors", or perhaps "I see two mistakes within the specification file that you submitted." Perhaps you do not want those unit-tests to fail as a result of this change.


Doing a mechanical text-pattern process is only going to take you so far.


Thus: VisuTest
("VisuTest" is a contraction of "Visual"-Test.)


Usage
-----

The command-line syntax for version .01 is:

`visutest [options]` where options may be

    `-runexe {path}` := Invoke the given executable file, which is expected to be, e.g. a WPF desktop application.
  
    `-runtest {path}` := Run the test-script as denoted by the given file path.
  
    `-runhttp {URL:port}` := Launch a browser pointed to the given URL (Uniform Resource Locator) and port-number.
                           for example: visutest -runhttp http://www.OurSite.com:5001
                           
    `-display {monitor-number}` := Run the test or whatever on the display monitor with the coresponding number
                               (same numbering as with Windows).
                               for example, if you have 2 monitors this can be '-display 0'
                               
  `-step s`  :=  Run the test as distinct steps, stopping at each step for s seconds.
  
  `-dump {path}` := Save the screenshots along with identifying annotations to the file denoted by path.
  
  `-stoponerror` := Stop (exit the testing) upon encountering the first test-failure.
  
  `-version` := Display the current visutest version.
  
  `-help` := Display help-information for the visutest command-line usage.
  




James W. Hurst

blog:  [Blog](http://www.JamesHurst.dev)
