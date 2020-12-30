# HMMs and Viterbi algorithm for POS tagging

 HMM-based POS tagger and implement the Viterbi algorithm using the Penn Treebank training corpus. The vanilla Viterbi algorithm written had resulted in ~90% accuracy. The approx. 10% loss of accuracy was majorly due to the fact that when the algorithm encountered an unknown word (i.e. not present in the training set, such as 'Twitter'), it assigned an incorrect tag arbitrarily. This is because, for unknown words, the emission probabilities for all candidate tags are 0, so the algorithm arbitrarily chooses (the first) tag.

 

We need to modify the Viterbi algorithm to solve the problem of unknown words using at least two techniques. Though there could be multiple ways to solve this problem, but we have used 2 techniques.

Which tag class do you think most unknown words belong to? Can you identify rules (e.g. based on morphological cues) that can be used to tag unknown words? You may define separate python functions to exploit these rules so that they work in tandem with the original Viterbi algorithm.
Why does the Viterbi algorithm choose a random tag on encountering an unknown word? Can you modify the Viterbi algorithm so that it considers only one of the transition or emission probabilities for unknown words?

Before going through the code, pseudo-code for the same.

- Create Tagged Treebank corpus (Sample data to training and test data set)
- Basic text and structure exploration
- Creating HMM model on the tagged data set.
- Calculating Emission Probabaility: P(observation|state)
- Calculating Transition Probability: P(state2|state1)
- Developing algorithm for Viterbi Heuristic
- Checking accuracy on the test data set
- Create 2 methods to modify viterbi to resolve the problem of unknown words
- List down cases which were incorrectly tagged by original POS tagger and got corrected by your modifications
