### Linear Algebra tricks II

Remember the linear algebra trick of yesterday? Lets use it again! 
If you add a column of ones to the vector $x$, for any example i in our new matrix $X\text{'}$, $X\text{'}_{i}^{(0)} = 1$.  
  
Therefore:  

$$
\nabla(J)_0 = \frac{1}{m}\sum_{i=1}^{m}(h_{\theta}(X\text{'}_i) - y^{(i)}) \\
\nabla(J)_0 = \frac{1}{m}\sum_{i=1}^{m}(h_{\theta}(X\text{'}_i) - y^{(i)}) \cdot 1 \\
\nabla(J)_0 = \frac{1}{m}\sum_{i=1}^{m}(h_{\theta}(X\text{'}_i) - y^{(i)})X\text{'}_{i}^{(0)}
$$

This means that you can encapsulate the gradient for both $\theta_0$ and $\theta_1$ with the same calculation! 
$$
\nabla(J)_j = \frac{1}{m}\sum_{i=1}^{m}(h_{\theta}(X\text{'}_i) - y^{(i)})X\text{'}_{i}^{(j)} \text{ for j = 0, 1}
$$

And thus (using more linear algebra):  

$$
\nabla(J)_j = \frac{1}{m} (X\text{'}\theta - y)X\text{'}^{(j)} \text{ for j = 0, 1}\\
\nabla(J) = \frac{1}{m} X\text{'}^T(X\text{'}\theta - y)
$$  

If it does not seems obvious, play a bit with your vectors until you get it. 