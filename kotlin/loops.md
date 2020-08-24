# Loops
- Practice writing for-loops, while-loops, and forEach statements
- Practice writing a constructor

## Prerequisites
- Hello World program
- Calculator program

## Instructions
1. Create a new project called `Loops` and a new Kotlin file within your project. Name the file `Main`.
Create your `main` method.

2. Create a new Kotlin class within your project and name it `Loops`. 

3. Create a method called `basicForLoops`. Write four seperate for loops that will...    
    - Part 1: print variable x in 0-10 inclusive
    - Part 2: print variable x in 0-10 not inlusive of 10
    - Part 3: print variable x in 0-10 inclusive skipping every other number
    - Part 4: print variable x in 10-0 inclusive skipping every other number
  
4. Create a method called `forLoops`. Write two seperate for loops.    
    - Part 1: declare a list called `colors` of three string elements. Using a for loop, print each element in the list.
    - Part 2: create a new for loop that will iterate through the index and value of each element in `colors`. In the body of your loop, print the index and value in one line.
  
5. Create a method called `whileLoop`. In your method declare an integer variable named `x` set to 0. Set your loop so that it prints the value of `x` while `x` is less than 10. Remember to increase `x` by 1 in the body of the loop. 
   
6. Create a method called `forEachStatement`. In your method create a list of two string elements and using a forEach statement, print each of the strings.
   
7. Create a method called `delay`. Add two print statements and add code for a 2 second delay between the statements.
   
8. At the top of your `Loops` class, add an initializing constructor that prints `Initialize`
   
9.  Go back to the file with your `main` method. Inside the `main` method, create an instance of your `Loops` class and then call each of the methods from that class. Print the outputs to the console.

## Results
Try it yourself before looking at these!

<details>
    <summary>Code</summary>
    <details>
        <summary>Main.kt</summary>

            fun main(){
                val loops = Loops()
                loops.basicForLoops()
                loops.forLoops()
                loops.whileLoop()
                loops.forEachStatement()
                loops.delay()
            }
    
</details>

<details>
    <summary>Loops.kt</summary>
    
        class Loops {

            //constructor
            init{
                println("Initialize")
            }

            fun basicForLoops(){
                print("\n Part 1: ")
                for (x in 0..10) print("$x, ") // Prints 0 through 10 (inclusive)
                print("\n Part 2: ")
                for (x in 0 until 10) print("$x, ") // Prints 0 through 9
                print("\n Part 3: ")
                for (x in 0..10 step 2) print("$x, ") // Prints 0, 2, 4, 6, 8, 10
                print("\n Part 4: ")
                for (x in 10 downTo 0 step 2) print("$x, ") // Prints 10, 8, 6, 4, 2, 0
            }

            fun forLoops(){
                val colors = listOf("red", "green", "blue")
                println("Part 1: ")
                for (color in colors){
                    println(color)
                }
                println("Part 2: ")
                for ((index, value) in colors.withIndex()) {
                    println("$index: $value")
                }
            }

            fun whileLoop(){
                var x = 0
                while (x < 10) {
                    println(x)
                    x++
                }
            }

            fun forEachStatement(){
                listOf("Green", "Hope").forEach { word ->
                    println(word)
                }
            }

            fun delay(){
                //print after delay of two sec
                    println("FRC")
                    Thread.sleep(2000)
                    println("5190")
            }
        }

</details>
</details>

<details>
    <summary>Console Output</summary>
        <details>
        <summary>basicForLoops</summary>
            
            Initialize

            Part 1: 0, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 
            Part 2: 0, 1, 2, 3, 4, 5, 6, 7, 8, 9, 
            Part 3: 0, 2, 4, 6, 8, 10, 
            Part 4: 10, 8, 6, 4, 2, 0, 
            Process finished with exit code 0
</details>
        <details>
        <summary>forLoops</summary>
        
        Initialize
        Part 1: 
        red
        green
        blue
        Part 2: 
        0: red
        1: green
        2: blue

        Process finished with exit code 0

</details>

<details>
        <summary>whileLoop</summary>
        
        Initialize
        0
        1
        2
        3
        4
        5
        6
        7
        8
        9

        Process finished with exit code 0

</details>

<details>
        <summary>forEachStatement</summary>
        
        Initialize
        Green
        Hope

        Process finished with exit code 0

</details>

<details>
        <summary>delay</summary>
        
        Initialize
        FRC
        5190

        Process finished with exit code 0

</details>
</details>