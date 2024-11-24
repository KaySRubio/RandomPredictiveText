# Generating Random Predictive Text Using a Markov Model
I created this Java project that uses text training data to generate novel random text in the style of the original text using a Markov model.

<!DOCTYPE html>
<html lang="en" data-color-mode="auto" data-light-theme="light" data-dark-theme="dark">

<body>
  <h2>Challenge:</h2>
  		<p>Code a program that analyzes a text file and produces new text randomly but in the style of the original text.</p>
  <h2>Solution:</h2>
    <p>I coded a program that uses a two-dimensional linked list structure to generate Markov models from a text file.</p>
  			<ol></ol>
          <li>User provides text training data as a file, for example, a chapter from Harry Potter</li>
          <li>Program opens the file and cleans the text data, for instance removing all digits, symbols, and making all letters lowercase</li>
          <li>Program iterates over the text to create a list of all unique words</li>
          <li>For each unique word, the program iterates over the text again to count the number of times each other word follows the given word. This data is then used to construct a probability matrix tells us, for a given state (e.g., a word), what is the probability of transitioning to the next state. For example, if “Harry” appears in the text 40 times, and is followed by “Potter” 20 times, then the probability of “Potter” given “Harry” is .5</li>
          <li>The probability matrix is stored in a two-dimensional linked list</li>
  			<br>
        <p>The user then asks the program to generate text of a specified length in the style of the original text.  Using the probability matrix, the program chooses an initial word, then picks words that are likely to be next in the sequence.</p>
        <p>The program also uses unigrams, bigrams, trigrams, and other n-grams. For example, if using bigrams, the program constructs probability matrices based not on single words, but on consecutive pairs of words. Given the bigram “Harry Potter” what is the probability of the next word being “thought” or “said” or “ran”? </p>

  <h2>Examples using the first chapter of Harry Potter as training data</h2>
  <p><b></strong>Random text generated using unigrams:</b></p>
  <p>vanished the other day and broken glasses and broken glasses and snakes were leaning right thirtyseven then said anything else to become until finally he reminded himself silly vernon bought him once on harry supposed was forbidden to the tank and piers and crushed it was aunt petunia had a nasty that couldnt imagine where he barked by the problem was sitting on their backs while piers polkiss walked in his hair at it winked harry his baggy clothes and thick blond harry made aunt rapped on this as though he could remember being hugged and nobody liked about them</p>
  <p><b></strong>Random text generated using bigrams:</b></p>
  <p>which was almost bald except for his age he looked back at the glistening brown coils make it move he whined at his mother the room held no sign at all had taken harry aside im warning you now boy any funny business anything at all that another boy lived in the house before starting on harry he was already laughed at for his bangs which she left to hide that horrible scar dudley had gotten it in the car that cars new hes not sitting in the car crash he couldnt be sure the snake didnt budge do it</p>
  <p><b></strong>Random text generated using trigrams:</b></p>
  <p>went down the hall into the kitchen the table was almost hidden beneath all dudleys birthday presents it looked as though dudley had gotten the new computer he wanted not to mention the second television and the racing bike exactly why dudley wanted a racing bike was a mystery to harry as dudley was very fat and hated exercise unless of course it involved punching somebody dudleys favorite punching bag was harry but he couldnt often catch him harry didnt look it but he was very fast perhaps it had something to do with him but before theyd left uncle</p>
  
   <h2>Skills Demonstrated:</h2>
  			<ul>
  				<li>Programmer-defined classes and methods</li>
  				<li>Defining relationships between classes</li>
  				<li>Complex data structures</li>
  				<li>Handling exceptions</li>
  				<li>Java library</li>
  				<li>Regular expressions</li>
  				<li>While/for loops</li>
  				<li>Conditional if/else logic</li>
  			</ul>
  <h2>Potential NLP Applications:</h2>
  				<ul>
  					<li>Predictive text suggestions in email or smart phones</li>
  					<li>Syntax-error checking in compilers</li>
  				</ul>
    <h2>How to run on your computer</h2>
      <ol>
        <li>Make sure you have java machine installed so you can compile the program</li>
        <li>Download the 3 .java files and save them in the same folder</li>
        <li>Compile them (you can compile Project2.java and this should compile the others)</li>
        <li>Save a text file in the same folder as Project2.java</li>
        <li>Run Project2 and answer the prompts. Include the name of the text file.</li>
        <li>Although the project can run in orders higher than 3, I suggest using orders 1-3 since order 4+ may be too similar to the original text</li>
        <li>Have fun!</li>
  </ol>
      <h2>Future Directions</h2>
      <p>To make things more interesting, and generate even more useful text, hidden layers could be incorporated such as parts of speech. For instance, the model could take into account not only the previous one word (or bigram or trigram) but also the part of speech of the previous word (e.g., noun, verb, adverb).</p>
<h2>Context</h2>
  <p>The project was part of Data Structures and Algorithms at Bridgewater State University in summer 2020. </p>
</body>
</html> 
