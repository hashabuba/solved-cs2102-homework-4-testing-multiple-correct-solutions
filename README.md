Download Link: https://assignmentchef.com/product/solved-cs2102-homework-4-testing-multiple-correct-solutions
<br>
<h1></h1>

<h2>Assignment Goals</h2>

To become familiar with the heap data structure

To be able to design test cases for methods that have more than one correct solution

<h2>Reminders</h2>

<strong> Please use the default package in your Java project.</strong> There will be a penalty for using a named package.

Please include a Javadoc statement above each method and class. There will be a penalty for forgetting your Javadoc statements.

In your test cases, please use descriptive names for your test case methods and/or comments above each test case explaining what the method tests. This will help the TAs and SAs in grading. There will be a penalty for forgetting this step.

<h2>Files</h2>

Here are the starter files referenced in the assignment description. They contain multiple classes and interfaces that you should parse out into separate files in your program:

<a href="https://canvas.wpi.edu/courses/16466/files/2217219/download?wrap=1"><strong>IBinTree.</strong></a><a href="https://canvas.wpi.edu/courses/16466/files/2217219/download?wrap=1"><strong>j</strong></a><a href="https://canvas.wpi.edu/courses/16466/files/2217219/download?wrap=1"><strong>ava</strong></a> <strong>    </strong><a href="https://canvas.wpi.edu/courses/16466/files/2217219/download?download_frd=1"><strong> </strong></a><a href="https://canvas.wpi.edu/courses/16466/files/2217219/download?download_frd=1"><strong>(https://canvas.wpi.edu/courses/16466/files/2217219/download?download_frd=1)</strong></a>

<a href="https://canvas.wpi.edu/courses/16466/files/2217218/download?wrap=1"><strong>IHeap.</strong></a><a href="https://canvas.wpi.edu/courses/16466/files/2217218/download?wrap=1"><strong>j</strong></a><a href="https://canvas.wpi.edu/courses/16466/files/2217218/download?wrap=1"><strong>ava</strong></a> <strong>    </strong><a href="https://canvas.wpi.edu/courses/16466/files/2217218/download?download_frd=1"><strong> </strong></a><a href="https://canvas.wpi.edu/courses/16466/files/2217218/download?download_frd=1"><strong>(https://canvas.wpi.edu/courses/16466/files/2217218/download?download_frd=1)</strong></a>

<a href="https://canvas.wpi.edu/courses/16466/files/2217217/download?wrap=1"><strong>TestHeap.</strong></a><a href="https://canvas.wpi.edu/courses/16466/files/2217217/download?wrap=1"><strong>j</strong></a><a href="https://canvas.wpi.edu/courses/16466/files/2217217/download?wrap=1"><strong>ava</strong></a> <strong>    </strong><a href="https://canvas.wpi.edu/courses/16466/files/2217217/download?download_frd=1"><strong> </strong></a><a href="https://canvas.wpi.edu/courses/16466/files/2217217/download?download_frd=1"><strong>(https://canvas.wpi.edu/courses/16466/files/2217217/download?download_frd=1)</strong></a>

<h1>Problem Statement</h1>

Our discussion of data structures has introduced a couple of methods that could return one of several answers: remElt() on BSTs has this property, as do the addElt() and remMinElt() functions on heaps.

Writing test cases for such methods clearly requires more than writing a specific, concrete answer (as you are used to doing). Instead of writing a concrete answer, you have to write a method that checks whether your answer meets the requirements of a correct answer and run that method within your test case. In other words, rather than checking whether you got <em>the</em> correct answer, you have to check whether you got <em>a</em> correct answer. This assignment is teaching you how to write tests for situations when you need “<em>a</em> correct answer”.

Your job here is to write two methods, the first of which is addEltTester() . addEltTester() takes a heap, an integer, and a binary tree (in that order) and returns true if the binary tree is a valid result of adding the given integer to the first Heap. In other words, you want to fill in

What should addEltTester() and remMinEltTester() actually do?

Each of these methods checks whether the binary tree is a valid result of performing addElt() or remMinElt() (respectively) on the original heap. A valid result is defined by the following conditions:

The binary tree returned must satisfy the definition of a heap (smallest element on top, left and right subtrees both heaps).

addElt() must retain all elements that were in the original heap, while adding only the new element

one time.

remMinElt() must retain all elements that were in the original heap, other than removing one

occurrence of the smallest element.

You may assume that running addElt() or remMinElt() on a heap does not modify the heap (this lets you reuse the same heap data in multiple test cases).

For this assignment, heaps may have duplicate elements.

<h2>Logistics</h2>

Put both of these methods in a new class called HeapChecker .

You do not need to implement addElt() or remMinElt() . We are giving them to you, along with the other <a href="https://canvas.wpi.edu/courses/16466/files/2217219/download?download_frd=1">heap operations. Here are both</a> <a href="https://canvas.wpi.edu/courses/16466/files/2217219/download?download_frd=1"><strong>a binar</strong></a><a href="https://canvas.wpi.edu/courses/16466/files/2217219/download?download_frd=1"><strong>y</strong></a><a href="https://canvas.wpi.edu/courses/16466/files/2217219/download?download_frd=1"><strong> tree implementation</strong></a> <a href="https://canvas.wpi.edu/courses/16466/files/2217219/download?download_frd=1"><strong> </strong></a>

<a href="https://canvas.wpi.edu/courses/16466/files/2217218/download?wrap=1"><strong>(https://canvas.wpi.edu/courses/16466/files/2217219/download?download_frd=1) </strong></a><a href="https://canvas.wpi.edu/courses/16466/files/2217218/download?wrap=1"> </a><a href="https://canvas.wpi.edu/courses/16466/files/2217218/download?wrap=1">and</a> <a href="https://canvas.wpi.edu/courses/16466/files/2217218/download?wrap=1"><strong>an initial correct </strong></a><a href="https://canvas.wpi.edu/courses/16466/files/2217218/download?download_frd=1"><strong>heap implementation</strong></a> <a href="https://canvas.wpi.edu/courses/16466/files/2217218/download?download_frd=1"><strong> </strong></a><a href="https://canvas.wpi.edu/courses/16466/files/2217218/download?download_frd=1"><strong>(https://canvas.wpi.edu/courses/16466/files/2217218/download?</strong></a>

<a href="https://canvas.wpi.edu/courses/16466/files/2217218/download?download_frd=1"><strong>download_frd=1) </strong></a><a href="https://canvas.wpi.edu/courses/16466/files/2217218/download?download_frd=1"> </a><a href="https://canvas.wpi.edu/courses/16466/files/2217218/download?download_frd=1">to use in writing your tester. You are getting both files because we build</a> heaps as subclasses of binary trees.

If you need additional methods in Heap or BinTree , modify the classes in these files as needed with your additional methods. <strong>Do not change</strong> the names of the classes, any of the existing methods, or make your own subclasses (that will break the auto-tester). Just edit these classes and/or interfaces by adding your own additional methods.

<strong>DO NOT call addElt() in the method body of addEltTester() or remMinElt() in the method body of remMinEltTester()!!!</strong> Doing so undermines the purpose of this assignment.

<strong>DO NOT use type-checking</strong>, i.e. do not use any of the following:

instanceof

casting getClass() static

<strong>BIG HINT:</strong> Please consider modifying the interfaces we give you.

<h2>Testing the Testers</h2>

Put your test cases in an Examples class, as usual. Your test cases need only to use addEltTester() and remMinEltTester() . They may use addElt() / remMinElt() if you wish (as shown in test1 above). You should have at least 6 tests for each method.

<strong>Make sure your test methods use highly descriptive names and/or comments.</strong> This will help the grader determine which situation you’re testing.

What makes for good tests?

Good tests will capture various ways that addElt() and remMinElt() might fail. Here’s another way to think about it. If you have a good addEltTester , then your tests will all pass if you use a correct implementation of addElt() . If you use a broken implementation of addElt() , then ideally one of your test cases would fail (because the addElt() used would produce the wrong answer).

Put differently, assume you wanted to add 8 to the following heap:

(which is wrong because it isn’t a heap [with min elts on top]). Then your addEltTester would return false, because the produced heap is not a valid answer when adding 8 to the original heap. A good set of test cases, then, will cover different elements to add to different configurations of heaps, looking for ways in which addElt / remMinElt might go wrong.

<h2>Checking bad implementations</h2>

This part is optional but will give you extra assurance that your testers have been written correctly.

The tests in your final Examples class should just be written using DataHeap , not these broken implementations. The broken implementations are just to help you in checking your work. Either delete or comment out any tests that used the TestHeap classes before you submit.


