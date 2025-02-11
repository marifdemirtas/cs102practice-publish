..  Copyright (C)  Brad Miller, David Ranum, Jeffrey Elkner, Peter Wentworth, Allen B. Downey, Chris
    Meyers, and Dario Mitchell.  Permission is granted to copy, distribute
    and/or modify this document under the terms of the GNU Free Documentation
    License, Version 1.3 or any later version published by the Free Software
    Foundation; with Invariant Sections being Forward, Prefaces, and
    Contributor List, no Front-Cover Texts, and no Back-Cover Texts.  A copy of
    the license is included in the section entitled "GNU Free Documentation
    License".


..  shortname:: Lab3Hello
..  description:: Run and compare C, Java, and Python

.. setup for automatic question numbering.

.. qnum::
   :start: 1
   :prefix: L3-

.. W2:

Lab 3: Language Comparison
#####################################


.. activecode:: c_hello
   :language: c

   Run this code to see what it does. What happens if your name is longer than 10 characters?
   ~~~~
   #include <stdio.h>
   #include <string.h>

   int main(void) 
   {
      // Prompt user for their name
      char name[10];
      printf("Hello. What's your name?\n");
      fgets(name,10,stdin);

      // Greet the user
      printf("Hi there, %s!\n", name);

      // Print the length of the name
      size_t length = strlen(name);
      printf("Your name has %s letters.\n", length);
      return 0;
   }

   ====

.. activecode:: java_hello
   :language: java

   Run this code to see what it does.
   ~~~~
   import java.util.Scanner;

   public class NameHelper {
      public static void main(String[] args) {
        // Create a Scanner object for user input
        Scanner scanner = new Scanner(System.in);
        
        // Prompt user for their name
        System.out.print("Hello. What's your name? ");
        String name = scanner.nextLine();
        
        // Greet the user
        System.out.println("Hi there, " + name + "!\n");
        
        // Print the length of the name
        System.out.println("Your name has " + name.length() + " letters.");
        
        // Close the scanner
        scanner.close();
      }
   }

   ====

.. activecode:: python_hello
   :language: python3

   Run this code to see what it does. What do you notice about this code compared to the two programs above?
   ~~~~
   name = input("Hello. What's your name? ")

   # Greet the user
   print(f"Hi there, {name}!")

   # Print the length of the name
   print(f"Your name has {len(name)} letters.")

   ====


.. note:: 
      
        .. raw:: html

           <a href="/index.html" >Click here to go back to the main page</a>


 
