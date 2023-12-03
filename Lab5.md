## PART 1

**1. student post:**

"Hi, I'm confused that why there were 2 failures when I run my script. It shows IndexOutOfBoundException. 
I guess it probably because my input was to large or I didn't throw the indexoutofbound exception? I put a screenshot of symptom here."
![image](https://github.com/graceswang/cse15l-lab-reports/assets/135576306/49955be8-2fb1-4ac4-b57a-5a1e19cbf72b)

symptom:
![image](https://github.com/graceswang/cse15l-lab-reports/assets/135576306/6ad1a02b-ceca-43b5-94b5-75cd86fe7f23)

**2. response from a TA:**
"Hi! It looks like your index was out of the range of the list. When you make the statement, you want to make sure your indexs are valid, 
which means inside the bound. As you can see from the explanation after the IndexOutOfBoundException on your screenshot,the first failure for example, 
it was saying 'Index 2 out of bounds or length 2'. When you locate the failure with the hint there 'at ListExamples.merge(ListExamples.java:28), that means 
you could check line 28 in Listexamples.java. Please try to check line28 in Listexamples.java to see whether your successfully limit your index inside the bound
and feel free to comment in this post if you have more problems."

**3.**
![image](https://github.com/graceswang/cse15l-lab-reports/assets/135576306/50b1122c-f1b5-45aa-aafb-c932f5afe3a8)
![image](https://github.com/graceswang/cse15l-lab-reports/assets/135576306/4526f49b-e716-433c-8e7c-be1820f62b86)
![image](https://github.com/graceswang/cse15l-lab-reports/assets/135576306/35e62f71-c9d2-4f58-aae0-a6d4a18b2f67)
![image](https://github.com/graceswang/cse15l-lab-reports/assets/135576306/12f46e46-8fa2-4f27-ac95-0728b53c4100)

Explantion:

I did ```vim```+ <space> + ```ListExamples.java```+ <enter> to try to find the error in ListExamples.java line 28 and edit it. 
I found that in line 28, the previous code was ```while(index1 <= list1.size() && index2 <= list2.size()) { ```, it would be a bug since when index1 = list1.size, 
it would be out of the bound, and same thing would happen to list2 and index2. For example, if we have a list1 {2,4,6} then list1.size()=3, and index1 starts from 0,
will be 0,1,2,3 continiously. However, list[0] is 2, list[1] is 4, list[2] is 6, but list[3] is out of bound, hence it will throw a indexoutofbound exception. 
To fix this error, we should correct the code as ```while(index1 < list1.size() && index2 < list2.size()) { ```, deleting two equals signs will make the index1 and index2
inside the bound of list1 and list2. 

**4.**

**The file & directory structure needed:**

```cd``` + <space> + ```lab-report-5``` + <enter>
change directory in to lab-report-5 first, where have the file and directory we needed, by ```ls``` + <enter>, list everything inside lab-report-5, and we can see 
there are ListExamples.java, ListExamplesTest.java, lib, and test.sh. 

![image](https://github.com/graceswang/cse15l-lab-reports/assets/135576306/12dde1b3-8693-4a42-b044-23525b7c0841)

**The contents of each file before fixing the bug:**
LIstExamples.java

![image](https://github.com/graceswang/cse15l-lab-reports/assets/135576306/b1f0213d-ea4c-4677-9edf-7c0a2ca06ae3)
![image](https://github.com/graceswang/cse15l-lab-reports/assets/135576306/14d933f2-9f38-4e48-8b8e-f7e535f20c11)

LIstExamplesTest.java
![image](https://github.com/graceswang/cse15l-lab-reports/assets/135576306/b5614183-93b1-47f1-9087-c41a91d88400)

test.sh
![image](https://github.com/graceswang/cse15l-lab-reports/assets/135576306/2e806b9a-06ef-4d6a-90ec-132e193029be)

**The full command line (or lines) you ran to trigger the bug**

I ran ```bash``` + <space> + ```test.sh``` + <enter> to trigger the bug, it is bascially run the test.sh scrpit, every command was wirttien in the script will be run
![image](https://github.com/graceswang/cse15l-lab-reports/assets/135576306/3c71d284-81a1-4aa5-89fd-58d4880781eb)

**A description of what to edit to fix the bug** 

As the explanation in **3.**.


## PART 2 - Reflection

I didn't know how to change directory, see what insde a file without opening before. After this class, I know that we could use ```cd``` to change directory and ```cat``` to print out the context inside the file. We could also use ```pwd``` to check where we are right now(currect directory). I found it was really helpful and fun, because when I was taking cse8a and cse11, I worked a lot with the autograder
when I submitted my PA each time, but I would never know how to build a autograder without the study of cse15l. I also wanted to thank the help from all tutors and TAs especially Will, Yash, and Nikhil, and also my lab section tutor but sorry I forgot her name. 

