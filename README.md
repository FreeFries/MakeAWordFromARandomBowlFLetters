# Make-Word-From-Random-Bowl-of-Letters
Given a random collection of alphabets (all caps), submit a word and see if you can make that word from the collection of letters without having to traverse thru the collection each time.

Supply 2 inputs, the 1st is a random set of letters generated for simplicity all capitals. For this supply on how large your bowl of alphabets is going to be. A number like 50 or 100. Then supply the word you would like to see that you can build like SuperCaliFragilisticExpialidocious.

In order to have an ORDER OF ONE in searching to see for your letters. I have ordered the collection of random letters into a HashMap<String,Integer> namely the Key is A and Integer is the count of how many times it occurs.

Step 1 Generate my Random bowl of Alphabets<br />
Step 2 Go thru my bowl and arrange then into an HashMap for fast access.<br />
Step 2a I then did a countback of these letters for the benefit of the user so that they could see how many of each letter existed <br />
Step 2b Validation of Parameters. Also validate to see that no numbers are sent. A Java8 stream and predicate are used here <br />
Step 3 Split the word you want create and then use a simple Java 8 lambda from a functional interface to check to see if the letter is available, Use it to form your word and then decrease the count for that letter in your HashMap <br />
Step 4 Spit out how much of the word you could make. ?=Letter was never there *=You ran out of that letter. <br />


Other features provided in this code Repo<br />
(1) Have provided a POM file for a Maven Build<br />
(2) Have provided a Bash script file to run the Maven stuff<br />
(3) In the Target folder there is a JAR file that you can use<br />
(4) The main class is xander.soupalphas.GenAlphas<br />
(5) Below is output of my program that takes 2 parameters, the 150 is the number of random alphabets available, and that long word is SuperCaliFragilisticExpialidocious you can use your own word.<br />
(6) There is validation for the parameters as well. Check out the use of a Java8 stream in validateNoNumbrsInWord()<br />
(7) It uses a HashMap to store an index (key) of an alphabet and how many times (count is value) it occurs and then it builds this word with a single seek into the Map without traversing all the alphabets so it is quick.<br />
(8) In my code I have also used some simple Java8 code snippets that include lambdas, functional interface and a simple use of a stream. Not claiming I am an expert but I have some understanding of their usage.<br />
(9) When it cannot build the word fully it will tell you where it could not find a letter or whether it had used the letter up. Example ..... Legend ?=bowl never had that letter *=bowl had that letter but it did not have enough<br />
S?PERCAL??R*G?*?S??C*XP?**?DOC?*?S<br />
(10) Example of OUTPUT below ......
 