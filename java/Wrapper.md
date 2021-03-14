# Wrapper Classes in Java
A **wrapper class** is a class which contains the **primitive data types** (int, char, byte, etc). In other words, wrapper classes provide a way to use **primitive data types** as object.

![](Wrapper-Class.png)

### Why we need Wrapper Class
> - Wrapper Class will **convert primitive data types into objects.** The object are necessary if we wish to modify the arguments passed into the method (because primitive types are **passed by value**).
> - **Data structures** in Collection framework such as **ArrayList and Vector** store only the objects(reference types) and not the **primitive types**.
> - The object is needed to support **synchronization in multithreading**.



### Autoboxing and Unboxing

- **Autoboxing** - conversion of int to Integer, long to Long, double to Double, etc. 


		import java.util.ArrayList; 
		class Autoboxing 
		{ 
		    public static void main(String[] args) 
		    { 
		        char ch = 'a'; 
		  
		        // Autoboxing- primitive to Character object conversion 
		        Character a = ch; 
		  
		        ArrayList<Integer> arrayList = new ArrayList<Integer>(); 
		  
		        // Autoboxing because ArrayList stores only objects 
		        arrayList.add(25); 
		  
		        // printing the values from object 
		        System.out.println(arrayList.get(0)); 
		    } 
		} 
		
- **Unboxing** - conversion of Integer to int, Long to long, Double to double, etc.


		import java.util.ArrayList; 
		  
		class Unboxing 
		{ 
		    public static void main(String[] args) 
		    { 
		        Character ch = 'a'; 
		  
		        // unboxing - Character object to primitive conversion 
		        char a = ch; 
		  
		        ArrayList<Integer> arrayList = new ArrayList<Integer>(); 
		        arrayList.add(24); 
		  
		        // unboxing because get method returns an Integer object 
		        int num = arrayList.get(0); 
		  
		        // printing the values from primitive data types 
		        System.out.println(num); 
		    } 
		} 