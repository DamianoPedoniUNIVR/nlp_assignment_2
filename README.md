## Assignment 2 - Natural Language Processing
##### Damiano Pedoni
### Development in NLTK of a pipeline that, starting from a text in input, in a given language (English, French, German and Italian are admissible) outputs the syntactic tree of the sentence itself, intended as a tree with root in S for sentence, and leaves on the tokens labelled with a single Part-of-speech.

A link to the code can be found [here](https://github.com/DamianoPedoniUNIVR/nlp_assignment_2), or visiting this url: https://github.com/DamianoPedoniUNIVR/nlp_assignment_2

#### - PURE SYMBOLIC APPROACH
I've deviced to approach this problem in a symbolic way. My goal was to create a context free grammar able to generate a syntactic tree for each sentence given as input.

#### - The pipeline
The pipeline to achieve this goal is very straight forward:<br>
1) I've created a basic grammar rules for each language
2) Each grammar needs some context, so we need to generate the part that describe each token's tag. I've used Spacy to get the pos tagging of each token in the sentence.
3) I've used nltk built-in function ChartParser to parse the grammar and generate all the possible trees.
4) We take only the first generated tree, in case of ambiguity.

#### - Results and conclusions
The grammar is able to generate a tree for simple sentences, as shown in the examples at the end of the python notebook. For more complex sentences, a longer grammar would be necessary but in that case it could be very computational heavy for the nltk parser to compute.

