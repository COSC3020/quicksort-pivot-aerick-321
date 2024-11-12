# Quicksort Pivots

in the lectures I only briefly mentioned strategies for determining a good pivot
for quicksort. The implementation on the slides simply picks the leftmost
element in the part of the array that we consider as a pivot. I also mentioned a
few other ways of picking a good pivot, e.g. randomly.

Median-of-three is also a good way of picking a pivot -- inspect the first,
middle, and last elements of the part of the array under consideration and
choose the median value. Using the probabilities for picking a pivot in a
particular part of the array (in the same way as we did on slide 34), argue
whether this method is more or less (or equally) likely to pick a good pivot
compared to simply choosing the first element. Assume that all permutations are
equally likely, i.e. the input array is ordered randomly.

Your answer must derive probabilities for choosing a good pivot and
quantitatively reason with them.

Add your answer to this markdown file. [This
page](https://docs.github.com/en/get-started/writing-on-github/working-with-advanced-formatting/writing-mathematical-expressions)
might help with the notation for mathematical expressions.

There are three elements to choose from and those three elements could land in three places, greater than pivot, good pivot, and less that pivot. The greater than and less than pivot are not the best choice and both have the probability of 1/4 while the good pivot in the middle has a probability of 1/2. The total number of permutations would be 3^3, 27 different ways. L-left of pivot, P- good pivot, R- right of pivot

All Bad (1/4* 1/4 *1/4) = 1/64: LLL, LLR, LRR, RRR, LRL, RLL, RRL, RLR;  1/64 * 8 = .125

Two bad(1/4 * 1/2 * 1/4)= 1/32: LLP, LRP, RRP, RLP, LPL, PRR, PLL, RPR, RPL, LPR, PLR, PRL; 1/32 * 12 = 0.375

One bad(1/2 * 1/2 * 1/4)= 1/16: LPP, RPP, PLP, PRP, PPL, PPR; 1/16 * 6 = .375 Good (1/2 * 1/2 *1/2)= 1/8 = .125: PPP

The median of three would be more likely to choose a better pivot the probability is 0.375 + 0.125 = 0.5, 50%. 

“I certify that I have listed all sources used to complete this exercise, including the use of any Large Language Models. All of the work is my own, except where stated otherwise. I am aware that plagiarism carries severe penalties and that if plagiarism is suspected, charges may be filed against me without prior notice.”
