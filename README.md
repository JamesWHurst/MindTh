VisuTest
========

VisuTest is a tool intended for the purpose of adding some semantic intelligence to your unit-tests.

The first use, at this point, is to enable fully-automated unit-tests for UX features. For example, test that when the user selects X, the UI shows a text-field that says Y. This tool would not require any special instrumentation of the target code. The UI is run, actually shows on the screen and a snapshot take (automatically), and Y is checked for. This tests whether Y is shown clearly and not occluded by some other widget nor clipped by the edges, and that the font in use does show the intended text.

Another intended feature for unit-testing, is semantic message checking. Ie, in some cases you may not care about the exact wording and punctuation of your error-message, but you do want you confirm that one is shown to the user and that it is grammatically and semantically correct. The only way to do this is for your test-system to understand the intent of the message -- in the same sense as you'd expect a human user to understand what to look for. Hence the A.I. nature of this test.

For example: You want your UI to show a message that says "There are 2 errors found within your file." 

So you create a unit-test that checks for this text. Then a dev changes it to say "two errors", or perhaps "I see two mistakes within the specification file that you submitted."

Doing a mechanical text-pattern process is only going to take you so far.

Thus: VisuTest


Note: "VisuTest" is a contraction of "Visual"-Test.


James W. Hurst
