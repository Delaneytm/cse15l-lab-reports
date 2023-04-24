# Lab Report 2
## Part 1
My code was adapted from the number server code in lab:
![Image](stringserver.png)

Running examples, We can see the outcome of adding messages
![Image](hi.png)
![Image](howareyou.png)
![Image](midterm.png)
My code has the method handleRequest within the handler class. The argument for this method is a url. In order to store all the inputs given by the user, we have to start with an empty string which I called `result`. All of my examples have `/add-message` so we ignore the if statement and move to the else statement. We then split the url into two parts at the `=` if `/add-message` is in the url. Everything on the right hand side of the `=` is the message and is added to `result` along with `\n` which is the code for starting a new line. We then return `result` which prints out every phrase in the `result` on a new line.
## Part 2
The following code has a bug
```
static double averageWithoutLowest(double[] arr) {
   if(arr.length < 2) { return 0.0; }
    double lowest = arr[0];
    for(double num: arr) {
      if(num < lowest) { lowest = num; }
    }
    double sum = 0;
    for(double num: arr) {
      if(num != lowest) { sum += num; }
    }
    return sum / (arr.length - 1);
  }
  ```
Next, create tests that have a correct output and a failure-inducing input
```
@Test
    public void averageWithoutLowestTest(){
        double [] arr= {0,0,4,5};
        assertEquals(4.5, ArrayExamples.averageWithoutLowest(arr), 0.0001);
      }
 @Test
    public void averageWithoutLowestTest2(){
      double [] arr2= {3,4,4};
      assertEquals(4.0, ArrayExamples.averageWithoutLowest(arr2), 0.0001);
    }
```
When we run these tests we get the following output:
![Image](result.png)
The symptom of this bug is that the result is the wrong answer. In order to fix this we need to account for multiple minimum values.

The following code has gotten rid of the bug:
```

```

Briefly describe why the fix addresses the issue.

## Part 3
I feel I have learned a lot in the last 2 labs. I did not know that I could create a server with the limited knowledge I have. I did struggle a bit to create the StringServer and have it work they way I wanted to. I still don't fully understand it, but I got it to run. I thought it was cool to use the remote server and be able to access other people's server.
