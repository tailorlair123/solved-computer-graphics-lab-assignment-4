Download Link: https://assignmentchef.com/product/solved-computer-graphics-lab-assignment-4
<br>
<strong>Computer Graphics, Lab Assignment 4 </strong>

+ LabAssignment2/

+ 1/

<ul>

 <li>py</li>

</ul>

+ 2/

<ul>

 <li>py</li>

</ul>

+ 3/

<ul>

 <li>py</li>

</ul>




<ul>

 <li>The submission time is determined not when the commit is made but when the git push is made.</li>

</ul>




<ol>

 <li>Write down a Python program to draw a transformed triangle in a 2D space.</li>

 <li>Set the window title to <strong>your student ID</strong> and the window size to (480,480).</li>

 <li>Complete the render() function below to draw a triangle in the manner described in C.</li>

 <li><strong> You have to use OpenGL transformation functions. Do not use numpy matrix multiplication for composing transformations. </strong></li>

</ol>

<table width="451">

 <tbody>

  <tr>

   <td width="451">

    <table width="251">

     <tbody>

      <tr>

       <td width="104"><strong>def</strong> render<strong>():</strong></td>

       <td colspan="2" width="147"> </td>

      </tr>

      <tr>

       <td colspan="3" width="251">    glClear<strong>(</strong>GL_COLOR_BUFFER_BIT<strong>)</strong></td>

      </tr>

      <tr>

       <td colspan="2" width="155">    glLoadIdentity<strong>()</strong></td>

       <td width="96"> </td>

      </tr>

      <tr>

       <td width="104"></td>

       <td width="51"></td>

       <td width="96"></td>

      </tr>

     </tbody>

    </table> # draw cooridnates     glBegin<strong>(</strong>GL_LINES<strong>)</strong>     glColor3ub<strong>(</strong>255<strong>,</strong> 0<strong>,</strong> 0<strong>)</strong>     glVertex2fv<strong>(</strong>np<strong>.</strong>array<strong>([</strong>0.<strong>,</strong>0.<strong>]))</strong>     glVertex2fv<strong>(</strong>np<strong>.</strong>array<strong>([</strong>1.<strong>,</strong>0.<strong>]))</strong>     glColor3ub<strong>(</strong>0<strong>,</strong> 255<strong>,</strong> 0<strong>)</strong>     glVertex2fv<strong>(</strong>np<strong>.</strong>array<strong>([</strong>0.<strong>,</strong>0.<strong>]))</strong>     glVertex2fv<strong>(</strong>np<strong>.</strong>array<strong>([</strong>0.<strong>,</strong>1.<strong>]))</strong>     glEnd<strong>()</strong> glColor3ub<strong>(</strong>255<strong>,</strong> 255<strong>,</strong> 255<strong>)</strong>


    <table width="243">

     <tbody>

      <tr>

       <td colspan="2" width="243">    ###########################</td>

      </tr>

      <tr>

       <td width="155">    # implement here</td>

       <td width="88"> </td>

      </tr>

      <tr>

       <td colspan="2" width="243">    ###########################</td>

      </tr>

     </tbody>

    </table> drawTriangle<strong>()</strong>


    <table width="267">

     <tbody>

      <tr>

       <td colspan="2" width="152"><strong>def</strong> drawTriangle<strong>():</strong></td>

       <td colspan="2" width="115"> </td>

      </tr>

      <tr>

       <td colspan="3" width="195">    glBegin<strong>(</strong>GL_TRIANGLES<strong>)</strong></td>

       <td width="72"> </td>

      </tr>

      <tr>

       <td colspan="4" width="267">    glVertex2fv<strong>(</strong>np<strong>.</strong>array<strong>([</strong>0.<strong>,</strong>.5<strong>])) </strong>    glVertex2fv<strong>(</strong>np<strong>.</strong>array<strong>([</strong>0.<strong>,</strong>0.<strong>])) </strong>    glVertex2fv<strong>(</strong>np<strong>.</strong>array<strong>([</strong>.5<strong>,</strong>0.<strong>]))</strong></td>

      </tr>

      <tr>

       <td width="83">    glEnd<strong>()</strong></td>

       <td colspan="3" width="184"> </td>

      </tr>

      <tr>

       <td width="83"></td>

       <td width="69"></td>

       <td width="43"></td>

       <td width="72"></td>

      </tr>

     </tbody>

    </table></td>

  </tr>

 </tbody>

</table>

<ol>

 <li>If you press or repeat a key, the triangle should be transformed as shown in the Table:</li>

</ol>

<table width="433">

 <tbody>

  <tr>

   <td width="36"><strong>Key </strong></td>

   <td width="397"><strong>Transformation </strong></td>

  </tr>

  <tr>

   <td width="36">Q</td>

   <td width="397">Translate by -0.1 in  x direction</td>

  </tr>

  <tr>

   <td width="36">E</td>

   <td width="397">Translate by 0.1 in x direction</td>

  </tr>

  <tr>

   <td width="36">A</td>

   <td width="397">Rotate by 10 degrees counterclockwise</td>

  </tr>

  <tr>

   <td width="36">D</td>

   <td width="397">Rotate by 10 degrees clockwise</td>

  </tr>

  <tr>

   <td width="36">1</td>

   <td width="397">Reset the triangle with identity matrix</td>

  </tr>

 </tbody>

</table>

<ol>

 <li>Transformations should be accumulated (composed with previous one) unless you press ‘1’.</li>

 <li>You may need a global variable (like a python list object) to store key inputs.</li>

 <li>Files to submit: A Python source file (Name the file whatever you want (in English). Extension should be .py) F.Expected result:</li>

</ol>




<ol start="2">

 <li>Write down a Python program to draw rotating point p=(0.5, 0) and vector v=(0.5, 0) in a 2D space.</li>

 <li>Set the window title to <strong>your student ID</strong> and the window size to (480,480).</li>

 <li>Use the following render() and fill “# your implementation” parts to render p and v.</li>

 <li>Hint: Render the vector v as a line segment starting from the origin (0,0).</li>

</ol>

<table width="451">

 <tbody>

  <tr>

   <td width="451">

    <table width="251">

     <tbody>

      <tr>

       <td width="112"><strong>def</strong> render<strong>(</strong>M<strong>):</strong></td>

       <td colspan="2" width="139"> </td>

      </tr>

      <tr>

       <td colspan="3" width="251">    glClear<strong>(</strong>GL_COLOR_BUFFER_BIT<strong>)</strong></td>

      </tr>

      <tr>

       <td colspan="2" width="155">    glLoadIdentity<strong>()</strong></td>

       <td width="96"> </td>

      </tr>

      <tr>

       <td width="112"></td>

       <td width="43"></td>

       <td width="96"></td>

      </tr>

     </tbody>

    </table>


    <table width="267">

     <tbody>

      <tr>

       <td colspan="2" width="163">    # draw cooridnate     glBegin<strong>(</strong>GL_LINES<strong>)</strong></td>

       <td colspan="2" width="104">  </td>

      </tr>

      <tr>

       <td colspan="3" width="195">    glColor3ub<strong>(</strong>255<strong>,</strong> 0<strong>,</strong> 0<strong>)</strong></td>

       <td width="72"> </td>

      </tr>

      <tr>

       <td colspan="4" width="267">    glVertex2fv<strong>(</strong>np<strong>.</strong>array<strong>([</strong>0.<strong>,</strong>0.<strong>])) </strong>    glVertex2fv<strong>(</strong>np<strong>.</strong>array<strong>([</strong>1.<strong>,</strong>0.<strong>]))</strong></td>

      </tr>

      <tr>

       <td colspan="3" width="195">    glColor3ub<strong>(</strong>0<strong>,</strong> 255<strong>,</strong> 0<strong>)</strong></td>

       <td width="72"> </td>

      </tr>

      <tr>

       <td colspan="4" width="267">    glVertex2fv<strong>(</strong>np<strong>.</strong>array<strong>([</strong>0.<strong>,</strong>0.<strong>])) </strong>    glVertex2fv<strong>(</strong>np<strong>.</strong>array<strong>([</strong>0.<strong>,</strong>1.<strong>]))</strong></td>

      </tr>

      <tr>

       <td width="83">    glEnd<strong>()</strong></td>

       <td colspan="3" width="184"> </td>

      </tr>

      <tr>

       <td width="83"></td>

       <td width="80"></td>

       <td width="32"></td>

       <td width="72"></td>

      </tr>

     </tbody>

    </table> glColor3ub<strong>(</strong>255<strong>,</strong> 255<strong>,</strong> 255<strong>)</strong>


    <table width="195">

     <tbody>

      <tr>

       <td colspan="2" width="139">    # draw point p</td>

       <td colspan="2" width="56"> </td>

      </tr>

      <tr>

       <td colspan="3" width="171">    glBegin<strong>(</strong>GL_POINTS<strong>)</strong></td>

       <td width="24"> </td>

      </tr>

      <tr>

       <td colspan="4" width="195"><strong>    </strong><strong># your implementation</strong></td>

      </tr>

      <tr>

       <td width="83">    glEnd<strong>()</strong></td>

       <td colspan="3" width="112"> </td>

      </tr>

      <tr>

       <td width="83"></td>

       <td width="56"></td>

       <td width="32"></td>

       <td width="24"></td>

      </tr>

     </tbody>

    </table>


    <table width="195">

     <tbody>

      <tr>

       <td colspan="3" width="147">    # draw vector v</td>

       <td colspan="2" width="48"> </td>

      </tr>

      <tr>

       <td colspan="4" width="163">    glBegin<strong>(</strong>GL_LINES<strong>)</strong></td>

       <td width="32"> </td>

      </tr>

      <tr>

       <td width="27"> </td>

       <td colspan="4" width="168"><strong># your implementation</strong></td>

      </tr>

      <tr>

       <td colspan="2" width="83">    glEnd<strong>()</strong></td>

       <td colspan="3" width="112"> </td>

      </tr>

      <tr>

       <td width="27"></td>

       <td width="56"></td>

       <td width="64"></td>

       <td width="16"></td>

       <td width="32"></td>

      </tr>

     </tbody>

    </table></td>

  </tr>

 </tbody>

</table>

<ol>

 <li>Expected result: Uploaded LabAssignment5-1.mp4</li>

 <li>Do not mind the initial angle.</li>

 <li>p and v should be t rad rotated when t seconds have elapsed since the program was executed.</li>

 <li>You need to somehow combine a rotation matrix and a translation matrix to produce the expected result.</li>

 <li>Files to submit: A Python source file (Name the file whatever you want (in English). Extension should be .py)</li>

</ol>


