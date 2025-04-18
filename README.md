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

## Part 2: Continuing your text-based adventure game

![alt text](https://github.com/CS200-S25/Assignment-4/blob/main/GUI.jpg?raw=true)
Complete your text-based adventure game by updating two aspects: 1) incorporating your hierarchy of classes representing the items that are available in your game into the rest of your game, 2) updating the health points for a player based on damage occured from animals in rooms. 

For 1) your Game class must be updated with the following addition to `parseCommand()` which will require you to create a new method for `drop()` and `eat()`. If a user drops an item from their inventory (by typing the string corresponding to the item) then the item is added to the treasure chest of the current room. If a user eats a food item, then their health should increase.

```
public void parseCommand(String input) {
        
        String[] wordList = input.split("[\s]");
        String verb;
        String noun;
        
        if(wordList.length < 2 || wordList.length > 2) {
            System.out.println("Only 2 word commands allowed!");
        } else {
            verb = wordList[0];
            noun = wordList[1];
            switch (verb) {
                case "take":
                    take(noun); 
                    break;
                case "drop":
                    drop(noun); // THIS IS A NEW ADDITION
                    break;
                case "eat":
                    eat(noun); // THIS IS A NEW ADDITION
                    break;
                case "go":
                    movePlayer(noun);
                    break;
                default:
                    System.out.println(verb + " is not a known verb!");
            }
        }
    }
```

For 2) you must also update your game to reduce a player's health by the damage of the animal when the player enters a room with that animal.

## COLLABORATION
This assignment is an individual assignment. You can discuss this assignment with your peers, TA and instructor. You cannot show code to your peers, you each write your own solutions. You can show code to the TAs and instructor. Additionally, you cannot use generative AI or online resources that are not linked from our course website to complete this assignment.  

## SUBMISSION
Submit the following files to Gradescope for Assignment 1:
* take a picture of your solutions to Part 1 and upload a .png or .jpeg file to Gradescope
* upload your code for the recipe management GUI and all of the files for your game to Gradescope

Note: You can resubmit your assignment as many times as needed until the deadline. Every time you resubmit, make sure you submit *all* of the files for your assignment every time.
