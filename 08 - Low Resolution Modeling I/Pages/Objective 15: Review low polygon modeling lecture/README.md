# Objective 15: Review low polygon modeling lecture

<p><iframe src="https://player.vimeo.com/video/452915573" width="960" height="540" allowfullscreen="allowfullscreen" allow="autoplay; fullscreen"></iframe></p>
<p>&nbsp;</p>
<h2><span style="font-weight: 400;">Low Poly in Today’s Industry</span></h2>
<p><span style="font-weight: 400;">As hardware has grown more powerful and software has grown more efficient, each generation we’re able to push the boundaries further and further. One big pitfall that many beginning game artists get caught up by is the level of detail expected in the game resolution mesh.&nbsp;</span></p>
<p><span style="font-weight: 400;">There is one big topic that always seems to be glaring us in the face:</span></p>
<p><strong>Polycount (or Triangle Count)</strong></p>
<p><span style="font-weight: 400;">It’s a scary topic that stems from the limitations of hardware in the early days of 3D games. But as each generation of hardware has hit the consumer market, we’ve been able to push further and further. The reality is that you can generally push your low poly a lot further than you might think you can.</span></p>
<p>&nbsp;</p>
<h2><span style="font-weight: 400;">Don’t Get Stuck in 2005</span></h2>
<p><span style="font-weight: 400;"><img src="https://vertexschool.instructure.com/courses/14/files/792/preview?verifier=9wwF6mktMYFuBdFDaeHkyrZ5P6qV0rlrSuCmTHrp" alt="image5.png" width="650" height="366" data-api-endpoint="https://vertexschool.instructure.com/api/v1/courses/14/files/792" data-api-returntype="File"></span></p>
<p><span style="font-weight: 400;">Many beginning game artists tend to get stuck in the idea that the current limitations for game art are the same as they were in previous generations. The instinct is to try to hit triangle counts that were typical of games from the PS3/XBox 360 era of games. Then they will get frustrated when their art doesn’t look as good as what they see in current gen games.</span></p>
<p><span style="font-weight: 400;">This is partly due to a wealth of information and forum posts on the internet from that era about triangle counts. As hardware has advanced, we’re able to push the triangle counts even further. With that evolution comes less conversation about triangle counts in general.&nbsp;</span></p>
<p><span style="font-weight: 400;">Let’s ask a question across a 15 year span:</span></p>
<p><strong>How many triangles should a low poly barrel have?</strong></p>
<ul>
<li style="list-style-type: none;">
<ul>
<li>
<strong>Answer in 2005:</strong><span style="font-weight: 400;"> 300 tris</span>
</li>
<li>
<strong>Answer in 2010:</strong><span style="font-weight: 400;"> 600 tris</span>
</li>
<li>
<strong style="font-family: inherit; font-size: 1rem;">Answer in 2020:</strong><span style="font-weight: 400;"> As many as it takes to capture the silhouette</span>
</li>
</ul>
</li>
</ul>
<p>&nbsp;</p>
<table style="border-collapse: collapse; width: 100%;" border="1">
<tbody>
<tr>
<td style="width: 100%;">
<h2 style="padding-left: 40px;"><span style="font-weight: 400;">Real World Examples of Exponential Growth</span></h2>
<p style="padding-left: 40px;"><span style="font-weight: 400;"><img src="https://vertexschool.instructure.com/courses/14/files/795/preview?verifier=ULo58LDUPO5ez9tVoBROokvqumMqPBdlcn53slqE" alt="image7.png" width="650" height="298" data-api-endpoint="https://vertexschool.instructure.com/api/v1/courses/14/files/795" data-api-returntype="File"></span></p>
<p style="padding-left: 40px;"><span style="font-weight: 400;">Let’s have a look at the evolution of Kratos from the God of War series.</span></p>
<ul>
<li style="list-style-type: none;">
<ul>
<li style="list-style-type: none;">
<ul>
<li>
<strong>God of War 2 (PS2):</strong><span style="font-weight: 400;"> 5700 triangles with gear</span>
</li>
<li>
<strong>God of War 3 (PS3):</strong><span style="font-weight: 400;"> 64,000 triangles with gear</span>
</li>
<li>
<strong>God of War 2018 (PS4):</strong><span style="font-weight: 400;"> 80,000 triangles without gear (up to 120k with gear)</span>
</li>
</ul>
</li>
</ul>
</li>
</ul>
</td>
</tr>
</tbody>
</table>
<p>&nbsp;</p>
<p><span style="font-weight: 400;">As you can see by the numbers from God Of War above, triangle count budgets have skyrocketed through the generations. Pushing the boundaries makes sense for main characters, but what about our props?</span></p>
<p><span style="font-weight: 400;">The main lesson to walk away with is that </span><strong>you shouldn’t get too hung up on triangle counts</strong><span style="font-weight: 400;">. Build whatever geometry is needed to</span><strong> capture the silhouette</strong><span style="font-weight: 400;">.&nbsp;</span></p>
<p><span style="font-weight: 400;">&nbsp;</span></p>
<h2><span style="font-weight: 400;">Capturing the Silhouette</span></h2>
<p><strong>Wait… what is a silhouette???</strong></p>
<p><span style="font-weight: 400;"><img src="https://vertexschool.instructure.com/courses/14/files/790/preview?verifier=OjdsCOtNohmWQsP0bbZBHOkqrnDEPOQGQ7Z2q7Ds" alt="image2.png" width="650" height="366" data-api-endpoint="https://vertexschool.instructure.com/api/v1/courses/14/files/790" data-api-returntype="File"></span></p>
<p><span style="font-weight: 400;">When we say build whatever it takes to capture the silhouette, that means </span><strong>the low poly geometry should capture the shape of the high poly</strong><span style="font-weight: 400;">. We build it like a shell around the high poly.</span></p>
<p><span style="font-weight: 400;">The low poly should have just enough geometry to capture the high poly’s silhouette shape. </span><span style="font-weight: 400;"><br><br></span></p>
<p><span style="font-weight: 400;"><img src="https://vertexschool.instructure.com/courses/14/files/799/preview?verifier=pdRwj5txQqiiuwqxWqRwHtsmCpe8Jfxj25S5bIaL" alt="image10.png" width="650" height="366" data-api-endpoint="https://vertexschool.instructure.com/api/v1/courses/14/files/799" data-api-returntype="File"></span></p>
<p><span style="font-weight: 400;">We should still be mindful of performance, however. Where the high poly is made of separate pieces and has all the detail, the low poly should be made of as few pieces as possible. We build it like a shell around the high poly.</span></p>
<p><span style="font-weight: 400;"><br><img src="https://vertexschool.instructure.com/courses/14/files/789/preview?verifier=AFcbeafRidJ2F0MScafxl9JVRqQ1k3pi9KSPQADS" alt="image1-1.png" width="650" height="366" data-api-endpoint="https://vertexschool.instructure.com/api/v1/courses/14/files/789" data-api-returntype="File"><br></span></p>
<p>&nbsp;</p>
<h2><span style="font-weight: 400;">Tip #1: No More Hard Edges</span></h2>
<p><span style="font-weight: 400;">With increased polycount budgets and better baking tools, we want to make sure that we avoid hard 90 degree edges wherever possible. By beveling the edges of our low poly model, we’ll get cleaner bakes and less texture seams.&nbsp;</span></p>
<p><span style="font-weight: 400;"><img src="https://vertexschool.instructure.com/courses/14/files/798/preview?verifier=yWTPvQmS8vdZZ0q9VbRCwNI1jwuNAIPHebKrtE4L" alt="image9.png" width="650" height="366" data-api-endpoint="https://vertexschool.instructure.com/api/v1/courses/14/files/798" data-api-returntype="File"></span></p>
<p><span style="font-weight: 400;"><img src="https://vertexschool.instructure.com/courses/14/files/791/preview?verifier=tSysnAmw1JS0gJsFw8FIQWluMHjSaad2zhRMoYQN" alt="image4.png" width="650" height="366" data-api-endpoint="https://vertexschool.instructure.com/api/v1/courses/14/files/791" data-api-returntype="File"></span></p>
<p>&nbsp;</p>
<h2><span style="font-weight: 400;">Tip # 2: Save On The Straights, Spend on the Curves</span></h2>
<p><span style="font-weight: 400;">Triangles are no longer an expensive limitation, but we do still have to be mindful of how much geometry we are using. We’re able to push the geometry further, but with hundreds of objects on screen at a time, that all still adds up.</span></p>
<p><span style="font-weight: 400;">A very important technique we can use to take control of our triangle budgets while still capturing the silhouette of our high poly is to always remember that we <strong>save on the straights so we can spend on the curves</strong>. This means we should avoid any additional edges or vertices that don’t change the silhouette, such as along a planar surface with straight edges. But we want to always spend whatever geometry is necessary to properly capture every curve.</span></p>
<p><span style="font-weight: 400;"><img src="https://vertexschool.instructure.com/courses/14/files/794/preview?verifier=9b5gSgcLlDhPX4NQQ88ecFCA8wTqR5loLyDy2rmD" alt="image6.png" width="650" height="366" data-api-endpoint="https://vertexschool.instructure.com/api/v1/courses/14/files/794" data-api-returntype="File"></span></p>
<hr>