# text-Autocomplete-trie

Let's suppose we have several words stored into the database like abc, abd, abb, abd, bcd, cde. So, If the user comes again, the user doesn't have to type again. We will se how we will implement this aucomplete using trie. One assumption we are making here when the machine will suggest the word/character it will be alphabatically sorted. 

Let's start by building a trie. So, trie always has a root and when we put the characters as the nodes in the trie. first abc a, a will have word end value of 0 ad c will have word end value of 1 (as the word abc is ending at c), similarly for others as well. Trie will look like the below:
![t1](https://github.com/vyaslkv/text-Autocomplete-trie/blob/master/t1.png)

 Using these word end value we will know what words to suggest. Let's take an example and we need suggest only 1 suggestion, the top one for letter a. We will start from a then b (word end value 0, so we move more) then to c (here the word end value is 1 that is greater than 1) so we will give this as an suggestion abb.
 ![t2](https://github.com/vyaslkv/text-Autocomplete-trie/blob/master/t2.png)
 
