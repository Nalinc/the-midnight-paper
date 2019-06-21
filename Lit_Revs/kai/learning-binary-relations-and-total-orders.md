## Learning binary relations and total orders
>  **Authors**: Goldman, S.A., Rivest, R.L., and Schapire, R.E    
**Venue**: SIAM Journal on Computing    
**Date**: 1993

### Summary
#### Motivation: It is important to acquire information about a relation between two sets ("has-part" relation between a set of animals and a set of attributes)
#### Problem Statement: Design a prediction algorithm to learn a binary relation when the learner has limited prior information about the predicate forming the relation.
#### Technique 
- Binary relation is represented as an n x m binary matrix, where an entry contains the value of the predicate for the corresponding elements.
- The learner is repeatedly given a pair of elements, one from each set and asked to predict the corresponding matrix entry. After making its prediction, the learner is told the correct value of the matrix entry.
- Aim is to minimize the number of incorrect predictions made by the learner.
- PAC model of learning: instances are chosen randomly from an arbitrary unknown probability distribution on the instance space. A concept class is PAC-learnable if the learner can output a hypothesis that is correct on most of the instances.
- They have extended the basic mistake-bound model to cover cases where 
    - a helpful teacher selects a query sentence
    - instances are chosen by an adversary
    - instances are sampled according to a probability distribution on the instance space.
- Conventionally, teachers have been used to provide (a) counterexamples to conjectured concepts, or to break the concepts into smaller sub-concepts. However, in this work, the teacher only selects the presentation order for the instances.

