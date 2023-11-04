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
![image](https://github.com/graceswang/cse15l-lab-reports/assets/135576306/12194c66-ec34-4d3a-be56-049b7efbad67)

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
    int[] temp = new int[arr.length];
    for(int i = 0; i < arr.length; i += 1) {
      temp[i] = arr[arr.length - i - 1];
    }
    for (int j = 0; j<temp.length;j++) {
      arr[j] = temp[j];
    }
}
```
