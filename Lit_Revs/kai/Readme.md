# Literature Review

## Peoples
1. [Xiaojin (Jerry) Zhu, University of Wisconsin Madison](http://pages.cs.wisc.edu/~jerryzhu/machineteaching/)
2. [Burr Settles, Duolingo/Carnegie Mellon University](http://burrsettles.com/)
3. [Jina Suh, Microsoft Reserach](https://www.microsoft.com/en-us/research/people/jinsuh/)

## Papers

1. [Learning binary relations and total orders](#learning-binary-relations-and-total-orders)
2. [On the Complexity of Teaching](#on-the-complexity-of-teaching)
3. [Mixed initiative interfaces for learning tasks](#mixed-initiative-interfaces-for-learning-tasks)
4. [Interactive Machine Learning](#interactive-machine-learning)
5. [CueFlik: interactive concept learning in image search](#interactive-concept-learning-in-image-search)
6. [The teaching dimension of linear learners](#the-teaching-dimension-of-linear-learners)
7. [Interactive Semantic Featuring for Text Classification](#interactive-semantic-featuring-for-text-classification)

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


## On the Complexity of Teaching
>  **Authors**: Goldman, S. and Kearns, M     
**Venue**: Journal of Computer and Systems Sciences    
**Date**: 1995

**Summary**

## Mixed initiative interfaces for learning tasks
>  **Authors**: Steven A. Wolfman, Tessa Lau, Pedro Domingos, Daniel S. Weld    
**Venue**: Proceedings of the 6th international conference on Intelligent user interfaces      
**Date**: January 2001. Santa Fe, New Mexico, USA.

**Summary**


## Interactive Machine Learning
> **Authors**: Jerry Alan Fails, Dan R. Olsen, Jr.    
**Venue**: 	Proceedings of the 8th international conference on Intelligent user interfaces    
**Date**:   January 2003. Miami, Florida, USA 

**Summary**

## Interactive concept learning in image search
> **Authors**: 	James Fogarty, Desney Tan, Ashish Kapoor, Simon Winder       
**Venue**: Proceedings of the SIGCHI Conference on Human Factors in Computing Systems 	    
**Date**: April 2008. Florence, Italy    

**Summary**

## The teaching dimension of linear learners
>  **Authors**: Ji Liu, 	Xiaojin Zhu
**Venue**: The Journal of Machine Learning Research     
**Date**: 2016

**Summary**


## Interactive Semantic Featuring for Text Classification
> **Authors**: Camille Jandot, Patrice Simard, Max Chickering, David Grangier, Jina Suh	       
**Venue**: ICML Workshop on Human Interpretability in Machine Learning 	    
**Date**: July 2016. New York, US    

**Summary**

