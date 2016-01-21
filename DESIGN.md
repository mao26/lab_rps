CompSci 308 : RPS Design
===================

> This is the link to the Lab Description: 
[Lab - RPS](http://www.cs.duke.edu/courses/compsci308/spring16/classwork/02_design_rps/index.php)

Initial Design
=======

###Class 1
Our first class will be our game loop and will hold our main method.
This will contain a read data method, game method:

1. We do not need to know how to read the data, so no need to specify how it would be read in

2. our game method will create a game object, this game objects constructor:

	* reads the data
	* creates a Collection with all of our objects
		1. This collection creates all of our possible objects from the data that is being read
		2. The collection then stores all of our RNS objects, so that the user can grab one object from the hashmap
	* allows the users to pick the number of rounds
	
3. The game loop will be made up of a couple of functions

	* If the combined score of the users is greater than the instances number of rounds, then the game is over; otherwise:
	* It first allows the users to pick their object
	* It will grab those objects from our hashmap, and call the compareTo of the first users object
	* According to our ints, the user wins loses of ties
	* From here, we call another method incScore():
	
		1. If obj.compareTo returns 0, it reinitializes the loop without increasing score
		2. If one it gives the user an increase in score and then reinitializes the loop

###Class 2
Our second class will be our User Class
The User class will have, two instance variables:

1. His score

2. His current object in RPN

Include a constructor that instantiates the score to be zero. 


###Class 3
Our third and final object will be a RPN Object Class
This class will hold two instance variables and implements Comparable interface and overrides the compareTo method

The instance variables are:

1. Name of object

2. List of objects that it beats

The compareTo method will go as follows: 
```java
    public int compareTo(RPNObject obj){
    	if(obj.name.equals(this.name) return 0;
    	else if(this.beats.contains(obj.name) return -1;
    	else return 1;
    }
    
```

Our CRC implementation of our classes

![This is cool, too bad you can't see it](crc.jpg "Our CRC cards")

###Class 1

* Bullets are made with asterisks

1. You can also order things with numbers


###Class 2



CRC Design
=======




You can add images as well:

![This is cool, too bad you can't see it](crc-example.png "Our CRC cards")


Use Cases
=======

You can put blocks of code in here like this:
```java
    public int getTotal (Collection<Integer> data) {
        int total = 0;
        for (int d : data) {
            total += d;
        }
        return total;
    }
```

