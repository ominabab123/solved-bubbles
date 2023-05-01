Download Link: https://assignmentchef.com/product/solved-bubbles
<br>
Consider the world of bubbles. We will only consider red and blue bubbles for now. First, look at what is in the provided abstract Bubble class. Your task will be to implement two subclasses: RedBubble and BlueBubble. Their behaviour is described below.

Do not change the Bubble class.

RedBubble

Red bubbles bounce of the world boundaries and like to eat blue bubbles. They will move towards (chase) the closest blue bubble in the world. This class should have the constructor

<pre class="ql-syntax"><span class="hljs-function"><span class="hljs-keyword">public</span> <span class="hljs-title">RedBubble</span><span class="hljs-params">(<span class="hljs-keyword">int</span> x, <span class="hljs-keyword">int</span> y, <span class="hljs-keyword">int</span> speedX, <span class="hljs-keyword">int</span> speedY, <span class="hljs-keyword">double</span> radius, <span class="hljs-keyword">int</span> health)</span></span></pre>

that sets its attributes based on the input parameters, and also sets its colour attribute to red (Bubble.COLOURS[0]).

The logic of a red bubble (applyLogic) is defined as follows:

<ul>

 <li>red bubbles ignore each other. They can overlap in space and do nothing when they collide.</li>

 <li>red bubbles will chase (move towards) the closest blue bubble in the world.</li>

 <li>when a red bubble collides with a blue bubble (catches a blue bubble), the blue bubble gives all of its health points to the red bubble.</li>

 <li>red bubbles bounce off of the world boundaries in a natural way. For example, if a red ball hits one of the vertical walls (left or right), it negates its speedX value.</li>

</ul>

BlueBubble

Blue bubbles always stay on either the left side of the world or the right. When two blue bubbles collide, they <em>share</em> some health points.

This class should have the constructor

<pre class="ql-syntax"><span class="hljs-function"><span class="hljs-keyword">public</span> <span class="hljs-title">BlueBubble</span><span class="hljs-params">(<span class="hljs-keyword">int</span> x, <span class="hljs-keyword">int</span> y, <span class="hljs-keyword">int</span> speedX, <span class="hljs-keyword">int</span> speed, <span class="hljs-keyword">double</span> radius, <span class="hljs-keyword">int</span> health)</span></span></pre>

that sets its attributes based on the input parameters, and also sets its colour attribute to blue (Bubble.COLOURS[1]).

The logic of a blue bubble (applyLogic) is defined as follows:

<ul>

 <li>a blue bubble will always stay on the left 1/2 of the world or the right 1/2 of the world. They will bounce (in a natural way) off of the world boundaries and the invisible boundary that separates the left and right sides of the world.</li>

 <li></li>

 <li>blue bubbles reverse their direction whenever they collide with another bubble (of any colour).</li>

 <li></li>

 <li>when a blue bubble collides with a red bubble (as described above), it loses all of its health points.</li>

 <li></li>

 <li>when a blue bubble collides with another blue bubble, if one of the bubbles has 2 or more health points compared to the other, it gives one of them to the other. That is, they share health points.</li>

 <li></li>

 <li>if a blue bubble has zero health points, it stops moving. If another blue bubble collides with it, and shares a health point with it, it will start to move in a random direction.</li>

 <li></li>

 <li>a blue bubble is allowed to move 1.5 times faster than a red bubble. (Override the update method of the blue bubble class to allow for this.)</li>

</ul>