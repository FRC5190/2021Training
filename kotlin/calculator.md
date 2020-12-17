# Calculator Program
- Practice writing methods to perform algebraic tasks
- Practice calling and implementing methods from a different class

## Prerequisites
- [Hello World](helloworld.md)

## Instructions
1. Create a new project called `Calculator` and add a new Kotlin file inside the `src` folder. Name the file `Main`.
Create your `main` method.

2. Create another Kotlin class in your `src` folder. Name it `Calculate`.
   
3. Create four new methods within the `Calculate` file that will compute and return the sum, difference, product, and quotient of two numbers passed to them.
 
4. Add another method that will convert inches to feet. The method should take in one input and return a string stating the total amount of feet as well as the inches left over.

5. Back in the `Main` file, in your `main` method, initialize three variables, create an instance of the `Calculate` class, call each of the five methods using the instance you created, and print the outputs to the console.


## Results
Try it yourself before looking at these!

<details>
    <summary>Code</summary>
        <details>
            <summary>Main.kt</summary>

            fun main() {
                val x = 5.0
                val y = 10.0
                val inches = 30.0
                val calculate = Calculate()
                println(calculate.add(x, y))
                println(calculate.subtract(x, y))
                println(calculate.multiply(x, y))
                println(calculate.divide(x, y))
                println(calculate.inchesTofeet(inches))
            }

</details>

<details>
            <summary>Calculate.kt</summary>

            import kotlin.math.round

            class Calculate {

                fun add(x : Double, y : Double) : Double{
                    return (x + y)
                }

                fun subtract(x : Double, y : Double) : Double{
                    return x - y
                }

                fun multiply(x : Double, y : Double) : Double{
                    return (x * y)
                }

                fun divide(x : Double, y : Double) : Double {
                    return x / y
                }

                fun inchesTofeet(x : Double) : String{
                    val feet = round(x / 12)
                    val inchesLeftOver = x % 12
                    return "$feet feet and $inchesLeftOver inches"
                }
            }
            
</details>
</details>

<details>
    <summary>Console Output</summary>

    15.0
    -5.0
    50.0
    0.5
    2.0 feet and 6.0 inches

    Process finished with exit code 0
</details>