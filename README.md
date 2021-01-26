<div data-v-5e9078c0=""><h1 data-v-5e9078c0="">
      Top 12 Heaps and Maps interview
      questions and answers in 2021.
    </h1> <p data-v-5e9078c0="" align="center"><a data-v-5e9078c0="" href="https://devinterview.io/"><img data-v-5e9078c0="" src="https://source.unsplash.com/collection/52661698/700x350"></a></p> <p data-v-5e9078c0="">
      You can check all
      12
      Heaps and Maps interview questions here 👉
      https://devinterview.io/data/heapsAndMaps-interview-questions
    </p> <br data-v-5e9078c0=""> <div data-v-5e9078c0="" class="unit"><div><h2>🔹 1. What is Priority Queue?</h2></div> <div><h3>Answer:</h3> <div class="answer"><div><div><div class="AnswerBody"><p>A <strong>priority queue</strong> is a data structure that stores <strong>priorities</strong> (comparable values) and perhaps associated information.  A <strong>priority queue</strong> is different from a "normal" queue, because instead of being a "first-in-first-out" data structure, values come out in order by <strong>priority</strong>. Think of a priority queue as a kind of bag that holds priorities. You can put one in, and you can take out the current highest priority.</p><p></p><div><div><div><div></div></div></div></div><p></p></div></div><div class="row my-2"><div><span><i>Source:</i>&nbsp;<span><a href="http://pages.cs.wisc.edu/~vernon/cs367/notes/11.PRIORITY-Q.html" rel="noreferrer" target="_blank" title="What is Priority Queue? Interview Questions Source To Answer">pages.cs.wisc.edu</a></span></span>&nbsp; &nbsp;</div></div></div></div></div> <br><br></div><div data-v-5e9078c0="" class="unit"><div><h2>🔹 2. What is Heap?</h2></div> <div><h3>Answer:</h3> <div class="answer"><div><div><div class="AnswerBody"><p>A <strong>Heap</strong> is a special Tree-based data structure which is an almost complete tree that satisfies the heap property:</p><ul><li>in a <strong>max heap</strong>, for any given node C, if P is a parent node of C, then the key (the value) of P is greater than or equal to the key of C. </li><li>In a <strong>min heap</strong>, the key of P is less than or equal to the key of C. The node at the "top" of the heap (with no parents) is called the root node.</li></ul><p>A common implementation of a heap is the binary heap, in which the tree is a <strong>binary tree.</strong></p><p></p><div><div><div><div></div></div></div></div><p></p></div></div><div class="row my-2"><div><span><i>Source:</i>&nbsp;<span><a href="https://www.geeksforgeeks.org/heap-data-structure/" rel="noreferrer" target="_blank" title="What is Heap? Interview Questions Source To Answer">www.geeksforgeeks.org</a></span></span>&nbsp; &nbsp;</div></div></div></div></div> <br><br></div><div data-v-5e9078c0="" class="unit"><div><h2>🔹 3. How is Binary Heap usually implemented?</h2></div> <div><h3>Answer:</h3> <div class="answer"><div><div><div class="AnswerBody"><p>A <strong>binary heaps</strong> are commonly implemented with an <strong>array</strong>. Any binary tree can be stored in an array, but because a binary heap is always a <em>complete</em> binary tree, it can be stored compactly. No space is required for pointers; instead, the parent and children of each node can be found by arithmetic on array indices:</p><ul><li>The root element is <code>0</code></li><li>Left child : <code>(2*i)+1</code></li><li>Right child : <code>(2*i)+2</code></li><li>Parent child : <code>(i-1)/2</code></li></ul><p></p><div><div><div><div></div></div></div></div><p></p></div></div><div class="row my-2"><div><span><i>Source:</i>&nbsp;<span><a href="https://www.geeksforgeeks.org/binary-heap/" rel="noreferrer" target="_blank" title="How is Binary Heap usually implemented? Interview Questions Source To Answer">www.geeksforgeeks.org</a></span></span>&nbsp; &nbsp;</div></div></div></div></div> <br><br></div><div data-v-5e9078c0="" class="unit"><div><h2>🔹 4. What is Binary Heap?</h2></div> <div><h3>Answer:</h3> <div class="answer"><div><div><div class="AnswerBody"><p>A <strong>Binary Heap</strong> is a <em>Binary Tree</em> with following properties:</p><ul><li>It’s a <em>complete</em> tree (all levels are completely filled except possibly the last level and the last level has all keys as left as possible). This property of Binary Heap makes them suitable to be stored in an array.</li><li>A Binary Heap is either <strong>Min Heap</strong> or <strong>Max Heap</strong>. In a Min Binary Heap, the key at root must be minimum among all keys present in Binary Heap. The same property must be recursively true for all nodes in Binary Tree. Max Binary Heap is similar to MinHeap.</li></ul><pre><code>            <span class="token cNum">10</span>                      <span class="token cNum">10</span>
         <span class="token cBase">/</span>      \               <span class="token cBase">/</span>       \  
       <span class="token cNum">20</span>        <span class="token cNum">100</span>          <span class="token cNum">15</span>         <span class="token cNum">30</span>  
      <span class="token cBase">/</span>                      <span class="token cBase">/</span>  \        <span class="token cBase">/</span>  \
    <span class="token cNum">30</span>                     <span class="token cNum">40</span>    <span class="token cNum">50</span>    <span class="token cNum">100</span>   <span class="token cNum">40</span></code></pre></div></div><div class="row my-2"><div><span><i>Source:</i>&nbsp;<span><a href="https://www.geeksforgeeks.org/binary-heap/" rel="noreferrer" target="_blank" title="What is Binary Heap? Interview Questions Source To Answer">www.geeksforgeeks.org</a></span></span>&nbsp; &nbsp;</div></div></div></div></div> <br><br></div><div data-v-5e9078c0="" class="unit"><div><h2>🔹 5. Insert item into the Heap. Explain your actions.</h2></div> <div><h3>Answer:</h3> <div class="answer"><div><div class="mb-2"><span class="h5">Problem</span></div><div><div class="AnswerBody"><p>Suppose I have a Heap Like the following:</p><pre><code>     77
    /  \
   /    \
  50    60
 / \    / \
22 30  44 55</code></pre><p>Now, I want to insert another item 55 into this Heap. How to do this?</p></div></div><div><div class="AnswerBody"><p>A <strong>binary heap</strong> is defined as a binary tree with two additional constraints:</p><ul><li><strong>Shape property</strong>: a binary heap is a complete binary tree; that is, all levels of the tree, except possibly the last one (deepest) are fully filled, and, if the last level of the tree is not complete, the nodes of that level are filled from left to right.</li><li><strong>Heap property</strong>: the key stored in each node is either greater than or equal to (≥) or less than or equal to (≤) the keys in the node's children, according to some total order.</li></ul><p>We start adding child from the most left node and if the parent is lower than the newly added child than we replace them. And like so will go on until the child got the parent having value greater than it.</p><p>Your initial tree is:</p><pre><code>     <span class="token cNum">77</span>
    <span class="token cBase">/</span>  \
   <span class="token cBase">/</span>    \
  <span class="token cNum">50</span>    <span class="token cNum">60</span>
 <span class="token cBase">/</span> \    <span class="token cBase">/</span> \
<span class="token cNum">22</span> <span class="token cNum">30</span>  <span class="token cNum">44</span> <span class="token cNum">55</span></code></pre><p>Now adding 55 according to the rule on most left side:</p><pre><code>     77
    /  \
   /    \
  50    60
 / \    / \
22 30  44 55
/
55</code></pre><p>But you see 22 is lower than 55 so replaced it:</p><pre><code>       77
      /  \
     /    \
    50    60
   / \    / \
  55 30  44 55
 /
22 </code></pre><p>Now 55 has become the child of 50 which is still lower than 55 so replace them too:</p><pre><code>       77
      /  \
     /    \
    55    60
   / \    / \
  50 30  44 55
 /
22</code></pre><p>Now it cant be sorted more because 77 is greater than 55.</p></div></div><div class="row my-2"><div><span><i>Source:</i>&nbsp;<span><a href="https://stackoverflow.com/questions/6482039/how-to-create-a-heap" rel="noreferrer" target="_blank" title="Insert item into the Heap. Explain your actions. Interview Questions Source To Answer">stackoverflow.com</a></span></span>&nbsp; &nbsp;</div></div></div></div></div> <br><br></div><div data-v-5e9078c0="" class="unit"><div><h2>🔹 6. When would you want to use a Heap?</h2></div> <div>
    👉🏼 Check
    <a href="https://devinterview.io/data/heapsAndMaps-interview-questions">all 12 answers</a></div> <br><br></div><div data-v-5e9078c0="" class="unit"><div><h2>🔹 7. Compare Heaps vs Arrays to implement Priority Queue</h2></div> <div>
    👉🏼 Check
    <a href="https://devinterview.io/data/heapsAndMaps-interview-questions">all 12 answers</a></div> <br><br></div><div data-v-5e9078c0="" class="unit"><div><h2>🔹 8. What is the advantage of Heaps over Sorted Arrays?</h2></div> <div>
    👉🏼 Check
    <a href="https://devinterview.io/data/heapsAndMaps-interview-questions">all 12 answers</a></div> <br><br></div><div data-v-5e9078c0="" class="unit"><div><h2>🔹 9. Name some ways to implement Priority Queue</h2></div> <div>
    👉🏼 Check
    <a href="https://devinterview.io/data/heapsAndMaps-interview-questions">all 12 answers</a></div> <br><br></div><div data-v-5e9078c0="" class="unit"><div><h2>🔹 10. Explain how Heap Sort works</h2></div> <div>
    👉🏼 Check
    <a href="https://devinterview.io/data/heapsAndMaps-interview-questions">all 12 answers</a></div> <br><br></div><div data-v-5e9078c0="" class="unit"><div><h2>🔹 11. Explain how to find 100 largest numbers out of an array of 1 billion numbers</h2></div> <div>
    👉🏼 Check
    <a href="https://devinterview.io/data/heapsAndMaps-interview-questions">all 12 answers</a></div> <br><br></div><div data-v-5e9078c0="" class="unit"><div><h2>🔹 12. What is the difference between Heap and Red-Black Tree?</h2></div> <div>
    👉🏼 Check
    <a href="https://devinterview.io/data/heapsAndMaps-interview-questions">all 12 answers</a></div> <br><br></div> <div data-v-5e9078c0="" class="end"></div> <br data-v-5e9078c0="">
    Thanks 🙌 for reading and good luck on your next tech interview!
    <br data-v-5e9078c0="">
    Explore 3800+ dev interview question here 👉
    <a data-v-5e9078c0="" href="https://devinterview.io/">Devinterview.io</a></div>
