**Step 4. Log into ieng6**
<img width="989" alt="Screenshot 2023-11-19 at 11 11 04" src="https://github.com/graceswang/cse15l-lab-reports/assets/135576306/56b9c514-823c-47f8-acad-01bd3a74850f">

Keys pressed: ``ssh``,``<space>``, ``cs15lfa23bo@ieng6.ucsd.edu``, ``<enter>``.



**Step 5. Clone your fork of the repository from your Github account (using the SSH URL)**
<img width="958" alt="Screenshot 2023-11-19 at 11 14 07" src="https://github.com/graceswang/cse15l-lab-reports/assets/135576306/8d14a02d-4b77-4e4d-bd8d-d9aad0a9f036">

Keys pressed: ``git``,``<space>``, ``clone``, ``<space>``, ``<command> - v ``(to paste the ssh url under github code button we copied before, can use ``<command>c`` to copy), ``<enter>``.



**Step 6. Run the tests, demonstrating that they fail**
<img width="741" alt="Screenshot 2023-11-19 at 11 16 24" src="https://github.com/graceswang/cse15l-lab-reports/assets/135576306/096818b9-bac1-4c2e-bc57-90dd75886c45">

Keys pressed: ``bash``, ``<sapce>``, ``test.sh``,``<enter>``. 
testMerge2 failed because test timed out after 500 milliseconds.



**Step 7. Edit the code file ListExamples.java to fix the failing test (as a reminder, the error in the code is just that index1 is used instead of index2 in the final loop in merge)**

Keys pressed: ``vim``,``<space>``, ``ListExamples.java``,  ``<enter>``(to open the ListExamples.java at terminal).
<img width="911" alt="Screenshot 2023-11-19 at 11 20 31" src="https://github.com/graceswang/cse15l-lab-reports/assets/135576306/ee94655c-4604-4280-b72d-82e60635b06b">

Keys pressed:`` <down><down><down><down><down><down><down><down><down><down><down><down><down><down><down><down><down>``(intotoal 17),``<i>``, ``<right>``, ``<delete>``,``2`` (change "1" into "2")
<img width="959" alt="Screenshot 2023-11-19 at 11 35 59" src="https://github.com/graceswang/cse15l-lab-reports/assets/135576306/6e6accc9-97a8-47c6-a141-fbbc3cab5fee">

Keys pressed: ``<esc>``, ``:wq`` , ``<enter>``
<img width="926" alt="Screenshot 2023-11-19 at 11 36 24" src="https://github.com/graceswang/cse15l-lab-reports/assets/135576306/64b6c396-10ac-404b-b81e-93f1a98f97a6">
<img width="779" alt="Screenshot 2023-12-01 at 13 12 24" src="https://github.com/graceswang/cse15l-lab-reports/assets/135576306/36aa903d-b255-4f84-9eeb-a9c258c692ae">



**Step 8. Run the tests, demonstrating that they now succeed**

Keys pressed: ``bash``, ``<sapce>``, ``test.sh``,``<enter>``
<img width="911" alt="Screenshot 2023-11-19 at 11 36 56" src="https://github.com/graceswang/cse15l-lab-reports/assets/135576306/e97d454b-3c2e-4a13-bde2-0cc02fc8812b">

Now, since we fixed the test in ListExamples.java, two tests are all passed. 



**Step 9. Commit and push the resulting change to your Github account**
Keys pressed: ``git``, ``<space>``,``add``, ``<enter>``, ``git``,``<space>``,``commit``,``<space>``, ``-m``, ``fix test(testMerge2) by chaging 1 to 2``, ``<enter>``
![image](https://github.com/graceswang/cse15l-lab-reports/assets/135576306/9aca61cf-8b6b-4818-9c7f-0d4395a08fcf)

Keys pressed: ``git``,``<space>``, ``push``, ``<enter>``
![image](https://github.com/graceswang/cse15l-lab-reports/assets/135576306/b3fd29b0-509b-4e82-925b-b68b36f6cf76)

