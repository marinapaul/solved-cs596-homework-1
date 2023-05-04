Download Link: https://assignmentchef.com/product/solved-cs596-homework-1
<br>
<strong>Problem 1: </strong>Consider the matrix

<ol>

 <li>a) Find the eigenvalues/eigenvectors of <em>A </em>assuming = 0. Force your eigenvectors to have unit norm. b) Diagonalize <em>A </em>using the eigenvalues/eigenvectors you computed. c) Start now sending</li>

 <li>What do you observe is happening to the matrices you use for diagonalization as becomes smaller and smaller? So what do you conclude when = 0?</li>

</ol>

<strong>Problem 2: </strong>Let <em>A,B </em>be two matrices of the same dimensions <em>k </em>×<em>m</em>. a) With direct computation show that trace(<em>AB</em><sup>|</sup>) = trace(<em>B</em><sup>|</sup><em>A</em>) = trace(<em>BA</em><sup>|</sup>) = trace(<em>A</em><sup>|</sup><em>B</em>). b) Use question a) to compute E[<strong>x</strong><sup>|</sup><em>A</em><strong>x</strong>] where E[·] denotes expectation, <em>A </em>is a constant matrix and <strong>x </strong>is a random vector for which we know that E[<strong>xx</strong><sup>|</sup>] = <em>Q</em>. <em>Hint: The trace of a scalar is the scalar itself. Trace and expectation are linear operations, so we can change their order of application. </em>c) Using the previous properties show that for any matrix <em>A </em>of dimensions <em>k </em>× <em>k </em>we have trace(<em>A</em>) = trace(<em>UAU</em><sup>−1</sup>) for any nonsingular matrix <em>U </em>of dimensions <em>k</em>×<em>k</em>. In other words that the trace does not change if we apply a similarity transformation. d) Use question c) to prove that if matrix <em>A </em>of dimensions <em>k </em>× <em>k </em>is diagonalizable then its trace is equal to the sum of its eigenvalues (actually this is true even if the matrix is not diagonalizable). e) Regarding question d) how do you explain this equality given that when <em>A </em>is real the trace is also real whereas the eigenvalues can be complex? f) Using again question d) what can you say about the coefficient <em>c<sub>k</sub></em><sub>−1 </sub>of the characteristic polynomial <em>λ<sup>k </sup></em>+ <em>c<sub>k</sub></em><sub>−1</sub><em>λ<sup>k</sup></em><sup>−1 </sup>+ ··· + <em>c</em><sub>0 </sub>of <em>A</em>. We recall that we already know that <em>c</em><sub>0 </sub>= (−1)<em><sup>k</sup>λ</em><sub>1 </sub>···<em>λ<sub>k </sub></em>= (−1)<em><sup>k </sup></em>det(<em>A</em>).

<strong>Problem 3: </strong>A matrix <em>A </em>is called <em>nilpotent </em>if <em>A<sup>r </sup></em>= 0 for some integer <em>r &gt; </em>1. a) Show that all eigenvalues of <em>A </em>must be equal to 0. b) Is such a matrix diagonalizable? c) Give an example of a 2 × 2 matrix which is nilpotent. c) If we apply a similarity transformation to a nilpotent is the resulting matrix nilpotent? Apply the previous observation to your example in c) to obtain a second example of a nilpotent matrix.

<strong>Problem 4: </strong>There is clock and at each period of the clock you obtain a new pair (<em>y<sub>t</sub>,X<sub>t</sub></em>) where <em>y<sub>t </sub></em>is scalar and <em>X<sub>t </sub></em>vector. We are interested in modeling <em>y </em>as a cross product of <em>X </em>with a vector <em>A</em>

<em>y<sub>n </sub></em>= <em>X<sub>n</sub></em><sup>|</sup><em>A </em>+ <em>e<sub>n</sub>, </em>for <em>n </em>= 1<em>,</em>2<em>,…,t</em>

where {<em>e<sub>n</sub></em>} denotes the error term between the model <em>X<sub>n</sub></em><sup>|</sup><em>A </em>and the target value <em>y<sub>n</sub></em>. At each time <em>t </em>we have available the data (<em>y<sub>t</sub>,X<sub>t</sub></em>)<em>,</em>(<em>y<sub>t</sub></em><sub>−1</sub><em>,X<sub>t</sub></em><sub>−1</sub>)<em>,…,</em>(<em>y</em><sub>1</sub><em>,X</em><sub>1</sub>) and we would like to find the best <em>A </em>the minimizes the sum of the squared errors, namely perform the minimization

<em>t</em>

<table width="624">

 <tbody>

  <tr>

   <td width="605">minX(<em>y</em><em>n </em>− <em>X</em><em>n</em>|<em>A</em>)2<em>A n</em>=1a) Show that if <em>A<sub>t </sub></em>denotes the solution, at time <em>t</em>, of the optimization in (1) then</td>

   <td width="19">(1)</td>

  </tr>

  <tr>

   <td width="605">                                                                              <em>t                                           t</em><em>A</em><em>t </em>= <em>R</em><em>t</em>−1<em>U</em><em>t, </em>where <em>R</em><em>t </em>= X<em>X</em><em>nX</em><em>n</em>|<em>,                      U</em><em>t </em>= X<em>y</em><em>nX</em><em>n.</em></td>

   <td width="19">(2)</td>

  </tr>

 </tbody>

</table>

<em>n</em>=1                                      <em>n</em>=1

<ol>

 <li>At the next time instant <em>t</em>+1 when we receive the new pair (<em>y<sub>t</sub></em><sub>+1</sub><em>,X<sub>t</sub></em><sub>+1</sub>) we need to reapply the formula in (2) to compute the new estimate <em>A<sub>t</sub></em><sub>+1</sub>. Express the computational complexity in terms of the size <em>k </em>of the vector <em>X<sub>t</sub></em>.</li>

 <li>Show that we can compute <em>A<sub>t</sub></em><sub>+1 </sub>by using the previous <em>A<sub>t </sub></em>and applying the following updating formulas</li>

</ol>

<em>e<sub>t</sub></em>+1 = <em>y<sub>t</sub></em>+1 − <em>X<sub>t</sub></em>|+1<em>A<sub>t</sub>,                K<sub>t</sub></em>+1 = <em>Q<sub>t</sub>X<sub>t</sub></em>+1<em>,                γ<sub>t</sub></em>+1 = 1 + <em>X<sub>t</sub></em>|+1<em>K<sub>t</sub></em>+1<em>,</em>

<em>,</em>

where <em>Q<sub>t </sub></em>= <em>R<sub>t</sub></em><sup>−1</sup>. What is the complexity of the algorithm in terms of <em>k</em>? This recursive algorithm is known as <em>Recursive Least Squares (RLS) </em>and is one of the most famous learning algorithms in the literature. <em>Hint: To prove the validity of RLS you need to apply the matrix inversion lemma onto R<sub>t</sub></em><sub>+1 </sub>= <em>R<sub>t </sub></em>+<em>X<sub>t</sub></em><sub>+1</sub><em>X<sub>t</sub></em><sup>|</sup><sub>+1 </sub><em>in order to compute Q<sub>t</sub></em><sub>+1 </sub><em>in terms of Q<sub>t</sub>. From </em>(2) <em>you must also use the fact that U</em><em>t</em>+1 = <em>U</em><em>t </em>+ <em>y</em><em>t</em>+1<em>X</em><em>t</em>+1 <em>and A</em><em>t</em>+1 = <em>Q</em><em>t</em>+1<em>U</em><em>t</em>+1<em>.</em>

<strong>There is a meeting on Friday, September 27, at 5PM, in CoRE-101 to discuss YOUR questions. Mr. Anastasios Stathopoulos, our TA, will answer them.</strong>

<strong>Your reports, in </strong><em>hard copy</em><strong>, are due on Monday, September 30, in CBIM, between 10:00 and 11:00AM. Mr Stathopoulos will collect them.</strong>

<strong>Please STRICTLY respect the indicated time period because Mr. Stathopoulos has many other tasks, besides TAing. Late/Early submission will NOT be accepted neither by the TA nor by me.</strong>


