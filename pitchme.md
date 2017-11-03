## Microservices

---
#####Overview:<br>
-What are microservices?<br>
-Why are they so good?<br>

---
##What Is TDD?

###More than "writing tests first"...<br>
TDD is continual testing, coding, design and documentation.
+++
####In a nutshell:
  1. Write a test.
  2. Run all tests. The test should fail.
  3. Write the minimum amount of code to pass the test.
  4. Run all tests. They should pass.
  5. Refactor your code - optional.
  
+++
![Image-Absolute](https://s3.amazonaws.com/media-p.slid.es/uploads/jlopezmo/images/587930/tdd-circle-of-life.png)
+++
###Uncle Bob's Three Laws of TDD:<br>
1. You can't write any production code until you have first written a failing unit test.<br>
2. You can't write more of a unit test than is sufficient to fail, and not compiling is failing.<br>
3. You can't write more production code than is sufficient to pass the currently failing unit test<br>
[Credit to Robert C. Martin](http://programmer.97things.oreilly.com/wiki/index.php/Uncle_Bob)
---
###Why Do We Use TDD?
1. Code is written to specification.

2. Tests serve as documentation for the intention behind the subject.

3. We can push up with confidence.
+++
###Why Do We Use TDD?
4. There is less duplication.

5. It promotes refactoring and more maintainable code.

6. Incremental development increases code coverage.

7. After the fact testing: less rigorous and not tied to functionality
