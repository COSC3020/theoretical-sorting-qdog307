# Theoretical Sorting

A Computer Science researcher claims to have come up with a sorting algorithm
that can sort arbitrary elements in $O(n)$ time based on comparisons of two
elements at a time. This would be asymptotically faster than any known general
sorting algorithm. The algorithm itself is proprietary and will be sold by a
company.

How would you verify this claim? You may assume that you have access to a
black-box implementation of the sorting algorithm, i.e. you cannot examine the
source code, but you can use it to sort any list you like. Explain in detail
your method for investigating whether X is correct, including any expected
results you would get.

Also give a theoretical argument for why X could or could not be correct, based
on the complexity of the general sorting problem we covered in class.

Add your answers to this markdown file.

To evaluate a claim like this, there are two main approaches to consider. First, we would want to conduct empirical testing by running numerous tests on the algorithm. This would involve creating various test cases with lists of different lengths and arrangements, such as randomly shuffled lists, already sorted lists, and reverse-sorted lists, among others. During this process, we would measure the runtime to determine if it matches the claimed $O(n)$ complexity. For comparison, we could use the same test cases with other well-known algorithms, such as QuickSort or MergeSort, to see how the proprietary algorithm performs relative to established benchmarks. Additionally, empirical testing should include edge cases, such as empty lists or single-element lists, and stress testing with very large inputs to assess the algorithm's scalability and robustness.

The second part of the evaluation would involve theoretical testing. From what we know, the lower bound for comparison-based sorting is $\Omega(n \log n)$ in the worst case, meaning that any general-purpose sorting algorithm relying purely on comparisons cannot perform better than this bound. If the proprietary algorithm truly sorts arbitrary elements in $O(n)$ time, there are two possible explanations: either the claim is false, or this represents a groundbreaking discovery in computer science. It is also possible that the algorithm does not function as a true comparison-based sorting algorithm but instead uses other techniques, such as exploiting properties of the input (e.g., bounded integers or specific structures), which would limit its general applicability.

By combining these two approaches, we can thoroughly investigate the validity of the claim. If the algorithm is genuinely comparison-based, the $O(n)$ claim would contradict established theoretical limits, making it highly unlikely. However, if the algorithm is not purely general-purpose, it might achieve $O(n)$ for specific cases while not fulfilling its broad claims.

I expect to see runtimes that are simialr to other algorithms with the claim of $O(n)$, we should see the runtime increase lineraly as the input grows. I will also expect consistency with testing and make sure as the stress of the tests increase for results to stay consistent. 

## Sources 
I used the lecture sides in sorting focusing on the theortical section of the slides for the information of bounds. 

I certify that I have listed all sources used to complete this exercise, including the use of any Large Language Models. All of the work is my own, except where stated otherwise. I am aware that plagiarism carries severe penalties and that if plagiarism is suspected, charges may be filed against me without prior notice. 
