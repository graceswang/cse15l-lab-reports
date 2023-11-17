## Part1

- A failure-inducing input:
```ruby
@Test
public void testReverseInPlace2() {
    int[] input2 = { 3,4 };
    ArrayExamples.reverseInPlace(input2);
    assertArrayEquals(new int[]{ 4,3 }, input2);
}
```
- An input that doesn’t induce a failure：
```ruby
@Test 
public void testReverseInPlace() {
    int[] input1 = { 3 };
    ArrayExamples.reverseInPlace(input1);
    assertArrayEquals(new int[]{ 3 }, input1);
}
```

- Symptom：
![image](https://github.com/graceswang/cse15l-lab-reports/assets/135576306/e3351954-01f6-48d9-86f2-57ed6fc59c27)

- Bug：
  
**code before**
```ruby
static void reverseInPlace(int[] arr) {
    for(int i = 0; i < arr.length; i += 1) {
      arr[i] = arr[arr.length - i - 1];
    }
}
```
**code after**
```ruby
static void reverseInPlace(int[] arr) {
    for(int i = 0; i < arr.length/2; i += 1) {
      int temp = arr[i];
      arr[i] = arr[arr.length - i - 1];
      arr[arr.length - i - 1] = temp;
    }
} 
```
Explanation:

The given method reverseInPlace attempts to reverse the elements of an array arr in place. However, when we iterates through the loop, we will overwirte values that we haven't yet used to swap. Therefore, we will lose data and deal with the same value in the very end. The method before doesn't reverse the array correctly. After we correct the code, we introduce a new variable called temp to temporarily store the original value of arr[i] and we find the element backward and swap with the element from forward, and then we give the variable temp with the original value back to the element backward, which helps us keep the original data. We also need to take care of the stop, since we swap two elements each time, we should stop at the middle point of the array, thus we can successfully reverse the elements of an array in place. 

## Part2
**I chose `grep` command.**

**source:**

``man grep``

``grep --help``

https://www.ibm.com/docs/sk/aix/7.1?topic=g-grep-command

1. "-v", --invert-match, selects non-matching lines, displays all lines not matching the specified pattern.
    - Eg1:
      ```ruby
      $ echo -e "apple\norange\nbanana" > ./technical/fruits.txt
      $ grep -v "orange" ./technical/fruits.txt
      ```
      output:
      ```
      apple
      banana
      ```
      This command searches for lines not containing the string "orange" in the file fruits.txt.
    - Eg2:
      ```ruby
      $ echo -e "apple\napple-orange\norange-apple" > ./technical/fruits_combo.txt
      $ grep -v "apple" ./technical/fruits_combo.txt
      ```
      This command returns no results because there is no line not matching the specified pattern"apple", every line in the file fruits_combo.txt contains the string "apple".

2. "-i", --ignore-case, ignores case distinctions(uppercase or lowercase of letters) in patterns and data.
    - Eg1:
      ```ruby
      $ echo "TARGET" > ./technical/sample2.txt
      $ grep -i "target" ./technical/sample2.txt
      ```
      output:
      ```
      TARGET
      ```
      This command searches for the string "target" in the file sample2.txt without considering the case and returns the match.
    - Eg2:
      ```ruby
      $ echo -e "case\nCASE\ncAsE" > ./technical/sample2.txt
      $ grep -i "case" ./technical/sample2.txt
      ```
      output:
      ```
      case
      CASE
      cAsE
      ```
      This command searches for the string "case" in the file sample2.txt without considering the case and returns all matches.

3. "-f",--file=FILE, takes PATTERNS from FILE, specifies a file containing search patterns.
     - Eg1:
       If I have a patterns file animals_patterns.txt with:
      ```
      dog
      cat
      ```
      And a file animals.txt with:
      ```
      dog
      bird
      cat
      fish
      ```
      Then when we put following code in command line,
      ```ruby
      $ grep -f ./technical/animals_patterns.txt ./technical/animals.txt
      ```
      we will get output
      ```
      dog
      cat
      ```
      This command searches for lines in animals.txt that match any pattern in animals_patterns.txt.
    - Eg2:
      If I have a patterns file words.txt with:
      ```
      apple
      grape
      pineapple
      ```
      And a file document.txt with:
      ```
      I love apple pie.
      Grape is great in juice.
      Banana is not in the list.
      Pineapple pizza is controversial.
      ```
      Then when we put following code in command line,
      ```ruby
      $ grep -f ./technical/words.txt ./technical/document.txt
      ```
      we will get output
      ```
      I love apple pie.
      Grape is great in juice.
      Pineapple pizza is controversial.
      ```
      This command searches for lines in document.txt that match any pattern in patterns.txt.

4. "-n", --line-number, prints line number with output lines, starts with 1.
   Given the file lines.txt that contains:
      ```
      first line
      second line
      third line
      fourth line
      ```
    - Eg1:
      When we put following code in command line,
      ```ruby
      $ grep -n "line" ./technical/lines.txt
      ```
      we will get output
      ```
      1:first line
      2:second line
      3:third line
      4:fourth line
      ```
      This command shows each line from lines.txt that contains the word "line", prefixed by its line number.
    - Eg2:
      When we put following code in command line,
      ```ruby
      $ grep -n "third" ./technical/lines.txt
      ```
      we will get output
      ```
      3:third line
      ```
      This command shows the word "third" appears on the third line.

