Gain beginning familiarity with writing front end tests

Objectives

Learning Objectives

After completing this assignment, you should:

* Be familiar with Mocha, Chai, and testing concepts

Performance Objectives

After completing this assignment, you should be able to to effectively use:

* Testing frameworks like Testem

Details

Deliverables:

* A fork of the repo we started in class (https://github.com/tiy-greenville-frontend-2016-feb/5.3-tooter)

Requirements

* Find the class demo repository at https://github.com/tiy-greenville-frontend-2016-feb/5.3-tooter
* Fork and clone the repository

Write the tests described below:

Tasks

I Can Test Things Mode

[ ] Create the file tests/create-test.js
[ ] Add the line var expect = chai.expect; at the top of the test file
[ ] Write a describe block for "create post form"
[ ] Write an empty test in the describe block: it('should trigger a create:post event on the document with the title and body');
[ ] Write the body of the test. It should include:
    * Create an event listener on the document element for the create:post event. The event listener function should have an
      expectation (i.e. expect(...).to...) that expects an object with a title and body. Then the function should call done()
    * Use jQuery to put text in the form inputs (even though they don't exist yet). Hint: Use $('.input-class-name').val("Title")
    * Use jQuery to click the form button (even though it doesn't exist yet).

You should now have a failing test.

[ ] Write the form and inputs into the app/templates/application.hbs
[ ] Write an event listener for the form's submit event in app/scripts/index.js that triggers a create:post event on the
    document element with a parameter that is an object with a title and body that are statically coded (e.g. .trigger('create:post', [{title: "Cool", body: "Cool"}])).

    *** student note: add the event listener for the form's submit event to the PostView, or require index.js in the test when you write it; if you don't, the event listener will not get created and the test will not pass

You should now have a passing test.
