# POS-tagging
One of the most important operations that is implemented by speech recognition devices is POS tagging. It consists in tagging each part of a sentence with the role of that term in the sentence (e.g., noun, verb, or modal).

Design a function pos_tagging(R, S, T, E) that takes in input
- a tuple R of roles,
- a tuple S of strings,
- a dictionary T whose keys are the roles in R plus the special role Start and values are dictionaries T[r] such that
  - the keys of T[r] are the roles in R plus the special role End
  - the values of T[r] are the transition probabilities between r and the corresponding role defined by the key
- a dictionary E whose keys are the strings in S and value are dictionaries E[s] such that
  - the keys of E[s] are the roles in R
  - the values in E[s] are the emission probabilities between s and the corresponding role defined by the key
  
The function returns a dictionary whose keys are the words in S and the values are the roles assigned to these words, so that the selected assignment is the one of maximum likelihood.

# DeviceSelection
You are asked to test several speech recognition devices in order to choose the one giving the right performances. Some preliminary tests on these devices have been run, but more massive tests are necessary. Unfortunately, these further tests are very expensive and time-consuming, and thus we would like to choose a small subset of “more relevant” devices and we would like to run tests only on the selected devices. Clearly, we would like to select devices to test so that the best device is included in the test.
