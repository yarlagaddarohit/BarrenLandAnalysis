# BarrenLandAnalysis

## Steps for Execuition
IDE - [IntelliJ IDEA CE](https://www.jetbrains.com/idea/download/#section=mac)

Download the zip file, and import the project using the pom.xml

Run the Main program in main->java->com.rohit->Main

Please Enter the BarrenRectangles Input: 


Sample Input: {“48 192 351 207”,“48 392 351 407”,“120 52 135 547”,“260 52 275 547”}


Sample Output: 22816 192608 


## Creating Fertile Land
Let us consider the fertile land on a graph sheet, a graph sheet is an 2-D space with X and Y co-ordinates. Now, create an matrix which can point to all the nodes in the graph using an 2-D array. I have created the array **int[][] fieldMatrix**.
Default values in the matrix are 0, considered as the fertile field.

|0|0|0|0|
|-------------|-------------:| -----:|-----:|
|0|0|0|0|
|0|0|0|0|
|0|0|0|0|
|0|0|0|0|
### This is an sample matrix which is considered to be fertile land.

## Marking the Barren Land
Next, user need to provide the co-ordinates of bottom left corner and top right corner of the barren land field which is in the form of rectangle, there can be multiple barren field inputs. All the rectangles of barren fields are stored in the **barrenRectangles**. So after knowing the co-ordinates of the barren fields the next thing I have done is marking the barren rectangles to x.

Case1 :

|x|x|0|0|
|-------------|-------------:| -----:|-----:|
|x|x|0|0|
|x|x|0|0|
|x|x|0|0|
|0|0|0|0|

This is an sample matrix which is considered to be fertile land with one part of Barren Field which is marked as x.
The output of this case will be a single value.

Case 2 :

|x|x|x|x|
|-------------|-------------:| -----:|-----:|
|0|0|0|0|
|x|x|x|x|
|0|0|0|0|
|x|x|x|x|

This is an sample matrix which is considered to be fertile land with two part of Fertile Field which is marked as 0 and they are divided by three barren lands marked as x.
The output of this case will be two values i.e area of second row and area of fourth row.

## Finding the Area of Fertile Land
Using the **Breadth-First Traversal** the traversal of the nodes which are marked as zero is done and the area is found.
To know about the BFS, here is a great video presented by an MIT Professor, understanding BFS makes this case study a simple task.
[BFS By Erik Demaine](https://www.youtube.com/watch?v=s-CYnVz-uh4)

