# Objective 6: Review video about high polygon modeling

<p><iframe src="https://player.vimeo.com/video/452898712" width="800" height="450" allowfullscreen="allowfullscreen" allow="autoplay; fullscreen"></iframe></p>
<hr>
<h2>Objective</h2>
<p>Our goal this week is to get you familiarized with the basics around high poly modeling. The important thing to remember here is that we want to approach this from a perspective of focus on the high poly only. So take a moment to separate your thought process from concepts like "low poly" or "game resolution".&nbsp;We won't be worrying about polygon counts or UVs. We have one focus:</p>
<p>Making a great looking high poly model.</p>
<p>&nbsp;</p>
<hr>
<p>&nbsp;</p>
<h2>The Construction Mesh Approach</h2>
<h3>What is a Construction Mesh?</h3>
<p>When modeling our high poly, we like to keep our geometry clean and quaded, trying to avoid things like pinching and too many poles.</p>
<p>Let’s look at some terminology.</p>
<p><strong>TERMINOLOGY</strong></p>
<p><img src="https://kajabi-storefronts-production.global.ssl.fastly.net/kajabi-storefronts-production/products/487294/images/9Yv0AZyUTkmNtW7FOrFy_Quad-Tri-Pole_horizontal.jpg" width="651" height="196"></p>
<p><strong>Quads </strong><span>- Faces with exactly 4 sides. These are the holy grail of 3D modeling. We usually try to keep our high poly meshes constructed from mostly quads. They make edge loops easy.</span></p>
<p><strong>Tris or Triangles</strong><span> - Faces with exactly 3 sides. Edge loops cannot cut through them because the math is too different. Final rendered meshes in game engines are triangulated because that is how real time rendering works, so when you hear the term “</span><em><span>polycount</span></em><span>”, they are referring to the number of triangles in a mesh.</span></p>
<p><strong>Poles </strong><span>- Poles are points (or vertices) where more than 2 sides meet, such as on the cap of a cylinder or the poles of a sphere. They are not bad; they are even necessary, but because they can cause pinching in your smooth mesh, we try to avoid them whenever we can.</span></p>
<p><strong>N-Gons</strong><span> - Faces with more than 4 sides. These are generally bad and best avoided wherever possible. Edge loops can’t cut through them and triangulation of N-Gons is very erratic.</span></p>
<h3>Why Do We Use the Construction Mesh Approach?</h3>
<p><span>There are many reasons why you want to use a construction mesh when modeling your high poly.</span></p>
<ul>
<li><span>It keeps the topology clean and easy to edit</span></li>
<li><span>It makes it easier to work with edge loops</span></li>
<li><span>It can act as a base for building a low poly</span></li>
</ul>
<h3>The Edge Loop Scenario</h3>
<p><span>One of the biggest reasons we want to keep our mesh clean with quads using the construction mesh approach revolves around working with edge loops. When inserting edge loops there are two truths:</span></p>
<ol>
<li><span>Inserting an edge loop will cleanly cut through a quad</span></li>
<li><span>Inserting an edge loop cannot cut through a triangle or N-Gon</span></li>
</ol>
<p><span><img src="https://kajabi-storefronts-production.global.ssl.fastly.net/kajabi-storefronts-production/products/487294/images/XYlbKSV5ScCkzcjbadFp_Edge-Loop_Quad-Yes_Tri-No.jpg" width="652" height="206"></span></p>
<p><span>This causes major problems when we go to add control loops to harden our edges. Inserting edge loops in the exact same way for both meshes above, we see that the quad mesh using the </span><strong>Construction Mesh Approach</strong><span> comes out as a smooth cube with nice bevels.</span></p>
<p><span>We try to insert edge loops in the same way for the bottom mesh. The mesh with the triangle won’t let our control loops cut through. When we smooth preview it, we get a strange shape with a lot of artifacting.</span></p>
<p><span><img src="https://kajabi-storefronts-production.global.ssl.fastly.net/kajabi-storefronts-production/products/487294/images/UTcKxowlQIa4KRLiEl4U_Control-Loop_Quad-Yes_Tri-No-2.jpg" width="652" height="206"></span></p>
<h2>&nbsp;</h2>
<hr>
<h2>Working With Parts</h2>
<p><span>Let’s look at the approach beyond just working with a cube. Below you will see the high poly mesh for a trunk. The mesh is rendered in <strong>smooth mesh preview</strong> so you can see the wireframe of the <strong>construction mesh</strong>.</span></p>
<p><span><img src="https://kajabi-storefronts-production.global.ssl.fastly.net/kajabi-storefronts-production/products/487294/images/rj7MXvxTpeB4uLQbkjEd_trunk-construction-mesh.jpg" width="650" height="247"></span></p>
<p><span>Take note of the wireframe on the right and see how everything is made of quads. Keeping it as quads made building the high poly both easier and faster.</span></p>
<p><span>Also take a moment to notice how each mechanical piece is modeled as a separate object. Building it like this adds authenticity to the model.</span></p>
<p><span><img src="https://kajabi-storefronts-production.global.ssl.fastly.net/kajabi-storefronts-production/products/487294/images/KCgVbz6yS0OBXK0PtG8i_trunk-construction-2.jpg" width="651" height="443"></span></p>
<p>&nbsp;</p>
<hr>
<h2>Working with Cylinders in a Construction Mesh Approach</h2>
<p><span>We’ve looked at cubes and how to work with easily quaded shapes, but what about cylindrical shapes? Cylindrical shapes can appear problematic because their caps are inherently not quads. Cylinder caps are poles.</span></p>
<h3><strong>The Rules of Working with Cylinders</strong></h3>
<p><span>When working with cylinders in a construction mesh approach, there are some rules that we can follow to make our lives easier and the mesh cleaner to work with.</span></p>
<ul>
<li>
<span>Always use a </span><strong>power of 8 number</strong><span> for sides. 8, 16, 32, 64</span><span><br></span><span><img src="https://kajabi-storefronts-production.global.ssl.fastly.net/kajabi-storefronts-production/products/487294/images/5txH0DmaRmSTSyiQSh4w_image5.png" width="650" height="252"><br><br></span>
</li>
<li>
<span>Keep your high poly cylinder sides </span><strong>as low as possible</strong><span> and </span><strong>let the smooth proxy/subdividing do the smoothing for you</strong><span>.<br><img src="https://kajabi-storefronts-production.global.ssl.fastly.net/kajabi-storefronts-production/products/487294/images/n6Kq9bxRgi0EUDSOGctA_image6.png" width="651" height="346"><br></span><span><br></span>
</li>
<li><span>Same power of 8 rules apply to the low poly, this way the mathematical exponent for the sides lines up.<br><img src="https://kajabi-storefronts-production.global.ssl.fastly.net/kajabi-storefronts-production/products/487294/images/P9qVXmlhR6WGjCn0kHSs_image8.png" width="651" height="345"></span></li>
</ul>
<p>&nbsp;</p>
<h2>Final Thoughts</h2>
<p><span>The Construction Mesh Approach is going to make your life easier as you model your high poly. It will also keep your meshes clean and easy to manage or manipulate.</span></p>
<p><span><img src="https://kajabi-storefronts-production.global.ssl.fastly.net/kajabi-storefronts-production/products/487294/images/96IeKtWJR1OTH69wg0gr_image7.png" width="650" height="341"></span></p>