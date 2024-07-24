# Objective 22: Explain the baking process from Maya to Substance Painter

<h2>Part 1: Setting Up Color IDs in Maya</h2>
<p><iframe src="https://www.youtube.com/embed/WPAn3XWVpLA?rel=0" width="960" height="540" allowfullscreen="allowfullscreen" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"></iframe></p>
<hr>
<h2>Part 2: Export Set Up for Baking</h2>
<p><iframe src="https://www.youtube.com/embed/KcevOHZG2pc?rel=0" width="960" height="540" allowfullscreen="allowfullscreen" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"></iframe></p>
<hr>
<h2>Part 3: Baking in Substance Painter</h2>
<p><iframe src="https://www.youtube.com/embed/nBbiAcbT_YQ?rel=0" width="960" height="540" allowfullscreen="allowfullscreen" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"></iframe></p>
<h3>The Interface</h3>
<p>When you open Substance Painter you will be greeted with a blank canvas. Let’s define some of the areas.</p>
<p><img src="https://canvas.instructure.com/courses/2292421/files/111562366/preview" alt="interface.jpg" width="650" height="366" data-api-endpoint="https://canvas.instructure.com/api/v1/courses/2292421/files/111562366" data-api-returntype="File"></p>
<p>&nbsp;</p>
<h3>Interface Areas</h3>
<ul>
<li style="font-weight: 400;">
<strong>Viewports</strong><span style="font-weight: 400;"> are where you will see the model upon import. You can manipulate the viewports with the familiar “Maya” style navigation. ALT+LMB rotate : ALT+RMB zoom (or scroll wheel) : ALT+MMB pan</span>
</li>
<li style="font-weight: 400;">
<strong>Viewport Tools</strong><span style="font-weight: 400;"> manipulate the viewports as well as the imported model.</span>
</li>
<li style="font-weight: 400;">
<span style="font-weight: 400;">The </span><strong>Brush and Selection Tools</strong><span style="font-weight: 400;"> operate within the viewports on your model.</span>
</li>
<li style="font-weight: 400;">
<span style="font-weight: 400;">The </span><strong>Active Tab Panel </strong><span style="font-weight: 400;">displays information related to the tabs across the top of the window.&nbsp;</span>
</li>
<li style="font-weight: 400;">
<span style="font-weight: 400;">The </span><strong>Properties Panel </strong><span style="font-weight: 400;">displays the properties and options available based on what is selected in the Active Tab. </span>
</li>
<li style="font-weight: 400;">
<strong style="font-family: inherit; font-size: 1rem;">The Library</strong><span style="font-weight: 400;"> is a collection of tools, materials, and utilities that alter your model or viewport.</span>
</li>
</ul>
<hr>
<h3>Creating Your Project</h3>
<p>To start, let’s create a New File.</p>
<p><img src="https://canvas.instructure.com/courses/2292421/files/111562786/preview" alt="fileNew.png" width="189" height="44" data-api-endpoint="https://canvas.instructure.com/api/v1/courses/2292421/files/111562786" data-api-returntype="File"></p>
<ol>
<li><span style="font-weight: 400;">In the New Project window: Select the Unreal Engine 4 (Allegorithmic) template from the drop-down box as we will be importing these into Unreal later.</span></li>
<li><span style="font-weight: 400;">Click the “Select…” box. Here you will navigate to your low poly models .FBX file. This will be the imported mesh.</span></li>
<li><span style="font-weight: 400;">Leave the Document Resolution at the default setting. This setting can be changed at any time, as Painter is non-destructive and only encodes the resolution on export.</span></li>
<li><span style="font-weight: 400;">Normal Map: Set to DirectX </span></li>
<li><span style="font-weight: 400;">Leave all other settings at default.&nbsp; AutoUVUnwrap is checked.&nbsp; Compute tangent… is checked.</span></li>
<li><span style="font-weight: 400;">Click OK. Your mesh will now import and you will have something resembling the first image, where your model is in the viewport. Now we are ready to start baking the maps!</span></li>
</ol>
<p>&nbsp;</p>
<h3>Baking Mesh Maps Using Match By Name (The Preferred Approach)</h3>
<p><span style="font-weight: 400;">Initializing the baker window. Edit &gt; Bake Mesh Maps.&nbsp;</span></p>
<p><span style="font-weight: 400;"><img src="https://canvas.instructure.com/courses/2292421/files/111562434/preview" alt="BakerWindow.jpg" width="625" height="996" data-api-endpoint="https://canvas.instructure.com/api/v1/courses/2292421/files/111562434" data-api-returntype="File"></span></p>
<ol>
<li><span style="font-weight: 400;">Set the Output Size to 2048.</span></li>
<li><span style="font-weight: 400;">Select your High Definition Mesh and click the little paper icon.&nbsp; This will allow you to select your high-resolution mesh.</span></li>
<li><span style="font-weight: 400;">Set Max Frontal and Max Rear Distance to 0.07</span></li>
<li><span style="font-weight: 400;">Set Anialiasing to Subsampling 4x4.</span></li>
<li><span style="font-weight: 400;">Set Match to By Mesh Name.</span></li>
<li><span style="font-weight: 400;">Check the ID box (The ID parameters will show up)</span></li>
<li><span style="font-weight: 400;">Set Color Source to Mesh ID/Polygroup.</span></li>
<li><span style="font-weight: 400;">Set Color Generator to Random.</span></li>
<li><span style="font-weight: 400;">Click Bake 1001 Mesh Maps.</span></li>
</ol>
<p>When the Baker is done it's time to check the maps for issues.</p>
<p>&nbsp;</p>
<h3><span style="font-weight: 400;">Common Problems</span></h3>
<ul>
<li style="font-weight: 400;"><span style="font-weight: 400;">Missing parts of the map: check your Max frontal/Rear Distance settings.</span></li>
<li style="font-weight: 400;"><span style="font-weight: 400;">Maps are not showing: check to see if the missing map is ticked in the baker window.</span></li>
<li style="font-weight: 400;">
<span style="font-weight: 400;">Maps still not showing:</span>
<ul>
<li style="font-weight: 400;" dir="ltr"><span style="font-weight: 400;">Confirm your mesh names are set: _high and _low.</span></li>
<li style="font-weight: 400;"><span style="font-weight: 400;">And Match: By Mesh Name.</span></li>
</ul>
</li>
<li style="font-weight: 400;"><span style="font-weight: 400;">ID is not showing: check to see if Color Source is set to Mesh ID/Polygroup.</span></li>
<li style="font-weight: 400;"><span style="font-weight: 400;">Stretching: check your UVs.</span></li>
<li style="font-weight: 400;">
<span style="font-weight: 400;">Artifacting:</span>
<ul>
<li style="font-weight: 400;"><span style="font-weight: 400;">check your Max frontal/Rear Distance settings.</span></li>
<li style="font-weight: 400;"><span style="font-weight: 400;">check your hard/soft edges in Maya.</span></li>
</ul>
</li>
</ul>
<p><span style="font-weight: 400;">&nbsp;</span></p>
<p><span style="font-weight: 400;">This Quick Start Guide is the general workflow for successful baking in Substance Painter.</span></p>
<hr>
<h2>Part 4: Explode Baking</h2>
<p><iframe src="https://www.youtube.com/embed/7Ff9V4H-cfU?rel=0" width="960" height="540" allowfullscreen="allowfullscreen" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"></iframe></p>
<h3 style="text-align: left;">BAKING SETUP</h3>
<div class="col span_12 dark left" style="text-align: left;">
<div class="vc_col-sm-12 wpb_column column_container vc_column_container col no-extra-padding instance-8" data-t-w-inherits="default" data-border-radius="none" data-shadow="none" data-border-animation="" data-border-animation-delay="" data-border-width="none" data-border-style="solid" data-border-color="" data-bg-cover="" data-padding-pos="all" data-has-bg-color="false" data-bg-color="" data-bg-opacity="1" data-hover-bg="" data-hover-bg-opacity="1" data-animation="" data-delay="0">
<div class="vc_column-inner">
<div class="wpb_wrapper">
<p style="padding-left: 40px;">1.In your modeling package of choice, group all the objects together.</p>
<p style="padding-left: 40px;">2.Low poly objects in one group</p>
<p style="padding-left: 40px;">3.High poly objects in another. (Make sure both groups are in the same world space)</p>
<p style="text-align: left;"><img src="https://canvas.instructure.com/courses/2292421/files/111708809/preview" alt="exBake_01.jpg" width="650" height="366" data-api-endpoint="https://canvas.instructure.com/api/v1/courses/2292421/files/111708809" data-api-returntype="File"></p>
<p style="text-align: left;">&nbsp;</p>
<p style="padding-left: 40px;"><span>4.Duplicate both groups.</span></p>
<p style="padding-left: 40px;"><span>5.Hide the original low poly and high poly groups.</span></p>
<p style="padding-left: 40px;"><span>6.Select the high and low corresponding objects and move them away. </span></p>
<p style="padding-left: 40px;"><span>7.Repeat this with all objects until there is a substantial distance between each object. </span></p>
<p style="padding-left: 40px;"><span>(For example: “outer box” high and low will still both occupy the same world space.)</span></p>
<p>&nbsp;</p>
<p><span><img src="https://canvas.instructure.com/courses/2292421/files/111708810/preview" alt="exBake_02.jpg" width="650" height="366" data-api-endpoint="https://canvas.instructure.com/api/v1/courses/2292421/files/111708810" data-api-returntype="File"></span></p>
<p>&nbsp;</p>
<p style="padding-left: 40px;"><span>8. Export the “exploded” low group as an fbx.</span></p>
<p style="padding-left: 40px;"><span>9. Repeat with the “exploded” high group. </span></p>
<p style="padding-left: 40px;"><span>10. Export your original low poly group with all the objects in the original world space as an fbx as well.</span></p>
<p style="padding-left: 40px;"><span>11. Inside of Substance Painter start a new project using the “exploded” low poly fbx</span></p>
<p>&nbsp;</p>
<p><span><img src="https://canvas.instructure.com/courses/2292421/files/111708807/preview" alt="exBake_03.jpg" width="650" height="366" data-api-endpoint="https://canvas.instructure.com/api/v1/courses/2292421/files/111708807" data-api-returntype="File"></span></p>
<p>&nbsp;</p>
<p style="padding-left: 40px;"><span>12. Bake the mesh maps using the “exploded” high poly fbx. </span></p>
<p style="padding-left: 40px;"><span>13. Once the bake is complete, navigate to the Edit menu. </span></p>
<p style="padding-left: 40px;"><span>14. Select the Project Configuration menu.</span></p>
<p style="text-align: left;">&nbsp;</p>
<p style="text-align: left;"><span><img src="https://canvas.instructure.com/courses/2292421/files/111708808/preview" alt="exBake_04.jpg" width="650" height="366" data-api-endpoint="https://canvas.instructure.com/api/v1/courses/2292421/files/111708808" data-api-returntype="File"></span></p>
<p style="text-align: left;">&nbsp;</p>
<p style="padding-left: 40px;"><span>15. Press "Select" and choose the low poly fbx that is NOT “exploded” and press OK.</span></p>
<p style="text-align: left;">&nbsp;</p>
<p style="text-align: left;"><span><img src="https://canvas.instructure.com/courses/2292421/files/111708806/preview" alt="exBake_05.jpg" width="618" height="602" data-api-endpoint="https://canvas.instructure.com/api/v1/courses/2292421/files/111708806" data-api-returntype="File"></span></p>
<p style="text-align: left;">&nbsp;</p>
<p style="text-align: left;"><span>This process enables you to make adjustments to your low poly model and preserve the baked maps, assuming the UV layout has not changed.&nbsp; While one can always bake by mesh name, there is still a risk of the normals being affected by touching or intersecting geometry. So if you have complex models and/ or many close objects the “exploded” method can save you time and stress!</span></p>
</div>
</div>
</div>
</div>