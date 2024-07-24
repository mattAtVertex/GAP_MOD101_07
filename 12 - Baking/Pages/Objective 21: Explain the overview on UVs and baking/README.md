# Objective 21: Explain the overview on UVs and baking

<p><iframe src="https://player.vimeo.com/video/452915604" width="960" height="540" allowfullscreen="allowfullscreen" allow="autoplay; fullscreen"></iframe></p>
<hr>
<h2>Objective</h2>
<p>In this handout, we’re going to explore the baking process a little more to understand how it is going to help us later in the texturing phase.</p>
<p><img src="https://vertexschool.instructure.com/courses/14/files/1652/preview?verifier=oPa3ln5oZMKKTMrFnfngpJzAcWDT37KXDkp4TpZ2" alt="image1.png" width="1920" height="1080" data-api-endpoint="https://vertexschool.instructure.com/api/v1/courses/14/files/1652" data-api-returntype="File"></p>
<hr>
<h2>Baked Maps in 3D Art</h2>
<h3>What is Baking?</h3>
<p>Baking is the process of extracting information from the high poly mesh and mapping it to the UV space of the low poly mesh. Through the baking process, we transfer the details from the high poly to the low poly.</p>
<p>The core map resulting from this process is the Normal Map. This very important map is what fakes lighting information to give the illusion that the low poly has more geometry than it actually does.</p>
<p>But the Normal Map is only one of the many maps that gets baked. There are several other maps generated in the process that contribute to the texturing phase.</p>
<p>&nbsp;</p>
<p><img src="https://vertexschool.instructure.com/courses/14/files/1653/preview?verifier=giT5k0hxqrai2X0ePWIGklU5pFkxXxtshFT0NaWl" alt="image8.png" width="900" height="506" data-api-endpoint="https://vertexschool.instructure.com/api/v1/courses/14/files/1653" data-api-returntype="File"></p>
<p>&nbsp;</p>
<h3>The Baked Maps</h3>
<p><span style="font-weight: 400;">During the baking process, several maps are generated. Each one contributes to the texturing process in a different way, but they are all important for successful texturing.</span></p>
<p>&nbsp;</p>
<p><strong>Normal</strong><span style="font-weight: 400;"> - Map that fakes lighting to show high poly details on the low poly. Responsible for making the low poly look like it has more geometry than it does.&nbsp;</span></p>
<p><span style="font-weight: 400;"><img src="https://vertexschool.instructure.com/courses/14/files/1654/preview?verifier=bB5JT0xa38DxS3E5YiRDVgjB1ZaT7pDbie76EvKe" alt="image6.png" width="1920" height="1080" data-api-endpoint="https://vertexschool.instructure.com/api/v1/courses/14/files/1654" data-api-returntype="File"></span></p>
<p><span style="font-weight: 400;">&nbsp;</span></p>
<p><strong>Curvature</strong><span style="font-weight: 400;"> - Map that defines the edges and cavities of the mesh. This is useful for generating edge highlights and controlling areas for dirt and dust.</span></p>
<p><span style="font-weight: 400;"><img src="https://vertexschool.instructure.com/courses/14/files/1655/preview?verifier=XQ7hSYkR3nxNNvI2Re3AjorVy5c8KmrV9LqKLHJq" alt="image7.png" width="1920" height="1080" data-api-endpoint="https://vertexschool.instructure.com/api/v1/courses/14/files/1655" data-api-returntype="File"></span></p>
<p>&nbsp;</p>
<p><strong>Ambient Occlusion</strong><span style="font-weight: 400;"> - Map that defines the shadowy areas of the mesh. This map is responsible for the shadows you see in the cracks and crevices, as well as contributing to the control of dust and dirt.</span></p>
<p><strong>Position</strong><span style="font-weight: 400;"> - Map that stores the position in 3D space as a gradient. This map is important for procedurally generating gradients in your texture work.</span></p>
<p><span style="font-weight: 400;"><img src="https://vertexschool.instructure.com/courses/14/files/1656/preview?verifier=Tt7oTcLrEVHUVluDmhJoZkNb56XrOHbDtJSPiG1u" alt="image3.png" width="1920" height="1080" data-api-endpoint="https://vertexschool.instructure.com/api/v1/courses/14/files/1656" data-api-returntype="File"></span></p>
<p>&nbsp;</p>
<p><strong>Thickness Map</strong><span style="font-weight: 400;"> - Simulates the thickness of the model. This map is useful for things like SubSurface Scattering.</span></p>
<p><span style="font-weight: 400;"><img src="https://vertexschool.instructure.com/courses/14/files/1657/preview?verifier=qnl4Rh7ZwZlW9MQFQfZkZgzkJkEQcwNmGPIrnmgM" alt="image2.png" width="1920" height="1080" data-api-endpoint="https://vertexschool.instructure.com/api/v1/courses/14/files/1657" data-api-returntype="File"></span></p>
<p>&nbsp;</p>
<p><strong>Material ID</strong><span style="font-weight: 400;"> - Color map that masks different areas meant for different materials. Another very important map that helps organize the physical materials into groups.</span></p>
<p><span style="font-weight: 400;"><img src="https://vertexschool.instructure.com/courses/14/files/1658/preview?verifier=F9tA0Yx3kpbI9fqTECTOgkmaoEyRVEcMdDMW3A5s" alt="image4.png" width="1920" height="1080" data-api-endpoint="https://vertexschool.instructure.com/api/v1/courses/14/files/1658" data-api-returntype="File"></span></p>
<p>&nbsp;</p>
<h3>THEY ALL WORK TOGETHER</h3>
<p>&nbsp;</p>
<p><img src="https://vertexschool.instructure.com/courses/14/files/1660/preview?verifier=fsiEpTwIEtTwjdaCz6A1VVtO1LZnY0V605ANW2OM" alt="image5.png" width="1920" height="1080" data-api-endpoint="https://vertexschool.instructure.com/api/v1/courses/14/files/1660" data-api-returntype="File"></p>