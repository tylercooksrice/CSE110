# My User Page
## Table of Contents
### 1. [Introduction](#introduction)
### 2. [Interests](#what-i-am-interested-in)
### 3. [Programming Language](#favorite-language)
### 4. [Quote](#favorite-quote)
### 5. [Code](#java-code-i-created)
### 6. [CSE 15L](#cse-15l)
### 7. [Goals](#goals)

## Introduction
  My name is **Tyler Khuc**. I am a first year transfer student and a computer science major. Transferring from ***Sacramento***, I attended the _ _Cosumnes River College_ _ in ***Sacramento*** before studying at the * *University of California of San Diego* *. As a programmer, the first language I have learned is ***C++***. The second language I explored was ***Java***. Currently I have been trying to learn ***Python*** and constructing my own website using react.

[University of California of San Diego Geisel Library](ucsd.jpg)

## What I am interested in:
- AI
- Frontend and Backend Development
- Game Development

### Favorite Language
1. C++
2. Java
3. Python

### Favorite Quote
> "A computer is like a violin.” You can imagine it making beautiful music, but you have to learn how to play it." - Bill Gates

### Java Code I Created
```
import java.util.Scanner;

public class dateConversion {
     public static void main(String[] args) {
        String month = ""; // String for month
	  String year = ""; // String for year
	  String day = ""; // String for day
	  int size = 0; // total size of array
	  int counter = 0; // counter for array
	  int[][]slashPos; // '/' position of data input
	  slashPos = new int[21][2]; // column 21, row 2 for slashPos 2d array
	  String[] data; // array for all data input
	  data = new String[21]; // array size 21
	  Scanner scanner = new Scanner(System.in); // scanner for taking in input
	  String input = ""; // String for user input	       

	  while(!input.equals("9999/")) { // while loop to take in input
	       System.out.println("\nplease enter a date in mm/dd/yyyy"); // display statement
	       System.out.println("(04/05/2018,4/5/2018, 04/5/2018, or");
	       System.out.println("4/05/2018) format or enter 9999/ to");
     	       System.out.println("terminate the program.");
	       input = scanner.next(); // take in next user input
	       data[counter] = input; // put input into corresponding data array index
	       slashPos[counter][0] = input.indexOf('/'); // find position of /
	       slashPos[counter][1] = input.indexOf('/', (slashPos[counter][0] + 1)); // find second position of /
	       counter++; // increment counter
		 if (counter == 20) { // if counter is 20
		      break; // break while loop
		 } // end if
	  } // end while

	  System.out.println("\nDisplay Date in  |       Display date in"); // display table title
	  System.out.println("Original format  |        other format");
	  System.out.println("-----------------|-----------------------");
	  size = counter; // set size equal to array counter
	  if (size == 0) { // if size is 0
	       System.out.println("      There is no data entered."); // display no data entered
	  } // end if
	  counter = 0; // set counter back to zero
	 
	  while(size != 1) { // while size is not 1
		month = data[counter].substring(0, slashPos[counter][0]); // set month
		year = data[counter].substring(slashPos[counter][1] + 1); // set year
		if ((slashPos[counter][0] + 1 != slashPos[counter][1]) && (year.indexOf('/') == -1)) { // 
		     day = data[counter].substring(slashPos[counter][0] + 1, slashPos[counter][1]); // set day
		}
		else if (slashPos[counter][0] + 1 != slashPos[counter][1]) {
		     int temp1 = data[counter].indexOf('/', slashPos[counter][1]); // set and create temp1 to 
		     day = data[counter].substring(slashPos[counter][0] + 1, slashPos[counter][1]);
		     year = data[counter].substring(temp1 + 2);	 
		}
		else if (slashPos[counter][0] + 1 == slashPos[counter][1]) {
		     int temp1 = data[counter].indexOf('/', slashPos[counter][1] + 1);
		     year = data[counter].substring(temp1 + 1);
		     day = data[counter].substring(slashPos[counter][1] + 1, temp1);
		     if (year.indexOf('/') != -1) {
		          year = year.substring(1);
		     }
		}
		if (day.indexOf('0') == 0) {
		    day = day.substring(1);
		}
	      System.out.print(String.format("  %-15s|", data[counter]));

		if (month.equals("01") || month.equals("1")) {
		    System.out.printf("      January %s, %s%n", day, year);
		}
		if (month.equals("02") || month.equals("2")) {
		    System.out.printf("      February %s, %s%n", day, year);
		}
		if (month.equals("03") || month.equals("3")) {
		    System.out.printf("      March %s, %s%n", day, year);
		}
		if (month.equals("04") || month.equals("4")) {
		    System.out.printf("      April %s, %s%n", day, year);
		}
		if (month.equals("05") || month.equals("5")) {
		    System.out.printf("      May %s, %s%n", day, year);
		}
		if (month.equals("06") || month.equals("6")) {
		    System.out.printf("      June %s, %s%n", day, year);
		}
		if (month.equals("07") || month.equals("7")) {
		    System.out.printf("      July %s, %s%n", day, year);
		}
		if (month.equals("08") || month.equals("8")) {
		    System.out.printf("      August %s, %s%n", day, year);
		}
		if (month.equals("09") || month.equals("9")) {
		    System.out.printf("      September %s, %s%n", day, year);
		}
		if (month.equals("10")) {
		    System.out.printf("      October %s, %s%n", day, year);
		} 
		if (month.equals("11")) {
		    System.out.printf("      November %s, %s%n", day, year);
		}
		if (month.equals("12")) {
		    System.out.printf("      December %s, %s%n", day, year);
		}
		counter++;
		size--;
 	       
	 }
   }
}
```

### CSE 15L
[Lab Reports](https://tylercooksrice.github.io/cse15l-lab-reports/index)

## Goals
- [x] Learn HTML
- [ ] Learn CSS
- [ ] Learn Javascript
- [ ] Learn Node.js
- [ ] Learn React