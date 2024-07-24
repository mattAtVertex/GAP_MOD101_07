# Objective 15: Explain advanced HP techniques with Floaters

<h1><span style="font-weight: 400;">Floaters and Kitbashing</span></h1>
<p><iframe src="https://www.youtube.com/embed/6uKmcf9VzuU?rel=0" width="800" height="450" allowfullscreen="allowfullscreen" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture"></iframe></p>
<hr>
<h2><span style="font-weight: 400;">Floaters vs Geometry</span></h2>
<h3><strong>What are floaters and why would I use them?</strong></h3>
<p><span style="font-weight: 400;">Floaters are helper meshes that float above geometry.&nbsp;</span></p>
<p>&nbsp;</p>
<p><span style="font-weight: 400;">A lot of 3D game artists in the beginning think they have to make their mesh watertight, where everything is connected and all one mesh. But this isn’t the case. </span><strong>Floaters</strong><span style="font-weight: 400;"> are a powerful tool we can use to make the process easier.</span></p>
<p>&nbsp;</p>
<p><span style="font-weight: 400;">Floaters give us an out to going in and figuring out complex geometry for how certain pieces fit together. Instead, we can just </span><strong>model the pieces out separately and stick them close to the surface</strong><span style="font-weight: 400;">.</span></p>
<p>&nbsp;</p>
<p><span style="font-weight: 400;">Instinct is going to tell us that we need to be careful of the intersection of the two objects. This is not something we have to worry about in most cases such as with screws, rivets, and bolts.</span></p>
<p>&nbsp;</p>
<p><span style="font-weight: 400;">When dealing with </span><strong>floaters that we need to appear as though they are a part of the geometry</strong><span style="font-weight: 400;">, the key part is that we give it a bottom edge that wraps down and around.</span></p>
<p>&nbsp;</p>
<p><span style="font-weight: 400;">Give it an</span><strong> edge that is parallel to the surface of the geometry </strong><span style="font-weight: 400;">it is going to be sitting on</span><strong>.</strong></p>
<p><br><br></p>
<p><span style="font-weight: 400;">Then, position the floater where it is </span><strong>sitting just slightly above that surface</strong><span style="font-weight: 400;">. Just enough to avoid Z-fighting.</span></p>
<p>&nbsp;</p>
<p><span style="font-weight: 400;">Then, when doing the baking, </span><strong>our cage will go out to the furthest point</strong><span style="font-weight: 400;">, encompassing the object and all floaters.</span></p>
<p><br><br></p>
<p><span style="font-weight: 400;">This will bake down nicely and the resulting normal map will make the low poly look like the floaters are a part of the mesh.</span></p>
<h3><strong>Using Floaters for Indentions</strong></h3>
<p><span style="font-weight: 400;">You can also use floaters for shapes that would cut into the main shape.&nbsp;</span></p>
<p>&nbsp;</p>
<p><span style="font-weight: 400;">In a similar process to what we did before, we can build floaters with the indented shapes and have them hovering just above the main surface. This works especially great for planar surfaces.</span></p>
<p>&nbsp;</p>
<p><strong>Floaters sitting above a planar surface</strong></p>
<p>&nbsp;</p>
<p><span style="font-weight: 400;">In situations where this causes problems due to the shape of our mesh, or whenever we need a more watertight model overall, we can cut a simple hole into the main shape and place the floaters on the inside.</span></p>
<p>&nbsp;</p>
<p><strong>Hole cut into main surface to fit floaters inside</strong></p>
<h2><span style="font-weight: 400;">Kitbashing</span></h2>
<h3><strong>What is Kitbashing?</strong></h3>
<p><span style="font-weight: 400;">Traditionally speaking,</span><strong> Kitbashing</strong><span style="font-weight: 400;"> is the process of taking </span><strong>different models and “bashing” them together</strong><span style="font-weight: 400;">.</span></p>
<p>&nbsp;</p>
<p><span style="font-weight: 400;">When we talk about kitbashing in high poly 3D modeling, we are referring to two main things:</span></p>
<p>&nbsp;</p>
<ol>
<li style="font-weight: 400;"><span style="font-weight: 400;">Models intersecting from bashing them together</span></li>
<li style="font-weight: 400;"><span style="font-weight: 400;">Kits of pieces to bash with</span></li>
</ol>
<p>&nbsp;</p>
<p><span style="font-weight: 400;">The first is the practice of using</span><strong> separate pieces</strong><span style="font-weight: 400;"> and </span><strong>slamming them together</strong><span style="font-weight: 400;"> to create detail </span><strong>without the worry of intersecting parts</strong><span style="font-weight: 400;">.&nbsp;</span></p>
<p><br><br></p>
<p><span style="font-weight: 400;">This can be a helpful technique when high poly modeling. </span><strong>The only thing that matters about your high poly when baking is what it looks like</strong><span style="font-weight: 400;">. As long as it doesn’t cause any strange errors or break </span><strong>authenticity</strong><span style="font-weight: 400;">, you should feel free to use this technique.</span></p>
<p>&nbsp;</p>
<p><span style="font-weight: 400;">Terms you might hear that refer to the same technique:</span></p>
<ul>
<li style="font-weight: 400;"><span style="font-weight: 400;">Bashing</span></li>
<li style="font-weight: 400;"><span style="font-weight: 400;">Slamming</span></li>
<li style="font-weight: 400;"><span style="font-weight: 400;">Jamming</span></li>
</ul>
<p>&nbsp;</p>
<p><span style="font-weight: 400;">Ultimately, they all refer to the process of models intersecting.</span></p>
<h3><strong>Creating a Kit to Bash With</strong></h3>
<p><span style="font-weight: 400;">Kitbashing and floaters go hand in hand. The second half refers to the process of creating small pieces that you reuse multiple times across a model. Most of the time, these are going to be floaters that you create.</span></p>
<p>&nbsp;</p>
<p><span style="font-weight: 400;">What you do for this is create a set of pieces for your kit, then duplicate those to position around your model.</span></p>
<p>&nbsp;</p>
<p><span style="font-weight: 400;">Common things you might make a kit out of as you work on a model:</span></p>
<p>&nbsp;</p>
<ul>
<li style="font-weight: 400;"><span style="font-weight: 400;">Screws &amp; Bolts</span></li>
<li style="font-weight: 400;"><span style="font-weight: 400;">Vents</span></li>
<li style="font-weight: 400;"><span style="font-weight: 400;">Knobs &amp; Buttons</span></li>
<li style="font-weight: 400;"><span style="font-weight: 400;">Brackets</span></li>
<li style="font-weight: 400;"><span style="font-weight: 400;">Plates</span></li>
</ul>
<p>&nbsp;</p>
<p><span style="font-weight: 400;">The list goes on.</span></p>
<p>&nbsp;</p>
<p><span style="font-weight: 400;">These kit pieces can then be used all over your model in places that make sense. A lot of the time, kit pieces such as screws, bolts, or any other tight floaters will be baked down into the normal maps. Other times, for larger kit pieces that cause a silhouette change, will need to be reflected in the low poly geometry.</span></p>
<p><br><br></p>