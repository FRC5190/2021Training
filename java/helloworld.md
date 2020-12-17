# Hello World

## Prerequisites
- IntelliJ ([IDE](../common/ide.md))

## Instructions
1. Create a new project in IntelliJ: `File` -> `New` -> `Project`. On the left, make sure `Java` is selected, then click `Next`. Skip the next page, then name your project and set where the project is saved.

2. Once your project loads, click the dropdown on your project folder. Right click the `src` folder and select `New` -> `Java Class`. Name the file `HelloWorld`
   
3. Write a method called `main` inside of your `HelloWorld` class. The body of the method should print `Hello World` onto the console when the program is run. You can run the program by clicking the green triangle next to your method.

## Results
Try it yourself before looking at these!

<details>
    <summary>Code</summary>

    public class HelloWorld {
        public static void main(String[] args) {
            System.out.println("Hello World");
        }
    }
</details>

<details>
    <summary>Console Output</summary>

    Hello World

    Process finished with exit code 0
</details>