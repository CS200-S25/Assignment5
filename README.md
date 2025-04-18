# Assignment-5

There are three parts for assignment 5:
- [ ] Part 1 - Practice with arrays
- [ ] Part 2 - Practice with Polymorphism
- [ ] Part 3 - Finalizing your text-based adventure game

## Part 1: Practice with arrays
In this exercise, you will revisit Question 1 from the midterm. Start by reviewing your answers to this midterm question and completing the three parts of the midterm in BlueJ. Create a new class in BlueJ called Frequencies. Sections 1.A, 1.B, and 1.C are the same as from the midterm but here you are asked to write them in BlueJ. Section 1.D and 1.E are new extensions to the midterm.

The definition of a frequency is as follows: The frequency of a particular data is the number of times the data value occurs.

1.A. In Frequencies, add an instance method frequencyTable(int[] nums)that returns an array of integers. This method should behave as follows: Assume that the input to the method is an array of positive integers (you should not validate that values are positive, assume they are). You should first determine what is the maximal value in the input array, and then create a new array that contains a spot for every possible value from 0 to the maximal value. The last index in the return array should correspond to the maximal value in the input array. Then, you should update the return array to contain the frequency for each value from the input array. 

1.B. Add an instance method to print the contents of the frequency table. The method header is: public void printFrequencies(int[] nums). You can decide how to print this data, there is no required format for this output.

1.C. Make sure to test your methods by running this main() in the Frequencies class. 

```
public static void main(String[] args){
    Frequencies f1 = new Frequencies();
    int[] arr = {1, 8, 5, 6, 8, 5, 8, 10, 2};
    int[] table = f1.frequencyTable(arr);
    f1.printFrequencies(table);
}
```

1.D. Create a new method public void printHistogram(int[] nums) to print a histogram of the frequency table. A histogram is a chart showing a frequency distribution. The format of your histogram must match the following example:

```
Printing a histogram for 9 values:
1  8  5  6  8  5  8  10  2  
1	|+
2	|+
3	|
4	|
5	|++
6	|+
7	|
8	|+++
9	|
10	|+
```

You can use the character sequence `\t` to add the spacing after each value so that the histogram results are aligned.

1.E.  Update your main method by adding 3 new integer arrays of different sizes and different values to test your program, make sure to pick useful test cases that consider edge cases and print the histogram for each of these arrays.

## Part 2: Practice with Polymorphism
In this exercise, you will write a program to manage a zoo of animals and check whether they are comfortable at the current daily temperature. For this exercise, you are given [the document for the program available here](https://cs.wellesley.edu/~cs200/AnimalDoc/package-summary.html). There are 7 classes that you will need to implement following the specifications in the documentation.

The requirements for this exercise are:
- Your classes must match the exact names and headers provided in the documentation.
- You can add getters, setters, and toString() that are not provided in the documentation if needed. This is not necessary to successfully complete this exercise but you can do this if it is helpful for you.
- You must add a main() in the Zoo class to test your program. The testing must thoroughly test your program and you must submit this main() with your Zoo file submission.

## Part 3: Complete the text-based adventure game
Make sure to test the functionality of your game so that a player can play your game. First, complete these two tasks:
1) Fix any remaining parts of your program to make your game playable through the text-based input.
2) Update any text displayed to the user to make the status of the game more clear and provide helpful feedback.

Then, finalize your game by conducting one full run-through of your game. Copy the output, which should include your user input and the program's output, and paste that into a new document. You will submit a pdf of this document along with your code.

## COLLABORATION
This assignment is an individual assignment. You can discuss this assignment with your peers, TA and instructor. You cannot show code to your peers, you each write your own solutions. You can show code to the TAs and instructor. Additionally, you cannot use generative AI or online resources that are not linked from our course website to complete this assignment.  

## SUBMISSION
Submit the following files to Gradescope for this assignment: Frequencies.java, the 7 classes for the Zoo, all of the classes for your game, and a pdf of a run-through of your game.

Note: You can resubmit your assignment as many times as needed until the deadline. Every time you resubmit, make sure you submit *all* of the files for your assignment every time.
