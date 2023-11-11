# class-7-reading
## All notes and answers are taken from reading. 
class 7 reading and questions
Domain Modeling (code fellows GitHub)<br> 
Domain modeling is process of creating a concept model in code for specific<br>
	problem<br>
	i. Model describes various att behaviors and constraints that govern prob domain<br>
     B.    Define a constructor and initialize properties.
	i. Define same properties betwixt many objects want constructor button<br>
	ii. Constructor function is defined using function expression.
	iii. The variable is declared and then assigned function with parameters<br>
	iv. When function is called data inside parameters is stored inside<br>
	     this.nameofthing and this.otherthing has props. 
	v. Storing data with props ensures any new obj can access later.<br>
	vi. After constructor functor def 2 objects are instantiated  with new keyword<br>
	vii. Props are initialized by calling the function<br>
     C. OOP in js at most fundamental level<br>
	1. The new keyword instantiates/creates object
	2. Constructor functor initializes props inside that obj using this variable.
	3. Object is stored in a var for later use.<br>
    D. Methods can be added to a constructor function prototype. 
	i. Prototype does work, and function takes credit.<br>
	ii. Best practice in js, even though takes longer<br>

  E. Tips and tricks<br>
	i. When modeling a single entity that’ll have many instances, build self contained<br>
              objects with same attributes and behaviors<br>
	ii. Model it’s attributes with a constructor function that def and initializes properties<br> 
	iii. Model it’s behaviors w. Small methods that focus on doing one job well<br>
	iv. Create instances using the new keyword followed by call to a constructor funct<br>
	v. Store new created obj in var so can access props and methods from outside
	vi. Use this variable with methods so you can access the obj props and methods<br>
	     inside<br>


II. HTML Tables<br>
What is a table?<br>
A data struck made of of rows and col (tabular data)<br>
Allows quick look up of vals that have some kind of connection<br>
How tables work<br>
Rigid<br>
Easily interp by making vis assoc betwixt col and row<br>
When created correctly HTML table are handled well by accessibility tools     <br> like screen readers<br>
Table Styling<br>
Tables need css as well as good html structure see following for table style<br>
https://developer.mozilla.org/en-US/docs/Learn/CSS/Building_blocks/Styling_tables <br>
When should you not use HTML tables. <br>
DO NOT USE HTML TABLES TO LAYOUT WEBSITES.<br>
Layout tables reduce accessibility for visually impaired users<br>
Tables produce tag soup/complex mark-up structures<br>
Tables are not automatically responsive<br>
Creating Table
Put down an opening and closing <table></table><br>
Set down a <td></td> for table data<br>
Need to put down as many as you need they are aligned next to each other not <br> down<br>
Put down <tr></tr> which is table row<br>
Adding header with <th> elements<br>
Special cells that go at start of row or col and define type of data row or col <br>
Contained<br>
Why are headers useful? <br>
                                                                           i.      Easy way to find data looking for header stand out and design looks <br>                                      better<br>
                                                                         ii.      Table headers have added benefit along w/scope attribute. Allow to <br>                                     to make tables more accessible. <br>
Allowing cells to span multiple rows and columns<br>
Can use colspan and rowspan to do this<br>
Both accept unitless num val which = equals the number of rows or col want<br>
Spanned. Ex colspan=”2”<br>
Styling w/o <col>
Html has method defining styling info for entire col of data all in one place <col><br>
Exists as can be tricky annoying or inefficient to spec styling on columns. <br>                                           generally need style infor on every <td>or <th> or use complex selector like :nth-child<br>
Styling with <col><br>
Can spec info on <col> element<col> spec inside<colgroup> below open table<br> 
tag<br>
III. Introing constructors<br>
Object basics<br>
An object is a collection of related data of functionality. Consists of several<br>
Variables and functions.
Creating objects begins with defining initializing a variable<br>
See following for object creation https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Objects/Basics#introducing_constructors <br>
Object is made of multiple members each has name and value. <br>
Name and Val pair must be separed by comma<br>
Each name val in each case separated by a colon<br>
Val of object member can be pretty much anything<br>
          i.      The first two items are data items and reffed as properties<br>
          ii.      Last two items are functions that allow obj to do something w/ data<br>
Reffed as object methods<br>
           iii.      Common to create an object using object literal when wanting to<br>
Transfer  data items in some manner like req to put into database<br>
Sending a single object is more efficient than sending several easier<br>
To work with array<br>
Dot Notation<br>
          i.      Dot notation accesses object properties, like person.age: or person.bio()<br>
         ii.      Objects as object properties<br.
An object prop can itself be an object see following<br>
https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Objects/Basics#introducing_constructors
         iii.      Bracket notation<br>
Bracket notation provides an alternative way to access object<br>
Properties instead of dot notation<br>
Like person[“name”][“first”]; <br>

d. Bracket notation<br>
		i. Gives other way to access object props helpful if name note conventional<br>
		ii. e. Setting object members.
			a. Can update Vals of exist prop and methods. 
			b. Can also create completely new members
		iii. Useful aspect of bracket notation can set member Vals dynamically and<br>
		     member names too. 
	e. What is “this”<br> GET IMAGE OF JACK
		i. this keyword refs to current obj the code being written insides.<br>
			a. Not helpful when make single obj<br>
			b. Create more than one this is useful<br>
	f. Introducing Constuctors<br>
		i. Object literals are fine, but need to write out  same code for every object<br>
		   created. Note efficient<br>
		ii. Can create as many objects awe we like reusing definition see<br>
		https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Objects/Basics#introducing_constructors<br>
		iii. Or better still use constructor<br>
			a. Just a function called using new keyword. When called will<br>
				1. Create object<br>
				2. Bind this to new obj so can ref  this in constructor code<br>
				3. Run code constuctor<br> 
				4. Return new obj<br>
			b. Constructors by convention start with CAP letter and are named<br>
			     type of object they create see above link for example<br>


IV. Beginners guid to js Prototype<br>
	a. Objects 
		i. Are key value pairs. 
	b. Need to create more than 1 “animal” “dish” thing<br>
		i. Next step would be to encapsulate that logic inside a function and<br> 
		   invoke whenever we need to create a new animal. ,br>
			a. Call this functional instantiation call the function<br>
			b. Call the funct itself “constructor function” as constructs new<br>
			     object<br>
		ii. Don’t do above do below<br>
			a. Instead of re-creating those methods when we create new animal<br>
			    gave them own object that can ref “animal” that object. 
	
c. object.create allow you to creat an object which will delegate to another object<br>
	    failed lookups.
		i. Whenever there is a failed property lookup on child js will delegate lookup<br>
		   to the parent obj.<br>
			a. If child doesn’t have heritage prop, parent does<br>
	d. Prototype<br>
		i. Every method in js has a prototype property that refs an object. 
		ii. Instead of creating a separate object to manage methods put each of<br>
		    those methods on function prototype. Do not need object.create to <br>
		    deleted, can use .prototype. <br>
		iii. Allows us to  share methods across all instances of a function.<br> 
			a. Rather than managing multi obj for each method we can just use<br>
			     another  object that comes built in. <br> 
		iv. WHISKEY TANGO FOXTROT THIS DUDE IS JUST RE-CREATING A <BR>
		    CRAPPIER VERSION OF A CLASS
			a. Wow can create classes now. 


1. Explain why we need domain modeling.
  a. It helps to clarify what’s needed, it works as a way for clients to communicate their needs, and for us to fufill those needs, like any dom. 
2. Why should tables not be used for page layouts?
  a. It’s poor layout, and should not be used, even though it’s tempting as everything is in a box, it’s not good. 
3. List and describe 3 different semantic HTML elements used in an HTML <table>.
  a. <td> creates the cell that the data you want to display appears in
  <tr> table row creates a line or cells when you wrap your table data(<td>) 
  Table Headers <th> which works just like <td> except that it denotes a special cell that looks different and   clearly stands out as a header
4. What is a constructor and what are some advantages to using it?
  a. A constructor is a method used for creating an object and initializing an object instance of that class.     It is used to create a new object and set values for an existing class. It makes it much faster than having     to write the same thing over and over for each object. 
5. How does the term this differ when used in an object literal versus when used in a constructor? 
  a. “This” makes it possible for you to used the same method definition in every object you create. It makes     it much faster to create as many objects as we want by reusing the definition. This in an object literals      connect a key value to be able to use it within an object without having to type the entire thing.
6. Explain prototypes and inheritance via an analogy from your previous work experience.
  a. Protoypes do all the work, prototypes are the things behind the scenes that get used before the photo is     taken. Say you are out on location in Alaska doing a photoshoot and you want your models to ski down a         mountain/hill/whatever you use a prototype, and then later you use a functional sample to to show the           actual product. The “sample”/function looks nicer and gets a bit more credit while the prototype is out         there doing the ski bit. Inheritance works like if you are genetically predisposed to something you           probably inherited it from your parents much like code, it might not be totally visible at first, but as       you are attached/code is attached you inherit things from a parent code inherits properties from a parent

## Things i want to know more about
practice with constuctors, and objects, and yay it's similar to classes in python. 
     
