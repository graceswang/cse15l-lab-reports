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



**Step 8. Run the tests, demonstrating that they now succeed**

Keys pressed: ``bash``, ``<sapce>``, ``test.sh``,``<enter>``
<img width="911" alt="Screenshot 2023-11-19 at 11 36 56" src="https://github.com/graceswang/cse15l-lab-reports/assets/135576306/e97d454b-3c2e-4a13-bde2-0cc02fc8812b">

Now, since we fixed the test in ListExamples.java, two tests are all passed. 



**Step 9. Commit and push the resulting change to your Github account**
Keys pressed: ``git``, ``<space>``,``add``, ``<enter>``, ``git``,``<space>``,``commit``,``<space>``, ``-m``, ``fix test(testMerge2) by chaging 1 to 2``, ``<enter>``
<img width="906" alt="Screenshot 2023-11-19 at 13 57 42" src="https://github.com/graceswang/cse15l-lab-reports/assets/135576306/6808c923-888b-4435-ab00-e17a82af99ea">

Keys pressed: ``<i>``,write the commit message
<img width="921" alt="Screenshot 2023-11-19 at 14 03 05" src="https://github.com/graceswang/cse15l-lab-reports/assets/135576306/e58444c0-97ac-4d4c-80ad-7427a967966f">

Keys pressed: ``<esc>``,``:wq``command,``<enter>``
<img width="870" alt="Screenshot 2023-11-19 at 14 04 51" src="https://github.com/graceswang/cse15l-lab-reports/assets/135576306/224f52d7-6785-4410-8f74-2f3773e4d04f">
<img width="920" alt="Screenshot 2023-11-19 at 14 06 08" src="https://github.com/graceswang/cse15l-lab-reports/assets/135576306/fd1eec84-b601-40db-a5b0-c7eb7b43e652">

Keys pressed: ``git``,``<space>``, ``push``, ``<enter>``
<img width="909" alt="Screenshot 2023-11-19 at 14 06 24" src="https://github.com/graceswang/cse15l-lab-reports/assets/135576306/d3e97239-7228-489c-944f-7a008767f840">
