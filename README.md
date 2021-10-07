# Test repository for Github Classroom

Here are some sample instructions for downloading the assignment and submitting.

## Assignment Workflow

Make sure that you create a Github account and have linked it to the classroom. Also make sure that you have `git` installed on your local machine.

1. You will be sent an invitation link for each assignment. Accepting this invitation will create a private remote repository with:
  * the assignment overview and questions (usually `assignment*.pdf`);
  * a solution template (`solution.jmd`);
  * files needed to ensure that you have a correct environment for compilation (`Project.toml`).
  * other repository files (such as `.gitignore` and `README.md`).
2. Create a local directory for the assignment. You may want to create a general directory for this class and create a new subdirectory for each assignment.
3. `git clone` the remote repository into your assignment subdirectory.
4. Commit your work as frequently as you'd like using `git commit`. The more frequently you commit, the better the history of your progress on the assignment. Add short but informative commit messages using `git commit -m <message>`. Best practice would be to commit every time you add something meaningful, such as getting a block of code to work or adding the answer to a question. If you fix a bug, commit it.
5. Push your local work to your remote repository using `git push`. You don't have to push after every commit, but you should definitely push when you'd like feedback or when you're ready to submit. **Note**: 
6. If you'd like feedback on an assignment, you can create an issue or a pull request for further commenting or Slack discussions.
7. Tests will be run when you push which will make sure that your code runs and produces meaningful output. Don't worry if you haven't finished the coding part of your assignment and it fails. The Github tests are identical to those that Gradescope will run when you submit, but are not used in grading, they're purely for your feedback and to make sure that everything will go smoothly when you upload to Gradescope. Make sure that you name models and/or variables as specified in the assignment overview (when specified; when not specified, names won't be used). 
6. When you're ready to submit, make sure that you've pushed your latest code. Go to Gradescope and submit by selecting Github as the source and choosing your assignment repository. Gradescope will automatically run and compile your `solution.jmd` file into a `.pdf`, which is what the TA will look at. Gradescope will also make sure that your code runs and produces meaningful output using the same tests that were applied when you pushed your code to Github.
7. You'll be able to see the rubric and feedback on Gradescope.

## Checking Your Code Locally

Even though Github will automatically run tests on your code, it won't build a PDF for you to look at. If you'd like to see how your solution will appear, you'll need to convert your solution from `.jmd` locally. There are a few options.

* By default, the template is set up to convert your `.jmd` file to `.pdf` using Pandoc and LaTeX. To use this workflow locally, you need installations of [Pandoc](https://pandoc.org/installing.html) to process the Markdown and some type of LaTeX installation.
* You can also generate a more "raw" PDF without Pandoc, though LaTeX will still be required. To do this, change the `doctype: pandoc2pdf` line in the header to `doctype: md2pdf`.
* Another option is to generate an HTML file, rather than a PDF. This is the easiest solution, as it will not require a LaTeX installation. To do this, change the `doctype: pandoc2pdf` line to `doctype: md2html`.

If you do change the doctype line in the header, make sure you change it back to `doctype: pandoc2pdf` before you submit your solution to Gradescope.