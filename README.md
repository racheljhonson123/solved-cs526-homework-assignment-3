Download Link: https://assignmentchef.com/product/solved-cs526-homework-assignment-3
<br>
This assignment is an implementation of a <strong><em>generic binary search tree</em></strong>, which extends the <em>LinkedBinaryTree</em> class. Binary trees are discussed in Section 8.2 and Section 8.3.1 in the textbook. Binary search tree is discussed in page 338 of the textbook.




The <em>LinkedBinaryTree.java</em>, which comes with the textbook, is a concrete implementation of a binary tree that uses a linked structure. It extends the <em>AbstractBinaryTree</em> class. The relevant class hierarchy is shown below:










The <em>LinkedBinaryTree</em> inherits variables and methods from its superclasses and it also implements its own methods.




The requirements of this assignment is given below:




<ul>

 <li>Create a generic binary search tree class named <em>java</em> and implement an <em>add</em> method within the class. An incomplete code is posted on Blackboard and you must complete the code.</li>

 <li>Perform an experiment that determines an average height of binary search trees.</li>

</ul>




Detailed requirements are given below.




Create a generic class named <em>MyBST</em> as a subclass of <em>LinkedBinaryTree</em>. The <em>MyBST</em> is an implementation of a binary search tree using a linked tree structure.




A <em>binary search tree</em> is a binary tree that satisfies the following <em>binary search tree property</em>.




For each internal position <em>p</em>:

<ul>

 <li>Elements stored in the left subtree of <em>p</em> are less than <em>p</em>’s element.</li>

 <li>Elements stored in the right subtree of <em>p</em> are greater than <em>p</em>’s element.</li>

</ul>




You are required to implement an <em>add</em> method using the following pseudocode:




Algorithm add(p, e)

Input parameters:

p: The position of the root of the tree (or subtree) to which

a new node is added

e: The element of the new node to be added

Output: Returns the position of the new node that was added.

If there already is a node with e in the tree, returns null.




if p == null // this is an empty tree

create a new node with e and make it the root of the tree

increment size // size is the number of nodes currently in the tree

return the root

x = p y = x

while (x is not null) {

if (the element of x) is the same as e, return null

else if (the element of x) &gt; e {

y = x

<ul>

 <li>= left child of x</li>

</ul>

}

else {

<ul>

 <li>= x</li>

</ul>

x = right child of x

}

} // end of while




temp = new node with element e y becomes the parent of temp if (the element of y) &gt; e   temp becomes the left child of y else

temp becomes the right child of y

increment size // size is the number of nodes currently in the tree

return temp




The following figure illustrates adding a node to a binary search tree. If you add a node with 70 to the tree on the left, the result is the tree on the right.










You may want to read and study the codes of <em>LinkedBinaryTree</em> and its superclasses and super interfaces carefully before writing a code.




An incomplete code of <em>MyBST.java</em> is posted on Blackboard. You need to complete this code as indicated and test your <em>add</em> method in the main method.




Then, perform the following experiment.




This experiment determines an average height of binary search trees when integers are added in a random order.




You are required to write a code segment in your main method to experimentally determine an average height of binary search trees.




First, you need to generate 1,000 distinct random integers in the range [0, 999999] and add them, one at a time, to an initially empty binary tree, using the <em>add</em> method you implemented. <strong>Make sure that the resulting tree has 1,000 distinct integers</strong>. Then, determine the height of the tree. Repeat this 100 times and calculate the average height of these 100 binary search trees. A sample code that generates a random integer in [0, 999999] is shown below:




int e;

Random r = <strong>new</strong> Random();

r.setSeed(System.<em>currentTimeMillis</em>()); e = r.nextInt(1000000);




You may want to refer to Java’s manual for more information about the <em>Random</em> class.




Output: For each iteration, your program must print the height of the tree and the number of nodes of the tree. Then, after 100 iterations, your program must print the average height of 100 trees. A sample output is shown below:




Height = xx, Size = 1000

Height = xx, Size = 1000

Height = xx, Size = 1000

Height = xx, Size = 1000

Height = xx, Size = 1000

Height = xx, Size = 1000




. . .




Average height = xx.xx // this is the average of 100 heights




<h1>Documentation</h1>




No separate documentation is needed. However, you must include sufficient inline comments within your program.




<h1>Grading</h1>




Your facilitator will test your <em>add</em> method by adding a sequence of integers. They will repeat this three times with three different sequences of integers and 10 points will be deducted for each sequence that generates an incorrect result or an error.




If the average height of binary search trees determined by your program is outside the generally expected range, 10 points will be deducted.




Points will be deducted up to 20 points if you do not include sufficient inline comments.




<h1>Deliverables</h1>




You need to complete the <em>MyBST.java</em> file. Combine this file with all other files, which are necessary to compile and execute your program, into a single archive file, such as a <em>zip</em> file or a <em>rar</em> file, and name it <em>LastName_FirstName_hw</em>3<em>.EXT</em>, where <em>EXT</em> is an appropriate file extension (such as <em>zip</em> or <em>rar</em>). Upload it to Blackboard.


