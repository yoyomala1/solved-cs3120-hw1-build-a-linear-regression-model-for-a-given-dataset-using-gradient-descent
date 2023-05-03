Download Link: https://assignmentchef.com/product/solved-cs3120-hw1-build-a-linear-regression-model-for-a-given-dataset-using-gradient-descent
<br>
(NumPy and data visualization packages are allowed.)

(Existing Linear Regression Model from any library/package is NOT allowed!)

<ol>

 <li>Import numpy and matplotlib.pyplot first in your python code</li>

</ol>

Installation could be done by pip3  (e.g. “pip3 install numpy”)

e.g.

<em>import numpy as np</em>

<em>import matplotlib.pyplot as plt</em>




<ol start="2">

 <li><strong>Generate data samples</strong>: generate 10 pair of data samples that satisfying</li>

</ol>

Y=2*X + 50 + a small random number

e.g.

<em>import numpy as np</em>

<em>x_data = np.array([35., 38., 31., 20., 22., 25., 17., 60., 8., 60.])</em>

<em>y_data = 2*x_data+50+5*np.random.random()</em>

X could be within any range, stored as an array (using numpy.array)




<ol start="3">

 <li><strong>Plot the landscape of the loss function. (2pts)</strong></li>

</ol>

For example, the following code will print the landscape of Z[i][j]. Z is the loss function value of different <em>ww</em> and <em>bb</em> values.

X_data and y_data are the arrays of your samples.

e.g.

<em>bb = np.arange(0,100,1) #bias</em>

<em>ww = np.arange(-5, 5,0.1) #weight</em>

<em>Z = np.zeros((len(bb),len(ww)))</em>

<em> </em>

<em>for i in range(len(bb)):</em>

<em>    for j in range(len(ww)):</em>

<em>        b = bb[i]</em>

<em>        w = ww[j]</em>

<em>        Z[j][i] = 0        </em>

<em>        for n in range(len(x_data)):</em>

<em>            Z[j][i] = Z[j][i] + (w*x_data[n]+b – y_data[n])**2 # this is the loss </em>

<em>        Z[j][i] = Z[j][i]/len(x_data)</em>







<ol start="4">

 <li>Build a linear regression model that minimizing the loss for the given dataset using “gradient descent” algorithm introduced in lecture2.<strong> (4pts)</strong></li>

</ol>

<table>

 <tbody>

  <tr>

   <td width="242"></td>

  </tr>

  <tr>

   <td></td>

   <td width="179">

    <table width="100%">

     <tbody>

      <tr>

       <td> –</td>

      </tr>

     </tbody>

    </table></td>

  </tr>

 </tbody>

</table>

<strong> </strong>

<strong> </strong>

<strong> </strong>




Randomly pick some weights to start the “gradient descent” process.

e.g.

<em>b = 0 # initial b</em>

<em>w = 0 # initial w</em>

<strong> </strong>

<strong> </strong>

<strong>Explain how your gradient descent process was terminated (e.g. by testing convergence or finishing certain number of iterations) and explain all threshold values you used in your report.    (1pt)</strong>

<strong> </strong>




<ol start="5">

 <li>Test different values of the learning rate “lr” and different number of iterations/convergence threshold values.</li>

</ol>

<strong>Explain how these values affect your program in your report.  (1pts)</strong>

e.g.

<em>lr = 0.0001 # example learning rate</em>

<em>iteration = 10000 # example iteration number</em>




<ol start="6">

 <li><strong>Track the change of the weight values (w and b) from each iteration and plot all the values out. (2pts)</strong></li>

</ol>

e.g.

<em># Store parameters for plotting</em>

<em>b_history = [b]</em>

<em>w_history = [w]</em>

<em># model by gradient descent</em>

<em>#…</em>

<em>b_history.append(b)</em>

<em>w_history.append(w)</em>

<em>#…</em>

<em>plt.plot(b_history, w_history, ‘o-‘, ms=3, lw=1.5,color=’black’)</em>

<em> </em>

<em>Example track change figure:</em>

<strong> </strong>

<ol start="7">

 <li><strong>Bonus (up to 2pts)</strong></li>

</ol>

<strong>Compare the prediction result using your model with the given target values (Y values)</strong>

<strong>Or </strong>

<strong>Any other type of model performance testing.</strong>

<em>——————————————————————————————————————–</em>

<strong>Submit your report and your code in two different files. </strong>

<strong>Please include the figure of your plot in your report.</strong>

<strong>e.g.</strong>

<strong>Assignment1_FengJiang.doc/.pdf (this is the report)</strong>

<strong>Assignment1_FengJiang.py (this is the code. only “.py” files accepted.)</strong>