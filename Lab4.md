Step 4. Log into ieng6
<img width="989" alt="Screenshot 2023-11-19 at 11 11 04" src="https://github.com/graceswang/cse15l-lab-reports/assets/135576306/56b9c514-823c-47f8-acad-01bd3a74850f">
Keys pressed: ``ssh cs15lfa23bo@ieng6.ucsd.edu`` command, then ``<enter>``.

Step 5. Clone your fork of the repository from your Github account (using the SSH URL)
<img width="958" alt="Screenshot 2023-11-19 at 11 14 07" src="https://github.com/graceswang/cse15l-lab-reports/assets/135576306/8d14a02d-4b77-4e4d-bd8d-d9aad0a9f036">
Keys pressed: ``git clone git@github.com:graceswang/lab7.git`` command, then <enter>.

Step 6. Run the tests, demonstrating that they fail
<img width="741" alt="Screenshot 2023-11-19 at 11 16 24" src="https://github.com/graceswang/cse15l-lab-reports/assets/135576306/096818b9-bac1-4c2e-bc57-90dd75886c45">
Keys pressed: ``bash test.sh`` command, then <enter>. 
testMerge2 failed because test timed out after 500 milliseconds.

Step 7. Edit the code file ListExamples.java to fix the failing test (as a reminder, the error in the code is just that index1 is used instead of index2 in the final loop in merge)
Keys pressed: ``vim ListExamples.java`` command, then <enter>,to open the ListExamples.java at terminal.
<img width="911" alt="Screenshot 2023-11-19 at 11 20 31" src="https://github.com/graceswang/cse15l-lab-reports/assets/135576306/ee94655c-4604-4280-b72d-82e60635b06b">
Keys pressed: <down>*17, <right>, <delete>,change "1" into "2"
<img width="959" alt="Screenshot 2023-11-19 at 11 35 59" src="https://github.com/graceswang/cse15l-lab-reports/assets/135576306/6e6accc9-97a8-47c6-a141-fbbc3cab5fee">
Keys pressed: <esc>， ``:wq`` command, <enter>
<img width="926" alt="Screenshot 2023-11-19 at 11 36 24" src="https://github.com/graceswang/cse15l-lab-reports/assets/135576306/64b6c396-10ac-404b-b81e-93f1a98f97a6">

Step 8. Run the tests, demonstrating that they now succeed
Keys pressed: ``bash test.sh`` command
<img width="911" alt="Screenshot 2023-11-19 at 11 36 56" src="https://github.com/graceswang/cse15l-lab-reports/assets/135576306/e97d454b-3c2e-4a13-bde2-0cc02fc8812b">


Step 9. Commit and push the resulting change to your Github account
