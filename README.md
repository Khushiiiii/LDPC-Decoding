# LDPC-Decoding

This is a group project with group size 3. I have worked on all the aspects of the project with my group members. 

This project aims to implement an efficient algorithm performing LDPC decoding on MATLAB, for both, Soft and Hard Decision Decoding. The transmission channel is  Binary Erasure Channel (BEC). 

Low Density Parity Check decoding is used often in the communication thoery for the transmission of encoded messages.

There are two types of nodes to represent decoding process. Check nodes and Variable Nodes. As the names suggest, the variable nodes are the received message that we want to decode and the check nodes are the nodes that we use to check if the currently decoded message can be correct. Check nodes are formed by taking some number of variable nodes and the sum of all those nodes modulo two should be zero for the message to be possibly correctly decoded. Low Density Parity Code implies that the number of variable nodes connected to a check node is very less compared to the total length of the transmitted message (total number of variable node). We can use Tanner Graph representations for the same. So, in other words, the degree of check nodes and variable nodes is very less as compared to the number of nodes. Hence these codes are called Low Density Parity Check Codes as their parity check matrix has very few 1s as compared to 0s.

We have implemented the decoding algorithm in MATLAB using hash tables and maps.

To get the accurate result, we have performed Monte Carlo simulations over the experiment and final expected probability has been calculated. For easier analysis of outcomes, this code works only on the all zero codeword. 

## Time-Space Complexity

The overall *time complexity* of the solution will be O((number of simulations)(dc)(CN)(max_it )) where 
dc = degree of checknode
CN = total number of checknodes.
max_it=maximum iterations done.

The overall *space complexity* of the algorithm will be O((dc)(CN)). This space is because of the storing of the CN and VN map(Working has been explained in the soft decision code).

## Contents: 
- Hard Decision Decoding MATLAB code (includes a pdf file to view the code without MATLAB)
- Soft Decision Decoding MATLAB code (includes a pdf file to view the code without MATLAB)
- Hard Decision Decoding Results
- Soft Decision Decoding Results
- Two large matrices to check the working of the code (Hmatrix and Hmatrix2)
- Comparison of *the Simulation* Results obtained for Hmatrix2 for soft decision decoding with the *results obtained using the Analytical Formula* (it compares the graph of number of erasures after decoding with the number of iterations performed)

## DSA- concepts used
- Graph Traversal
- Hash/Unordered map

## What is next?
- We can implement the decoding for non-zero messages.
- We can try to build a code for Binary Symmetric Channel.
