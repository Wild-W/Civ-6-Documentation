<!-- FRONT MATTER -->
<!DOCTYPE html>
<html lang="en">
                <head>
                                <meta charset="utf-8">
                                <meta http-equiv="X-UA-Compatible" content="IE=edge">
                                <meta name="google" content="notranslate" />
                                <meta name="viewport" content="width=device-width, initial-scale=1">
                                <title>Civilization VI Content Creation</title>
                                <link type="text/css" href="css/bootstrap.min.css" rel="stylesheet" />
                                <link type="text/css" href="css/bootstrap-theme.min.css" rel="stylesheet" />
                                <link type="text/css" href="css/lightbox.min.css" rel="stylesheet" />
                                <link type="text/css" href="css/Civ6Docs.css" rel="stylesheet" />
                                <script type="text/javascript" src="js/jquery-2.1.4.min.js"></script>
                                <script type="text/javascript" src="js/bootstrap.min.js"></script>
                                <script type="text/javascript" src="js/lightbox.min.js"></script>
                                <script type="text/javascript" src="js/Civ6Docs.js"></script>
                </head>
                <body>
					<div class="container-fluid">
						<div class="page-header">
							<h1>Civilization VI <small>Content Creation</small></h1>
						</div>
						<div class="row">
						<div class="col-md-9"><div class="panel panel-primary" id="Animation">
<div class="panel-heading">
<div class="panel-title">Animation
</div>
</div>
<div class="panel-body">

<p>Animation (.anm)</p>
<p>Animations consist of animation track information for one or more bones. Currently we support importing geometry directly from 3DSMax and Maya</p>

<p>Using the Asset Editor</p>

<ul>
<li>
<p>In the Asset Editor go to 'File &gt; New' and select Animation from the list.</p>
</li>
</ul>


<p><img src="Animation/media/image1.png" width="603" height="477" /></p>


<ul>
<li>
<p>In the Class Name dropdown select the class that you want (1). It can be tricky to change the class for entities after they are created, so try to make sure you have the correct class.</p>
</li>
</ul>


<p><img src="Animation/media/image2.png" width="624" height="342" /></p>


<ul>
<li>
<p>Click on the line for '<em><strong>Source File Path</strong></em>' (2), and browse to the Max or Maya file that has your animation.</p>
</li>
</ul>



<ul>
<li>
<p>When you select your file, the editor will parse the file and find which animation objects are available for export. This will fill out the '<em><strong>Source Object</strong></em>' dropdown (3) with all the available animations for you to pick from, so click the dropdown and select the animation object that you want.</p>
</li>
</ul>



<ul>
<li>
<p>The '<em><strong>Name</strong></em>' (4)of the animation will get set automatically to the name of the source object, but you can change it to whatever you want before saving the Animation.</p>
</li>
</ul>



<ul>
<li>
<p>Go to &quot;<em><strong>File &gt; Save</strong></em>&quot; and you're done.</p>
</li>
</ul>



</div> <!-- panel body --> 
</div> <!-- panel -->

<div class="panel panel-primary" id="ArtDefFiles">
<div class="panel-heading">
<div class="panel-title">ArtDefFiles
</div>
</div>
<div class="panel-body">

<p>Working with ArtDef Files</p>
<p>ArtDef files are XML files that tell the engine how to use assets and entities packaged in BLP files.</p>

<p>ArtDef files reference XLP entries and add meta information needed by the engine to correctly render the XLP entry. Because each engine system requires different information ArtDef files are structured differently for each system.</p>

<p>You can edit ArtDef files using the Asset Editor. Simply click the Open an existing art definition document and select the ArtDef file you wish to edit. Most of the ArtDef files you will need have been created already for you.</p>

<p><img src="ArtDefFiles/media/image1.png" width="427" height="273" /></p>

<p>Generally, ArtDef files consist of <strong>Collections</strong> and <strong>Parameters</strong>. Collections are unbounded lists of elements which you create. Each element has a finite number of Parameters which you edit. An element can also contain one or more Collections.</p>

<p><img src="ArtDefFiles/media/image2.png" width="624" height="374" /></p>

<p>A Collection can be identified by a triangle to the left of it, which is used to expand it. You can <strong>right click</strong> on a Collection and add a new element to it, which is automatically named after the Collection and appended a running count.</p>

<p><img src="ArtDefFiles/media/image3.png" width="391" height="501" /></p>

<p>Parameters cannot be expanded and upon selecting them the right-hand pane allows you to edit their value. ArtDefs support different Parameter types:</p>
<ul>
<li>
<p><strong>Integer</strong> (a whole number, e.g. 42),</p>
</li>
<li>
<p><strong>Float</strong> (a decimal number, e.g. 4.2),</p>
</li>
<li>
<p><strong>String</strong> (ASCII text, e.g. &quot;forty two&quot;),</p>
</li>
<li>
<p><strong>Boolean</strong> (true or false),</p>
</li>
<li>
<p><strong>Enumeration</strong> (drop-down selection from a pre-set set of values, e.g. 2 from 1, 2, or 3),</p>
</li>
<li>
<p><strong>RGB</strong> (red-green-blue color values 0-255 for each color, e.g. R:122 G:255 B:34),</p>
</li>
<li>
<p><strong>2D Coordinate</strong> (a two-dimensional coordinate along X and Y axes, e.g. X:0.5 Y:1.2),</p>
</li>
<li>
<p><strong>BLP Entry</strong> (the identifier from an XLP file referencing an asset or entity, e.g. Features_Marsh),</p>
</li>
<li>
<p><strong>ArtDef Reference</strong> (a reference to another ArtDef entry in the same file, e.g. Collection1), and</p>
</li>
<li>
<p><strong>Collection</strong> (an array of Parameters, e.g. [42, 13, 55]).</p>
</li>
</ul>

<p>ArtDef files are parsed directly by the engine, so the only way to discover any mistakes made is to save your changes and run the game. ArtDef errors usually manifest through so-called assertions, which are pop-up dialogs with a red X. Usually they tell you what is wrong and sometimes even how to fix it.</p>

<p><img src="ArtDefFiles/media/image4.png" alt="Machine generated alternative text: Assert Failed File: ..X..XSrcXAppXGraphicsXStrategicView.cpp Line: 1234 Expression: false Message: This is an assertion, please pay attention to what it says&#39; Press Cancel to debug Press Try Again to ignore once Press Continue to ignore always Cancel Try Again Continue " width="466" height="258" /></p>

</div> <!-- panel body --> 
</div> <!-- panel -->

<div class="panel panel-primary" id="BuildingsProcess">
<div class="panel-heading">
<div class="panel-title">BuildingsProcess
</div>
</div>
<div class="panel-body">


<p>Concept Process</p>
<p>Monday, July 13, 2015</p>
<p>1:23 PM</p>


<p>Steps </p>


<ol style="list-style-type: decimal">
<li>
<p>Talk with Design, or make sure you understand the design purpose of the structure. – Discussion with team (Kat, Matt and Brian – Design if necessary)</p>
</li>
<li>
<p>Loose thumbnails – rough layouts and shapes. 6 -10 at least. These shouldn’t take much time. General massing and rough shapes. – Approval</p>
</li>
<li>
<p>Thumbnail that incorporates feedback. – Approval Needed</p>
</li>
<li>
<p>Move onto final B/W line art – Approval Needed</p>
</li>
<li>
<p>Final Color - Small tweaks may be necessary at this point, but nothing major. Final Approval Needed</p>
</li>
</ol>


<p>Points to keep in mind</p>


<ol style="list-style-type: decimal">
<li>
<p>Hex point should be on bottom of page.</p>
</li>
<li>
<p>Lighting source is from the SW (See game)</p>
</li>
<li>
<p>Safe frame should be indicated.</p>
</li>
<li>
<p>Thumbnails should really push the shapes of the buildings for each thumbnail. Try multiple different shapes for buildings and not just focus on arrangement of one set.</p>
</li>
<li>
<p>Want to see it in reference to other buildings for scale purposes.</p>
</li>
<li>
<p>Moving on to other tasks is fine when waiting on feedback.<br />
<br />
<br />
<br />
-When concepting a building always make an effort to include scale context using screenshots or other existing buildings for comparison. How big will this structure ACTUALLY appear to be on our map? For example:</p>
</li>
<li>
<p><img src="BuildingsProcess/media/image1.png" alt="Machine generated alternative text: " width="679" height="360" /></p>
</li>
</ol>





<p><em>What to consider when asking for or providing Feedback:</em></p>

<p><em>-Does it hit our art style?</em></p>
<p><em>-Does it solve the visual problem it needs to solve?</em></p>
<p><em>-What are the reasons behind your visual choices?</em></p>

<p><strong>Concept Stage and Timeframe:</strong></p>
<p>When a piece is emailed out for crit the concept artist should make an effort to clearly state the <em><strong>Stage</strong></em> of the assignment and their best estimate of a <em><strong>Timeframe</strong></em> for delivery if they have one. For example, “These are my <em>early exploratory sketches</em> <strong>(Stage)</strong> for X so I’m exploring some pretty wild pie in the sky things. However, I have about a week left <strong>(Timeframe)</strong> before we want to try to zero in on a final design for X,” or “This is my final design <strong>(Stage)</strong> for Y. Our goal is to send it to the modeling team this afternoon <strong>(Timeframe)</strong>”</p>

<p>Try not to let emails asking for feedback go unanswered. Even a simple “Looks great! Keep going!” is better than silence. If you believe the piece hits all the marks it needs to hit then say so. If you have thoughts or feedback but need some time to formulate them before sending them over then say so. “Hey Beth, I’m pretty bogged down in my own painting at the moment, but I have some thoughts about your vampiric empire hovercraft assignment. How about we round up about it later?”</p>

<p><strong>Email Sucks For Conveying Concept Feedback:</strong></p>
<p>When possible, all feedback or critique should be conveyed in person, verbally. If goals or changes are decided on during the verbal communication they should then be documented in a succinct email so that no one forgets what was said and they can get right back on track after their week long vacation to wrestle ice gators in Antarctica where they will probably forget all about what concepts they’d been working on. “Frank and I talked about the laser cannons on his giraffe creature concept this morning. We agreed that they need to be much bigger and maybe he should try green lasers instead of purple lasers. Well, folks, I’m off to wrestle some ice gators. See you in a week.”</p>

<p>When giving someone feedback you should be clear about what you believe is a must-do and what is merely a suggestion. “I think you definitely need to change the size of the dragon’s horns. It needs to have horns larger than the other dragons because our design team has specified this as the <em>Great Horned Dragon</em>. Maybe you could also try adding some spines to make it look more menacing?”</p>

<p><em>Documentation</em></p>

<p><strong>Tell a Story:</strong></p>
<p>All concepts have a narrative from their early stages to their completion. Document this story somewhere! It can be informally in an email, or formally via One Note or Discourse or whatever documentation platform the team has agreed upon for the project but DO write it down somewhere and do it consistently for each piece you produce as the narrative unfolds. This will come in handy months down the line when you’ve long forgotten why that purple dolphin helicopter went through so many iterations. A good example in our One Note right now is John Curtin's Leader Concept page: (link following )Concept</p>

<p>“<strong>First</strong> I began by gathering reference images (link to ref image folder) <strong>then</strong> I drew a few pages of rough sketches (link to the rough sketches.) <strong>After that</strong> I spoke with my lead and art director and they both agreed that sketch #16 was the strongest. <strong>Next</strong>, I refined that sketch (link to the sketch) and presented it again. My art director liked where it was going but decided that the design needed more laser cannons. <strong>Next</strong>, I revised the design to include more laser cannons (link to revised design) <strong>and then</strong> worked it up to a final stage (link to final concept)”</p>

<p><strong>Save Your Ref:</strong></p>
<p><em>Always</em> save all of the reference images you used in a little folder with your concept. This is particularly important if you photobashed anything or borrowed closely from an existing design in a photo or painting. Do the same for fonts or other resources.</p>


<p><strong>Folder Structures and Naming Conventions:</strong></p>
<p><img src="BuildingsProcess/media/image2.png" alt="Machine generated alternative text: Organize Computer New Volume (D:) projects 8ALW-K8ERKLEY virtual_clv6-Art ArtDev Buildings Villages Barbarian Village 01 Concept Industrial Barb Architecture Include in library Share with REF Slide show New folder Favo rites Desktop Downloads Recent Places Libraries Documents Music AOY Pictures OSEO Videos Computer os CG New Volume (D:) Network CSX2kgames.t2.corp) (N:) Barb Architecture ScaKlI Barb Architecture SketchesKBOI Barb Architecture SketchesK 2 Barb Architecture Sketch C oncepr 06 kberkley CN12kgames.t2.corpXNetworkX2KGBALXUsel " width="1058" height="406" /></p>


<p>Buildings Art Style Breakdown</p>
<p>Monday, August 29, 2016</p>
<p>2:21 PM</p>

<p>The shapes of our buildings are <strong>simple</strong>, <strong>exaggerated</strong> and <strong>chunky</strong>!<br />
<br />
Remember that our players will often be looking at these buildings from really far away. They may have hundreds of buildings on the screen at once and they need to be able to pick them out of a crowd. A good rule of thumb is to imagine them as little toy models rather than representations of real world buildings.<br />
<br />
-Big, simple shapes<br />
-Roof detail is important because of the player camera angle. Avoid blank roofs<br />
-Focus on shape clusters. Groups of 2-3 with varied heights work well<br />
-Keep things simple. Avoid too much visual noise</p>
<p>-Avoid straight lines where possible<br />
-Avoid making all of your shapes the same size<br />
 </p>
<p><img src="BuildingsProcess/media/image3.png" alt="Machine generated alternative text: XI&#39;AN " width="543" height="646" /></p>

<p><img src="BuildingsProcess/media/image4.png" alt="Machine generated alternative text: " width="522" height="448" /></p>

<p><img src="BuildingsProcess/media/image5.png" alt="Machine generated alternative text: " width="471" height="402" /></p>
<p><em><strong><em>SHAPES:</em></strong></em><br />
Divide forms into <em><strong>Big Shapes</strong></em>, <em><strong>Intermediate Shapes</strong></em> and <em><strong>Fine details</strong></em> with a 3, 2, 1 ratio. Your <em><strong>Big Shapes</strong></em> are things like the entire body of the house or the entire roof. Your <em><strong>Intermediate Shapes</strong></em> are things like awnings or really big beams or balconies or chimneys. Your <em><strong>Fine Details</strong></em> are things like itty bitty planks of wood or individual bricks or clumps of thatch.<br />
<br />
Example:<br />
 </p>
<p><img src="BuildingsProcess/media/image6.png" alt="Machine generated alternative text: A—BIG SHAPES B:INTERMEDIATES SHAPES C:FINE DETAILS " width="667" height="448" /></p>
<p>The <strong>Big Shapes</strong> and <strong>Intermediate Shapes</strong> should be the only ones that that really affect the silhouette of your buildings. Don't focus too much on the fine details. Think about the <em><strong>Big Shapes</strong></em> of your buildings first.<br />
<br />
 </p>
<p><img src="BuildingsProcess/media/image7.png" alt="Machine generated alternative text: / Ein " width="576" height="281" /></p>


<p><img src="BuildingsProcess/media/image8.png" alt="Machine generated alternative text: " width="394" height="499" /></p>

<p>-Break the silhouette with your <strong>Big Shapes</strong> and <strong>Intermediate Shapes</strong><br />
-Keep your shapes fun and wonky. Avoid boring straight lines<br />
-Avoid making all of your shapes the same size<br />
-<strong>If you dropped a marble on it would it rest there quietly or would it roll? It should roll!<br />
<br />
<br />
<br />
<br />
</strong>Concept Checklists</p>
<p>Wednesday, September 21, 2016</p>
<p>11:17 AM</p>

<p><strong>Improvements<br />
</strong>1)Are you considering the hex tile safe frame boundaries?<br />
2)Are there any opportunities for animation?<br />
3)How will you distinguish between a Worked state vs an Unworked state?<br />
<br />
 </p>


<p>Building Modeling Pipeline</p>
<p>Monday, August 10, 2015</p>
<p>10:42 AM</p>

<p>This section will describe many areas of the building pipeline, from texturing to setting it up in engine.</p>

<p>List of resources:</p>

<p>Hex with safe zone</p>
<p>\ArtDev\Reference_Files\Official_Hex.max</p>
<p>3dsmax Unit Setup</p>
<p><img src="BuildingsProcess/media/image9.png" alt="Machine generated alternative text: System Unit Setup System Unit Scale 1 Linit- 1.0 Inches units Setup System Unit Setup Display Llnit Scale Me tric LIS Standard Custom • Generic Units Lighting IJnits International V Respect System Llnits Files 16777215. o Distance from origin: 1.0 Resulting Accuracy: 0.0000001192 " width="646" height="469" /></p>

<p>Building Textures</p>
<p>Thursday, July 17, 2014</p>
<p>4:27 PM</p>

<p>Texturing, in most cases, should be done using a modular, atlased approach, which results in a mostly grid-like texture set. Obviously there will be things which need explicit mapping or peaks which might stray from that but try to keep it as modular as possible. The typical texture size is roughly 128 pixels per story. While we are using a PBR model for the game, because our assets are so small on the screen, real-time shadows and ambient occlusion are often tough to see. As a result, placing shadows in the textures still seems to be a viable method that works. Below are a few examples: (left, industrial city), (mid-left, modern city), (mid-right, encampment), (right, Big Ben), bottom (Mughal with color variants).</p>


<p><img src="BuildingsProcess/media/image10.png" alt="Machine generated alternative text: &#39;EIEI&#39; a. iiii " width="1256" height="712" /><img src="BuildingsProcess/media/image11.png" alt="Machine generated alternative text: " width="1256" height="628" /></p>

<p>Using a gray diffuse and gradient ramp for gloss only. White: more gloss, Black: less gloss. Notice you don't really get any shine till you hit about 50% gray.</p>


<p><img src="BuildingsProcess/media/image12.png" alt="Machine generated alternative text: " width="326" height="326" /></p>

<p>Asset name: Material_Gloss_Test</p>
<p><img src="BuildingsProcess/media/image13.png" alt="Machine generated alternative text: " width="1648" height="300" /></p>

<p>Using the same map for gloss and metalness at the same time. Notice metalness makes your basecolor black (+ ambient). The more metalness the more chrome-like it becomes. Asset: Material_Metalness_Test</p>

<p><img src="BuildingsProcess/media/image14.png" alt="Machine generated alternative text: " width="1648" height="300" /></p>

<p>Gloss Left, Metalness/Gloss Right</p>
<p><img src="BuildingsProcess/media/image15.png" alt="Machine generated alternative text: 7111!!&#39; " width="840" height="670" /><img src="BuildingsProcess/media/image16.png" alt="Machine generated alternative text: " width="827" height="669" /></p>
<p>Gloss map example, Barracks - the value variation creates more contrast in the way the light hits the shingles on the roof.</p>

<p><img src="BuildingsProcess/media/image17.png" alt="Machine generated alternative text: " width="598" height="463" /><img src="BuildingsProcess/media/image18.png" alt="Machine generated alternative text: " width="130" height="255" /><img src="BuildingsProcess/media/image19.png" alt="Machine generated alternative text: " width="130" height="255" /></p>

<p><img src="BuildingsProcess/media/image20.png" alt="Machine generated alternative text: CORRESPONDING NORMAL MAPS Rough Stone IN-GAME EXAMPLES AVERAGE VALUES Rough Wood Medium Stone Roof Shingles Smooth Wood Smooth Stone Glass/Polished Metal 255 " width="1425" height="502" /></p>
<p>Normal map generation seems to work quickest through Ndo or Crazybump. The normal map support is generated by taking the basecolor and removing any lighting, simplifying the shapes and considering the heightmap of the texture. There shouldn't be any situations where the normal support is made by just desaturating the basecolor.</p>

<p>Below samples - Left: Basecolor, Middle: Normal support correct, Right: Normal support incorrect</p>
<p><img src="BuildingsProcess/media/image21.png" alt="Machine generated alternative text: &#39;EIEI&#39; . d AEIEII&amp; LEE&#39; " width="1053" height="702" /><img src="BuildingsProcess/media/image22.png" alt="Machine generated alternative text: &#39;EIEI&#39; " width="1056" height="703" /></p>
<p>Ndo workflow order</p>
<p><img src="BuildingsProcess/media/image23.png" alt="Machine generated alternative text: No fm Co EIEI - ECTRuM HEIGHT TO NORMAL ID LARGE SOFT SPECTRUM CLOSEUP CRACKED ASPHALT Co m CuNe S th 999 Chi *led ChiÆled " width="1059" height="891" /></p>
<p>One last consideration: normal maps are our friends!</p>
<p><img src="BuildingsProcess/media/image24.png" alt="Machine generated alternative text: th p on a flat polygon Mapping it aroun d the front of the building p.ctured g helps to &quot;11the lily " width="912" height="643" /></p>

<p>We have basic functionality for tint masks on Districts. The TintMask texture is simply a black and white texture assigned to the TintMask slot in the asset. The color can be previewed in the Lighting tab and assigned in the Landmarks &gt; District artdef.</p>
<p><img src="BuildingsProcess/media/image25.png" alt="Machine generated alternative text: Info sun sale sky sale —1 Siu Spe E &quot;He Em ble L i ghtMapWe&#39;ht —O with th is Lig h tMap NO TINT MASK (&quot;2,512) LSI 2*512) (Slb512) 01S ; ABLAC K AND WHITE MAP TINT MASK " width="1056" height="667" /></p>

<p>New functionality has been added for AO maps. We now can assign ambient occlusion to the <em>asset</em> instead of on each material contained within that asset. Asset-level AO will overwrite any material based AO on that particular asset. Otherwise it will default to the individual material AO maps. This is an important tool for multi-sub assets. (this is also outlines in Building Naming Conventions).</p>
<p><img src="BuildingsProcess/media/image26.png" alt="Machine generated alternative text: DIS ENC Barracks Classical.ast DIS CTY RM House 05 DIS REL Temple.ast Behaviors Properties Name Class Name Desc ri pticn C ategorization Tags Cook Pa rams Value Animations Particles DIS ENC Barracks Classical HeroBuiIding (I items) O HeroBuiIdinq Geometries Attachments Building Obstruction Profile " width="579" height="344" /></p>

<p>District/Improvement Setup</p>
<p>Wednesday, August 17, 2016</p>
<p>1:38 PM</p>

<p>There are typically 7 elements when it comes to setting up Districts and Improvements</p>

<ol style="list-style-type: decimal">
<li>
<p><strong><em>Tilebases</em> (TB)</strong> - These are the base asset which hold any combination of attachments and herobuildings and typically are paired with a matching decal.</p>
</li>
<li>
<p><strong>Attachments</strong> - An individual asset which is referenced by a tilebase. Has terrain following and culling.</p>
</li>
<li>
<p><strong>Herobuildings (HB)</strong> - Main building assets which are usually referenced by gameplay and are part of a tilebase.</p>
</li>
<li>
<p><strong>Decals</strong> - Can be part of a tilebase or an attachment - a second geometry added to an asset.</p>
</li>
<li>
<p><strong>Obstruction Blockers (OBs)</strong> - Used to cull out resources (or curve a road around them in the case of certain improvements). The do not prevent roads from entering into the hex.</p>
</li>
<li>
<p><strong>Road Connection Points (RoadCP)</strong> - Use to connect roads to a district/improvement at given points. Usually try to shoot for 1 per hex-edge.</p>
</li>
<li>
<p><strong>FX Nodes</strong> - Can be placed on tilebases, attachments, or herobuildings.</p>
</li>
</ol>

<p>Let's look more in depth at each one:</p>

<p><strong>Tilebases</strong></p>

<p>Below illustrates a typical district setup. This is the production (PRD) district, industrial era.</p>

<p><img src="BuildingsProcess/media/image27.png" alt="Machine generated alternative text: " width="1190" height="427" /></p>

<p>Improvement tilebases (not pictured here) do not usually contain herobuildings and therefore are typically limited to only era tilebases (4). Districts, on the other hand, have a progression of herobuildings and will require many more tilebases to accommodate both them and the era changes. The only way you can save time and energy when it comes to district tilebases is if your layout doesn't change in the Ancient &gt; Industrial eras where you can make all adjustments on decal materials in editor.</p>

<p>All models you see here are attachments.</p>

<p>The TB on the far left is one which has no herobuildings in it. 1. indicates where the first HB (Workshop) will go and so the attachments have been removed from this area to accommodate for it. The third TB makes allowances for both the Workshop and 2. where the (Factory) will go.</p>

<ol style="list-style-type: decimal">
<li>
<p>Tilebase attachment point helper object (DIS_PRD_Industrial_Base_01)</p>
</li>
<li>
<p>Tilebase decal point helper object (DIS_PRD_Industrial_Base_01_Decal) (this is typical for decal naming conventions)</p>
</li>
<li>
<p>Road Connection Points</p>
</li>
</ol>

<p><strong>Resource Assets</strong></p>

<p>Tilebases that get various resources added to them are done a little differently.</p>

<p><img src="BuildingsProcess/media/image28.png" alt="Machine generated alternative text: Standard Primitives ObJect Type Sphere C ylinder Torus Teapo t Cone Geo Spher e Tube Pyramid Name and Color RES Bld A002 " width="885" height="397" /></p>

<p>First, you need resource attachments. (See more on attachments below).</p>

<p>Attachments will ultimately get their resource name culled from the attachment. In this example, I have a Deer asset named RES_Deer_Bld_A and a Fox named RES_Fox_Bld_A. So my attachment helpers get that name with the resource name culled (RES_Bld_A). On import, you will be asked what type of resource tilebase you are using if the Editor finds 'RES' in the tilebase asset attachments anywhere.</p>

<p><strong>Attachments</strong></p>

<p>These can either be assets that live in the tilebase Max file or in another Max file. General rule of thumb is if they are specific to a certain improvement or tilebase then keep the attachments in that file.</p>

<p><img src="BuildingsProcess/media/image29.png" alt="Machine generated alternative text: " width="323" height="218" /></p>
<p>The above example shows an attachment in the PRD district file. Windmill on the left (DIS_PRD_Windmill) is the Worked version in the game (with bones for animation). The pivot is place where you want the object to sit. The windmill on the right (DIS_PRD_Windmill_PIL) is the pillaged version. It should have the same pivot. Most attachments do not get CON (construction) states.</p>

<p>Original attachment names are <strong>extremely important</strong>. These are the name the cloud uses to reference that asset and its references. Once these are created they're locked in (unless you go through the painstaking task of deleting from the database and creating a new asset). After naming the original attachment (and making sure its transforms are reset), you can copy the attachment around on the tilebases, making references. Later in the editor, PROP_Barrel023 will have its numbers removed, making it PROP_Barrel and looking for PROP_Barrel in an XLP (which references the original asset).</p>

<p><strong>Herobuildings</strong></p>

<p>Similar to attachments, herobuildings typically live inside the Max file they're referenced by. They differ in that their pivots are typically located based on their placement inside the hex/district and they typically have both PIL and CON states. Example:</p>

<p><img src="BuildingsProcess/media/image30.png" alt="Machine generated alternative text: " width="933" height="336" /></p>

<p>Far left: Worked state. (DIS_AQD_Bath) Middle: PIL and CON building state (DIS_AQD_Bath_PIL) Right: CON scaffolding (DIS_AQD_Bath_CON)</p>

<p>By using the same geometry for the PIL and CON states, we save time and performance/memory. It also saves us texture space for AO maps.</p>

<p><strong>Decals</strong></p>

<p>As indicated above, decals are a separate geometry within an asset. Therefore, they get their own point helper in which their parented to (_decal). We'll get into the setup later, but each decal usually includes an ancient era decal and then an additional era decal above it.</p>

<p>Building Decal Heights</p>

<p>Ancient Decals: 6-10 units +Z from pivot</p>
<p>Classical-Modern Road Decals:  11-15 units +Z from pivot</p>
<p>Other decals which sit on top of the road: 16-20 units +Z from pivot</p>
<p>Burn/Damage Decals: 21-25 units +Z from pivot</p>

<p><strong>Obstruction Blockers (OBs)</strong></p>

<p>As started above, OBs do the following:</p>

<ol style="list-style-type: decimal">
<li>
<p>Prevent city buildings from entering into an area and culling out any attachments inside that area (Districts only)</p>
</li>
<li>
<p>Remove resources from the covered area</p>
</li>
<li>
<p>Make roads wrap around the given area (Improvements only, if no CPs are present)</p>
</li>
</ol>

<p>Example of OB used in Pasture improvement (in this case road would wrap around that OB). OB (pink) can be turned on and off in the Editor.</p>

<p><img src="BuildingsProcess/media/image31.png" alt="Machine generated alternative text: groun Skybox Toggle Joints Toggle Joint Names Toggle Wireframe Show FOW Toggle Decals Expand Decals AlphaFade Graph ics Settings Diffuse Medium Defac IMP Pasture AN O IMP Pasture AN IMP Pasture Base Motion Display Transfo Knobs Show Model Center Show Obstructions Asset State Worked " width="724" height="377" /></p>

<p>Blockers do not get made for individual attachments, just tilebases.</p>

<p>Blockers are generally made quickly my drawing out the borders with a spline in the top view and assigning an Edit Mesh modifier to it. They should be 2D, no height information, pivot centered to the tilebase Point Helper object, and ended with the _OB suffix. (example IMP_Pasture_AN_OB)</p>

<p><strong>Road Connection Points (RoadCP)</strong></p>

<p>As described above - try for 1 per hex. Made with Point Helpers. Road connects and is aligned on the Y+ direction. These should be named Road_CP(XX) in Max.</p>

<p><strong>FX Nodes</strong></p>

<p>When possible, put FX nodes on the attachments, not the tilebase (as they instance as well). FX nodes can be turned on and off in any state and can receive any sorts of transforms. They can be parented to any portion of the asset but typically are parented to the helper object of the asset.</p>

<p>FX nodes are usually labeled FX_(effecttype). (example FX_Smoke)</p>










<p>District/Improvement Import</p>
<p>Wednesday, August 17, 2016</p>
<p>1:38 PM</p>

<p>As a reminder from before, these are the elements you will typically find in a district or improvement:</p>

<ol style="list-style-type: decimal">
<li>
<p><strong><em>Tilebases</em> (TB)</strong> - These are the base asset which hold any combination of attachments and herobuildings and typically are paired with a matching decal.</p>
</li>
<li>
<p><strong>Attachments</strong> - An individual asset which is referenced by a tilebase. Has terrain following and culling.</p>
</li>
<li>
<p><strong>Herobuildings (HB)</strong> - Main building assets which are usually referenced by gameplay and are part of a tilebase.</p>
</li>
<li>
<p><strong>Decals</strong> - Can be part of a tilebase or an attachment - a second geometry added to an asset.</p>
</li>
<li>
<p><strong>Obstruction Blockers (OBs)</strong> - Used to cull out resources (or curve a road around them in the case of certain improvements). The do not prevent roads from entering into the hex.</p>
</li>
<li>
<p><strong>Road Connection Points (RoadCP)</strong> - Use to connect roads to a district/improvement at given points. Usually try to shoot for 1 per hex-edge.</p>
</li>
<li>
<p><strong>FX Nodes</strong> - Can be placed on tilebases, attachments, or herobuildings.</p>
</li>
</ol>

<p>Typical importing workflow:</p>

<p><strong>Import Attachments</strong></p>

<p>First, import your attachments. The longhand method would be to go under File &gt; New in Asset Editor and select Asset from the list. This only does one asset at a time.</p>

<p><img src="BuildingsProcess/media/image32.png" alt="Machine generated alternative text: aa Pick the file type to create Tenure Analytic Light Light Rig Game At Specifi. File Type Entities Animation Environment I_jght Behavior Packages Material Particle Efect " width="388" height="276" /></p>

<p>That method is longer and serves only as a backup in the event scripts are broken.</p>

<p>Instead, use File &gt; Run Scripts and navigate to <em>C:\Program Files\Civ6\Asset Cloud - Civ6\AssetEditor\Scripts.</em> This will do one or multiple assets at a time.</p>

<p>Run <em>Create_Assets_From_Source_File.py</em></p>

<p>The next dialog will give you a list of classes to choose. Tilebase attachments (which are used in Districts, Improvements, and Wonders) will always be the Tilebase class. After this, you will be prompted for a Max File and assets within that Max File which you would like to make attachments out of. Select the assets you want (as Landmarks) and import. The time it takes for this is dependent on how many assets you're importing.</p>

<p>After import it will prompt you to put the assets in an .xlp. Tilebases go in the Tilebase.xlp. If that .xlp is open in the Asset Editor, it will automatically added them without prompt. As always, <em><strong><em>make sure you have the latest .xlp before adding your new assets to it</em></strong></em>.</p>

<p><strong>Import Tilebases</strong></p>

<p>Tilebases are imported the same way attachments are except they should have their attachments flagged in Max with <em>Export as Bone</em>.</p>

<p><img src="BuildingsProcess/media/image33.png" alt="Machine generated alternative text: Firaxis Model Manager Objects In Scene Objects To Export Clear List Advanced IJVW Remo ve Perspective Ma tch Selected Object DIS PRO ald A002 V Ex»rtasaone Llse Granny Tangents Clean Scene TileBase Cleanup o o o o o o o o o o o o o o o o o o o o o o o o o o) DIS DIS DIS DIS DIS DIS DIS DIS DIS DIS DIS DIS DIS DIS DIS DIS DIS DIS DIS DIS DIS DIS DIS DIS DIS DIS Pot Pot Pot Pot Pot Pot Pot Pot Pot Pot Pot Pot Pot Pot Pot Pot Pot Pot Pot Pot Pot Pot Pot Pot orange007 Orange012 Orange014 OrangeOIS Orange016 orange017 Orange018 OrangeOIg orange020 Orange021 orange022 Orange024 orange025 orange026 orange027 orange028 orange02g orange030 Orange031 orange032 orange033 Orange034 orange035 orange038 ald A ald 4001 DIS DIS DIS DIS DIS DIS DIS DIS DIS DIS DIS DIS DIS DIS DIS DIS DIS DIS DIS Pot Pot Pot Pot Pot Pot Pot Pot Pot Pot Pot Pot Pot Pot Pot Pot Pot OrangeOIg (Bone Only) Orange020 Gone Only) Orange021 (Bone Only) Orange022 (Bone Only) Orange024 (Bone Only) Orange025 (Bone Only) Orange026 (Bone Only) Orange027 (Bone Only) Orange028 (Bone Only) Orange02g Gone Only) Orange030 (Bone Only) Orange031 (Bone Only) Orange032 (Bone Only) Orange033 (Bone Only) Orange034 (Bone Only) Orange035 (Bone Only) _Orange038 (Bone Only) ald A ald 4001 (Bone only Granny Models in Expy t List DIS DIS DIS DIS DIS Num PRO Factory PRD Classical Base 01 PRD Classical Base 01 Decals PRD Classical Base 02 Decals PRD Industrial Base 03DecaI of Granny Models: 169 V Auto-sync Selecton " width="999" height="354" /></p>


<p>Notice the difference. Attachments will have geometries listed as well as meshes listed under that.</p>

<p><img src="BuildingsProcess/media/image34.png" alt="Machine generated alternative text: Properties Name IMP SILO Launch Pad Class Name Tile Base Desc ri pticn Landmark Activated M... M... Last Refreshed At: 3:34:45 pm Time Of Day: Day Text (I items) Tile Base Animations Particles Behaviors Burn Defat Categorization Tags Cook Params Geometries Attachments IMP SILO Launch _ Pad (IMP SILO Launch _ Pad); Vettex Count: ICE2; Primitive Count: 738; Bone Count 2 IMP SILO Launch Pad PIL (IMP SILO Launch Pad PIL). Vertex Count: ISO. Primitive Count: 1065. Bone Count IMP SILO Launch Pad PIL Decal (IMP SILO Launch Pad PIL Decal); VertexCount 8. PrimitiveCount 4. BoneCount 2 Mesh IMP IMP IMP IMP IMP SILO SILO SILO SILO SILO Launch Launch Launch Launch Launch Pad Pad Pad Pad Pad Group IMP SILO IMP SILO IMP SILO IMP SILO IMP SILO B... Worked U nwor ked B.. . Pillaged Constructi Unbuilt State Material IMP SILO IMP SILO IMP SILO IMP SILO IMP SILO Visible v I FOWMateriaI Base B ase Base B ase Base True T rue False False FOW/DefauIt M aterial FOW/DefauItMateriaI FOW/Defau It M aterial FOW/DefauItMateriaI FOW/DefauIt M aterial " width="576" height="273" /></p>

<p>Tilebases do not have this. All of their information is contained at the attachment level.</p>

<p><img src="BuildingsProcess/media/image35.png" alt="Machine generated alternative text: IMP SILO.ast IMP SILO Launch Pad. ast et H reviewer Last Refreshed At: 3:3444pm Time Of Day: Day Behaviors Properties Basic Name Class Name Desc ri pticn Animations Particles IMP SILO Tile Base Text C ategorization Tags Cook Params (I items) Tile Base Geometries Attachments IMP SILO (IMP SILO); Vertex Count: O. Primitive Count: O. Bone Count O IMP SILO Decals (IMP SILO Decals); VertexCount 940. Primitive Count 582. Bone Count 73 IMP SILO Launch Pad PIL (IMP SILO Launch Pad PIL). VertexCount 1660. PhmtiveCount 1065. Bone Count IMP SILO Launch Pad PIL Decal (IMP SILO Launch Pad PIL Decal); VertexCount 8. PnmtiveCount 4. Bone Count 2 Mesh Group State " width="576" height="306" /></p>

<p>This means that states, covered later, are done at the attachment level (not the tilebase level)</p>

<p><strong>Import Herobuildings (Districts only)</strong></p>

<p>Importing is the same as Tilebase assets. Herobuildings, like Tilebases, may contain attachments. Attachments cannot support other attachments, however. Herobuildings get added to the <em>Herobuildings.xlp</em>.</p>

<p><strong>Geometry States and Parameters</strong></p>

<p><img src="BuildingsProcess/media/image36.png" alt="Machine generated alternative text: Cook Params Geometries Attac h ments Animations Particles Behaviors Burn Material Default Burn M aterial IMP SILO Launch _ Pad (IMP SILO Launch _ Pad:.; Vettex Count: ICE2; Phmitive Count: 738; Bone Count 2 IMP SILO Launch Pad PIL (IMP SILO Launch Pad PIL). Vertex Count: ISO. Primitive Count: 1065. Bone Count IMP SILO Launch Pad PIL Decal (IMP SILO Launch Pad PIL Decal); VertexCount 8. Primitive Count 4. Bone Count 2 Mesh 1M P SILOLaunchPad Mesh Mesh Mesh Mesh Group IMP SILOBase Stat U nwor ked Pillaged Construction U nbuilt Material Visible True T rue False False True FOWMateriaI FOW/DefaultM FOW/DefauItMateriaI FOW/Defau It M aterial FOW/DefauItMateriaI FOW/Defau It Mate rial IMP IMP IMP IMP IMP SILO SILO SILO SILO SILO Base B ase Base B ase Base IMP SILO IMP SILO IMP SILO IMP SILO Launch Launch Launch Launch Pad Pad Pad Pad IMP SILO IMP SILO IMP SILO IMP SILO B ase Base B ase Base " width="864" height="282" /></p>

<p>The red circle indicates how to bring in new or existing geometries. You can use this to add decals to your asset (tilebase decals, pillaged decals, etc.) or PIL or CON states (as outlined in District/Improvement Setup)</p>


<p><strong>Mesh</strong> indicates the name of the geometry in the Max file.</p>
<p><strong>Group</strong> is the name of the material assigned to the asset in the Max file.</p>
<p><strong>State</strong> is used for visibility of the asset. In this case our non-destroyed version is set to be visible in the Worked/Unworked/Unbuilt states. The PIL geometry would be set to True for the Pillaged and Construction states. This can vary from asset to asset. Improvements, for example, have specific Worked and Unworked states and may have assets turned on and off during those states.</p>
<p><strong>FOWMaterial</strong> can usually be left to the default. If an asset has transparent edges there is a &quot;No Lines&quot; version of the material which turns off the transparent geometry edges.</p>
<p><strong>BurnMaterial</strong> is on Pillaged states by default. It applies a burn shader to the pillaged version of the asset programmatically.</p>


<p><strong>Adding attachments and parameters</strong></p>

<p>So how do we get the attachments on the Tilebase?</p>

<p>They are already assigned to the asset, we just cannot see them yet. Currently there is a script which will update attachments on an asset. It will add any new attachments to the tilebase. It is <em>Update_Asset_Attachments.py.</em> This will look at any bone objects you have parented on an asset and make an attachment for it.</p>

<p>If you are doing an asset which uses resources (meaning, there are bones with the name RES in it) it will ask if you want to assign resources to it by asking you what type of resource asset it is. Setup for this was previously discussed.</p>

<p>The editor <em>does</em> allow us to add our own attachments directly (without having them in Max) but this is typically used by FX artists who don't want to deal with Max files. This button is circled below.</p>

<p><img src="BuildingsProcess/media/image37.png" alt="Machine generated alternative text: Filter: acne Name Position o.o.o Rotation Scale Asset IMP IMP IMP IMP Connection Type NONE NONE NONE NONE Rescu rceTy pe Terrain FollowMode Pivot Height Pivot Height Pivot Height Pivot Height I Cull Mode VI TerrainType RandomizeAnims Model Instance Point Name Fort Truck Modern Fort Truck Modern002 SILO Contr01001 SILO Launch Pad001 IMP IMP IMP IMP IMP IMP IMP Fort Truck Modern Fort Truck Modern002 SILO Contr01001 SILO Launch Pad001 Fort Truck Modern Fort Truck Modern SILO Control SILO Launch Pad IMP IMP IMP IMP SILO SILO SILO SILO DON DON DON DON &#39;T CARE &#39;T CARE &#39;T CARE &#39;T CARE OPTIONAL OPTIONAL OPTIONAL OPTIONAL DON DON DON DON &#39;T CARE &#39;T CARE &#39;T CARE &#39;T CARE True T rue True True " width="1101" height="118" /></p>



<p>Let's look at parameters.</p>


<p><strong>Attachment Point Name</strong> is the name of the asset in Max. You can rename this without it affecting anything but by default it does use the name in Max.</p>
<p><strong>Model Instance</strong> is the name of the parent the attachment point is a child of.</p>
<p><strong>BoneName</strong> is the literal asset name in Max that a bone was created out of. You can assign this to other bones if you want to make the asset appear somewhere else but by default this is typically left alone.</p>
<p><strong>Position, Rotation, Scale</strong> allow for manual transforms on an attachment in the Editor. This can end up desyncing Max files so use with caution.</p>
<p><strong>Asset</strong> is the name of the asset being attached to the attachment point. Notice the numbers have been removed as discussed in District/Improvement Setup<strong>.</strong> If it is an effect, it should not have anything here.</p>
<p><strong>Connection Type</strong> refers to road connections. If you have your helpers named <em>Road_CP</em> in Max, this will default to <em>Road</em>.</p>
<p><strong>ResourceType</strong> used for resource types if you have an asset which uses a specific asset on a specific resource hex, such as mines and quarries.</p>
<p><strong>TerrainFollowMode</strong> Pivot is the default and usually what you want. Average and maximum both sample the bounding box and place the asset accordingly. None uses no terrain following.</p>
<p><strong>CullMode</strong> <em>Optional</em> (default) - makes the asset get removed by city buildings, roads, and bodies of water. <em>Important</em> - only gets culled from water. <em>Permanent</em> - never gets removed.</p>
<p><strong>TerrainType</strong> will set the asset to render only on certain terrain types.</p>
<p><strong>RandomizeAnims</strong> offsets animations on a given attachment, creating variation across the same repeated attachment.</p>


<p><strong>FX</strong></p>

<p>Any FX nodes you create should show up on the attachment list as stated above. And again, there should be no assets attached to it.</p>

<p>FX can be done manually or with a script.</p>


<p><strong>Manually</strong></p>



<p><img src="BuildingsProcess/media/image38.png" alt="Machine generated alternative text: DIS CTY Properties Name Class Name Desc ri pticn MGG Block_LG SQ01ast DIS CTY MGG Block LG C ityB lock Standard Landmark Asset Previewer Last Refreshed At: Time Of Day: Day Type W&#39;avior ktachment P oint Duration TimeSeconds Global Previewer Info CityBIock Base Camera H Knobs Reset Lighting Hide Skybox Text Color Sac kgrcu nd Color Skybox Toggle Joints Toggle Joint Names Toggle Wireframe Show FOW Toggle Decals Expand Decals AlphaFade Graph ics Settings Text (I items) C ityB lock Animations Particles Behaviors Categorization Tags Cook Params Geometries Attachments Filter: Attachment Point Name FX_Light Blink FX Smoke EX Smoke005 Asset Trigger : Properties PILLAGED A H,&#39;ORKEC Acti on ArtOefVFX Asset VFX Asset VFX Light Trans fer Model Instance DIS CTY MGG DIS CTY MGG DIS CTY MGG Position History Bone Name FX_Light Blink EX PIL EX Smoke005 Block LG 01 Default DIS CTY Bock LG SQ_OI Attachment Point EX Smoke005 FX_Smoke LG_SQOI_ Reset To Defat Attac DIS CTY MGG Block LG DIS CTY Base Motion Display Transform Asset VFX FX FX Smoke005 Asset Previewer LOOP Building_Steam (FX SmokeOOö) Light Fader Red Building (FX Light Blink) " width="981" height="532" /></p>



<p>You can see the FX attachments on this asset in the middle. Just like animations, you need to have a DSG assigned. First, (1) Create a Timeline. Name it whatever the state is under animations. In this case, the asset has two timelines, Worked State (light blinks at night and steam effects) and Pillaged State (burn smoke). Here was can see the WORKED_A timeline was created. (2) Beside Asset VFX (where the red line is), R-Click and create a new keyframe. Keyframes can then be selected (3) and have an effect assigned to it (4). Asset refers to the effect that will play and Attachment Point refers to the bone you want that effect to play on. If it is a loopable animation, Duration should be set to -1.</p>



<p>(5) shows options to toggle on the bone and bone names in the event you need to troubleshoot an effect not playing properly.</p>

<p>Currently this system is a little buggy and sometimes requires a close down and re-open of the asset to work.</p>



<p><strong>Script</strong></p>

<p>The script can save a ton of time in regards to FX setup. Go to File&gt;Run Script and select <em>Add_FX_To_Tilebases.py.</em></p>

<p><img src="BuildingsProcess/media/image39.png" alt="Machine generated alternative text: a Assign FX to Tilebases Fltter AO Emitter Large Archer Amow Trail Balloons FAce Radial 3D Face Velocity AA aplo Aero Windsock ArcraftCamer AntiAr Muzzleflash ArcraftCamer BowWake Wake ArcraftCamer Bow Wake Aircraft Camer Wake Airstrip Windsock AmphitheaterFIag AntiAr Muzzleflash 01 Fltter kt achment P Oint WORKED A Add Assets FXto Add FX Duration - Process Assets Apostle Apostle Apostle Apostle Apostle Apostle Dirt Grass Sand Snow Water ktack Ground O ktack Staff 01 Martyr 01 Shock Ground O Sparkles In 01 Arc Sparks Burst Arc Sparks Continuous Arc Sparks Parent Arc Sparks Wonder Animation Add FXto Selection " width="681" height="472" /></p>



<p>First, select <em>Add Assets</em> in the upper right. This will prompt you with a dialog which will allow you to select a group of assets to add FX to. <em>Important! These assets must already have attachment bones for FX added to it.</em></p>

<p><img src="BuildingsProcess/media/image40.png" alt="Machine generated alternative text: Assign FX to Tilebases Rher blink 2 02 2 04 2 06 2 08 2sec &#39;sec 7%ec Animation Fltter ktachmentPoint 02 PIL DIS DIS DIS DIS DIS DIS CTY CTY CTY CTY CTY cry CTY CTY MCG MCG MCG MCG MCG MGG Block Block Block Block Block Block Block Block so SQ SQ SQ SQ so SQ SQ Add Assets FXto Add 01 01 02 02 03 03 Process Assets Ljght Light Ljght Ljght Light Light Ljght Ljght Ljght Light Ljght Blinker Red Blinker White EX WORKED A Light _ Blink Smoke 005 Smoke LG SQ O PIL Smoke are MCG Block LG SQ Light_BIinkCCI SmokeOOE F,re LG SQ 03 PIL Broadway Broadway Broadway Broadway Broadway Broadway Broadway Broadway Bro adway Blink Blink Blink Blink Blink Blink Blink Blink Blink Add FXto Selection " width="679" height="472" /></p>

<p>First you select your effect (1). Next you (2) select which attachment points you want that effect to be on. (3) Select your Timeline and Duration (4), remembering what was discussed in the manual method. (5) Assign the effect to the selected attachment points. You can do as many effects and timelines as you want. When ready, Process Assets (6).</p>

<p>Using the script will automatically add the DSG, Timelines, and all FX to selected attachment points.</p>


<p><strong>Animations</strong></p>

<p>Setup has been previously documented here - Adding animation to Buildings</p>

<p><strong>Obstruction Blockers (OBs)</strong></p>

<p>OBs are added in the Cook Parameters of a tilebase or attachment.</p>


<p><img src="BuildingsProcess/media/image41.png" alt="Machine generated alternative text: DIS CTY Properties Name Class Name Desc ri pticn MGG Block LG SQ01.ast DIS CTY AWW Tile Base Landmark WaterMiII DIS CTY AWW.ast Asset Previewer Last Refreshed At: 10: 19: 14 am Time Of Day: Day Text Text (2 items) HeroBuiIding Tile Base Categorization Tags Cook Pa rams Value 3urnEdge31end Bu rn Height CastAO CastSh adows GradientScaIe Obstruction Animations Particles Behaviors Geometries Attachments DIS CTY Watermill_ 0 23 Obstruction Profile AutcGenera... " width="992" height="442" /></p>



<p><strong>Obstruction Profile AutoGenerate</strong> is the default if no manual blockers are added. <strong>Obstruction Profile</strong> is where you can add a new or existing profile to an asset for better control.</p>


<p><strong>Artdef Setup</strong></p>

<p>After you have your assets set up you need to add your District and Improvement tilebases (not attachments) to the Artdef.</p>

<p><img src="BuildingsProcess/media/image42.png" alt="C:\74741245\F0A4F1AD-AE5D-4B3D-84B4-FD2A3508EFC1_files\image048.png" width="93" height="37" /></p>

<p>District and Improvements use the Landmarks.artdef.</p>

<p>In this example we will look at the IMP_Fort setup:</p>

<p><img src="BuildingsProcess/media/image43.png" alt="Machine generated alternative text: Landmarks.artdef Alt Definition Template Landmarks Remove DEFAULT FEATURE OASIS Open Source file Filter: Name Eras001 Eras002 Eras003 Tag _ Era DEFAUL ARTERA INDUSTRIAL ARTERA MODERN Medieval Base Industrial Base Modern Base Tag Culture DEFAULT DEFAULT DEFAULT Tag Appeal ANY ANY ANY Asset IMP Fort IMP Fort IMP Fort M M M AIRSTRIP CAMP BEACH RESORT CAMP CHATEAU COLOSSAL HEAD FARM FISHING BOATS FORT " width="858" height="418" /></p>

<p>Here you can see the dropdown under the fort has settings for Eras. Most improvements have 2 assets.The fort has 3. In this case the Classical Era fort is used <em>as long as it isn't the Industrial or Modern</em> eras. The industrial fort asset is used during the Industrial Era and the modern fort asset in the Modern Era. Each of these eras was added with the gear+ icon at the top.</p>

<p>In most cases <strong>Name</strong>, <strong>Culture</strong> and <strong>Appeal</strong> will not be used and can be left at default values.</p>

<p>Districts are a bit more complicated:</p>

<p><img src="BuildingsProcess/media/image44.png" alt="Machine generated alternative text: Districts DEFAULT DISTRICT DISTRICT DISTRICT DISTRICT CISTRICT ACROPOLIS AERODROME AQUEDUCT BATHS Name Name Value DistrictGeneratcr TintCcIcr IsAuthcred ISA ig n edToCcast blJseCityScaIe FlattenTerrain Generator DISTRICT CAMPUS Gen GenericDistrict .18, 55, 193 Bas ants BuildingVariants C:&#39; BuildingSets DISTRICT CITY CENTER " width="576" height="181" /></p>

<p>With Campus selected, you can see a number of parameters. Honestly, you shouldn't need to adjust most of these settings. I do want to highlight:</p>


<p><strong>TIntColor</strong> - this is the district color. It tints anything with a tint mask that color in that district.</p>
<p><strong>FlattenTerrain</strong> - this feature <em>is</em> actually available on improvements as well. This softens the hills on terrain and allows the tilebase to have less issues with clipping. An example of something that doesn't use this is farms.</p>


<p>First we add to our Building Sets</p>

<p><img src="BuildingsProcess/media/image45.png" alt="Machine generated alternative text: Land marks.artdef Alt Definition Template Landmarks Remove Districts Open Source file Name Name LIBRARY, UNIVERSITY ACROPOLIS AERODROME AQUEDUCT BATHS CAMPUS DEFAULT DISTRICT DISTRICT DISTRICT DISTRICT DISTRICT Values Set O Element Element (2 items) BUILDING LIBRARY BUILDING UNIVERSITY BaseVariants BuildingVariants BuildingSets LIBRARY LIBRARY, LIBRARY, LIBRARY. LIBRARY, MADRASA MADRASA. REASEARCH LAB UNIVERSITY UNIVERSITY, RESEARCH LAB " width="858" height="454" /></p>

<p>This is a list of different configurations we can have on a district. It should follow the order of the Design One Note (City Districts) and use the herobuilding names lower in the Landmarks.artdef. Add new entries with the gear+ icon.</p>

<p>Under each entry on the list, add new buildings with the green + icon, selecting the buildings with the dropdown on the right.</p>

<p><img src="BuildingsProcess/media/image46.png" alt="Machine generated alternative text: Districts DEFAULT DISTRICT DISTRICT DISTRICT DISTRICT DISTRICT ACROPOLIS AERODROME AQUEDUCT BATHS CAMPUS Filter: Name Bu ildingVariants002 B uiIdingVariants004 BuildingVariants005 B uiIdingVariants2 Tag Herc3uiIding Tag Era ARTERA MODERN DEFAULT DEFAULT DEFAULT DEFAU Tag Culture DEFAULT CIVILIZATION DEFAULT DEFAULT DEFAU ARABIA Asset DIS CMP Research DIS CMP Madrasa HB ERROR DIS CMP Library DIS_CM niversity Tag Appeal ANY ANY ANY ANY AN BUILDING BUILDING BUILDING BUILDING RESEARCH LAB MADRASA OBSERVATORY LIBRARY UNIVERS BaseVariants C:&#39; BuildingSets " width="1058" height="148" /></p>

<p>Next we can fill out the BuildingVariants, adding a new entry with the gear+ icon. Here we can set one of the herobuildings as defined in our BuildingSets, set it to display in a certain era and which art asset we want to use for that entry.</p>

<p><img src="BuildingsProcess/media/image47.png" alt="Machine generated alternative text: DISTRICT DISTRICT DISTRICT DISTRICT AERODROME AQUEDUCT BATHS CAMPUS Name BaseVariantsOOI BaseVariants002 BaseVar iants003 BaseVar iants004 BaseVariants005 BaseVariants005001 BaseVariants006 BaseVar iants007 BaseVariants008 BaseVa nts008001 BaseVar iants009 BaseVariantsOIO BaseVariantsOI I BaseVariantsOIIOOI BaseVariants012 Base VariantsOI 2001 Set Herc3uiIdings Tag _ Era ARTERA ANCIENT ARTERA ANCIENT ARTERA CLASSICAL ARTERA CLASSICAL ARTERA CLASSICAL ARTERA CLASSICAL ARTERA INDUSTRIAL ARTERA INDUSTRIAL ARTERA INDUSTRIAL Tag Culture DEFAULT DEFAULT DEFAULT DEFAULT DEFAULT CIVILIZATION DEFAULT DEFAULT DEFAULT CIVILIZATION DEFAULT DEFAULT DEFAULT CIVILIZATION DEFAULT CIVILIZATION Asset Tag Appeal ANY ANY ANY ANY ANY ANY ANY ANY ANY ANY ANY ANY ANY ANY ANY ANY C MP Ancient EMPTY LIBRARY EMPTY LIBRARY LIBRARY, LIBRARY, EMPTY LIBRARY LIBRARY, LIBRARY, EMPTY LIBRARY LIBRARY, LIBRARY, LIBRARY, LIBRARY, UNIVERSITY MADRASA UNIVERSITY MADRASA UNIVERSITY MADRASA UNIVERSITY, RESEARCH MADRASA REASEARCH LAB LAB ARABIA ARABIA ARABIA ARABIA DIS DIS DIS DIS DIS DIS DIS DIS DIS DIS DIS DIS DIS DIS DIS DIS Base B ase Base B ase Base B ase 01 02 01 02 03 CMP CMP CMP CMP CMP CMP CMP CMP CMP CMP CMP CMP CMP CMP CMP Ancient C lassical C lassical C lassical C lassical BaseVariants Bui Idi ngVariants C:&#39; BuildingSets DISTRICT DISTRICT DISTRICT DISTRICT DISTRICT DISTRICT DISTRICT DISTRICT DISTRICT DISTRICT DISTRICT CITY CENTER COMMERCIAL HUB ENCAMPMENT ENTERTAINMENT COMPLEX HARBOR HOLY SITE INDUSTRIAL ZONE LAVRA MBANZA NEIGHBORHOOD Industrial Base 01 Industrial Base 02 Industrial Base 03 Industrial Base 03 ARTERA ARTERA ARTERA ARTERA ARTERA ARTERA ARTERA INDUSTRIAL MODERN MODERN MODERN MODERN MODERN MODERN M odern Modern Modern Modern M odern Mode r n Base B ase Base B ase Base B ase 01 02 03 04 04 " width="1053" height="282" /></p>

<p>Lastly is the BaseVariants, for tilebases, which is similar to what we did for BuildingVariants. Here we can select one of our BuildingSets and then set the era and tilebase assets to use.</p>

<p><strong>Finalizing</strong></p>

<p>After all of this you should be able to cook the Landmarks.artdef and Tilebases.xlp and see your asset in game.</p>


<p>City Building Setup</p>
<p>Monday, August 22, 2016</p>
<p>4:37 PM</p>
<p>City buildings consist of <em><strong>blocks</strong></em> and <em><strong>blds</strong></em> (individual buildings). The process works as follows:</p>

<p>City sets are found in the following directory, by era:</p>
<p>\ArtDev\Buildings\Districts\Cities</p>

<p>When starting a new set, it's best to load up an existing one, to ensure pivots will all be in the right area.</p>

<p><strong>Filler</strong></p>

<p>The first step is to create all of the filler buildings which will be both use on their own as well as used in populating the city blocks. Typically you can get away with about 10-15 variations and color variants as well.</p>


<p>Ancient Wood (AW) filler buildings:</p>



<p><img src="BuildingsProcess/media/image48.png" alt="Machine generated alternative text: " width="576" height="345" /></p>



<p>Another good reason to use an existing file is to make sure buildings have a similar height and base scale, which grows as eras progress.</p>

<p>Filler buildings should have their pivots centered - pivots will be Z (0) so make sure to extend the buildings down past that to account for hills.</p>

<p><em><strong>Before you actually start make sure to read these other helpful links!</strong></em></p>
<p>Naming conventions for filler buildings are found here - Building Naming Conventions and Sizes</p>
<p>There is also documentation regarding building shapes and sizes and how they relate to setup found here - City Filler IDs</p>

<p><strong>Decals</strong></p>

<p>Each filler building gets a decal associated with it, based on era. These should use the same naming convention with an <em>_decal</em> at the end. Decals should never be more than 2 draws (i.e. 1 classical and 1 ancient under it), so make sure to attach any similar material decals.</p>

<p><strong>FX</strong></p>

<p>FX nodes are applied similarly to districts/improvements (good example can be seen here - District/Improvement Import) and should use the <em>FX_effectname</em> naming convention. These can be parented to the building directly or everything to a point helper with the building name.</p>

<p><strong>AO</strong></p>

<p>City blds get their own AO map in UV channel 2, typically at 512x512. If there is only one material being used on the buildings, having the AO in the material works fine. You can have it in the Cook Params as well. It would be recommended to use the script <em>MultiAssign_Landmark_AO.py</em> though if you would choose to do that. This applies the AO map to every building's AO cook param slot. When in doubt, use the material method - it requires less setup/overhead in the event you changed which AO map the building was using.</p>


<p><strong>Blocks</strong></p>

<p>Blocks are then made up of the individual buildings. On your first time through, it is recommended to parent the buildings as is to the block helper nodes. Once they have been appropriately evaluated in the game then they should be attached and optimized.</p>

<p>Typically a cultural set will have 15 blocks (5 types + 3 variants each).</p>


<p>Ancient Wood Block:</p>

<p><img src="BuildingsProcess/media/image49.png" alt="Machine generated alternative text: " width="435" height="418" /></p>



<p>Aside from our current modern set, we wanted to share the blocks amongst a variety of cultural sets and as a result, broke them off into their own geometries. Therefore, they are not included in the parenting/export of a specific block. In the shot above you can see what is group together and what is not. The red node here is the main parent helper of this asset <em>DIS_CTY_LG_SQ_Block_01</em>. The green nodes are Worked FX nodes (torches in this case) and the black nodes represent Pillaged FX (smoke).</p>

<p><img src="BuildingsProcess/media/image50.png" alt="Machine generated alternative text: perties dame lass Name ripticn DIS CTY AW Block_LG C ityB lock Standard Landmark T Of Dav: Dav Text (I items) C ityB lock C ategorizat ion Cook Params Animations Particles Behaviors Geometries Attachments CTY AW Block LG SQ 01 (DIS CTY AW Block LG SQ 01); 7089. 4064. BoneCo CTY Foundation LG SQ Decal Ancient (DIS CTY Foundation LG SQ Decal Ancient); Vertex Count 8. Primitive CTY Foundation LG SQ LgGrayBIock (DIS CTY Foundation LG SQ LgGrayBIock). Vertex Count 96. Primitive Co Group State " width="839" height="414" /></p>

<p>Above shows the setup in Asset Editor. You can see we have three (3) geometries - the buildings/effect nodes as one, the foundation (gray block) as the second, and a decal as the third. You can multi-assign the foundations and the decals to block shapes easier by using the script, <em>Assign_Geo_To_MultipleAssets.py</em>.</p>

<p>Block shapes are defined by their naming conventions and should not need to be modified by the user within the Cook Params.</p>

<p><img src="BuildingsProcess/media/image51.png" alt="Machine generated alternative text: Cook Params Geometries Value Attachments Animations Particles Behaviors DIS CTY AW Base A 310ckShape SQUARE Bu rn Edges lend " width="576" height="147" /></p>

<p><strong>AO</strong></p>

<p>AO on city blocks needs to be done at the asset level since it pulls in multiple materials/meshes. City blocks get their own dedicated AO map, on channel 2. Again, using the <em>MultiAssign_Landmark_AO.py</em> script can be super helpful in making this quicker.</p>

<p>The block foundations get their UV2 mapping shoved up into roughly the top 16x16 pixels in the upper right hand corner. Therefore, in order to make sure they don't appear too dark in the game, after you generate your block AO map you should make sure at least 32x32 pixels in the upper right corner are made white in Photoshop.</p>

<p><img src="BuildingsProcess/media/image52.png" alt="Machine generated alternative text: " width="576" height="576" /></p>


<p><strong>Importing</strong></p>

<p>After all of your assets are imported they should be added to the <em>city_buildings</em>.<em>xlp</em>.</p>

<p>Next open up the <em>CityGenerators.artdef</em> and go to the <em>Gen_CityCenter &gt; Block</em> section. This is where all of the building assignments are made. To add new buildings to this list, run the script <em>CreateCityBlocks.py.</em> This will provide you with buildings in the <em>city_buildings.xlp</em> and add them to the list. From there you just have to bulk assign the era and culture to the assets.</p>

<p><img src="BuildingsProcess/media/image53.png" alt="Machine generated alternative text: THIS ARTOEF IS INCOMPLETE MAY CHANG Generator DEFAULT Gen CityCenter Block G rcmthStage C:&#39; EraOistribution C:&#39; Gen GenericOistrict PriorityTag GroundingMateriaIs Filter: Name Block001 Block002 Block003 Block004 Block005 Block006 Block007 Block008 Block009 Block010 Block011 Tag Culture Ancient Earth Ancient Earth Ancient Earth Ancient Earth Ancient Earth Ancient Earth Ancient Earth Ancient Earth Ancient Earth Ancient Earth Ancient Earth v I Tag_Era ARTERA ANCIENT ARTERA ANCIENT ARTERA ANCIENT ARTERA ANCIENT ARTERA ANCIENT ARTERA ANCIENT ARTERA ANCIENT Asset City310ck MD B 02 MD B 01 SM B 02 SM B 01 Cabana B 01 XSM B 02 XSM B 01 SM B 03 Tower B 01 Cabana A 01 SM A 03 DIS DIS DIS DIS DIS DIS DIS DIS DIS DIS DIS CTY AE CTY AE CTY AE CTY AE CTY AE CTY AE CTY AE CTY AE CTY AE CTY AE CTY AE Bid Bid Bid Bid Bid Bid Bid Bid Bid Bid Bid ARTERA ARTERA ARTERA ARTERA ANCIENT ANCIENT ANCIENT ANCIENT " width="873" height="267" /></p>

<p>Cooking the <em>CityGenerators.artdef</em> and <em>city_buildings.xlp</em> should allow you to see your new assets in game.</p>

<p>City Filler IDs</p>
<p>Monday, August 08, 2016</p>
<p>12:07 PM</p>

<p>To improve performance, City Filler buildings need to be categorized by size and marked with group IDs in the Asset Editor.</p>

<p>Ted Maselko's overview of the system:</p>

<p><em>&quot;The more CityBlock shapes there are, the longer cities take to update when they grow or change.</em></p>
<p><em>CityBlocks can be assigned into one of several specific 'Block' shapes, or one of several generic 'Filler' shapes.</em></p>
<p><em>Blocks are large, so they fill a city quickly. There are 5 (technically 7) of them, and their shapes are fixed.</em></p>
<p><em>Filler are small, so they take much longer to fill a city. The more filler shapes available, the slower it will run. These shapes can change from set to set.</em></p>

<p><em>The optimal range for different Filler shapes in a set is <strong>four or less</strong>.&quot;</em></p>


<p>To determine the groups for Filler buildings, you need to evaluate the bounding boxes for each model in a City Set.</p>

<p><img src="BuildingsProcess/media/image54.png" alt="Machine generated alternative text: " width="576" height="457" /></p>
<p><em>Ancient Brick City Filler (bottom) and corresponding bounding boxes (top)</em></p>

<p>In the .max file for each city set, select the Filler buildings and run the Edited Bounding Box script to create a corresponding bounding box mesh for each Filler. One handy Maxscript for doing this can be found here:</p>
<p>N:\2KGBAL\Users\tbergantz\Todd Tools Maxscripts\TranslatedBoundingBox_EDIT_DB.mcr. This will show up as the command &quot;Edited Bounding Box&quot; in the 3DS Max Customize User Interface panel. Once installed, this can be triggered by hotkey or as a toolbar button.</p>

<p>Move these bounding boxes off to the side and create a Layer for them called &quot;BB.&quot;</p>

<table>
<tbody>
<tr class="odd">
<td>Make sure to use the Unlink Selection (</td>
<td><img src="BuildingsProcess/media/image55.png" alt="C:\74741245\F0A4F1AD-AE5D-4B3D-84B4-FD2A3508EFC1_files\image061.png" width="40" height="37" /></td>
<td>) button to remove any associations with export models, and remove the bounding box models (all begin with &quot;UBX_&quot; as their prefix) from the Civ 6 Model Manager.</td>
</tr>
</tbody>
</table>

<p>Evaluate all the bounding boxes and note any whose the major axis is inconsistent with the majority. All Filler for a given City set need to have their long axis in the same direction as the rest. If any are not, rotate the Filler building (and its decals), make sure any affected parts have their Xforms Reset, and repeat the process to capture the bounding boxes.</p>

<p>Sort the bounding boxes by size, grouping them into four or less sets ideally. Any Filler whose dimensions on both side is less than 45 Max Units will automatically be padded up to that by the engine and should be grouped together. No group should have only one Filler building.</p>

<p><img src="BuildingsProcess/media/image56.png" alt="Machine generated alternative text: " width="576" height="534" /></p>
<p><em>Ancient Earth City Filler (bottom) and sorted bounding boxes (top)</em></p>

<p>Once you've sorted the bounding boxes into their respective sets, note the contents of each category (see charts below for the core game City Sets). Reimport any Filler that was rotated for consistency; don't forget to update the decals as well.</p>

<p>In the Asset Editor, open each Filler for the set. In the Cook Parameters tab, set the BlockShape value to the corresponding number for the group, starting with Filler_0. The actual number for a group doesn't matter, so long as the assignments for the group are correctly set.</p>

<p><img src="BuildingsProcess/media/image57.png" alt="Machine generated alternative text: DIS CTY AB Bid 10.ast Animations Particles Behaviors Properties Name Class Name Desc ri pticn DIS CTY AB Bid 10 C ityB lock Standard Landmark Attachme. Categorization Tau Co. Para. Geometries Value FILLER 4 310ckShape Burn Edge31end 3urnHeight CastS had cws B lockShape The shape this city block occupies when added to a city. " width="571" height="646" /></p>
<p><em>An Ancient Brick Filler building, set to Filler ID 4</em></p>

<p>Save the .ast file, cook the game, verify there are no asserts, and you're done.</p>

<p><em><em>FAQ</em></em></p>

<p>Q: Why am I doing this again?</p>
<p>A: Talk to Ted</p>

<p>Q: How do I know if I set the Filler IDs correctly?</p>
<p>A: Talk to Ted</p>

<p>Q: Will anyone appreciate this extra step of work on Cities?</p>
<p>A: Talk to Ted</p>

<p>Q: If Ted leaves the project, who do I talk to about this?</p>
<p>A: Unless Ted was fired and/or is dead, talk to Ted.</p>
<p>If you're having issues getting Ted to come out and answer questions, try luring him with snack foods.</p>

<p>Meanwhile, here are the base game assignments for reference:</p>

<table>
<thead>
<tr class="header">
<th>DIS_CTY_AB_Base</th>
<th>Filler_0:</th>
<th>Filler_1:</th>
<th>Filler_2:</th>
<th>Filler_4 (skipped 3):</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td> </td>
<td><p>DIS_CTY_AB_Bld_01*</p>
<p>DIS_CTY_AB_Bld_03</p>
<p>DIS_CTY_AB_Bld_04*</p>
<p>DIS_CTY_AB_Bld_05</p>
<p>DIS_CTY_AB_Bld_08</p>
<p>DIS_CTY_AB_Bld_11</p>
<p>DIS_CTY_AB_Bld_18</p></td>
<td><p>DIS_CTY_AB_Bld_12</p>
<p>DIS_CTY_AB_Bld_13</p>
<p>DIS_CTY_AB_Bld_14</p>
<p>DIS_CTY_AB_Bld_15</p>
<p>DIS_CTY_AB_Bld_16</p>
<p>DIS_CTY_AB_Bld_19</p></td>
<td><p>DIS_CTY_AB_Bld_02</p>
<p>DIS_CTY_AB_Bld_09*</p>
<p>DIS_CTY_AB_Bld_07</p></td>
<td><p>DIS_CTY_AB_Bld_06</p>
<p>DIS_CTY_AB_Bld_10</p>
<p>DIS_CTY_AB_Bld_17</p></td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr class="header">
<th>DIS_CTY_AE_CityLayout - 21</th>
<th>Filler_0:</th>
<th>Filler_1:</th>
<th>Filler_2:</th>
<th>Filler_3:</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td> </td>
<td><p>DIS_CTY_AE_Bld_Cabana_A_01</p>
<p>DIS_CTY_AE_Bld_Cabana_B_01</p>
<p>DIS_CTY_AE_Bld_SM_A_03</p>
<p>DIS_CTY_AE_Bld_SM_B_03</p>
<p>DIS_CTY_AE_Bld_Well_01</p>
<p>DIS_CTY_AE_Bld_XSM_A_01</p>
<p>DIS_CTY_AE_Bld_XSM_A_02</p>
<p>DIS_CTY_AE_Bld_XSM_B_01</p>
<p>DIS_CTY_AE_Bld_XSM_B_02</p></td>
<td><p>DIS_CTY_AE_Bld_SM_A_01</p>
<p>DIS_CTY_AE_Bld_SM_A_02</p>
<p>DIS_CTY_AE_Bld_SM_B_01</p>
<p>DIS_CTY_AE_Bld_SM_B_02</p>
<p>DIS_CTY_AE_Bld_Tower_A_01</p>
<p>DIS_CTY_AE_Bld_Tower_B_01</p></td>
<td><p>DIS_CTY_AE_Bld_MD_A_01</p>
<p>DIS_CTY_AE_Bld_MD_B_01</p></td>
<td><p>DIS_CTY_AE_Bld_LG_A_01</p>
<p>DIS_CTY_AE_Bld_LG_B_01</p>
<p>DIS_CTY_AE_Bld_MD_A_02</p>
<p>DIS_CTY_AE_Bld_MD_B_02</p></td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr class="header">
<th>DIS_CTY_AW_Base - 22</th>
<th>Filler_0:</th>
<th>Filler_1:</th>
<th>Filler_2:</th>
<th>Filler_3:</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td> </td>
<td><p>DIS_CTY_AW_Bld_A_11</p>
<p>DIS_CTY_AW_Bld_B_07</p></td>
<td><p>DIS_CTY_AW_Bld_A_02</p>
<p>DIS_CTY_AW_Bld_A_05</p>
<p>DIS_CTY_AW_Bld_A_06</p>
<p>DIS_CTY_AW_Bld_A_07</p>
<p>DIS_CTY_AW_Bld_A_10</p>
<p>DIS_CTY_AW_Bld_B_01</p>
<p>DIS_CTY_AW_Bld_B_02</p>
<p>DIS_CTY_AW_Bld_B_05</p>
<p>DIS_CTY_AW_Bld_B_06</p>
<p>DIS_CTY_AW_Bld_B_09</p></td>
<td><p>DIS_CTY_AW_Bld_A_01</p>
<p>DIS_CTY_AW_Bld_A_03</p>
<p>DIS_CTY_AW_Bld_A_09</p>
<p>DIS_CTY_AW_Bld_B_08</p>
<p>DIS_CTY_AW_Bld_B_10</p>
<p>DIS_CTY_AW_Bld_B_11</p></td>
<td><p>DIS_CTY_AW_Bld_A_04</p>
<p>DIS_CTY_AW_Bld_A_08</p>
<p>DIS_CTY_AW_Bld_B_03</p>
<p>DIS_CTY_AW_Bld_B_04</p></td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr class="header">
<th>DIS_CTY_RNA_Base - 12</th>
<th>Filler_0:</th>
<th>Filler_1:</th>
<th>Filler_2:</th>
<th>Filler_3:</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td> </td>
<td><p>DIS_CTY_RNA_Bld_01</p>
<p>DIS_CTY_RNA_Bld_09</p>
<p>DIS_CTY_RNA_Bld_10</p>
<p>DIS_CTY_RNA_Bld_17</p></td>
<td><p>DIS_CTY_RNA_Bld_11</p>
<p>DIS_CTY_RNA_Bld_12</p></td>
<td><p>DIS_CTY_RNA_Bld_23</p>
<p>DIS_CTY_RNA_Bld_24</p></td>
<td><p>DIS_CTY_RNA_Bld_13</p>
<p>DIS_CTY_RNA_Bld_21</p>
<p>DIS_CTY_RNA_Bld_22</p>
<p>DIS_CTY_RNA_Bld_25</p></td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr class="header">
<th>DIS_CTY_RMED_Base - 16</th>
<th>Filler_0:</th>
<th>Filler_1:</th>
<th>Filler_2:</th>
<th>Filler_3:</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td> </td>
<td><p>DIS_CTY_RMED_Bld_01</p>
<p>DIS_CTY_RMED_Bld_02</p>
<p>DIS_CTY_RMED_Bld_09</p></td>
<td><p>DIS_CTY_RMED_Bld_04</p>
<p>DIS_CTY_RMED_Bld_07</p>
<p>DIS_CTY_RMED_Bld_013</p>
<p>DIS_CTY_RMED_Bld_014</p>
<p>DIS_CTY_RMED_Bld_016</p></td>
<td><p>DIS_CTY_RMED_Bld_03</p>
<p>DIS_CTY_RMED_Bld_05</p>
<p>DIS_CTY_RMED_Bld_010</p>
<p>DIS_CTY_RMED_Bld_012</p>
<p>DIS_CTY_RMED_Bld_015</p></td>
<td><p>DIS_CTY_RMED_Bld_06</p>
<p>DIS_CTY_RMED_Bld_08</p>
<p>DIS_CTY_RMED_Bld_011</p></td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr class="header">
<th>DIS_CTY_RM_Pieces - 22</th>
<th>Filler_0:</th>
<th>Filler_1:</th>
<th>Filler_2:</th>
<th>Filler_3:</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td> </td>
<td><p>DIS_CTY_RMUG_Bld03</p>
<p>DIS_CTY_RMUG_Bld09</p>
<p>DIS_CTY_RMUG_Bld10</p>
<p>DIS_CTY_RMUG_Bld13</p>
<p>DIS_CTY_RMUG_Bld14</p>
<p>DIS_CTY_RMUG_Bld17</p>
<p>DIS_CTY_RMUG_Bld18</p></td>
<td><p>DIS_CTY_RMUG_Bld01</p>
<p>DIS_CTY_RMUG_Bld02</p>
<p>DIS_CTY_RMUG_Bld04</p>
<p>DIS_CTY_RMUG_Bld05</p>
<p>DIS_CTY_RMUG_Bld12</p>
<p>DIS_CTY_RMUG_Bld15</p>
<p>DIS_CTY_RMUG_Bld19</p>
<p>DIS_CTY_RMUG_Bld20</p>
<p>DIS_CTY_RMUG_Bld21</p></td>
<td><p>DIS_CTY_RMUG_Bld06</p>
<p>DIS_CTY_RMUG_Bld08</p>
<p>DIS_CTY_RMUG_Bld11</p>
<p>DIS_CTY_RMUG_Bld16</p></td>
<td><p>DIS_CTY_RMUG_Bld07</p>
<p>DIS_CTY_RMUG_Bld22</p></td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr class="header">
<th>DIS_CTY_RSA_Base - 23</th>
<th>Filler_0:</th>
<th>Filler_1:</th>
<th>Filler_2:</th>
<th>Filler_3:</th>
<th>Filler_4:</th>
<th>Filler_5:</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td> </td>
<td><p>DIS_CTY_RSA_Bld_04</p>
<p>DIS_CTY_RSA_Bld_22</p></td>
<td><p>DIS_CTY_RSA_Bld_03</p>
<p>DIS_CTY_RSA_Bld_05</p>
<p>DIS_CTY_RSA_Bld_11</p>
<p>DIS_CTY_RSA_Bld_19</p></td>
<td><p>DIS_CTY_RSA_Bld_01</p>
<p>DIS_CTY_RSA_Bld_06</p>
<p>DIS_CTY_RSA_Bld_13</p>
<p>DIS_CTY_RSA_Bld_18</p>
<p>DIS_CTY_RSA_Bld_21</p>
<p>DIS_CTY_RSA_Bld_23</p></td>
<td><p>DIS_CTY_RSA_Bld_02</p>
<p>DIS_CTY_RSA_Bld_09</p>
<p>DIS_CTY_RSA_Bld_14</p></td>
<td><p>DIS_CTY_RSA_Bld_07</p>
<p>DIS_CTY_RSA_Bld_10</p>
<p>DIS_CTY_RSA_Bld_15</p>
<p>DIS_CTY_RSA_Bld_16</p>
<p>DIS_CTY_RSA_Bld_20</p></td>
<td><p>DIS_CTY_RSA_Bld_08</p>
<p>DIS_CTY_RSA_Bld_12</p>
<p>DIS_CTY_RSA_Bld_17</p></td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr class="header">
<th>DIS_CTY_RE_Base - 42</th>
<th>Filler_0:</th>
<th>Filler_1:</th>
<th>Filler_2:</th>
<th>Filler_3:</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td> </td>
<td><p>DIS_CTY_RE_Bld_Brick_Tower_B_01</p>
<p>DIS_CTY_RE_Bld_Brick_Tower_B_02</p>
<p>DIS_CTY_RE_Bld_Brick_Tower_B_03</p>
<p>DIS_CTY_RE_Bld_Brick_Tower_B_04</p>
<p>DIS_CTY_RE_Bld_Brick_Tower_B_05</p>
<p>DIS_CTY_RE_Bld_Brick_Tower_B_06</p>
<p>DIS_CTY_RE_Bld_Tower_B_01</p>
<p>DIS_CTY_RE_Bld_Tower_B_02</p>
<p>DIS_CTY_RE_Bld_Tower_B_03</p>
<p>DIS_CTY_RE_Bld_XSM_A_01</p>
<p>DIS_CTY_RE_Bld_XSM_A_02</p>
<p>DIS_CTY_RE_Bld_XSM_B_01</p>
<p>DIS_CTY_RE_Bld_XSM_B_02</p></td>
<td><p>DIS_CTY_RE_Bld_Brick_Tower_B_7</p>
<p>DIS_CTY_RE_Bld_Brick_Tower_B_8</p>
<p>DIS_CTY_RE_Bld_MD_A_01</p>
<p>DIS_CTY_RE_Bld_MD_A_02</p>
<p>DIS_CTY_RE_Bld_MD_B_03</p>
<p>DIS_CTY_RE_Bld_MD_B_04</p>
<p>DIS_CTY_RE_Bld_Tower_B_04</p></td>
<td><p>DIS_CTY_RE_Bld_MD_A_03</p>
<p>DIS_CTY_RE_Bld_MD_A_04</p>
<p>DIS_CTY_RE_Bld_MD_A_011</p>
<p>DIS_CTY_RE_Bld_MD_A_024</p>
<p>DIS_CTY_RE_Bld_MD_B_01</p>
<p>DIS_CTY_RE_Bld_MD_B_02</p>
<p>DIS_CTY_RE_Bld_SM_A_01</p>
<p>DIS_CTY_RE_Bld_SM_A_02</p>
<p>DIS_CTY_RE_Bld_SM_B_01</p>
<p>DIS_CTY_RE_Bld_SM_B_02</p></td>
<td><p>DIS_CTY_RE_Bld_LG_A_01</p>
<p>DIS_CTY_RE_Bld_LG_A_02</p>
<p>DIS_CTY_RE_Bld_LG_A_03</p>
<p>DIS_CTY_RE_Bld_LG_A_04</p>
<p>DIS_CTY_RE_Bld_LG_A_05</p>
<p>DIS_CTY_RE_Bld_LG_A_06</p>
<p>DIS_CTY_RE_Bld_LG_B_01</p>
<p>DIS_CTY_RE_Bld_LG_B_02</p>
<p>DIS_CTY_RE_Bld_LG_B_03</p>
<p>DIS_CTY_RE_Bld_LG_B_04</p>
<p>DIS_CTY_RE_Bld_LG_B_05</p>
<p>DIS_CTY_RE_Bld_LG_B_06</p></td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr class="header">
<th>DIS_CTY_RJ_Base - 16</th>
<th>Filler_0:</th>
<th>Filler_1:</th>
<th>Filler_2:</th>
<th>Filler_3:</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td> </td>
<td><p>DIS_CTY_RJ_Bld_01</p>
<p>DIS_CTY_RJ_Bld_02</p>
<p>DIS_CTY_RJ_Bld_04</p>
<p>DIS_CTY_RJ_Bld_12</p>
<p>DIS_CTY_RJ_Bld_16</p></td>
<td><p>DIS_CTY_RJ_Bld_06</p>
<p>DIS_CTY_RJ_Bld_10</p>
<p>DIS_CTY_RJ_Bld_11</p>
<p>DIS_CTY_RJ_Bld_14</p></td>
<td><p>DIS_CTY_RJ_Bld_05</p>
<p>DIS_CTY_RJ_Bld_09</p>
<p>DIS_CTY_RJ_Bld_15</p></td>
<td><p>DIS_CTY_RJ_Bld_03</p>
<p>DIS_CTY_RJ_Bld_07</p>
<p>DIS_CTY_RJ_Bld_08</p>
<p>DIS_CTY_RJ_Bld_13</p></td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr class="header">
<th>DIS_CTY_RC_Base - 16</th>
<th>Filler_0:</th>
<th>Filler_1:</th>
<th>Filler_3 (skipped 2):</th>
<th>Filler_4:</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td> </td>
<td><p>DIS_CTY_RC_Bld_04</p>
<p>DIS_CTY_RC_Bld_07</p>
<p>DIS_CTY_RC_Bld_12</p>
<p>DIS_CTY_RC_Bld_13</p>
<p>DIS_CTY_RC_Bld_16</p></td>
<td><p>DIS_CTY_RC_Bld_01</p>
<p>DIS_CTY_RC_Bld_03</p>
<p>DIS_CTY_RC_Bld_11</p>
<p>DIS_CTY_RC_Bld_14</p></td>
<td><p>DIS_CTY_RC_Bld_05</p>
<p>DIS_CTY_RC_Bld_15</p>
<p>DIS_CTY_RC_Bld_02</p></td>
<td><p>DIS_CTY_RC_Bld_06</p>
<p>DIS_CTY_RC_Bld_08</p>
<p>DIS_CTY_RC_Bld_09</p>
<p>DIS_CTY_RC_Bld_10*</p></td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr class="header">
<th>DIS_CTY_RSS_CityLayout - 27</th>
<th>Filler_0:</th>
<th>Filler_1:</th>
<th>Filler_2:</th>
<th>Filler_3:</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td> </td>
<td><p>DIS_CTY_RSS_Bld_01</p>
<p>DIS_CTY_RSS_Bld_02</p>
<p>DIS_CTY_RSS_Bld_12</p>
<p>DIS_CTY_RSS_Bld_13</p>
<p>DIS_CTY_RSS_Bld_14</p>
<p>DIS_CTY_RSS_Bld_23</p>
<p>DIS_CTY_RSS_Bld_24</p>
<p>DIS_CTY_RSS_Bld_26</p></td>
<td><p>DIS_CTY_RSS_Bld_04</p>
<p>DIS_CTY_RSS_Bld_07</p>
<p>DIS_CTY_RSS_Bld_08</p>
<p>DIS_CTY_RSS_Bld_10</p>
<p>DIS_CTY_RSS_Bld_18</p>
<p>DIS_CTY_RSS_Bld_19</p>
<p>DIS_CTY_RSS_Bld_21</p></td>
<td><p>DIS_CTY_RSS_Bld_03</p>
<p>DIS_CTY_RSS_Bld_06</p>
<p>DIS_CTY_RSS_Bld_09</p>
<p>DIS_CTY_RSS_Bld_15</p>
<p>DIS_CTY_RSS_Bld_17</p>
<p>DIS_CTY_RSS_Bld_20</p>
<p>DIS_CTY_RSS_Bld_25</p>
<p>DIS_CTY_RSS_Bld_27</p></td>
<td><p>DIS_CTY_RSS_Bld_05</p>
<p>DIS_CTY_RSS_Bld_11</p>
<p>DIS_CTY_RSS_Bld_16</p>
<p>DIS_CTY_RSS_Bld_22</p></td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr class="header">
<th>DIS_CTY_INDCL_Base - 9</th>
<th>Filler_0:</th>
<th>Filler_1:</th>
<th>Filler_2:</th>
<th> </th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td> </td>
<td>DIS_CTY_INDCL_Bld_07</td>
<td><p>DIS_CTY_INDCL_Bld_01</p>
<p>DIS_CTY_INDCL_Bld_04</p>
<p>DIS_CTY_INDCL_Bld_05</p>
<p>DIS_CTY_INDCL_Bld_06</p>
<p>DIS_CTY_INDCL_Bld_09</p></td>
<td><p>DIS_CTY_INDCL_Bld_02</p>
<p>DIS_CTY_INDCL_Bld_03</p>
<p>DIS_CTY_INDCL_Bld_08</p></td>
<td> </td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr class="header">
<th>DIS_CTY_IC_Base - 18</th>
<th>Filler_0:</th>
<th>Filler_1:</th>
<th>Filler_2:</th>
<th>Filler_3:</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td> </td>
<td><p>DIS_CTY_IU_Bld_Tall_04</p>
<p>DIS_CTY_IU_Bld_Tall_06</p>
<p>DIS_CTY_IU_Bld_Tall_07</p>
<p>DIS_CTY_IU_Bld_Tall_08</p>
<p>DIS_CTY_IU_Bld_Tall_09</p>
<p>DIS_CTY_IU_Bld_Tall_12</p>
<p>DIS_CTY_IU_Bld_Tall_13</p>
<p>DIS_CTY_IU_Bld_Tall_14</p>
<p>DIS_CTY_IU_Bld_Tall_15</p>
<p>DIS_CTY_IU_Bld_Tall_16</p>
<p>DIS_CTY_IU_Bld_Tall_18</p></td>
<td><p>DIS_CTY_IU_Bld_Tall_01</p>
<p>DIS_CTY_IU_Bld_Tall_03</p>
<p>DIS_CTY_IU_Bld_Tall_05</p>
<p>DIS_CTY_IU_Bld_Tall_11</p></td>
<td><p>DIS_CTY_IU_Bld_Tall_10</p>
<p>DIS_CTY_IU_Bld_Tall_17</p></td>
<td>DIS_CTY_IU_Bld_Tall_02</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr class="header">
<th>DIS_CTY_MG_Base - 19</th>
<th>Filler_0:</th>
<th>Filler_1:</th>
<th>Filler_2:</th>
<th>Filler_3:</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td> </td>
<td><p>DIS_CTY_MG_Bld_01</p>
<p>DIS_CTY_MG_Bld_03</p>
<p>DIS_CTY_MG_Bld_05</p>
<p>DIS_CTY_MG_Bld_06</p>
<p>DIS_CTY_MG_Bld_10</p>
<p>DIS_CTY_MG_Bld_11</p>
<p>DIS_CTY_MGG_Bld_03</p>
<p>DIS_CTY_MGG_Bld_04</p>
<p>DIS_CTY_MGG_Bld_07</p>
<p>DIS_CTY_MGG_Bld_08</p></td>
<td><p>DIS_CTY_MG_Bld_04</p>
<p>DIS_CTY_MG_Bld_07</p>
<p>DIS_CTY_MG_Bld_08</p>
<p>DIS_CTY_MGG_Bld_02</p></td>
<td><p>DIS_CTY_MG_Bld_02</p>
<p>DIS_CTY_MG_Bld_09</p>
<p>DIS_CTY_MGG_Bld_05</p></td>
<td><p>DIS_CTY_MG_Bld_12</p>
<p>DIS_CTY_MGG_Bld_01</p></td>
</tr>
</tbody>
</table>

<p>Building Naming Conventions and Sizes</p>
<p>Thursday, May 07, 2015</p>
<p>11:21 AM</p>


<p><em>Naming Conventions</em></p>

<p>For all districts and cities:</p>

<p>DIS_CTY_XX_Base is the basis for the max file, max file material setup, in game materials, textures, where XX corresponds to era and culture (i.e. DIS_CTY_AW_Base for <em>a</em>ncient <em>w</em>ood DIS_CTY_RE_Base for <em>r</em>enaissance <em>E</em>uropean)</p>

<p>Max files would be called DIS_CTY_XX_Base.max</p>

<p>Models can drop the ‘base’ since they’re more specific.</p>

<p>Block meshes should be named:</p>
<p><em>Rectangular </em></p>
<p>DIS_CTY_XX_Block_REC_01</p>
<p>DIS_CTY_XX_Block_REC_02</p>
<p>DIS_CTY_XX_Block_REC_03</p>

<p><em>Large Square</em></p>
<p>DIS_CTY_XX_Block_LG_SQ_01</p>
<p>DIS_CTY_XX_Block_LG_SQ_02</p>
<p>DIS_CTY_XX_Block_LG_SQ_03</p>

<p><em>Small Square</em></p>
<p>DIS_CTY_XX_Block_SQ_01</p>
<p>DIS_CTY_XX_Block_SQ_02</p>
<p>DIS_CTY_XX_Block_SQ_03</p>

<p><em>Wedge Right</em></p>
<p>DIS_CTY_XX_Block_WR_01</p>
<p>DIS_CTY_XX_Block_WR_02</p>
<p>DIS_CTY_XX_Block_WR_03</p>

<p><em>Triangle Right</em></p>
<p>DIS_CTY_XX_Block_TR_01</p>
<p>DIS_CTY_XX_Block_TR_02</p>
<p>DIS_CTY_XX_Block_TR_03</p>

<p>Individual meshes (examples) should be named:</p>
<p><em>DIS_CTY_AE_Bld_01</em></p>
<p><em>DIS_CTY_AE_Bld_02</em></p>
<p><em>DIS_CTY_AE_Bld_03</em></p>

<p>Main Textures would be:</p>
<p>DIS_CTY_XX_Base_B (basecolor)</p>
<p>DIS_CTY_XX_Base_A (ambient occulsion)*</p>
<p>DIS_CTY_XX_Base_O (opacity)</p>
<p>DIS_CTY_XX_Base_N (normal)</p>
<p>DIS_CTY_XX_Base_G (gloss)</p>
<p>DIS_CTY_XX_Base_M (metalness)</p>
<p>DIS_CTY_XX_Base_E (emissive)</p>
<p>DIS_CTY_XX_Base_L (lightmaps)</p>
<p>DIS_CTY_XX_Base_T (tintmaps)</p>

<p>*Ambient Occlusion can be applied at the single material level or at the asset level. In the case of any asset where you have more than one material being used (City Blocks being a great example), you will want to use ambient occlusion at the Asset's Cook Parameter level, which overrides the material AO.</p>

<p>Note here where there is an AO map being used in the <em>DIS_CTY_RMED_Base</em> material for the individual buildings (which are only one material)</p>

<p><img src="BuildingsProcess/media/image58.png" alt="Machine generated alternative text: Cook Parameters Value 3aseCcIcr Emissive Emissive Minimum Weight Gloss LightMap LightMap Minimum Weight Metal ness Normal Opac ity TintMask ScrollRate DIS CTY DIS CTY DIS CTY DIS CTY RMED RME RMED RMED M N " width="900" height="270" /></p>

<p>Where blocks, because there are more than one material, use it at the Asset's Cook Parameter level.</p>

<p><img src="BuildingsProcess/media/image59.png" alt="Machine generated alternative text: 310ckShape SQUARE Bu rn Edges lend 3urnHeight had cws GradientScaIe " width="899" height="117" /></p>

<p>Wonders, and improvements should follow similar, swapping out the DIS_CTY part. Example WON_Great_Library.*</p>

<p>*Wonders have an additional file for their animation states which should be named similar with &quot;Wonder_Movie&quot; added at the end. Example WON_Great_Library_Wonder_Movie.max</p>

<p>Districts use DIS but then a 3-letter naming convention which identifies with the actual district.  Examples:</p>

<p>DIS_CMP (Campus)</p>
<p>DIS_ENC (Encampment)</p>

<p><em>Texture Sizes</em></p>

<p>These are basic texture sizes and may be subject to change depending on the amount of assets being baked.</p>

<p><strong><em>Cities</em></strong></p>
<p>1024x512 – Basecolor, Normal, Metalness, Gloss, Opacity</p>
<p>1024x1024 – City Block AO</p>
<p>512x512 – Building (Individual) AO</p>
<p>512x512 – Lightmap</p>
<p>256x256 – Emissive</p>
<p>512x512 (Max) – Basecolor, Normal, Metalness, Gloss on Bases</p>
<p>256x256 - Palace AO</p>

<p><strong><em>Districts </em></strong></p>
<p>1024x1024 – Basecolor, Normal, Metalness, Gloss, Opacity</p>
<p>1024x1024 – AO</p>
<p>512x512 – Lightmap</p>
<p>256x256 – Emissive</p>

<p><strong><em>Improvements</em></strong></p>
<p>1024x512 – Basecolor, Normal, Metalness, Gloss, Opacity</p>
<p>512x512 – AO</p>
<p>512x512 – Lightmap</p>
<p>256x256 – Emissive</p>

<p><strong><em>Wonders</em></strong></p>
<p>1024x1024 – Basecolor, Normal, Metalness, Gloss, Opacity</p>
<p>1024x1024 – AO</p>
<p>1024x1024 – Basecolor, Normal, Metalness, Gloss, Opacity (Construction Props/Shared)</p>
<p>1024x512 – Basecolor, Normal, Metalness, Gloss, Opacity (Brick/Shared)</p>
<p>512x512 – Lightmap</p>
<p>256x256 – Emissive</p>

<p>P4 Folder Structure</p>

<p><img src="BuildingsProcess/media/image60.jpg" alt="C:\74741245\F0A4F1AD-AE5D-4B3D-84B4-FD2A3508EFC1_files\image066.jpg" width="403" height="288" /></p>



<p><strong>01_Concept</strong></p>

<p>•         The root folder is where the final (approved) concept lives.</p>
<p>•         There is also an <strong>“InProgress”</strong> sub-folder that holds PSDs, conceptual dead-end, thumbnails, etc.</p>
<p>•         This folder can also showcase feedback mockups, mood-boards, and off-site contactor kickoff information.</p>


<p><strong>02_Model </strong></p>

<p>•         The root folder is where the final or most up to date max files lives.</p>
<p>•         There is also an <strong>“InProgress”</strong> sub-folder where you can put all your working files or any other modeling related files</p>


<p><strong>03_Texture</strong></p>

<p>•         The <strong>“PSDs”</strong> folder is where you can store your master PSDs.</p>
<p>•         The root folder will have you final .tgas for export</p>



<p>Night/Lens Lighting</p>
<p>Wednesday, August 03, 2016</p>
<p>4:59 PM</p>
<p>This page details the process for setting up models for nighttime or specialty lens use. In most cases, only an emissive map is used on buildings, but some assets (particularly Wonders) benefit from a lightmap, either instead of emissive or in conjunction with it. Alternatively, the analytic lighting system can also be used to light assets sparingly.</p>

<p><em>Anatomy of Asset UVs</em></p>

<p>Building assets in the game make use of 2-3 UV channels, dependent on their need for lighting.</p>
<p>This example uses the IMP_Chateau_Main model from //civ6/main/ArtDev/Buildings/Improvements/Chateau/02_Model/IMP_Chateau.max</p>

<p><img src="BuildingsProcess/media/image61.png" alt="Machine generated alternative text: " width="489" height="420" /></p>
<p><em>The Chateau asset in game, with emissive and dynamic light applied</em></p>

<table>
<thead>
<tr class="header">
<th>UV Channel 1 - this is the base art channel handling Basecolor, Metalness, Gloss, Normal, etc.</th>
<th>UV Channel 2 - this channel is used primarily for Ambient Occlusion (AO), but if a Lightmap is necessary for the asset, the Lightmap also uses UV2</th>
<th><p>UV Channel 3 - this channel is only used for Emissive maps.</p>
<p>A model in an asset should only have UV3 if it needs to be lit</p>
<p>with Emissive.</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><em>Chateau - UV1 over Basecolor texture</em></td>
<td><em>Chateau - UV2 over AO texture</em></td>
<td><em>Chateau - UV3 over Emissive texture</em></td>
</tr>
<tr class="even">
<td><img src="BuildingsProcess/media/image62.png" alt="Machine generated alternative text: " width="421" height="421" /></td>
<td><img src="BuildingsProcess/media/image63.png" alt="Machine generated alternative text: " width="421" height="421" /></td>
<td><img src="BuildingsProcess/media/image64.png" alt="Machine generated alternative text: " width="423" height="423" /></td>
</tr>
<tr class="odd">
<td><em>Chateau - Editor view: normal daytime</em></td>
<td><em>Chateau - Editor view: AO daytime</em></td>
<td><em>Chateau - Editor view: night time with emissive enabled</em></td>
</tr>
<tr class="even">
<td><img src="BuildingsProcess/media/image65.png" alt="Machine generated alternative text: " width="423" height="405" /></td>
<td><img src="BuildingsProcess/media/image66.png" alt="Machine generated alternative text: " width="399" height="403" /></td>
<td><img src="BuildingsProcess/media/image67.png" alt="Machine generated alternative text: " width="385" height="403" /></td>
</tr>
</tbody>
</table>

<p>In 3DS Max, you can view the channel information for a model or group models via Tools&gt;Channel Info…</p>

<p><img src="BuildingsProcess/media/image68.png" alt="Machine generated alternative text: Map Channel Info COP/ Buffer Info: Object Name Subcomp Channel Name -none - -none- Lock Update Num Verts 1401 1401 Num Faces Dead Verts Size(KE) 67kb poly -2:AIpha -1:111um O:vc I:map 2:map 3:map Main Main Main Main Main Main Main Main IMP IMP IMP IMP IMP IMP IMP IMP Chateau Chateau Chateau Chateau Chateau Chateau Chateau Chateau " width="526" height="261" /></p>
<p><em>The Map Channel Info dialog for IMP_Chateau_Main</em></p>

<p>In order for Emissive to display on an asset in game, the geometry must have three UV channels. Our editor doesn't understand the numbering of UV channels, only the quantity. If an asset only has UV1 and UV3, the emissive would not function within the editor or the game because it would be interpreted as UV1 and UV2.</p>

<p>It's not uncommon to encounter an asset with all three channels, despite not having been processed for emissive or even needing it. This will cause the entire asset to light up as if it has an emissive checkerboard applied, as the default UV layout for an added channel in 3DS Max is a top down projection of variable size:</p>

<p><img src="BuildingsProcess/media/image69.png" alt="Machine generated alternative text: " width="390" height="391" /></p>
<p><em>Image showing what IMP_Chateau_Main UV3 would look like by default</em></p>

<p>If you encounter an asset that should not have material lighting, you can clear the 3:map channel via the dialog above by right clicking on the channel and choosing Clear:</p>

<p><img src="BuildingsProcess/media/image70.png" alt="Machine generated alternative text: Map Channel Info Name COP/ Buffer Info: Object Name Clear poly v sel -2:AIpha -1:111um O:vc I:map 2: map 3:map Add Subcomp Channel Name -none - -none- -none- -none- Lock Update Num Verts 1401 Num Faces Copy Paste Name Clear Add Update Dead Verts Size(KE) 67kb 25kb 24b Main002 Main002 Main002 Main002 Main002 Main002 Main002 IMP IMP IMP IMP IMP IMP IMP IMP Chateau Chateau Chateau Chateau Chateau Chateau Chateau Chateau " width="445" height="403" /></p>
<p><em>Image showing the right-click options for Map Channel Info</em></p>

<p>After doing this, a <em><strong>UVW Mapping Clear</strong></em> modifier will be added to the Modifier Stack. Collapse the stack to resolve this or delete the modifier to restore the channel information.</p>



<p><em>Emissive</em></p>
<table>
<tbody>
<tr class="odd">
<td><img src="BuildingsProcess/media/image71.png" alt="Machine generated alternative text: " width="462" height="333" /></td>
<td><img src="BuildingsProcess/media/image72.png" alt="Machine generated alternative text: " width="421" height="333" /></td>
<td><p><img src="BuildingsProcess/media/image73.png" alt="Machine generated alternative text: 20 14 BALTI " width="380" height="330" /></p>
</td>
</tr>
</tbody>
</table>
<p><em>Examples of assets using only Emissive lighting</em></p>

<p>The primary goal of Emissive maps is to provide the impression of interior lighting on a structure. The Emissive can also be used to fake the look of projected lighting, taking on the role of the Lightmap and thus saving texture memory. The Emissive texture, however, visually overrides the Basecolor texture, so the use of the Emissive for fake projected lighting should be limited.</p>

<p>The setup for one or more models in a given asset to use Emissive mapping varies depending on the type of asset, but the general procedure is the same:</p>

<ol style="list-style-type: decimal">
<li>
<p>Select the model or models in a given file that need emissive and that share materials</p>
</li>
<li>
<p>Set up UV Channel 3 on those models to isolated faces that need emissive lighting, secluding non-lit faces to the top left pixel</p>
</li>
<li>
<p>Bake the resulting UV3 channel's basecolor to a reference image</p>
</li>
<li>
<p>Pick the appropriate size Emissive template file and add the reference image</p>
</li>
<li>
<p>Use the layer masks in the template file to define and detail the Emissive image</p>
</li>
</ol>



<p>These steps are described in detail later in this section.</p>

<p>The type of asset will largely determine how the Emissive texture is focused:</p>

<p><strong>Improvements and Districts:</strong> Select the model or models in the Max file which should receive the emissive treatment. Isolate those models and evaluate their material usage both in Max and in the Asset Editor. Ideally, they will all share the same material, but particularly in Districts sharing of models from one file to another is common. You will need to make sure the Emissive texture is only applied to materials in use in the given scene, or accidental lighting can occur on other assets.</p>

<table>
<tbody>
<tr class="odd">
<td><img src="BuildingsProcess/media/image74.png" alt="Machine generated alternative text: " width="576" height="345" /></td>
<td><img src="BuildingsProcess/media/image75.png" alt="Machine generated alternative text: " width="345" height="345" /></td>
</tr>
</tbody>
</table>
<p><em>Example: The Entertainment District's set of Emissive models. Despite having 18 different tilebase layouts and almost 3000 parts in the .max file, only these 12 models need to share the emissive UV layout.</em></p>

<p><strong>Cities:</strong> Cities require that all building parts - the city blocks (not including foundation or ground plates), filler buildings, and the related Palace - are included in a shared UV3 layout. This is true even if the Palace uses a unique texture set. Due to the high amount of geometry in use, especially on Ancient sets, it is sometimes necessary to process the UVs in groups. This is most easily broken down into quadrants of the Emissive texture layout.</p>

<table>
<tbody>
<tr class="odd">
<td><img src="BuildingsProcess/media/image76.png" alt="Machine generated alternative text: " width="797" height="327" /></td>
<td><img src="BuildingsProcess/media/image77.png" alt="Machine generated alternative text: " width="327" height="327" /></td>
</tr>
</tbody>
</table>
<p><em>Example: The Renaissance/Chinese Population Building Set - All of the parts shown, including the Palace, share a single Emissive texture and UV layout.</em></p>

<p><strong>Wonders:</strong> Wonders are usually only require one model to be processed for Emissive. This model is not pulled from the individual model directory, but from the final frame of the Wonder movie. This is due to the fact that Wonder models often change in the course of being cut up for the movie, and thus have differing UV1/UV2 changes to accommodate those cuts. It is necessary to work with the Wonder movie artist (currently Rambo) to ensure that a single, optimized model (or main model with attachments) is available through that Wonder movie file. Once the final movie components are selected, the process for creating the Emissive is the same, but less sharing of faces (see below) is typically performed since the Wonders are showcase models seen closer in game.</p>

<table>
<tbody>
<tr class="odd">
<td><img src="BuildingsProcess/media/image78.png" alt="Machine generated alternative text: " width="576" height="377" /></td>
<td><img src="BuildingsProcess/media/image79.png" alt="Machine generated alternative text: " width="375" height="375" /></td>
</tr>
</tbody>
</table>
<p><em>Example: Bolshoi Theatre final frame model and Emissive texture layout</em></p>

<p>Detailed process:</p>

<p><em><em>Select the model or models in a given file that need emissive and that share materials</em></em></p>

<p>The first step, as mentioned above, is to decide which models in the .max file you're working with is meant to receive emissive. Outside of Ancient buildings, this is usually a straightforward choice, as you're looking for windows , open doors, and parts of the model that represent light sources (lamp posts, lanterns, etc.) predominantly. Open archways, notable inset detail, or even the opportunity to add projected light without using a lightmap are options as well. The latter is especially important, as emissive maps tend to be cheaper than lightmaps, which should be used sparingly. The most expensive setup is a model with both emissive and lightmap, reserved for only a few Districts and Wonders as necessary.</p>

<p>We'll use the DIS_AQD_Base_Bath model as an example and walk through the process. The final result for this model has window detail, recessed arches, and faked projection:</p>

<p><img src="BuildingsProcess/media/image80.png" alt="Machine generated alternative text: " width="576" height="390" /></p>
<p><em>The mesh for DIS_AQD_Base_Bath model, with Composite emissive enabled in 3DS Max</em></p>

<p><em><em>Set up UV Channel 3 on those models to isolated faces that need emissive lighting, secluding non-lit faces to the top left pixel</em></em></p>

<p>Once you've determined which models need Emissive, you'll need to get the lit faces of each model onto a shared UV layout. After selecting the models in the Max viewport, apply a shared Unwrap UVW to all of the them. Unwrap UVW defaults to Map Channel 1. Set the Map Channel value to 3 on the modifier panel rollout, and then choose &quot;Move&quot; from the Channel Change Warning dialog that pops up. &quot;Move&quot; will actually copy the UV information from your current channel (1) to the new channel (3).</p>

<p><img src="BuildingsProcess/media/image81.png" alt="Machine generated alternative text: Channel Change Warning This modifier contains edits to only one LIVW channel at a time. You have chosen a new channel. Would you like to: Move the UVs from the current channel to the chosen channel. Abandon changes in this modifier and display the existing UVs in the chosen channel Unwrap I_JVW IJVW Map Edit Poly IJ—wrap L&quot;VW Modify Selection: Select By: Edit UVs Open LIV Editor . Tweak In View Load... Map Channel: Vertex Color Channel " width="1137" height="615" /></p>
<p><em>Example of two selected models with a shared Unwrap UVW being set to Channel 3</em></p>

<p>Once this is complete, Open the UV Editor and you'll use the UV1 layout as your starting point. It's often beneficial to use the Basecolor texture to locate and select openings for Emissive. This method creates your initial groups of faces for emissive, and also helps with locating hidden geometry or partially cut detail that you don't want to light up. Faces may need to be manually selected if there is significant overlap, or if you're intentionally lighting an area that is not an opening.</p>

<p>As a general rule, avoid applying Emissive to a face that shows off an error in the texturing of a model - windows that are cut in half, areas with extreme UV distortion, etc. This is also a good chance to evaluate the model geometry and look for errors and optimization.</p>

<p><img src="BuildingsProcess/media/image82.png" alt="Machine generated alternative text: Reshape Elements Sttch Weld Threshold: 0.00 Detach Arrange Elemen ts V Rescale Rotate Padding: Elemen t Pr oper bes Rescale Priority: Gr oups: " width="1281" height="501" /></p>
<p><em>The two components of the Aqueduct District are slated for Emissive. Window openings on the Bath and archways on both structures were selected via the texture layout, so all instances of those opening are captured. Additionally, the floor, walls, and inner column faces of the Bath opening are selected as an area for faux projected lighting.</em></p>

<p>Once you've isolated the faces you want to light up, invert your selection, Detach the faces to break any possible shared verts or edges, and move the non-lit areas away from the 0-1 space for now. It's best not to leave these parts at the current scale until your UV layout is complete, in case you missed a face or decide you want to light up additional areas.</p>

<p>For the lit areas, your goal is to provide options for variety while maximizing the UV space. Working with each type of opening or area, judge how often the face is used as well as whether there are multiple faces using that section near one another. If a section is used sporadically, one instance on the UV layout may be enough. For windows in particular, it's beneficial to separate a section in three or more groups, so that the same lit window is not side-by-side with itself. The number of times a given group can be split will be determined by how many other elements you have to pack in the UV layout without wasting texture space.</p>

<p><img src="BuildingsProcess/media/image83.png" alt="Machine generated alternative text: Reshape Elemen ts Sttch Weld Thr eshold: Detach Arrange Elemen ts V Rescale Rotate Padding: Elemen t Pr oper bes Rescale Priority: Gr oups: No groups selected " width="1287" height="637" /></p>
<p><em>One of three sections of wall with small arch windows selected, showing which faces are active for that section of the UV layout.</em></p>

<p>Once you've determined the appropriate number of groups for a given model, pack the UV as normal, making sure that there is some buffer in the corners. In some cases, especially where models have towers with window openings only at the top of a rectangular UV element, you can overlap UV islands to save space. For areas where you plan to fake projected lighting, you may find it better to discreetly unwrap in order to overlay diffuse detail in the texture.</p>

<p>*All faces that do not receive Emissive lighting are scaled down to the size of one pixel (give or take a few) and are placed in the top left corner of the UV layout. In the screen below, the small green pixel in the top left is all of the unselected faces for both models. Do not skip this step, and again make sure there is sufficient gutter at each corner of the UV layout.*</p>

<p>Once the UV layout is complete, collapse all the affected models.</p>

<p><img src="BuildingsProcess/media/image84.png" alt="Machine generated alternative text: w w w Reshape Elements Sttch Weld Thr eshold: 0.00 Detach Arr ange Elements V Rescale Rotate Elemen t Proper ties Rescale Priority: Gr oups: No groups selected " width="1286" height="610" /></p>
<p><em>Image showing the final UV3 unwrap for the Aqueduct District models. Note the open archways and window sections are split into trios, and the front entrance walls and ground are discreetly unwrapped with their lighting in mind. This image has the baked Basecolor reference visible in the Unwrap UVW dialog.</em></p>


<p><em><em>Bake the resulting UV3 channel's Basecolor to a reference image</em></em></p>

<p>With your UV3 layout complete, select all of the affected models and clone them, moving the resulting copies off to one side. Combine these copied meshes into one model. Rename the resulting model &quot;[Name of Asset]_Emissive.&quot; (e.g. DIS_AQD_Emissive). Add the new model to its own layer called &quot;Emissive.&quot;</p>

<p><img src="BuildingsProcess/media/image85.png" alt="Machine generated alternative text: Decal Classical Decal Industrial Decal Modern Emissive DIS AQD ENC Ha and PIL FINAL " width="556" height="145" /></p>

<p><em>Before doing anything else</em>, perform these two steps:</p>

<ol style="list-style-type: decimal">
<li>
<p>Unlink the geometry to prevent it from being associated with any export models</p>
</li>
</ol>




<ol style="list-style-type: decimal">
<li>
<p>Open the Civ6 Model Manager and remove the Emissive model from the Object to Export list.</p>
</li>
</ol>

<p>This backs up step 1 as well as making sure the entity isn't visible when bringing in new geometry in the Asset Editor</p>

<p><img src="BuildingsProcess/media/image86.png" alt="Machine generated alternative text: Firaxis Model Manager Objects In Scene Tower Tower Tower Tower Tower Decal Decal Mesh Mesh p IL PIL Objects To Export AQD wall 0B bathhfire aox002 aox003 aox004 aoxoos Patch Pat&amp;1001 Pat&amp;1002 Pat&amp;1003 Pat&amp;1004 Pat&amp;oos Pat&amp;1006 Patch007 Pat&amp;1008 Patch Sm Pat&amp;l smool Pat&amp;l sm002 Pat&amp;l sm003 Patch Sm004 Clear List Advanced Selected Object Emissiv e Export as Bone Use Granny Tangents o o o o o o o o o o o o o o o o o o o o o o o o o DIS DIS DIS DIS DIS DIS DIS DIS DIS DIS DIS DIS DIS DIS DIS DIS DIS DIS DIS DIS DIS DIS DIS DIS DIS DIS AQD_ AQD_ AQD_ AQD_ AQD_ AQD_ AQD_ AQD_ AQD_ AQD_ AQD_ AQD_ AQD_ AQD_ AQD_ AQD_ AQD_ AQD_ AQD_ AQD_ AQD_ AQD_ _AQD_ AQD_ AQD_ AQD_ Base Base Base Base Base Base Base Base Base Base Base Base Base Base Base Base Base Base Base Base Base Base Cir de Cirde Cirde Cirde Cirde Cirde Cirde Cirde Cirde Cirde Cirde Cirde Cirde Cirde wallool Wall Decal wall Decal PIL Wall Mesh Wall Mesh PIL Decal Decal Decal Decal Decal Decal Decal Decal Decal Decal Decal Decal Decal Decal ANC ANC ANC ANC ANC ANC ANC ANC ANC ANC ANC ANC ANC ANC wall PIL Waterwheel Waterwheel Waterwheel W a terwh eel Waterwheel Waterwheel Waterwheel Waterwheel Waterwheel Waterwheel Waterwheel Anim Anim Reversed FX001 Mesh Mesh Reversed p IL Rev ersed Rot Bone Rot Sone Reversed Decal 01 01 Decal Granny Models in Export List DIS DIS DIS DIS Num. AQD aase Tower PIL AQD_aase aath CON AQD_aase Gate PIL AQD_aase wall PIL Classical Base 01 of Granny Models: 126 Classical Base 01 Classical Base 01 Constructon Base Constructon Base Auto-sync Selecton " width="576" height="257" /></p>


<p>Once this complete, select the combined Emissive model and use Render to Texture to render the UV3's layout as a Basecolor reference texture.</p>

<p><img src="BuildingsProcess/media/image87.png" alt="Machine generated alternative text: Render To Texture Output Path: D: Skip Existing Files Render Settings Netnork Render File Name DIS AQD Emissi... Output Element Name DiffrseMap 512x512 Dele te General Se tnngs AL W -TBERGANTZ2 Civ6-main t V Rendered Fr ame Window Setup... Sub-Object Channel Edge Padding Selected Element Common Settings V Enable Name: DiffseMa File Name and Type: DIS A D EmissiveDiffuseMa 0000 Target Map Slot: Elemen t Type: diffuseMap Elemen t Backgr ound: Use Automabc Map Size Objects to Bake Object and Output Settngs Preset: Name Name DIS AQD Emissive Selected Object Se tings V Enabled Projection Mapping Object Channel Obje... Padding: sub-o. Pick... Width: 512 Height: 512 128K 128 256x256 512x512 768768 1024x1024 2048x2048 Selected Element Linique Settings Ligh ting Shado Baked Ma terial Baked Material Settings • Output Into Source Save Source (Create Shell) Projection Modifier Object L Options... @ Put to Baked Material Put to Baked Material Ful Size Pr opor tonal Mapping Coor dina tes Update Baked Materials Render to Files Only ObJect: Sub-objects: • Use Existing Channel Use Automabc Unwrap use Existing Channel use Automatic unwrap Clear Unwrappers • All Selected Clear Shell Materials Keep Source Ma terials Keep Baked Ma terials Au toma tic Mapping Views Render Unwrap Only Close Original: Baked: All Prepared Render " width="576" height="574" /></p>

<ol style="list-style-type: decimal">
<li>
<p>Choose the destination directory - this should always be the 03_Texture\PSDs folder relevant to the asset</p>
</li>
<li>
<p>Add a DiffuseMap to the Output</p>
</li>
<li>
<p>Choose the size of the rendered image. This is where you need to decide what size the Emissive needs to be. For Cities, large Wonders, and complex Districts, start at 1024. For everything else, use 512x512 or less, especially if you're only dealing with a handful windows. There are plenty of references available through the base game's artdev to use as a guide. Remember that you'll be authoring the texture one size up from the final output.</p>
</li>
<li>
<p>Select &quot;Output Into Source&quot; before rendering. This will prevent 3DS Max from creating a Shell material which will alter the material assignment on your target model. The Emissive model doesn't export out, but it's nonetheless easier to avoid the Shell material to begin with. Sadly, this button choice doesn't save with the .max file, so you'll need to set it each time open the file, even if you're repeating a render.</p>
</li>
</ol>

<p>When you're done, click &quot;Render&quot; at the bottom right, which will save a file to the PSDs folder like this:</p>

<p><img src="BuildingsProcess/media/image88.png" alt="Machine generated alternative text: IC11211nII@ &#39;EDIÉII@I " width="333" height="333" /></p>
<p><em>DIS_AQD_EmissiveDiffuseMap.tga</em></p>

<p><em><em>Pick the appropriate size Emissive template file and add the reference image</em></em></p>

<p>A set of template for Emissive texture work are stored in Perforce at this location:</p>

<p><strong>//civ6/main/ArtDev/Buildings/Shared/EmissiveTemplates/</strong></p>

<p>Pick the size that matches the UV3 Diffuse render, and save that file in the relevant PSDs folder with the name of the original model's material and &quot;_E&quot; as the suffix. For example, the PSD for Aqueduct District's standard textures is named &quot;DIS_AQU_Base.psd,&quot; so your Emissive file would be named &quot;DIS_AQU_Base_E.psd&quot;</p>

<p><img src="BuildingsProcess/media/image89.png" alt="Machine generated alternative text: Kind PattE v Opzity: EMISSIVE M u ltipty IDY,&#39;. IDY,&#39;. Red cwe... Blyck DIS AQD ErrissiveDiffuÆ... E.zkg,w-€ " width="240" height="529" /></p>
<p><em>The starting layer stack with the DIS_AQD_Emissive render added above the Background layer</em></p>

<p>Each template has preset layers with layer masks used to create the Emissive mask. The masks for each layer are currently occupied, so you can toggle the layers to get the general idea of how they work. Before commencing work, you'll need to black out all of the layer masks - select each one and fill with 0,0,0.</p>

<p>Paste a copy of your rendered UV3 Diffuse just above the Background layer, outside of the Emissive layer group.</p>


<p><em><em>Use the layer masks in the template file to define and detail the Emissive image</em></em></p>

<p>Once your UV3 Render is installed, turn off the Emissive Base Black layer and work your way up the layer stack from the bottom using the mask:</p>

<ol style="list-style-type: decimal">
<li>
<p>Base Orange - this is the most important layer, as the mask from this layer is copied up the stack for most of the other effects. This mask defines all of the window and door openings as well as gradients for faux light within archways or across surfaces.</p>
</li>
</ol>



<ol style="list-style-type: decimal">
<li>
<p>Color - the name of this layer is misleading, as the layer mode is actually an Overlay. It is called color, though, because it where you can push the emissive color towards yellow or red, depending on your needs. This layer is where your implied lighting within the opening of your building is defined. Use a copy of the Base Orange layer mask for this layer</p>
</li>
</ol>



<ol style="list-style-type: decimal">
<li>
<p>ANC Red Overlay - The purpose of this layer is to push all of the emissive color towards red, for models that are introduced in the Ancient or Classical (Classical, Renaissance, Medieval) eras. The intensity of this layer should be 30% or less - just enough to nudge it in game towards &quot;fire&quot; instead of &quot;light bulbs.&quot; Use a copy of the Base Orange layer mask as a starting point, but remove any features on the texture that apply to parts introduced later in the game. This will come up most often on Districts or Improvement textures where there is a mix of buildings per era. This layer can be changed to the MOD Color layer (see below) for Modern buildings.</p>
</li>
</ol>



<ol style="list-style-type: decimal">
<li>
<p>Multiply - aka &quot;cats in windows&quot; - This layer is where the larger variety in detail in openings is applied. Start by copying the Base Orange layer mask to this layer, then select the mask by holding Ctrl and left clicking the layer mask icon. With 255, 255, 255 as your color, foreground fill this mask twice to add padding to the mask. Deselect, and paint the RGB on this layer using predominantly darker colors, though spots of color (greens, blues, etc.) don't hurt. The goal is to give the impression of shadow within a room, items silhouetted against the frame, and depth.</p>
</li>
</ol>
<table>
<tbody>
<tr class="odd">
<td><p><img src="BuildingsProcess/media/image90.png" alt="Machine generated alternative text: " width="763" height="87" /></p>
</td>
<td><p><img src="BuildingsProcess/media/image91.png" alt="Machine generated alternative text: .21 " width="339" height="142" /></p>
<p>=</p></td>
</tr>
</tbody>
</table>

<p><em>Examples of using the Multiply layer to vary intensity and color in a set of windows.</em></p>


<ol style="list-style-type: decimal">
<li>
<p>Blackout - this layer is available to adjust the value of individual window/door openings in order to adjust the intensity of the Emissive in game. It's not necessary, but can be an easy way to make gross adjustments or correct an errant glow on one edge of an opening. This layer doesn’t use a copy of the Base Orange layer mask. Instead, the layer mask is solely to apply black to the image as needed.</p>
</li>
</ol>

<p>When working on Emissive for Modern buildings, it's desirable to push the window color towards a light blue, to emulate fluorescent or LED lighting. For this, you'll need to change the color of the <em>ANC Red Overlay</em> layer (if there is no need for it) or create a new layer. The standard color for MODern Blue is 217, 226, 224, and the blending mode should be set to Color. The opacity for the layer is usually around 40%, varying by subject.</p>

<p>Once the Emissive PSD is ready for implementation, save a TGA copy of it in the 03_Texture folder. With the exception of complicated cities and a handful of Wonders, reduce the size of this TGA to 50% of your master PSD (e.g. if the PSD is 1024x1024, the TGA should be 512x512). It's important that you always reduced the TGA and not the PSD, as reducing the PSD and then saving out produces pixel color shifting around the texture, which has the side effect of adding color to the areas that should be black. As the unlit parts of your model reside in the top left corner, this will cause them to take on a partial glow if you reduce the texture side in the wrong order.</p>

<p><em><em>Displaying the Emissive texture in 3DS Max</em></em></p>

<p>To see the Emissive texture on the affected models in your .max file, you'll need to set up a Composite map. You can make a copy of the original material or add the Composite to the existing material.</p>
<p>If you copy the material, add &quot;_COMP&quot; to the name of the material, so it's clear that it's for special use, and don't forget to re-apply the original material before you export.</p>
<p>If you use the existing material, don't forget to turn off the Composite layer (see below) before saving the file for future users.</p>

<table>
<tbody>
<tr class="odd">
<td><img src="BuildingsProcess/media/image92.png" alt="Machine generated alternative text: Material Editor -DIS CTY AB Modes Material Navigation Options Utilities ÜQQQQ DIS CTY AB Base Shader Basic Parameters Wir e Face Map alinn Basic Parameters Sel f-lllumina bon Color Opacity: 100 Standard 2-sided Face ted Ambient: Specular Highlights Specular Level: GIO ssiness: Soften: 0.1 Extended Paramete ; Super Sampling Amount Ambient Color . . 100 V Diffise Color . . 75 (DIS CTY AE aase_a.tga) . 100 Specular Color . 100 Specular Level . 100 Glossiness Self-Illumina bon . 100 " width="207" height="460" /></td>
<td><p><img src="BuildingsProcess/media/image93.png" alt="Machine generated alternative text: Material Editor -DIS CTY AB Modes Material Navigation Options Utilities ÜQQQQ Diffise Color: Map #1075 Coordina tes Bitmap icit Map Channel Texture Environ Mapping: Show Map on Back Llse Real-World Scale Offset -riling U: 0.0 v: 0.0 • vw Map Channel : Mirror Vile w: Angle 0.0 0.0 Rotate Blur: 1.0 Bitmap: Blur offset: 0.0 Bitmap Parameters AncientErickIP3 TextureVIS CTY AE aase_a.tga Cropping Placemen t Apply View Image • Crop v: 0.0 Jitter Placement: I O Alpha Source RGB Intensity None (Opaque) Fil tering • pyramidal Summed Area Mono Channel Output: • RGB Intensity RGE Channel Output: • RGE " width="207" height="460" /></p>
</td>
<td><img src="BuildingsProcess/media/image94.png" alt="Machine generated alternative text: Material/Map Browser Search by Name - 16Grids.mat Diffuse Color: Map #1078 (16grid 1024x512.tga) Diffuse Color: Map #1077 (16grid 512x2 Topaottom.tga) Diffuse Color: Map #1077 (16grid 1024x2.tga) - Maps - Standard Camera Map Per Pixel Cellular Checker IorCorrection mbustion mposite Dent Falloff Flat Mirror Gradient G radient Ramp Map Output Selector Marble . Mask Noise . N ormal Bump . O utput article Age article MBIur Perlin Marble Refl ect/Refract . RG3MuItipIy . RGa Tint Smoke . Speckle . Splat " width="258" height="441" /></td>
<td><img src="BuildingsProcess/media/image95.png" alt="Machine generated alternative text: Replace Map Discard old map? Keep old map as sub -map? " width="147" height="93" /></td>
<td><p><img src="BuildingsProcess/media/image96.png" alt="Machine generated alternative text: Material Editor -DIS CTY AB Modes Material Navigation Options Utilities ÜQQQQ Diffise Color: Map #1075 Composite Layers Composite Total Layers: Layer 2 opacity: 73.0 None None Addition Layer I Opacity: 100 0 aarmel " width="207" height="460" /></p>
</td>
<td><img src="BuildingsProcess/media/image97.png" alt="Machine generated alternative text: Material Editor -DIS CTY AB Modes Material Navigation Options Utilities Diffise Color: Map #1075 Composite Layers Composite Total Layers: Layer 2 opacity: 73.0 None Addition Layer I Opacity: 100 0 None rac.rmel " width="207" height="460" /></td>
</tr>
</tbody>
</table>

<p>To set up a Composite map:</p>
<ol style="list-style-type: decimal">
<li>
<p>Click the existing Diffuse (Basecolor) Map slot in the Max material</p>
</li>
<li>
<p>Select the Map type for that entry</p>
</li>
<li>
<p>Choose Standard&gt;Composite Map from the Material/Map Browser</p>
</li>
<li>
<p>When the Replace Map dialog comes up, choose &quot;Keep old map as sub-map?&quot; and hit OK. This will make the original texture the first layer in the new Composite setup</p>
</li>
<li>
<p>5a: Click the &quot;Add a New Layer&quot; button to…well, you get it. Then click the <em>left</em> &quot;None&quot; box in the new layer and add your Emissive texture as a Bitmap</p>
</li>
<li>
<p>Adjust the blending mode to Addition and set the Opacity to 80, then click the button to <em>Show Standard Map in Viewport</em> to do just that. The small &quot;eyes&quot; next to the texture image will let you toggle this Composite layer on and off.</p>
</li>
</ol>

<p>Depending on the .max file and the complexity of the scene, you may find the display of the Emissive is sometimes wrong. Usually this is resolved by toggling <em>Show Standard Map in Viewport</em> off and then on again.</p>

<p>You may also find that the Emissive texture doesn't automatically update in 3DS Max after you've saved the file in Photoshop. Save your file and reload the scene, and that should resolve. This happens on complex scenes in particular, where a lot of geometry is displaying the Composite.</p>


<p><em><em>Adding the Emissive texture and viewing the models in the Asset Editor</em></em></p>

<p>Once your Emissive texture is ready for implementation, you'll need to add it to the corresponding MTL in the Asset Editor.</p>

<p>Open the models you'll be updating with Emissive in the Asset Editor. For this example, we'll use the Aqueduct District Bath. Using the Open function on the model's Material entry, open the corresponding MTL for each affected piece.</p>

<p><img src="BuildingsProcess/media/image98.png" alt="Machine generated alternative text: DIS AQD Base Bath.ast Basic Name Class Name Landmark Base 8 Base Base N (I items) Landmark DIS AQU DIS_AQU Desc ri pticn C ategorization Tags Cook Parameters Value 3aseCcI or Emissive Text Emissive Minimum Weight Gloss LightMap LightMap Minimum Weim Metal ness Normal Opac ity DIS AQU DIS AQU " width="472" height="613" /></p>
<p><em>The Aqueduct Bath model's MTL setup, with Emissive noted</em></p>

<p>In the Cook Parameters for each MTL is an Emissive slot. Use &quot;Add New&quot; or &quot;Add Existing,&quot; as applicable to add your Emissive texture from artdev to the MTL file, creating the new .tex and .dds files as needed.</p>

<p>Below the Emissive slot is an Emissive_Minimum_Weight value, which defaults to 0. Unless your name is Arthur, leave it at 0. Seriously, don't touch it.</p>

<p>You'll then need to adjust the Asset Previewer to display texture lighting. There are three parameters in the Global Previewer Info panel which allow this to happen: Sun Scale, Sky Scale, and Light Map Weight.</p>

<table>
<thead>
<tr class="header">
<th><img src="BuildingsProcess/media/image99.png" alt="Machine generated alternative text: Global Previewer Info Module Landmark Base Camera Hex Knobs Bounce Color Sun Scale Sky Scale Shadow Bias Spec Enable Diffuse Enable Show Base Color Show Metalness Show AO Scene Exposure Light Map Weight Day Threshold Night Threshold Time Of Day Culling H LID Lighting .46, 65, 6 Add Asset " width="321" height="421" /></th>
<th><img src="BuildingsProcess/media/image100.png" alt="Machine generated alternative text: Global Previewer Info Module Landmark Base Camera Hex Knobs Bounce Color Sun Scale Sky Scale Shadow Bias Spec Enable Diffuse Enable Show Base Color Show Metalness Show AO Scene Exposure Light Map Weight Day Threshold Night Threshold Time Of Day Culling H LID Lighting .46, 65, 6 Add Asset " width="321" height="421" /></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><em>Global Previewer Info - Default &quot;Day&quot; Settings</em></td>
<td><em>Global Previewer Info - &quot;Night&quot; Settings</em></td>
</tr>
</tbody>
</table>

<p>Sun Scale and Sky Scale are used to control the Asset Previewer environment. Both default to 1. To change the scene from &quot;Day&quot; to &quot;Night,&quot; reduce the Sun Scale to 0 and the Sky Scale to 0.15.</p>

<p>The Light Map Weight is a global value to that controls the overall day/night cycle in the game. The Light Map Weight defaults to 0. To see the Emissive map at full value in the Asset Previewer, set the Light Map Weight to 4.</p>

<table>
<tbody>
<tr class="odd">
<td><img src="BuildingsProcess/media/image101.png" alt="Machine generated alternative text: Global Previewer Info Module Landmark Base Camera Hex HUD Lighting Knobs Bounce Color Sun Scale Sky Scale Shadow Bias Spec Enable Diffuse Enable Show Base Color Show Metalness Show AO Scene Exposure .46, 65, 6 Add Asset DefaultGameEn.. I Reset To Default Attached Assets Light Map Weight Day Threshold Night Threshold Time Of Day Culling DIS Base Bath Attachment Point DLBONE BathPool DIS AQD_Base Bath DIS AQD_Base Bath O Base Motion Display Transform Animation Knobs Show Model Center Show Obstructions Asset State Worked " width="576" height="472" /></td>
<td><img src="BuildingsProcess/media/image102.png" alt="Machine generated alternative text: Asset Previewer Global Previewer Info FPS: 58.8 Draws: 14 Module Landmark Last Refreshed At: pm Time Of Day: Night Base Camera Hex Knobs Bounce Color Sun Scale Sky Scale Shadow Bias Spec Enable Diffuse Enable Show Base Color Show Metalness Show AO Scene Exposure Light Map Weight Day Threshold Night Threshold Time Of Day Culling H LID Lighting .46, 65, 6 Add Asset DefaultGameEn.. I Reset To Default Attached Assets DIS Base Bath Attachment Point DLBONE BathPool DIS AQD_Base Bath DIS AQD_Base Bath O Base Motion Display Transform Animation Knobs Show Model Center Show Obstructions Asset State Worked " width="576" height="472" /></td>
</tr>
</tbody>
</table>
<p><em>Asset Previewer comparison of Aqueduct District Bath model at &quot;Day&quot; (Left) and &quot;Night&quot; (Right), showing an enabled Emissive map. Note that the blue lighting inside the bath is from an analytic lighting point (see section below).</em></p>

<p>The Asset Previewer is a critical tool for evaluating the color, intensity and placement of the Emissive texture on a given model. It should be noted, though, that the display in this isolated environment is not 100% accurate with the game itself, and the settings provided do not allow you to evaluate the Emissive at anything other than late night. No asset should be considered final without review directly in the game.</p>

<p>If you're working on a Wonder asset, this is where you stop. Wonder_EM models need to be added to the corresponding Wonder movie file before they can display correctly in game. Talk to you Wonder specialist (Rambo) for further information.</p>

<p><em><em>Reviewing Emissive models in game</em></em></p>

<p>After your model and materials are updated in the Asset Editor and you've cooked latest, you'll be able to see the effects in game. Once you've loaded up a map and placed your buildings, use the tilde (~) key to toggle the debug menu. Click the left (downward) arrow to open the Debug View panel, tick the <em>Show Time of Day</em> option, and click and drag the slider to change the time of day. 0.00 is midnight, where evaluation of Emissive is most useful. You can alter and hotload your Emissive textures.</p>

<table>
<thead>
<tr class="header">
<th><img src="BuildingsProcess/media/image103.png" alt="Machine generated alternative text: oo WORLD TRACKER CHOOSE RESEARCH CODE OF LAWS T urns: " width="430" height="290" /></th>
<th><img src="BuildingsProcess/media/image104.png" alt="Machine generated alternative text: Debug View nshow Frame Statistics Oshow VFX Statistics @show Time Of Day nshow Camera Oshow Lua Statistics Oshow Memory Time O f Day — Time: 0:00 am Rendered TOD 0.00 " width="430" height="290" /></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="BuildingsProcess/media/image105.png" alt="Machine generated alternative text: 16 CLEVELAND T urns: oo WORLD TRACKER CHOOSE RESEARCH CODE OF LAWS €0, " width="576" height="499" /></td>
<td><img src="BuildingsProcess/media/image106.png" alt="Machine generated alternative text: Debug View nshow Frame Statistics Oshow VFX Statistics @show Time Of Day nshow Camera Oshow Lua Statistics Oshow Memory Time O f Day — Time: 0:00 am Rendered TOD 0.00 16 CLEVELAND " width="576" height="499" /></td>
</tr>
</tbody>
</table>


<p><img src="BuildingsProcess/media/image107.png" alt="C:\74741245\F0A4F1AD-AE5D-4B3D-84B4-FD2A3508EFC1_files\image113.png" width="40" height="37" /></p>

<p><em>Lightmap</em></p>
<table>
<tbody>
<tr class="odd">
<td><img src="BuildingsProcess/media/image108.png" alt="Machine generated alternative text: " width="420" height="333" /></td>
<td><img src="BuildingsProcess/media/image109.png" alt="Machine generated alternative text: " width="380" height="332" /></td>
<td><img src="BuildingsProcess/media/image110.png" alt="Machine generated alternative text: " width="360" height="332" /></td>
<td> </td>
</tr>
</tbody>
</table>
<p><em>Examples of assets with only a Lightmap (Oracle) or combinations of Emissive and Lightmap (Sydney Opera House, Broadway)</em></p>

<p>A Lightmap is similar to an Emissive map in that it adds lighting information to a model, but the process and the application of a Lightmap is different. A Lightmap produces a visual of broad area lighting, but does not override the base color information of a model's textures like an Emissive map. Lightmaps have more of an additive function in game, and tend to result in more subtle color. Lightmaps can be used alone or in conjunction with an Emissive setup.</p>

<p>Unlike Emissive maps, Lightmaps do not use a unique UV channel. They use the UV2 layout of a model or model set which has been previously set up for Ambient Occlusion (AO). This recycled UV2 usage keeps the model itself from becoming more expensive, but there are negatives to consider with Lightmapping:</p>

<ol style="list-style-type: decimal">
<li>
<p>The shared usage of the UV2 channel means that the UV layout is prone to changing if the asset isn't 100% through its pipeline. Any change to the AO needs of the model will result in the Lightmap having to be rebaked.</p>
</li>
<li>
<p>Lightmaps are expensive in terms of texture memory. The UV2 layout has every face of a model discreetly unwrapped, often including geometry of parts that won't receive lighting like Under Construction or Pillage states or simple sections of the building(s) that are unaffected. As a result, Lightmaps usually need to be 1024x1024, even though only some of the geometry is lit.</p>
</li>
<li>
<p>Lightmaps cannot affect decals or the terrain in game.</p>
</li>
<li>
<p>In the case of Districts, the shifting nature of attachments means that a single Lightmap can't properly affect all of the different tilebase layouts. Lighting in this case needs to be restricted to only affecting an individual structure.</p>
</li>
<li>
<p>In the case of Cities, the random placement and rotation of Blocks and Buildings means the source of light is never set. Thus, Lightmapping will likely produce visual errors instead of enhancing the set.</p>
</li>
</ol>

<p>In the three screens provided at the top of this section, you can see that two of the three have specific foundations on which the Wonders sit. This is the best case scenario for Lightmapping, as the asset is self-contained and lighting is isolated from the terrain. Broadway, by contrast, is a city -like asset that does not have randomly rotating parts, so subtle lighting between buildings as well as lighting to and from billboards is possible.</p>



<p><em><em>Setting up a model for Lightmapping</em></em></p>

<p>There are two primary methods for generating a Lightmap in 3DS Max: standard Max lighting and the Architectural material</p>

<p><strong>Max lighting</strong></p>

<p>This section assumes you are familiar with the basics of lighting objects in 3DS Max, and will only cover a few particulars.</p>
<p>Mental Ray is produces a good render for Lightmaps, and render time is not long provided you stick with a few specific parameters.</p>
<p>Before moving on, change the Render Preset in the Render Setup menu to <em>mental.ray.no.gi.</em></p>

<p><img src="BuildingsProcess/media/image111.png" alt="Machine generated alternative text: Render Setup: NVIDIA mental ray Render Elements Renderer Global Illumina bon Time Output • Single Processing Common Par ame ters Every Nth Frame: Active Time Segment: O To 100 Range: O File Number Base: Frames Area to Render Outp_lt Size Custom Width: Height: Image Aspect: 1.333 V Atmospherics Effects V Displacement Video Color Check Render to Fields Advanced Ligh ting Auto Region Selected Aperture Width(mm): 36.0 320x240 640x480 720x486 800x600 Pixel Aspect: 1.0 Render Hidden Geometry Area Lights/Shadows as Points For ce 2-Sided Super alack V Use Advanced Lighting Compute Advanced Lighting when Required Bitmap Performance and Memory Options Bitmap Proxies / Paging Disabled Render Ou tput Put Image File List(s) in Output Path(s) Setup... Create Now Autodesk ME Image Sequence File Imsq) Legacy 3ds max Image File List ifl) V Rendered Frame Window Skip Existing Images EmF&#39;l , tficabons Kripts Preset: View : 3dsmax scanline no advanced lighting draft 3dsmax scanline no advanced lighting high 3dsmax. scanline radiosity. draft 3dsmax. scanline radiosity high lighting analysis assistant. preset mental. ray. daylightng.high mental. ray daylightng mental. ray. hidden line. contours mental. ray. photometric. lightng. with .gi Load Preset Save Preset " width="207" height="648" /></p>

<p>Use Mental Ray Standard lights in your scene, with the shadow casting of your choice. Consistent use of the Far Attenuation parameters will help reduce render time.</p>
<table>
<tbody>
<tr class="odd">
<td><img src="BuildingsProcess/media/image112.png" alt="Machine generated alternative text: Stenderd Object Type AutoGrid Target Spot Free Spot Targe t Direct Free Direct Skylight mr Area Omni mr Area Spo t Name and Color " width="186" height="281" /></td>
<td><p><img src="BuildingsProcess/media/image113.png" alt="Machine generated alternative text: FM Use Start: I&quot;. 024 V Show B-,d: : " width="175" height="60" /></p>
</td>
</tr>
</tbody>
</table>

<p>Using the final asset model(s), set up a lighting rig that fits the desired look. As the lighting is pre-rendered, you can use as few or as many lights as your prefer, though fewer lights are easier to modify and reduce render time as usual.</p>

<table>
<thead>
<tr class="header">
<th><img src="BuildingsProcess/media/image114.png" alt="Machine generated alternative text: non_syan o ra House " width="495" height="415" /></th>
<th><img src="BuildingsProcess/media/image115.png" alt="Machine generated alternative text: " width="496" height="417" /></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="BuildingsProcess/media/image116.png" alt="Machine generated alternative text: " width="496" height="417" /></td>
<td><img src="BuildingsProcess/media/image117.png" alt="Machine generated alternative text: " width="495" height="415" /></td>
</tr>
</tbody>
</table>
<p><em>Top Left: Sydney Opera House Basecolor; Top Right: the model's Max lighting result; Bottom Left: Wireframe showing the many lights in use; Bottom Right: Max lighting plus a Light Emitting Object setup (next section)</em></p>



<p><strong>Architectural Material</strong></p>

<p><img src="BuildingsProcess/media/image118.png" alt="Machine generated alternative text: " width="972" height="433" /></p>
<p><em>Left to right: The Sydney Opera House model, the model's light rig, and the Light Emitting Object model with an applied Architectural Material.</em></p>

<p>In addition to using Max lighting, some models can benefit from the use of Light Emitting Object. Usually this Object is a copy of the Emissive parts of a model, which is then set up with an <em>Architectural</em> material in the Material Editor. An Architectural material is a Standard material that can be obtained from the Material/Map Browser.</p>
<p>Using the screens above and below as a reference, you can see the parts of the Sydney Opera House that were detached as a Clone and set up with the Architectural material. While standard lighting could be used to give the same impression of lighting onto the base model, this alternate approach can be faster and more accurate for unusual and oblong shapes (of which there are many on the depicted model).</p>

<p>Once you've changed the Material type to Architectural, you are concerned with two settings in the Physical Qualities section:</p>

<p>Diffuse Map: For this map slot, you'll use the Emissive texture you created for the model. The Emissive texture will provide the color and the beginning intensity for the projected lighting</p>

<p>Luminance cd/m²: This value controls how bright the Light Emitting Object is in the scene. It's not uncommon for values to range from 3000-6000 for a typical Wonder model.</p>

<p>One important note when using this approach: in order to get the Light Emitting Object to render out correctly, you need at least one light in the scene. This light doesn't need to be used for anything; in fact, it can be turned off and the LEO will still render correctly. A light just has to exist for the render to properly acknowledge the LEO contribution.</p>

<p><img src="BuildingsProcess/media/image119.png" alt="Machine generated alternative text: ial Ed&#39; rvlcclä Meteriel Ny.:igeticn Opticn: OOOQQ &#39;i oooce 24 - Default Architectural Templa tes user Defined Ph ysical Qualities Diffise Color: V iney Opera House E.jpg) Diffise Map: 100.0 Transpar ency: Index of Refraction: 1.5 Luminance cd 1m 2: 4000.0 Raw Diffise Texture 2-Sided Special Effects Advanced Lighting Override Super Sampling Dir ecü Manager Save as .FX File Enable Plugin mental ray Connection " width="969" height="815" /></p>

<table>
<tbody>
<tr class="odd">
<td><img src="BuildingsProcess/media/image120.png" alt="Machine generated alternative text: " width="426" height="318" /></td>
<td><img src="BuildingsProcess/media/image121.png" alt="Machine generated alternative text: " width="426" height="318" /></td>
<td><img src="BuildingsProcess/media/image122.png" alt="Machine generated alternative text: " width="426" height="318" /></td>
</tr>
</tbody>
</table>
<p><em>Left to right: The Sydney Opera House model lit with standard Max lighting; the same model lit only with the Light Emitting Object geometry; the rendered result of both standard and LEO lighting</em></p>

<p>Further information can be found online for this approach. A quick and easy tutorial can be found here: <a href="http://www.cgarena.com/freestuff/tutorials/max/glowingmaterial/" class="uri">http://www.cgarena.com/freestuff/tutorials/max/glowingmaterial/</a></p>

<p><em><em>Rendering the Lightmap in 3DS Max</em></em></p>

<p>Once your lighting is set up, you're ready to render the Lightmap. Refer to the Render to Texture information in the Emissive section for basic setup. Here we'll focus on Lightmap specific parameters.</p>

<p>In the Render Setup panel, go to the <em>Global Illumination</em> tab. This tab only shows up if your preset is set to use Mental Ray.</p>
<table>
<tbody>
<tr class="odd">
<td><img src="BuildingsProcess/media/image123.png" alt="Machine generated alternative text: Render Setup: NVIDIA mental ray Renderer Render Elements Common Global Illumina bon Processing Skylights &amp; Environment Lighting (EL) Skyligh t Mode Skylight Illumination from Final Gather (FG) Skylight Illumination from IBI_ Shadow Quaitv Shadow Mode anal Gathering (FG) V Enable anal Ga ther FG Precision Presets: Mulbplier: 1.0 Project FG Points From Camera Position (aest for Stills&quot; Divide Camera Path by Num. Segments: Inital FG Point Density: Rays per FG Point: Interpolate Over Num. FG Points: Diffise Bounces Adv anced Noise Fil tering (Specke Reducto . Draft Mode Co Precalculabons) Final Gathering Trace Depth Stenderd Max. Depth: Max. Refections: Max. Refractions: 5 Llse Falloff (Limits Ray Distance) FG Point Interpolation Llse Radius Interpolaton Method (Instead of Num. FG Points) Racii in Pixels Min. Radius: 0.5 " width="291" height="610" /></td>
<td>
<ol style="list-style-type: decimal">
<li>
<p>Change the Skylight Mode to Skylight Illumination from Final Gather (FG). If the Enable Final Gather button in the next section of the panel is not enabled, check it on.</p>
</li>
</ol>



<ol style="list-style-type: decimal">
<li>
<p>The Rays per FG Point can be considered a general quality setting - more rays means better quality. Set it to 600 to begin with. At the scale the Lightmaps are rendered to, you may not see much difference even if you vary this value in increments of 100, but as long as you don't go into the thousands, you shouldn't see a significant impact on render time.</p>
</li>
</ol>



<ol style="list-style-type: decimal">
<li>
<p>The Diffuse Bounces is the other quality settings to look at. Set it to 1 or 2. More bounces will produce more subtle color and light interaction between sections of the model, but will also increase render time. Higher values also tend to make the final render a bit brighter, but again our rendered image size is small enough that the difference may be negligible.</p>
</li>
</ol></td>
</tr>
</tbody>
</table>
<table>
<tbody>
<tr class="odd">
<td><img src="BuildingsProcess/media/image124.png" alt="Machine generated alternative text: Render To Texture Objects to Bake Object and Output Settings Preset: Name Name WON Sydney Opera_House... Selected Object Se tings V Enabled Projection Mapping Object Sub-Object Edge Channel Channel Padding Obje... sub-o. Padding: Pick... Options... Projection Modifier Put to Baked Material Put to Baked Ma terial Mapping Coor dina tes ObJect: Sub-objects: File Name WON Sydney WON_Sydney • Use Existing Channel Llse Automatc Unwrap @ Use Existing Channel use Automabc Unwrap Clear Unwrappers • All Selected Output Element Name LightingMap CompleteMap All Pr epared 1024x1024 1024x1024 Dele te a House EMLi( Selected Element Common Settings V Enable Name: ht Ma File Name and Type: WON S dne Target Map Slot: Elemen t Type: Elemen t Backgr ound: bngMap 512x512 768768 1024x1024 2048x2048 Views Render Use Automabc Map Size W&#39;dth: 1024 Height: 1024 128K 128 256x256 Selected Element Linique Settings V Shadows V Direct Light On V Indirect Light On Baked Ma terial Baked Material Settings Output Into Source Save Source (Create Shell) @ D*ate Close Render Unwrap Only Original : Baked: " width="294" height="963" /></td>
<td><ol style="list-style-type: decimal">
<li>
<p>When you work with the Render To Texture dialog on an asset that hasn't already been set up to use it, the Channel setting will default to the highest UV channel present on the model. If you are working with a model that has already been through the Emissive pipeline, make sure you change this value to 2 prior to rendering.</p>
</li>
</ol>



<ol style="list-style-type: decimal">
<li>
<p>Add a LightingMap to the Output list. A CompleteMap can also be rendered at the same time, and that type of map can sometimes be used as an overlay to the LightingMap to restore detail or adjust colors.</p>
</li>
</ol>



<ol style="list-style-type: decimal">
<li>
<p>Set the texture size for each map in the Output list to 1024x1024</p>
</li>
</ol>



<ol style="list-style-type: decimal">
<li>
<p>Make sure Output Into Source is checked to avoid having a Shell material created and applied to your target model. Remember, this setting does not save with the file in Max 2015.</p>
</li>
</ol></td>
</tr>
</tbody>
</table>

<p>In most cases, the rendered output can simply be saved as a TGA in the corresponding 03_Texture folder, with a &quot;_L&quot; suffix (e.g. WON_Sydney_Opera_House_L.tga). With Wonders in particular, though, you're often working blind, so Photoshop alterations are always an option. You will notice that the Lightmap tends to have lower values than you might expect - keep in mind that this is strictly light value and color, with no information of the model underneath.</p>

<p><img src="BuildingsProcess/media/image125.png" alt="Machine generated alternative text: " width="511" height="511" /></p>
<p><em>Example: The final Lightmap for Sydney Opera House</em></p>

<p><em><em>Lightmap setup in Asset Editor</em></em></p>

<p>The process for adding a Lightmap to an Asset Editor Material is the same as for all texture maps, except that it goes in the Lightmap slot. As with the Emissive map paramaters, do not change the <em>LightMap_Minimum_Weight</em> value from the default of 0.</p>

<p>Refer to the Emissive section above for information on viewing models in Night mode to evaluate the asset's Lightmap.</p>

<table>
<tbody>
<tr class="odd">
<td><img src="BuildingsProcess/media/image126.png" alt="Machine generated alternative text: WON Sydney_Opera House EM.ast WON Sydney Opera_House Emissive.mtl Basic Name WON Sydney_Opera_House Emissive (I items) Landmark WON Sydney_Opera House AO WON Class Name Landmark Desc ri pticn C ategorization Tags Cook Parameters Value 3aseCcI or Emissive Emissive Minimu Gloss LightMap Text eight Remove WON Sydney Opera House WON Sydney_Opera WON Sydney_Opera WON Sydney_Opera House L House M House N LightMap Minimum Weim Metal ness Normal Opac ity " width="402" height="439" /></td>
<td><img src="BuildingsProcess/media/image127.png" alt="Machine generated alternative text: " width="576" height="439" /></td>
</tr>
</tbody>
</table>

<p><em>&quot;Remove Emissive&quot; Script</em></p>

<p>After a District, Improvement, or (sometimes) Wonder asset has received its emissive and/or lightmap setup and the asset is working in game, it is necessary to disable the display of lighting for the (Under) Construction and Unworked states. To do this, the Remove_Emissive.py script is run.</p>

<p><em><strong>*Close the Asset Previewer BEFORE you run the script*</strong></em></p>

<p>From within the AssetEditor, go to File&gt;Run Script:</p>
<p><img src="BuildingsProcess/media/image128.png" alt="Machine generated alternative text: H New Open Entity open XLP Open Aft Def Open Game Aft Specification Import Open Source file Sav e Save As Save All Cook Close Enable tuner connection Hot Load Run Script Window Help Alt* Ctrl+N Ctrl+O Ctrl+Shift+O Ctrl+Shift+O Ctrl+Shift+I Ctrl+S Ctrl+Shift+S Ctrl*Shlft+C Ctrl* ; Ctrl*F4 Ctrl* Shift* H Ctrl*Shift+R DIS DIS DIS Pin SPACE Bid Recent Files Bid Bid Bid A A A SPACE SPACE SPACE DIS DIS DIS SPACE SPACE SPACE U nwor ked Corwtruction " width="368" height="397" /></p>

<p>From the dialog, choose Remove_Emissive.py:</p>
<p><img src="BuildingsProcess/media/image129.png" alt="Machine generated alternative text: Open 000 Organize Desktop Computer OSDi5k (C:) New folder Program Files Name cp.6 Asset Cloud AssetEditor Scripts Scrip ts Type py Fi py Fi py Fi py Fi py Fi py Fi py Fi py Fi py Fi py Fi py Fi py Fi py Fi Size 20 KB 27 KB 34 KB 25 KB 10 KB 17 KB Date modified 7/20/20161:11 PM 5/24/2016 6:59 PM 5/27/2016 4:25 AM 7/20/2016 3:42 PM 5/27/2016 4:25 AM 2/23/2016 5:59 PM 5/27/2016 4:25 AM 7/20/20161:11 PM 6/9/2016 3:08 PM 7/20/20161:11 PM 7/28/2016 5:27 PM 2/9/201612:56 PM 5/27/2016 4:25 AM 7/5/2016 3:27 PM Todd Bergantz (Firaxis) Computer OSDisk AMD Autodesk MSOCache PerfLogs Program Files Adobe Autodesk CCIeaner Ci,.6 Asset Cloud - Civ6 AssetCIoudServer AssetEditor Scripts ImportTooI Project8uiIder File name: Add FX To Tilebases.py Assign Geo To MultipleAssets.py Create Assets.py Create Assets From Source File.py CreateCity810cks.py GlobalScriptingVariabIes.py MenuSetupWizardCommand.py MultiAssign Landmark AO.py Nudge_Triggers.py Preview Unit.py Remove Emissive.py ResaveAssets.py UnitMember from Asset.py Update Asset Attachments.py Remove Emissive.py Python Script C.py) Open Cancel " width="576" height="360" /></p>
<p>The script will display a dialog of all assets in the Tilebases.xlp:</p>
<p><img src="BuildingsProcess/media/image130.png" alt="Machine generated alternative text: aa Please Pick the Assets to have the emmissive remov... Replace any emissive materials in the given assets wth non-emissive copies Assets AW Monument Ancient AW Monument Classical AW Monument Industhal AW Monument Modem AnimatedWater EM Right Right_EM Right Right_EM Right Right EM Attach Attach Attach Attach Attach Attach Attach Attach Attach Attach Build Build Build Build Build Build Build Build Build Build Left Left Low Low Mid Mid _ Top _ Top _ Top _ Top ktachment Collumn Build Paik Left Mid Build Paik Right Build Paik_Top aty wall MED Tower TEMP Chsto Chsto Chsto Chsto Chsto Chsto Chsto Shub a Shub b Shub c Shub d stone a stone stone " width="372" height="553" /></p>

<p>From this list, pick the assets that have not been run before, or that have been altered since the last run. The script will open each file and evaluate the material (MTL) usage on the parts.</p>

<p>If a material with emissive is in use, the script will create a copy of the MTL, append &quot;_Non_Emissive&quot; to the name, and remove any emissive or lightmap entries.</p>

<p>The script will then assign the new Non-Emissive MTL to the Unworked and Construction states of any geometry in the file and save it, resulting in a set up like this:</p>
<p><img src="BuildingsProcess/media/image131.png" alt="Machine generated alternative text: Cook Params Geometries Attachments Animations Particles Behaviors DIS DIS DIS DIS DIS DIS DIS DIS SPACE Bid SPACE Bid SPACE Bid SPACE Bid SPACE Bid SPACE Bid SPACE Bid SPACE Bid SPACE Bid Material DIS SPACE DIS SPACE DIS SPACE DIS SPACE DIS_SPACE_ B ase Base B ase Non Non Em issive Em issive Visible True T rue False False A (CIS _ SPACE Bld A); Vertex Count: 183; Primitive Count: Bone Count I A CON (DIS SPACE Bid A CON): VettexCount 5715, Count 2725, Bone Count 2 A DECAL PIL(DIS SPACE Bid A DECAL PIL). Ve,texCount 8. BoneCount4 A PIL(DIS SPACE_81d Ve,texCount 371 Pnmitive Count 723, Bone Count A A A A Group DIS SPACE DIS SPACE DIS SPACE DIS SPACE DIS_SPACE_ B ase Base B ase State Worked U nwor ked Pillaged Construction " width="1056" height="284" /></p>
<p>Note that the Pillaged state was not affected: The Pillage shader itself does not support emissive or lightmap inputs, so it is not necessary for the material to be altered.</p>

<p>Some Improvements are intended to stay lit during their Unworked state, due to how they're used in game. This list currently includes:</p>
<p>IMP_Airstrip</p>
<p>IMP_Fort (Medieval, Industrial, and Modern)</p>
<p>In the cases above, these assets can be placed outside of city borders and are intended to appear active regardless of whether they're actively Worked. After the Remove_Emissive script is run on any parts that have emissive in this situation, the Material assignment must be manually reverted in the .ast.</p>
<p><img src="BuildingsProcess/media/image132.png" alt="Machine generated alternative text: Cook Params Geometries Attachments Animations Particles Behaviors Material IMP IMP Airstrip 1M P_Airstrip IMP Airstrip_ IMP Non Em issive Visible True T rue True T rue IMP AÆthp_Hangar flMP AÆthp_Hangar); Veltex Count: 142; Phmitive Count: 12C&#39;; Bone Count 1M P_Airstrip _ Hangar IMP Airstrip_ Hangar 1M P_Airstrip_ Hangar IMP Airstrip_ Hangar IMP Airstrip_ Group IMP IMP Airstrip 1M P_Airstrip IMP Airstrip IMP_ State Worked U nwor ked Pillaged Construction " width="1062" height="290" /></p>
<p>If the Remove_Emissive script processes these parts again, the manual restoration will have to be repeated.</p>

<p>Districts themselves are currently never considered to be Unworked, so gamecore does not pass data to the model in game to change states on those tilebases and their attachments. The Remove_Emissive script is run on these parts regardless to accommodate a possible change to this approach in the future. As of this writing, it is unclear if Hero Buildings in Districts are affected by Worked/Unworked states, so again the Remove_Emissive script is run to allow for that function regardless.</p>

<p>If you encounter issues with the script, especially output errors or failure to process errors, please see Arthur.</p>

<p><em>Analytic Lighting</em></p>
<table>
<tbody>
<tr class="odd">
<td><p><img src="BuildingsProcess/media/image133.png" alt="Machine generated alternative text: " width="414" height="308" /></p>
</td>
<td><p><img src="BuildingsProcess/media/image134.png" alt="Machine generated alternative text: " width="442" height="306" /></p>
</td>
<td><p><img src="BuildingsProcess/media/image135.png" alt="Machine generated alternative text: " width="387" height="306" /></p>
</td>
</tr>
</tbody>
</table>
<p><em>Examples of assets using Analytic (Dynamic) lighting alone (Oil Well), Analytic Lighting combined with Emissive (Airstrip), and FX Dynamic Lighting with Emissive (Chateau)</em></p>

<p>In situations where you only need a small area of light or you want light to affect the ground as well as a model, an Analytic Light (also called a dynamic light) can be used in place of or in conjunction with Emissive or Lightmaps.</p>

<p>Analytic Lights are set up through the Asset Editor, and behave similar to Omni lights in 3DS Max, though with a much smaller range of controls. The Fork FX system also provides an option for dynamic lighting that goes through the same Analytic system, but requires the asset be set up through FX.</p>

<p>The main advantages of Analytic Lighting are a minimal impact on performance if restrictions are observed (see below) and no texture memory usage. The primary disadvantages of Analytic Lighting are the lack of shadow casting, significant performance impact if the system is abused, and limited animation if not set up through the FX system.</p>


<p><em><em>Restrictions</em></em></p>

<p>Before going over setup, it's important to understand the primary restrictions of the system. When looking at assets with dynamic lighting from any source in game, there should be no more than <strong><em>four</em></strong> dynamic light points in a four-hex area. Cities in particular had a number of dynamic entities added to them late in core development, and core city hexes often go above a count of four on their dynamic FX. Be aware of how your asset will be placed in game.</p>

<p>Analytic Lighting has no shadow-casting properties. When setting up a light, be aware of how the light will go through any nearby geometry, as this may cause visuals that will be counted as errors. This can be mitigated with negative lights (see below) to a limited degree.</p>


<p><em><em>3DS Max setup</em></em></p>

<p>The process for setting up an asset in 3DS Max for Analytic Lighting is the same as it is for effects: Create one or more Point Helpers and link them to a parent mesh or control dummy. Dynamic Lighting-only helpers should be named with the prefix &quot;DLBONE_&quot; or &quot;DL_&quot; and a descriptive name.</p>

<p><img src="BuildingsProcess/media/image136.png" alt="Machine generated alternative text: hematic View I Edit Select Laycut Opticn: DIS AQD aase aath Schemabc View : water DIS AQD aase aath Mesh001 DLBONE aathP001 Click or dick-and-drag to select objects " width="921" height="453" /></p>
<p><em>Example: The Aqueduct District Bath asset with DLBONE selected, and a Schematic View shot of the hierarchy. </em></p>


<p><em><em>Creating the Light in Asset Editor</em></em></p>

<p>Before proceeding, an important note: this system is a framework of ideas, and may not behave 100% consistently inside the Asset Editor. At times, the display of lights in the Asset Previewer will fail, even when the light is first created. It's a good idea to create the .lit entity, close the Asset Editor and reopen it before getting too far into tweaking parameters.</p>

<p>To create a new light in the Asset Editor, choose File&gt;New, and select Analytic Light from the Entities panel:</p>

<p><img src="BuildingsProcess/media/image137.png" alt="Machine generated alternative text: Pick the file type to create Ten_lre Analytic Light Light Rig Game Alt Specifi File Type Entities Animation Environment Light Behavior Packages Material Particle Efect " width="451" height="321" /></p>

<p>This will create a new .lit entity. Begin by naming the entity with the &quot;DL_ &quot; prefix and a descriptive name that references the object you'll be using the light on (e.g. DL_AQDBathGlow.lit)</p>

<p><img src="BuildingsProcess/media/image138.png" alt="Machine generated alternative text: Edit View Window Help Open Source file DLTEST Negative.lit DIS AQD Bath.ast DL_AQDBathG10w.1it Basic Name Class Name Desc ri pticn DL_AQDBathGlow Generic PointLight Text Text Text (3 tems) Generic PointLight Generic PointLight C ategorization Tags Cook Parameters Behavior ApplyLightMapWeight TimeOfDay Value Atten uaticn Color Intensity Night 7.87008 0.54. " width="576" height="598" /></p>

<ol style="list-style-type: decimal">
<li>
<p>Once named, you need to set the Class Name for the .lit entity to <em>Generic_PointLight</em>. The Class Name entry will be blank when you first create a new .lit, but fortunately you only have one choice in the pulldown menu. Until you do this, the Cook Parameters for the light will be unavailable.</p>
</li>
</ol>

<ol style="list-style-type: decimal">
<li>
<p>The Behavior section specifies how the light will react to the game's time of day system:</p>
</li>
</ol>



<ol style="list-style-type: lower-alpha">
<li>
<p><em><strong>ApplyLightMapWeight</strong></em> - this flag determines whether your light’s intensity should be multiplied by the current light map weight prior to it being passed to the dynamic light system. You'll usually want this on.</p>
</li>
</ol>



<ol style="list-style-type: lower-alpha">
<li>
<p><em><strong>TimeOfDay</strong></em> - This pulldown menu gives you the option of specifying whether the light is on all the time (All), day time only (Day), or night time only (Night), using the day/night threshold in the game.</p>
</li>
</ol>



<ol style="list-style-type: decimal">
<li>
<p>The Value section specifies the size and color of the light entity:</p>
</li>
</ol>



<ol style="list-style-type: lower-alpha">
<li>
<p><em><strong>Attenuation</strong></em> - Range 0.01 to 100 - This controls the falloff of the light, and adjusts the curve of that falloff from the center of the light the outer edge as defined by the Radius. The 3DS Max equivalent of this control would be <em>Decay</em> set to Inverse Square.</p>
</li>
</ol>



<ol style="list-style-type: lower-alpha">
<li>
<p><em><strong>Color</strong></em> - Range 0,0,0 to 255, 255, 255 - Not surprisingly, this defines the color of the light. When viewing the light only in the Asset Previewer, 255 white will have a yellow halo - this is caused by the blending of the light into the default green hex.</p>
</li>
</ol>



<ol style="list-style-type: lower-alpha">
<li>
<p><em><strong>Intensity</strong></em> - Range -100 to 100 - How bright the light is. 0 is effectively &quot;off.&quot; Negative numbers are used to define negative lights (see next section). The 3DS Max equivalent for this setting would be the <em>Multiplier</em>.</p>
</li>
</ol>



<ol style="list-style-type: lower-alpha">
<li>
<p><em><strong>Radius</strong></em> - Range 0.025 to 500 - This is the outer bounds of the light. This setting and the Attenuation play off each other to define the size the light appears in game. The 3DS Max equivalent for this setting would be the End value for <em>Far Attenuation</em>.</p>
</li>
</ol>

<p>When you view the light the Asset Previewer, keep an important fact in mind: the default light objects in the Previewer window is only slightly above the reference hex. Thus, the size, attenuation, and even the color are not quite what you will see when placed properly on a model, unless you're also placing it extremely close to the ground (which you shouldn't do). You'll need to actually apply the light to the model it goes with and make adjustments thereafter to the .lit entity to correctly gauge these Values.</p>

<table>
<tbody>
<tr class="odd">
<td><img src="BuildingsProcess/media/image139.png" alt="Machine generated alternative text: " width="576" height="432" /></td>
<td><img src="BuildingsProcess/media/image140.png" alt="Machine generated alternative text: " width="576" height="430" /></td>
</tr>
</tbody>
</table>
<p><em>Left: the DL_AQDBathGlow.lit entity as shown in the Asset Previewer; Right: the DL_AQDBathGlow.lit as it looks applied to the Aqueduct District Bath asset. Note the difference in perceived color and size.</em></p>


<p>After you've created the .lit entity, you'll need to add that new entry to the light.xlp file. While you'll be able to preview and assign the light to assets in the Asset Editor, you will not be able to see the light in game if its entry doesn't exist in the XLP.</p>

<p><img src="BuildingsProcess/media/image141.png" alt="Machine generated alternative text: Edit View Window Help Open Source file DLTEST Negative.lit Light.xlp DI.. AQ.. Ba...as.. DL AQDBathGlow.lit Module Name Light Pac kage Name Light Ljn1A XLP Class Light @ Windows C) Mecos Entity Name DL_AQDBathG D L _ NegativeShar p D rangeG low D L_Ora ngeG low B D L_OrangeGranaryLight DL_StepweIIG low DL YellowAirstipBeacon DL_YeIIowBoatLight DL_YeIIowBoatLightB DLTEST Negative DLTest RedLight LT Warning C) iOS Filter: Entry, ID DL_AQDBathG&#39;ow D L _ NegativeShar p D rangeG low D L_Ora ngeG low B D L_OrangeGranaryLight DL_StepweIIG low DL YellowAirstipBeacon DL_YeIIowBoatLight DL_YeIIowBoatLightB DLTEST Negative DLTest RedLight LT Warning " width="576" height="600" /></p>
<p><em>The light.xlp listing. Hit the button that the red arrow is pointing to in order to add your new light. </em></p>


<p><em><em>Negative Light</em></em></p>

<p>Analytic Lights do not (currently) have any properties to allow them to be anything other than point lights. You cannot choose a cone, direct, or hemispherical shape, as the extra calculations to display lights in those shapes was deemed too expensive. You do, however, have the option to use Negative lights, which will mask out any dynamic lighting within their area.</p>

<table>
<tbody>
<tr class="odd">
<td><img src="BuildingsProcess/media/image142.png" alt="Machine generated alternative text: " width="576" height="465" /></td>
<td><img src="BuildingsProcess/media/image143.png" alt="Machine generated alternative text: " width="535" height="465" /></td>
</tr>
</tbody>
</table>
<p><em>Left: The DLBONEs for the Oil Well Improvement's Shack. The yellow helper is the positive orange light, and the remainder are negative lights. The circle splines approximate the radius as set in the Asset Editor. Right: The Oil Well Improvement as seen in the Asset Previewer. Without the negative lights, the barrels and ground on all sides of the shack would be lit.</em></p>


<p><img src="BuildingsProcess/media/image144.png" alt="Machine generated alternative text: Basic Name Class Name Desc ri pticn C ategorization Tags Cook Parameters Behavior Ba...as Light.xlp DLT„ DL AQDBath...li.. IMP Oil Well.ast DLTEST Negative Generic PointLight Test analytic for negative light effect Text Text Text (3 tems) Generic PointLight Generic PointLight ApplyLightMapWeight TimeOfDay Value Atten uaticn Color Intensity Night " width="576" height="538" /></p>

<p>The process for creating a Negative light is the mostly the same, with two exceptions:</p>

<ol style="list-style-type: decimal">
<li>
<p>Your color should be 255,255,255</p>
</li>
</ol>



<ol style="list-style-type: decimal">
<li>
<p>The Intensity of the light must be negative, and is usually -100</p>
</li>
</ol>

<p>When you set up a Negative light in the Asset Editor, you will see nothing in the Asset Previewer.</p>

<p>After setting those two Values, the remainder of the work with setting up Negative lights is position and size. Attenuation will allow you to produce a very sharp or very soft edge to the &quot;mask,&quot; as you prefer. As with positive lighting, you'll get your best results by setting up the light entities on the model and using that to guide your choices.</p>

<p>As Negative lights are spherical, it often takes more of them to produce the effect you want (i.e. lighting on the side of a building, masking the underside of a raised structure). Remember the 4x4 rule for dynamic lights, as Negative lights count towards that total.</p>


<p><em><em>Assigning the light to an asset</em></em></p>

<table>
<tbody>
<tr class="odd">
<td>Once you've imported the model with associated DLBONEs, make sure to hit the Add Attachment Points to All Bones button (</td>
<td><img src="BuildingsProcess/media/image145.png" alt="C:\74741245\F0A4F1AD-AE5D-4B3D-84B4-FD2A3508EFC1_files\image151.png" width="28" height="27" /></td>
<td>) in the Attachments tab and verify that the bones are listed.</td>
</tr>
</tbody>
</table>
<p>From there, you'll move to the Asset Trigger Editor:</p>

<p><img src="BuildingsProcess/media/image146.png" alt="Machine generated alternative text: Cook Params Geometries Attachments Filter: Attachment Point Name bathhfire DLBONE BathP001 Animations Particles Behaviors Bath PIL Bath acne Name bathhfire DLBONE BathP001 A Model Instance DIS AQD_Base " width="1077" height="175" /></p>

<p><img src="BuildingsProcess/media/image147.png" alt="Machine generated alternative text: Asset Trigger Editor rlLL_qeeu Action ArtOefVFX Asset VFX Light Transfer Action ArtOefVFX Asset VFX Light Trans fer RKED OL AQoaathGIow COLBONE_aathPooI) Type Wiavior ktachment Point Duration Time TimeSeconds Ljght DL PODBathGow DLBONE BathP001 -0001852 Name of the asset to associate wth this tngger " width="1086" height="347" /></p>


<ol style="list-style-type: decimal">
<li>
<p>Verify that the proper state for the asset is defined. For Analytic Lighting, this is typically the <em>WORKED_A</em> state. If the state you want is missing, define it with the Add Timeline button</p>
</li>
</ol>

<p><img src="BuildingsProcess/media/image148.png" alt="C:\74741245\F0A4F1AD-AE5D-4B3D-84B4-FD2A3508EFC1_files\image154.png" width="24" height="21" /></p>


<ol style="list-style-type: decimal">
<li>
<p>Open the rollout for the state and locate the Light track.</p>
</li>
</ol>



<ol style="list-style-type: decimal">
<li>
<p>Right click within the timeline for the Light track and choose <em>Keys&gt;Light</em> to add an event</p>
</li>
</ol>

<ol style="list-style-type: decimal">
<li>
<p>Set the duration of the event. For most Analytic Lighting, right-click the event and choose <em>Set Duration to Infinity</em>.</p>
</li>
</ol>

<ol style="list-style-type: decimal">
<li>
<p>Within the panel on the right, select the <em>Asset</em> line item and add the specific Analytic Lighting entity that you want to display from the dialog that comes up.</p>
</li>
</ol>

<ol style="list-style-type: decimal">
<li>
<p>The next line item down is <em>AttachmentPoint</em>. The pulldown menu will display only valid Attachment Points for the asset you're working with. Choose the appropriate DLBONE entry for the lighting that you're applying.</p>
</li>
</ol>

<ol style="list-style-type: decimal">
<li>
<p>Rinse and repeat the steps above for each Attachment Point you want to assign a light to.</p>
</li>
</ol>


<p>After you've set up all of the Analytic Lights you want for a given asset, save the file. Then, click the name of the state you want to view and use the play controls to play the animation. This should display the Analytic Lighting in the Asset Previewer. Each time you adjust the parameters for a .lit entity, the animation will be off when you return to the assigned asset. Press play again to view the updated lighting. When using the Loop function to see lighting on non-animated assets, it is normal to see a skip in the display of the lighting - this will not happen in game, only in the Asset Previewer.</p>


<p><em><em>FAQ</em></em></p>

<p>Q: I set up a light a new light in the editor and added it to a model. In game, it turned into a large blue light. WTF?</p>
<p>A: If a new light isn't added to the light.xlp and cooked, the game will use the &quot;LT_Warning&quot; .lit instead, which is, in fact, a large blue light.</p>

<p>Q: Is there any way to get these lights to animate other than setting them up as FX?</p>
<p>A: Yes, you can use the timeline in the Asset Trigger Editor to specify when Analytic Lights turn on and off. For instance, the runway lights for IMP_Airstrip are set up this way. In the case of IMP_Airstrip, this also serves to keep the number of Analytic Lights in the hex at the maximum of four per hex, as there are two lights that are on permanently, and only two of the six runway lights are on in a given frame.</p>


<p>Adding animation to Buildings</p>
<p>Tuesday, September 08, 2015</p>
<p>4:50 PM</p>
<p>Animation Steps:</p>

<p>(In Max)</p>
<p>- It can be tricky to edit the model once it's been animated, so whenever possible, try to get it to the right scale and orientation before rigging it.</p>
<p>- Add all your bones, parent them under the mesh, set up your hierarchy, and skin your mesh to them.</p>
<p>- You need the skeleton to be part of the geometry that gets imported, so everything needs to be parented to the root of the geometry.</p>
<p>- Create your animation.</p>
<p>- Add the animation to the animation manager and give it a good name.</p>

<p>(In Asset Editor)</p>
<p>- Add the DSG. This is a State Graph that tells the asset to loop a single animation for each state.</p>
<p>- The animations don't just live in a vacuum, they are associated with different asset states.</p>
<p>- Click &quot;Add New&quot; which just imports the animations into the cloud.</p>
<p>- Then assign the animation to the state you want by clicking on the box to the right of the state.</p>
<p>- Then reimport your geometry because it needs to contain the bones</p>

<p>- There's two ways to play your animation:</p>

<p>- On the Asset Knobs tab (the one with the name of the asset) on the right, go to the 'Animation' tab. Where is says &quot;To State&quot; you need to select the state you want to play on the dropdown on the right</p>
<p>Or:</p>
<p>- Open up the &quot;Trigger Editor&quot; panel (By default it's at the bottom of the Asset Editor). Click on the button to add a Timeline to every state with an animation assigned to it.</p>
<p>- Double click on the Timeline to play it. You can use the Timeline editor to better scrub through your animation.</p>


<p>- You may notice that your animation is now off-Center, because that's where the animation is in your Max file. If this is not what you intended, you need to go back into the animation manager, Select your animation, and set its RMA (Root Motion Accumulation) to 1. Then save and reimport the animation.</p>
<p>- You can assign the same animation to multiple states, or you can have a separate animation per state.</p>
<p>- You can only have one animation per state, so all the geometries have to contain the skeleton being used in the animation.</p>


<p>(TroubleShoot)</p>
<p>Animation not playing:</p>

<p>- Make sure you reimport your geometry if you just added some animation, or if the names or hierarchy of bones has changed.</p>
<p>- Check that the bones are assigned to export in the model manager (they should be by default, but check nonetheless).</p>
<p>- Make sure the animation is assigned to the correct state.</p>

<p>My object is rotated wrong when the animation is not playing:</p>

<p>- It could be that you baked the objects rotation into the animation (i.e. you rotated it after you'd animated your object)</p>

<p>I need to modify my mesh but its already animated:</p>

<p>- You have two options:</p>
<p>- You can try adding an 'EditPoly' modifier under the 'Skin' modifier and make all your changes in there.</p>
<p>- You can remove the skin modifier, make your changes and re-skin the mesh.</p>


<p>(Notes)</p>
<p>- Visibility animation for the Wonder Movies is done on a per-mesh basis, and is independent of the skinned bone animation.</p>
<p>- Only attachment point animation will contour to the terrain (i.e. donkey).</p>
<p>- Be careful with trashing effects and sound triggers assigned to animations that already exist by changing the names of things</p>

<p>Approval Process</p>
<p>Tuesday, December 01, 2015</p>
<p>2:45 PM</p>

<p>Each approval stage should be sent to the Lead, Art Director, Concept Artist who created the concept, and the Producer</p>

<p><strong><em>Asset Modeling Checklist</em></strong></p>

<table>
<thead>
<tr class="header">
<th><em><strong>BLOCK OUT</strong></em></th>
<th> </th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Create models according to concept/review</td>
<td> </td>
</tr>
<tr class="even">
<td>Compare to similar assets</td>
<td> </td>
</tr>
<tr class="odd">
<td>Block out decals</td>
<td> </td>
</tr>
<tr class="even">
<td>Test all applicable conditions in-game</td>
<td> </td>
</tr>
<tr class="odd">
<td>Add to OneNote – email link</td>
<td> </td>
</tr>
<tr class="even">
<td>Approval #1 (Requires lead approval)</td>
<td> </td>
</tr>
<tr class="odd">
<td><em><strong>MODELING</strong></em></td>
<td> </td>
</tr>
<tr class="even">
<td>Models/Attachments complete</td>
<td> </td>
</tr>
<tr class="odd">
<td><p>Textures adhere to OneNote guidelines</p>
<ul>
<li>
<p>Basecolor</p>
</li>
<li>
<p>Normal</p>
</li>
<li>
<p>Glossiness</p>
</li>
<li>
<p>Metalness</p>
</li>
</ul></td>
<td> </td>
</tr>
<tr class="even">
<td>Tilebase(s) set up per era using models/attachments and in-game</td>
<td> </td>
</tr>
<tr class="odd">
<td>Create Obstruction profile</td>
<td> </td>
</tr>
<tr class="even">
<td>Create Road Connection Points (where applicable)</td>
<td> </td>
</tr>
<tr class="odd">
<td>Test all applicable conditions in-game</td>
<td> </td>
</tr>
<tr class="even">
<td>Approval #1 – Base tilebases/assets (Requires lead approval)</td>
<td> </td>
</tr>
<tr class="odd">
<td>Create construction and pillaged states (where applicable)</td>
<td> </td>
</tr>
<tr class="even">
<td>Create unworked states (where applicable)</td>
<td> </td>
</tr>
<tr class="odd">
<td>Create AO map</td>
<td> </td>
</tr>
<tr class="even">
<td>Create emissive/lightmaps</td>
<td> </td>
</tr>
<tr class="odd">
<td><p>Add FX nodes</p>
<ul>
<li>
<p>Assign FX if it exists</p>
</li>
<li>
<p>If no FX exists, send email to FX lead, building lead, producer to let them know an effect is ready to be added. Nodes should still be ready to go.</p>
</li>
</ul></td>
<td> </td>
</tr>
<tr class="even">
<td>Create animation (where applicable)</td>
<td> </td>
</tr>
<tr class="odd">
<td>Test all applicable conditions in-game</td>
<td> </td>
</tr>
<tr class="even">
<td>Add to OneNote – email link</td>
<td> </td>
</tr>
<tr class="odd">
<td>Approval #2 (Requires lead approval)</td>
<td> </td>
</tr>
</tbody>
</table>





<p>Crane</p>


<p>The * is the ground bases in which assets sit on and include all the decals, road connection points (Districts and Improvements where applicable)</p>

<p>Building Wishlist</p>
<p>Wednesday, August 17, 2016</p>
<p>11:31 AM</p>
<p>-Tommy</p>
<ul>
<li>
<p>Possible variation to the metalness mask, instead of just black and white. Something Subtle.</p>
</li>
<li>
<p>A better decal system, I'm still noticing issues with connections points, and even with the newly implemented wraparound system when building custom roads.</p>
</li>
<li>
<p>Pillage states for all buildings, even city fillers.</p>
</li>
<li>
<p>More variation with filler objects or plants within districts and city blocks.</p>
</li>
</ul>



<p>-Rambo</p>

<ul>
<li>
<p>Cloud shadows</p>
</li>
<li>
<p>Caustics in shallow water</p>
</li>
<li>
<p>Weather</p>
</li>
<li>
<p>Larger variety of vegetation</p>
</li>
<li>
<p>Building variations for improvements</p>
</li>
<li>
<p>Wild animals</p>
</li>
<li>
<p>Wider rivers and having the ability to build bridges to cross them</p>
</li>
<li>
<p>Map parchment variations</p>
</li>
<li>
<p>Seasons. Have a model variation for vegetation, and buildings with a shader to tint it spring, fall, or winter?</p>
</li>
<li>
<p>A pile of resources that replaces your WIP wonder model when another leader beats you to that wonder. Currently your wonder just disappears.</p>
</li>
</ul>



<ul>
<li>
<p>Squirrels running from tree to tree on the wood tiles</p>
</li>
<li>
<p>Darker/brighter patches of ancient dirt</p>
</li>
<li>
<p>More life in water. (maybe something like algae around the base of the lighthouse)</p>
</li>
</ul>




<p>Jerome-</p>

<ul>
<li>
<p>Some of the smaller buildings could use a hint of simple plants, small bushes, objects to help break the edges up and connect them to the ground.</p>
</li>
</ul>





<p>Wonder Modeling Pipeline</p>
<p>Friday, March 27, 2015</p>
<p>2:56 PM</p>

<p>Here are the instructions on how to set up a wander asset and hook it up in the game</p>

<p>Wonder Movie</p>
<p>Wednesday, February 24, 2016</p>
<p>3:55 PM</p>


<p><strong>Wonder Movie Buildups </strong></p>
<p><strong>Objective</strong></p>
<p>Create an animation for the specific wonder, using pre made pieces, and textures. The animation should be fluid and be a believable presentation of a building being constructed.</p>
<p><strong>Visibility Animations</strong></p>
<p>Wonder movies can support movement and scaling animations but a majority of the animation will be done with visibility. Also the majority of the animations will be done in tangent linear mode (right pic)</p>
<p><img src="BuildingsProcess/media/image149.jpg" alt="C:\74741245\F0A4F1AD-AE5D-4B3D-84B4-FD2A3508EFC1_files\image155.jpg" width="204" height="213" /></p>

<p><img src="BuildingsProcess/media/image150.jpg" alt="C:\74741245\F0A4F1AD-AE5D-4B3D-84B4-FD2A3508EFC1_files\image156.jpg" width="204" height="213" /></p>
<p><img src="BuildingsProcess/media/image151.jpg" alt="C:\74741245\F0A4F1AD-AE5D-4B3D-84B4-FD2A3508EFC1_files\image157.jpg" width="144" height="210" /></p>
<p>Right click on selected object  Go to object properties  Turn visibility to 0 or 100 to animate</p>
<p>A max script will be provided, that will make it so you can bind this action to a key or to a button in max.</p>
<p><strong>Hot Keying:</strong></p>
<p><img src="BuildingsProcess/media/image152.jpg" alt="C:\74741245\F0A4F1AD-AE5D-4B3D-84B4-FD2A3508EFC1_files\image158.jpg" width="218" height="228" /></p>

<p><img src="BuildingsProcess/media/image153.jpg" alt="C:\74741245\F0A4F1AD-AE5D-4B3D-84B4-FD2A3508EFC1_files\image159.jpg" width="219" height="228" /></p>
<p>Run script “switchVisibility.ms”  Go to Customize  Customize User Interface  Go to Keyboard tab  Madrid Tools  Bind key to Visibility Switch Hotkey.</p>

<p><img src="BuildingsProcess/media/image154.jpg" alt="C:\74741245\F0A4F1AD-AE5D-4B3D-84B4-FD2A3508EFC1_files\image160.jpg" width="190" height="198" /></p>
<p><img src="BuildingsProcess/media/image155.jpg" alt="C:\74741245\F0A4F1AD-AE5D-4B3D-84B4-FD2A3508EFC1_files\image161.jpg" width="354" height="93" /></p>

<table>
<thead>
<tr class="header">
<th> </th>
<th> </th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td> </td>
<td> </td>
</tr>
</tbody>
</table>

<p><strong>Binding Visibility to a Button:</strong></p>

<p>Go to Toolbars tab  Click and drag Visibility Switch to max tool bar  Click on button</p>

<p><strong><em>Pipe Line</em></strong></p>
<p>Walls &amp; Ground Frames Scaffolding Wonder Pieces Decals Attachments Camera Animations FX Attaching helpers</p>
<p>When you first open the file you will see the in-game wonder model, ground decals, two dummy attachments, and a hex geo with a safe frame geo. The material editor should contain the standard Max materials used on the model and the decals.</p>
<p><strong>Before you start</strong></p>

<ul>
<li>
<p>Do not modify material names, because our tools pull those materials from the cloud based on their naming convention.</p>
</li>
<li>
<p>Do not modify the wonder low poly geo (Other than cutting it into pieces).</p>
</li>
<li>
<p>While building it’s best to rough out the animations a little. Don’t worry too much about timing yet.</p>
</li>
<li>
<p>Leave room in the beginning and end of the animations for decals and scaffolding to come in and out.</p>
</li>
<li>
<p>Use layers, with a minimum of one layer for each step of the pipe line (i.e. Walls, Frames, etc..).  Refer to sample assets.</p>
</li>
<li>
<p>You can create your own pieces as long as you use the same textures. Some texture space has been given for unique textures, but consult with us before doing so.</p>
</li>
<li>
<p>You should set the viewport to “Consistent Colors” to avoid lag and help with readability.</p>
</li>
</ul>
<table>
<thead>
<tr class="header">
<th> </th>
<th> </th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td> </td>
<td><ul>
<li>
<p><img src="BuildingsProcess/media/image156.jpg" alt="C:\74741245\F0A4F1AD-AE5D-4B3D-84B4-FD2A3508EFC1_files\image162.jpg" width="215" height="121" /></p>
</li>
</ul></td>
</tr>
</tbody>
</table>






<p><strong>Walls &amp; Ground: </strong></p>
<p><img src="BuildingsProcess/media/image157.jpg" alt="C:\74741245\F0A4F1AD-AE5D-4B3D-84B4-FD2A3508EFC1_files\image163.jpg" width="303" height="171" /></p>

<p><img src="BuildingsProcess/media/image158.jpg" alt="C:\74741245\F0A4F1AD-AE5D-4B3D-84B4-FD2A3508EFC1_files\image164.jpg" width="308" height="172" /></p>

<ul>
<li>
<p>You will be given a Max file named “WON_Wonder_movie_Base” Merge in which ever construction material you are using in the wonder animation. Only merge in the assets from the “Asset_Library” layer.</p>
</li>
<li>
<p>Each wall set has two versions: One that is used for walls that has the bottom faces removed (B and D), and one that can be used for floors or other areas that does not have bottom faces removed (A and C). These objects are labeled in the max file. Any bottom faces that are not needed, from the A and C set, will be optimized at the very end.</p>
</li>
<li>
<p>The wall sets currently have 3 different texture swaps. A Red brick, yellow brick, and a modern grey brick texture. Use the texture set directed by our modeler.</p>
</li>
<li>
<p>The wall sets are made up of single bricks animating up to the top.  Once the wall fills up, the single bricks are replaced with one of the solid, big wall pieces</p>
</li>
<li>

</li>
</ul>
<table>
<thead>
<tr class="header">
<th> </th>
<th> </th>
<th> </th>
<th> </th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td> </td>
<td><ul>
<li>
<p><img src="BuildingsProcess/media/image159.jpg" alt="C:\74741245\F0A4F1AD-AE5D-4B3D-84B4-FD2A3508EFC1_files\image165.jpg" width="297" height="243" /></p>
</li>
</ul></td>
<td> </td>
<td><ul>
<li>
<p><img src="BuildingsProcess/media/image160.jpg" alt="C:\74741245\F0A4F1AD-AE5D-4B3D-84B4-FD2A3508EFC1_files\image166.jpg" width="240" height="240" /></p>
</li>
</ul></td>
</tr>
<tr class="even">
<td> </td>
<td> </td>
<td> </td>
<td> </td>
</tr>
</tbody>
</table>
<ul>
<li>
<p>Using the wonder low poly as a guide, make sure that the final wonder geometry contains the brick buildup structures. (Right Picture)</p>
</li>
<li>
<p>The bricks do not have to be scaled to the wonder’s details.</p>
</li>
<li>
<p>Use the single bricks to fill in areas that are too small for the wall sets, such as beveled corners and stairs.</p>
</li>
<li>
<p>You can use any modifier to modify the wall sets to fit your wonder. Most of the time you will just use the Bend Modifier. (Left Picture)</p>
</li>
</ul>

<p><img src="BuildingsProcess/media/image161.jpg" alt="C:\74741245\F0A4F1AD-AE5D-4B3D-84B4-FD2A3508EFC1_files\image167.jpg" width="184" height="269" /></p>

<ul>
<li>
<p>If a wonder has a brick ground, you can use the wall (A and C) set that still has bottom faces and flip it on its side.</p>
</li>
</ul>



<ul>
<li>
<p>When you are done with the ground level wall sets, you can duplicate the set up and move the duplicated wall set’s animation frames further down the timeline. (Right Picture)</p>
</li>
</ul>








<table>
<thead>
<tr class="header">
<th> </th>
<th> </th>
<th> </th>
<th> </th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td> </td>
<td><img src="BuildingsProcess/media/image162.jpg" alt="C:\74741245\F0A4F1AD-AE5D-4B3D-84B4-FD2A3508EFC1_files\image168.jpg" width="330" height="219" /></td>
<td> </td>
<td><img src="BuildingsProcess/media/image163.jpg" alt="C:\74741245\F0A4F1AD-AE5D-4B3D-84B4-FD2A3508EFC1_files\image169.jpg" width="261" height="219" /></td>
</tr>
</tbody>
</table>

<p><strong>Wood and Steel Frames:</strong></p>
<p><strong> </strong></p>

<ul>
<li>
<p>There are 2 different frames. Metal and wood. The ancient wonders will use wood, but the more modern wonders will use more metal frames. If you are unsure of which one you should use, please let us know.</p>
</li>
</ul>



<ul>
<li>
<p><img src="BuildingsProcess/media/image164.jpg" alt="C:\74741245\F0A4F1AD-AE5D-4B3D-84B4-FD2A3508EFC1_files\image170.jpg" width="246" height="192" /></p>
</li>
</ul>

<p>Place the frames where frame support should be in real buildings. As a general rule, the frames should be placed just directly inside of a wall.  These frames could be used for roofs, wall beams, and floor supports<strong>.</strong> Modern buildings frame levels should be started (horizontal and vertical pieces) before filling in with brick.</p>



<p><img src="BuildingsProcess/media/image165.jpg" alt="C:\74741245\F0A4F1AD-AE5D-4B3D-84B4-FD2A3508EFC1_files\image171.jpg" width="329" height="175" /></p>
<p><strong>Scaffolding:</strong></p>

<ul>
<li>
<p>There two different scaffolding sets. Wooden and Metal. (Top Picture)</p>
</li>
<li>
<p>The wooden one is for ancient wonders, and the metal one is for modern wonders.</p>
</li>
<li>
<p>Have the scaffolding come up before the bricks.</p>
</li>
<li>
<p>Like the walls, the scaffolding sets already have animation on them. And again, when you’re done with the first level, you can duplicate the original scaffolding up and move the duplicate set’s animation forward on the timeline. (Bottom Picture)</p>
</li>
<li>
<p>Add enough scaffolding to show the wonder is under construction but not too much that it would cover up the wonder’s silhouette.</p>
</li>
<li>
<p>The scaffolding also has a deconstruction animation further down the timeline. </p>
</li>
<li>
<p><img src="BuildingsProcess/media/image166.jpg" alt="C:\74741245\F0A4F1AD-AE5D-4B3D-84B4-FD2A3508EFC1_files\image172.jpg" width="318" height="279" /></p>
</li>
</ul>

<p>Once you have your wonder structure movie completed, adjust the key frames for the scaffolding deconstruction so they match up with the finalization of the building finishing</p>

<ul>
<li>
<p>You can ungroup the scaffolding sets to create your own sets, but remember about the premade frames.</p>
</li>
</ul>






<p><img src="BuildingsProcess/media/image167.png" alt="C:\74741245\F0A4F1AD-AE5D-4B3D-84B4-FD2A3508EFC1_files\image173.png" width="378" height="353" /></p>
<p><strong>Wonder Pieces</strong></p>
<p><strong> </strong></p>

<ul>
<li>
<p>Cut up the wonder low poly into pieces. Cut out enough pieces so they will animate in smoothly. The more pieces there are, the more smoothly the pieces will animate in.</p>
</li>
<li>
<p>The wonder pieces should be animated in, once the construction passes the piece (Right Picture)</p>
</li>
<li>

</li>
</ul>
<table>
<thead>
<tr class="header">
<th> </th>
<th> </th>
<th> </th>
<th> </th>
<th> </th>
<th> </th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td> </td>
<td><ul>
<li>
<p><img src="BuildingsProcess/media/image168.jpg" alt="C:\74741245\F0A4F1AD-AE5D-4B3D-84B4-FD2A3508EFC1_files\image174.jpg" width="264" height="168" /></p>
</li>
</ul></td>
<td> </td>
<td><ul>
<li>
<p><img src="BuildingsProcess/media/image169.jpg" alt="C:\74741245\F0A4F1AD-AE5D-4B3D-84B4-FD2A3508EFC1_files\image175.jpg" width="151" height="165" /></p>
</li>
</ul></td>
<td> </td>
<td><ul>
<li>
<p><img src="BuildingsProcess/media/image170.jpg" alt="C:\74741245\F0A4F1AD-AE5D-4B3D-84B4-FD2A3508EFC1_files\image176.jpg" width="153" height="165" /></p>
</li>
</ul></td>
</tr>
<tr class="even">
<td> </td>
<td> </td>
<td> </td>
<td> </td>
<td> </td>
<td> </td>
</tr>
</tbody>
</table>



<ul>
<li>
<p>For some wonders you would want to take some of the pieces you cut out, duplicate it, and remap it to the plaster texture, having the plaster version come in before the actual wonder piece. This technique works well for wonder pieces with a lot of paintings on it, making the transitions smoother</p>
</li>
<li>
<p>Sometimes you would need to create custom geo pieces. An example would be the gears in the Big Ben wonder movie. In this case, we were able to use already existing textures to kitbash together some gears. That may work for some wonders while others may need custom textures created for them (discussed prior)</p>
</li>
</ul>

<p><img src="BuildingsProcess/media/image171.jpg" alt="C:\74741245\F0A4F1AD-AE5D-4B3D-84B4-FD2A3508EFC1_files\image177.jpg" width="556" height="147" /></p>
<p><strong>Decals</strong></p>
<p><img src="BuildingsProcess/media/image172.jpg" alt="C:\74741245\F0A4F1AD-AE5D-4B3D-84B4-FD2A3508EFC1_files\image178.jpg" width="206" height="121" /></p>

<ul>
<li>
<p>There are 4 decal sets - modern, industrial, classical, and ancient.  Every set should use the ancient set underneath.  As a general workflow, it is usually advised to lay out all of your decals with the ancient set first, make a duplicate, and apply a more modern decal material to the duplicate</p>
</li>
<li>
<p>Place the ancient decal at 6 units on the Z axis and for the rest of the decals place them at 11 units.</p>
</li>
</ul>



<table>
<thead>
<tr class="header">
<th> </th>
<th> </th>
<th> </th>
<th> </th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td> </td>
<td><img src="BuildingsProcess/media/image173.jpg" alt="C:\74741245\F0A4F1AD-AE5D-4B3D-84B4-FD2A3508EFC1_files\image179.jpg" width="308" height="181" /></td>
<td> </td>
<td><img src="BuildingsProcess/media/image174.jpg" alt="C:\74741245\F0A4F1AD-AE5D-4B3D-84B4-FD2A3508EFC1_files\image180.jpg" width="309" height="181" /></td>
</tr>
</tbody>
</table>

<p><strong> </strong></p>

<ul>
<li>
<p>There are two main decal events in the wonder movies. The decal that comes in before and while the construction happens and the final wonder decal. The final wonder decal should already be done and be part of the wonder low poly. So the only decal event you would need to create is the beginning one.</p>
</li>
<li>
<p>For the buildup you will pretty much exclusively using the ancient decal set.  You can overlap multiple decals to create more complex shapes.  The culmination of these shapes should not be random and should correlate to the building footprint, giving it the illusion that an excavation took place.</p>
</li>
<li>
<p>Animate them coming in before and while the construction starts.</p>
</li>
<li>
<p>Make sure the decals are flat and are all in the same Z axis position.</p>
</li>
<li>
<p>Do not have the decals go outside of the hex too much.</p>
</li>
<li>
<p>When the wonder construction is done. Animate the ancient decal out and have the final decals come in.</p>
</li>
<li>
<p>Do not change the size of the decals if you can.</p>
</li>
</ul>


<p><strong>Attachments:</strong></p>
<p><img src="BuildingsProcess/media/image175.jpg" alt="C:\74741245\F0A4F1AD-AE5D-4B3D-84B4-FD2A3508EFC1_files\image181.jpg" width="288" height="195" /></p>

<p><img src="BuildingsProcess/media/image176.jpg" alt="C:\74741245\F0A4F1AD-AE5D-4B3D-84B4-FD2A3508EFC1_files\image182.jpg" width="278" height="195" /></p>

<ul>
<li>
<p>You will be given a Max file named “WON_Wonder_movie_Base” This file will have animated construction clutter. Merge in which ever construction material you are using in the wonder animation. Only merge in assets from the “Attachment_Library” layer.</p>
</li>
<li>
<p>Most wonders will have other assets aside from the main building.  Generally these are referred to as “attachments” and serve two purposes – 1. They terrain conform and 2. They are instanced geometry, allowing for the original to be changed and all instances be affected globally across the game</p>
</li>
<li>
<p>All the wonders should have the attachment objects already set up, so you most likely won’t need to do the wonder attachments. But you will need to set up the construction clutter attachments.</p>
</li>
<li>
<p><img src="BuildingsProcess/media/image177.jpg" alt="C:\74741245\F0A4F1AD-AE5D-4B3D-84B4-FD2A3508EFC1_files\image183.jpg" width="303" height="192" /></p>
</li>
</ul>

<p>Make sure all the attachment objects are named the same as the ones you referenced from the master file (left pic).  Then add 3 digits after that name – 001, 002, 003 etc (right pic).”</p>

<ul>
<li>
<p>Copy and place them around the wonder. Make sure they are not off the Hex or over lapping anything other geo.</p>
</li>
<li>
<p>Then you adjusts the animation on the clutter sets to match up with your wonder animations</p>
</li>
</ul>













<p><strong>Camera: </strong></p>
<p><img src="BuildingsProcess/media/image178.jpg" alt="C:\74741245\F0A4F1AD-AE5D-4B3D-84B4-FD2A3508EFC1_files\image184.jpg" width="284" height="201" /></p>

<p><img src="BuildingsProcess/media/image179.jpg" alt="C:\74741245\F0A4F1AD-AE5D-4B3D-84B4-FD2A3508EFC1_files\image185.jpg" width="276" height="204" /></p>

<ul>
<li>
<p>Import the Camera_Spline from the WON_Camera_Movie_Base max file</p>
</li>
<li>
<p>Import the Camera_Spline from the WON_Camera_Movie_Base max file</p>
</li>
<li>
<p>Have the Camera animation follow the spline</p>
</li>
<li>
<p>Go to Motion Tab  Add Path  Select Spline</p>
</li>
</ul>

<p><strong>Animation:</strong></p>
<p><img src="BuildingsProcess/media/image180.jpg" alt="C:\74741245\F0A4F1AD-AE5D-4B3D-84B4-FD2A3508EFC1_files\image186.jpg" width="151" height="222" /></p>

<p><img src="BuildingsProcess/media/image181.jpg" alt="C:\74741245\F0A4F1AD-AE5D-4B3D-84B4-FD2A3508EFC1_files\image187.jpg" width="433" height="166" /></p>

<ul>
<li>
<p>Remember to switch back to tangent linear (Left Pic). Most of the time you will be working in that mode.</p>
</li>
<li>
<p>Some of the models already have animations on them. All you need to do is just slide the animations on the time line.</p>
</li>
<li>
<p>When you are done roughing out the animations, you will most likely want to make changes to the timing.  You can use the scale tool under the timeline to scale the animations to make them longer or shorter, which is quicker than hand moving sets of frames. It is recommended to be careful when scaling more than once as it can scale improperly and you will lose important keys</p>
</li>
<li>
<p>Have the objects furthest away from the camera build up faster than the objects closer to create depth.</p>
</li>
<li>
<p>Try to keep everything animating at the same speed.</p>
</li>
<li>
<p>Have multiple objects animating in the same time to create more depth in the animation. But do not have more than 5000 objects.</p>
</li>
<li>
<p>Remember to leave time in the beginning of the animation for decals to come in and at the end for the scaffolding to come down.</p>
</li>
<li>
<p>Have everything animate away by frame 499, so that the final wonder will be shown in frame 500.</p>
</li>
<li>
<p>Animation can go over 500 if needed, but do not go over 600 frames.</p>
</li>
<li>
<p>Have some of the wall sets, and frames disappear when the wonder pieces cover it, to save memory.</p>
</li>
<li>
<p>Change up the animation timing in the wall and scaffolding sets so that not everything is animating in the same time.</p>
</li>
<li>
<p>The last frame of the wonder movie will be the model you see when the wonder is finished in game.</p>
</li>
</ul>


<p><strong>FX: </strong></p>
<p><img src="BuildingsProcess/media/image182.jpg" alt="C:\74741245\F0A4F1AD-AE5D-4B3D-84B4-FD2A3508EFC1_files\image188.jpg" width="197" height="206" /></p>

<p><img src="BuildingsProcess/media/image183.jpg" alt="C:\74741245\F0A4F1AD-AE5D-4B3D-84B4-FD2A3508EFC1_files\image189.jpg" width="201" height="210" /></p>

<ul>
<li>
<p>You will need to create dummy helpers so FX can be attach to them in the engine.</p>
</li>
<li>
<p>Name the nodes “WON_name_Movie_FX” and add numbers after 001, 002 ,003 ,etc..</p>
</li>
<li>
<p>Have the helpers animate up with the wonder construction. Not all the helpers will need to be at the very top.</p>
</li>
</ul>

<p><strong> </strong></p>

<ul>
<li>
<p>Have the helpers spread out equally.</p>
</li>
</ul>

<p><img src="BuildingsProcess/media/image184.jpg" alt="C:\74741245\F0A4F1AD-AE5D-4B3D-84B4-FD2A3508EFC1_files\image190.jpg" width="315" height="305" /></p>
<p><strong><em>Cranes</em></strong></p>
<p><img src="BuildingsProcess/media/image185.jpg" alt="C:\74741245\F0A4F1AD-AE5D-4B3D-84B4-FD2A3508EFC1_files\image191.jpg" width="269" height="221" /></p>

<ul>
<li>
<p>Merge in crane from the WON_Cranes_Movie_Base max file.</p>
</li>
<li>
<p>There are 3 different kinds of cranes. Ancient, Industrial, and Modern</p>
</li>
<li>
<p>Place 1 or 2 cranes attachments around the wonder.</p>
</li>
<li>
<p>Have the cranes only interact with the brick pile attachments.</p>
</li>
<li>
<p>Makes sure the cranes do not collide with anything in the scene</p>
</li>
<li>
<p>Dummies can’t have visibility animation on them, so swap the crane geo’s name with the crane dummies name.</p>
</li>
<li>
<p>Export only the crane geo, and export it as a bone.</p>
</li>
<li>

</li>
</ul>

<p><strong><em>Road point helpers</em></strong></p>
<p><img src="BuildingsProcess/media/image186.jpg" alt="C:\74741245\F0A4F1AD-AE5D-4B3D-84B4-FD2A3508EFC1_files\image192.jpg" width="327" height="251" /></p>

<ul>
<li>
<p>If a road decals comes close to the borders of the safe frame hex, put a point helper object on it. Place only one point helper for each edge of the hex.</p>
</li>
<li>
<p>Name of the point “Road_CP001”.. ect</p>
</li>
<li>
<p>Have the points Y axis perpendicular to the decal it is on</p>
</li>
</ul>


<p><strong>Attaching helpers</strong></p>
<p><img src="BuildingsProcess/media/image187.jpg" alt="C:\74741245\F0A4F1AD-AE5D-4B3D-84B4-FD2A3508EFC1_files\image193.jpg" width="282" height="222" /></p>

<ul>
<li>
<p>As a reminder, the file we provided should already have two helper objects</p>
</li>
<li>
<p>Rename the big helper “WON_name_Movie” and rename the other ”WON_name_Movie_Decal”</p>
</li>
<li>
<p>“Attach all the models to the “WON_name_Movie” helper, using the Select and Link tool in the upper toolbar (above pic) and the decals to “WON_name_Movie_Decal” using the same tool.</p>
</li>
<li>
<p>Sometimes there are too many objects to attach all at once. So attach them in groups.</p>
</li>
<li>
<p>Attach the Fx helpers to the “WON_name_Movie” helper.</p>
</li>
<li>
<p>Do not attach the camera to any of the helpers</p>
</li>
</ul>

<p><strong>Exporting models and animations</strong></p>
<p><img src="BuildingsProcess/media/image188.jpg" alt="C:\74741245\F0A4F1AD-AE5D-4B3D-84B4-FD2A3508EFC1_files\image194.jpg" width="327" height="233" /></p>

<ul>
<li>
<p>Before you export you must have the 3DSMax Civ 6 Max tools installed.  Once it is installed you should be able to go to your Utilities Panel &gt; Max Script and under utilities Select Civ 6 Tools from the drop down and click on it.  A list of tools should now be available in the panel below.</p>
</li>
<li>
<p>The model manager is a tool which enables/disables models for export.  It is important that any model being exported into the game be in the Objects to Export Window on the right.  A typical workflow could be as follows:</p>
</li>
<li>
<p>Clear list in model manager to prevent unwanted files from exporting (clear list button is above Objects to Export Window).</p>
</li>
</ul>



<ul>
<li>
<p>Select all models and FX nodes you want to export and click the  Arrow to move it. You can also do this in groups, if there are too many.</p>
</li>
<li>
<p>Select the models that are <strong>attachments</strong> and check off “Export as bone”</p>
</li>
<li>
<p><img src="BuildingsProcess/media/image189.jpg" alt="C:\74741245\F0A4F1AD-AE5D-4B3D-84B4-FD2A3508EFC1_files\image195.jpg" width="312" height="264" /></p>
</li>
</ul>

<p>In the “Granny Models in export List” you should only see the wonder movie camera, wonder movie, and wonder movie decal nodes.</p>

<ul>
<li>
<p>Name the animation” WON_name_Wonder_Movie”</p>
</li>
<li>
<p>Type in your start animation and ending animations, and click “Add Anim”</p>
</li>
<li>
<p>Save Max file</p>
</li>
<li>
<p><strong>Importing:</strong></p>
</li>
</ul>

<p><img src="BuildingsProcess/media/image190.jpg" alt="C:\74741245\F0A4F1AD-AE5D-4B3D-84B4-FD2A3508EFC1_files\image196.jpg" width="231" height="163" /></p>

<p><img src="BuildingsProcess/media/image191.jpg" alt="C:\74741245\F0A4F1AD-AE5D-4B3D-84B4-FD2A3508EFC1_files\image197.jpg" width="275" height="243" /></p>

<ul>
<li>
<p>In the engine go to File  New  Create new asset</p>
</li>
<li>
<p>Fill out the new asset like shown above (Right picture), but for name replace “test” with the name of the wonder. Then click on Geometries tab, then click on the second icon.</p>
</li>
</ul>


<p><img src="BuildingsProcess/media/image192.jpg" alt="C:\74741245\F0A4F1AD-AE5D-4B3D-84B4-FD2A3508EFC1_files\image198.jpg" width="276" height="254" /></p>

<ul>
<li>
<p>Import the two helpers and the wonder camera.</p>
</li>
<li>
<p>Do not import the Camera Target.</p>
</li>
<li>
<p>The textures should come in automatically because all the material in max were named correctly.</p>
</li>
</ul>








<ul>
<li>
<p>Run script “Update_Asset_Attachments.py” and rerun it whenever update the attachment list.</p>
</li>
</ul>


<p><img src="BuildingsProcess/media/image193.jpg" alt="C:\74741245\F0A4F1AD-AE5D-4B3D-84B4-FD2A3508EFC1_files\image199.jpg" width="541" height="272" /></p>

<ul>
<li>
<p>Click on Animations Tab  Click on Reveal_A row, and Import animation from your Max file.</p>
</li>
<li>
<p>Save the new asset.</p>
</li>
</ul>

<p><img src="BuildingsProcess/media/image194.jpg" alt="C:\74741245\F0A4F1AD-AE5D-4B3D-84B4-FD2A3508EFC1_files\image200.jpg" width="309" height="239" /></p>

<ul>
<li>
<p>You can view you animations by going to the right side menu.</p>
</li>
<li>
<p>Click on Animation tab, select ANY for From State, and REVEAL for To State.</p>
</li>
<li>
<p>Then push Play.</p>
</li>
</ul>








<ul>
<li>
<p><img src="BuildingsProcess/media/image195.jpg" alt="C:\74741245\F0A4F1AD-AE5D-4B3D-84B4-FD2A3508EFC1_files\image201.jpg" width="315" height="171" /></p>
</li>
</ul>

<p>Go to the WonderMovie.xlp and add the new asset you created. This tells the engine to place your asset when the player create that wonder in game.</p>




<ul>
<li>
<p> WIP</p>
</li>
<li>
<p>Rebake tilebases if you updated it.</p>
</li>
<li>
<p>Rebake WonderMovie.xlp and WonderMovie.artdev before launch the game</p>
</li>
</ul>



<p><strong>Idle FX</strong></p>
<p>Idle FX are FX that will be playing during the construction of the wonder.</p>
<p>Create a box, and name it “FX_Sparks001, or FX_Dust001”</p>
<p>Place it when you want to have the fx to turn on when the construction builds up to that point.</p>
<p>Then turn the visibility of the object</p>
<p>Always have at least 1 idle fx on, but have no more than 4 or 5.</p>
<p>Export as bone</p>

<p><strong>How to view them</strong></p>
<p><strong>Ruined States</strong></p>
<p>Display ruined state</p>
<p>Make sure burn materal is on the objects u want</p>
<p>Creat new attachment</p>
<p>Rename bone, and position it</p>
<p>Create time ruined A</p>
<p>Add asset</p>
<p>Assign asset and attachment point pick fire or smoke</p>
<p>Set loop to -1</p>
<p><strong>Max Scripts New Scripts</strong></p>
<p>Delete downward faces</p>
<p>Clean duplicated material</p>
<p>Wonder Merge – do this last, you can’t undo it</p>
<p><strong>Put in Emissive model</strong></p>
<p>Have everything turn off at frame 500, then have it replaced by the emmisive model</p>
<p>Make sure the emissive material is on it the object</p>
<p><strong> </strong></p>
<p><strong>Make sure nodes are not scaled</strong></p>
<p><strong>Adding fire and smoke to ruined states</strong></p>
<p><strong>Artdev stuff like frame starting and frame ending and time of day</strong></p>
<p><strong>Needs to 500 frames</strong></p>


<p>How to author Wonder Movie (3dsMax)</p>
<p>Thursday, July 02, 2015</p>
<p>9:15 AM</p>

<p>Wonder movies need a very specific file organization in order to work with the time-lapse wonder movie system. Some of the instruction here are required, while some are just best practice to make your life easier.</p>

<p>Scene Hierarchy</p>

<p>There's 3 different ways of setting up the scene hierarchy for a wonder movie, depending on how you want it to work:</p>

<ul>
<li>
<p><strong><em>Parent Objects to root bone</em></strong>: Any objects that are parented to a root bone will keep their relative position to the bone itself. That means that the objects will not conform to the terrain individually. When importing into the engine, all the objects will come in as a single geometry file.</p>
</li>
</ul>

<p><img src="BuildingsProcess/media/image196.png" alt="Machine generated alternative text: Root Sone Terrain Children objects will not follow the terrain, but will keep their positions relative to the root model 1 The root will follow the terrain " width="568" height="332" /></p>



<ul>
<li>
<p><strong><em>Keep objects separate</em></strong>: If you keep all the objects separate in the hierarchy, then they will all conform to the terrain. When importing into the engine, each separate object will be treated as a separate geometry file, which makes it a bit trickier to manage if there are many different objects.</p>
</li>
</ul>


<p><img src="BuildingsProcess/media/image197.png" alt="Machine generated alternative text: All the individual geometries will follow the terrain model 1 Root Sone model 2 Terrain " width="393" height="282" /></p>

<ul>
<li>
<p><strong><em>Bring in separate objects as attachments</em></strong>: For this to work, you need to create an attachment point for each separate object and then create each attachment as a separate asset and attach them. Each attachment will then conform to the terrain. The main benefit to this method over just using individual geometries is that the same asset can be attached multiple times without paying for the memory of having multiple copies. This really only makes sense if the pieces are not unique, and they will only be used by wonders.</p>
</li>
</ul>





<p><img src="BuildingsProcess/media/image198.png" alt="Machine generated alternative text: model 2 Attachment Point model 1 Attachment Point The attached objects (Attachments) will follow the terrain at the x,y position of their attachment point model 1 Root Sone model 2 Terrain " width="543" height="299" /></p>



<ul>
<li>
<p>All the geometry for the wonder and the movie should be under a dummy object. Both the pieces that animate during the wonder movie, and the pieces of the completed wonder.</p>
</li>
<li>
<p>Decals should be under their own root dummy as well</p>
</li>
<li>
<p>The Camera should be at the top of the hierarchy</p>
</li>
<li>
<p>The root dummy for the wonder pieces and the decals should not have any scaling or rotation on them, and they should be at the world origin</p>
</li>
</ul>



<p><img src="BuildingsProcess/media/image199.png" alt="Machine generated alternative text: camera001 CameraOOI.Target Decals Root Dummy Wonder Root Dummy Completed Wonder Piece_OO Completed Wonder Piece 01 Wonder Movie Piece Wonder Movie Piece Wonder Movie Piece Wonder Movie Piece Wonder Movie Piece Wonder Movie Piece Wonder Movie Piece Wonder Movie Piece Wonder Movie Piece Wonder Movie Piece Wonder Movie Piece Wonder Movie Piece 00 01 02 03 04 06 07 08 10 11 " width="243" height="412" /></p>

<p>Materials</p>

<p>Because the wonders have so many separate pieces, it is useful to take advantage of the Asset Editor's automatic material assignment. For the automatic system to work, the materials assigned to the pieces in Max have to have the same name as the materials in the Asset Cloud that will be assigned to the WonderMovie. The automatic matching happens when you add the wonder geometry to your WonderMovie asset, so you should have created your materials in the Editor before adding the geometry to your asset.</p>

<p><img src="BuildingsProcess/media/image200.png" alt="Machine generated alternative text: AssetEditor - D: ro ctsXBALW-AGOULD Civ6 mainXCiv6 n File Edit View Window Open Source file Pyramid Material 01.mtI ateriaIsXP ramid M.. Material Editor - ramid Material 01 Modes Material Ny.:igeticn Opticn: 00000 eeeee eeeee Basic Name Pyramid Material 01 Same erspective) (Realistic Name Pyramid Material 01 Shader Basic Parameters Wir e Face Map alinn Basic Parameters Sel f-llluminabon Color O Opacity: 100 Standard 2-sided Face ted (I items) items) Specular Class Nam Landmark Description C ategorization Tags Groups Landmark o Cook Parameters Value 3aseCcIcr Emissive Gloss LightMap Metal ness Normal Opac ity Document Saved Specular Highligh ts Specular Level: GIO ssiness: Soften: 0.1 Extended Par ame ters Super Sampling mental ray Connection " width="1041" height="709" /></p>

<p>Wonder Animations</p>

<p>Each wonder needs two animations, an <strong>IDLE</strong> animation and a <strong>REVEAL</strong> animation</p>

<p>The REVEAL animation is the animation that will be played during the wonder reveal when it's built by the player. This is the time-lapse style animation where the visibility of pieces is switched on an off. This animation is also used to show the progress of the wonder while it's being built by the player</p>

<p>The IDLE animation is the animation that get played by the wonder while it's on the map. This animation should be a looping animation of the cranes and the like doing idle work. This animation will be played only on the object that are visible.</p>

<p>You need to set up the two animations in the &quot;Animation Manager&quot;. To find the animation manager go to the &quot;Utilities&quot; Tab in the command panel(1), Select the Maxscript button (2), and then select &quot;Civ 6 Tools&quot; under the &quot;Utilities&quot; dropdown (3), there you will find the &quot;Animation Manager&quot; button (4)</p>

<p><img src="BuildingsProcess/media/image201.png" alt="Machine generated alternative text: CameraOO I.Target More... Utilibes Sets Asset ar owser Perspective Ma tch Color Clipboard Measure MO bon Capture Rese t XForm Flight Studio (c) MAX Script Open Listener New Script Open Script Run Script Lltlites Civ S Tools Close Civ 6 Tools Anima bon Manager Model Manager Clean Scene TileBase Cleanup " width="225" height="776" /></p>

<p>That will bring up the &quot;Animation Manager&quot; window where you can add animations that can be exported. To add an animation click on the &quot;(+) Add Animation&quot; (1) button. Then select the animation that just got created, and give it an identifying name (something like &quot;[Wonder Name]_Idle&quot;) (2), then select the frame-range where your animation is (3). Once the animation are created you can close the manager. You will need to go back to the Animation Manager if you change the frames of the animation, or decide to add more animations to your file.</p>

<p><img src="BuildingsProcess/media/image202.png" alt="Machine generated alternative text: Firaxis Animation Manager Animation Name WonderName Idle WonderName Reveal Start End loof loof Selection Set None None Selected Animaton Notes Anima bon Name Start Frame End Frame Does Expor t No tes (+) Add Anim WonderName Idle Scene Time 100 (-) Remove Advanced. Impor t De fini bons Expor t De fini bons AutoSync Timeline V AutoSync Render Dialog AutoPlay Animaton " width="576" height="318" /></p>


<p>TroubleShooting</p>

<p><strong>-The wrong materials are showing up on the model:</strong> Make sure that there is a material in the Asset Cloud that has the same name as the materials you have assigned in 3dsMax.</p>

<p><strong>-The wrong geometry is showing up or not refreshing:</strong> Make sure that in the model manager in your Max file all the correct objects are flagged for export. Alternatively, make sure that the geometry that is in the Asset Cloud is pointing to the right Max file. You can do that by opening the geometry directly ( 'File&gt;</p>

<p>Hooking up into the game</p>
<p>Friday, March 27, 2015</p>
<p>2:58 PM</p>

<p>1.- Check to see if the Wonder already has a placeholder:</p>

<p>Open the Asset Editor, and open <strong>WonderMovie.xlp</strong>. Check the entry list to see if there is already one entry with the name of your wonder. Most of the wonders are already hooked up, but they are pointing to use the Great Library asset, so all you have to do is point the entry to your wonder asset.</p>

<p>If there was already a placeholder for your wonder and you switched which asset it's pointing to, you can skip to <strong>step 5</strong>. Otherwise you have to move on to <strong>step 2</strong> and follow the rest of the steps.</p>

<p>2.- Finding the Building Type name:</p>

<p>First you need to find the name that gameplay is using to refer to the wonder you want to hook up. This is called the <strong>BuildingType</strong>. To find the building type for the wonder you care about, go to the file:</p>

<p>[Your Game's project folder]Civ6\Game\installed_assets\Gameplay\Data\Buildings.xml</p>

<p>And find the wonder that you want to hook up. Say we're trying to hook up the <strong>Oracle</strong> wonder, so we look in the file and find the tag for the Oracle wonder entry:</p>

<p><img src="BuildingsProcess/media/image203.png" alt="Machine generated alternative text: CROW C Row C Row C Row C Row CROW CROW C Row C Row C Row C Row C Row C Row C Row c Row — Medieval Era—— - Wonders n BUILDING AMPHITHEATER&quot; BUILDING CASTLE&quot; BUILDING AMPHITHEATER&quot; BUILDING AMPHITHEATER DESCRIPTION&quot; DRAMA POETRY&quot; Loc BUILDING CASTLE&quot; BUILDING CASTLE DESCRIPTION&quot; FORTIFICATION&quot; BUILDING uurvrnsl&#39;l%&#39;&quot; BUILDING uurvrnsl&#39;l&quot;l&#39;&quot; BUILDING uurvrnsl&#39;l%&#39; DESCRIPTION&quot; EDUCATION&quot; BUILDING WORKSHOP&quot; BUILDING WORKSHOP&quot; BUILDING WORKSHOP DESCRIPTION&quot; METALWORKING&quot; BUILDING ARMORY&quot; BUILDING ARMORY&quot; BUILDING ARMORY DESCRIPTION&quot; MACHINERY&quot; EN BUILDING SHIPYARD&quot; BUILDING SHIPYARD&quot; BUILDING SHIPYARD DESCRIPTION&quot; ASSEMBLY LINE&quot; BUILDING BANK&quot; BUILDING BANK&quot; BUILDING BANK DESCRIPTION&quot; BANKING&quot; coblERCIAL BUILDING STAR PORT&quot; BUILDING STAR PORT&quot; BUILDING STAR PORT DESCRIPTION&quot; MILITARY ENGINEERING&quot; BUILDING MUSEUM&quot; BUILDING MUSEUM&quot; BUILDING MUSEUM DESCRIPTION&quot; preregcivic—ncrv&#39;lc HUMANISM&quot; the following fields should only be used for wondersÄdjacentDistrict, AdjacentRescurce, Coast, RequiresPIacement NCTE: the follow should NOT be use BUILDING BUILDING BUILDING BUILDING BUILDING BUILDING BUILDING BUILDING BUILDING BUILDING BUILDING &quot;BUILDING BUILDING BUILDING BUILDING BUILDING BUILDING BUILDING BUILDING ALHAMBRA&quot; BUILDING ALHAMBRA&quot; BUILDING ALHAMBRA DESCRIPTION&quot; FORTIFICATION&quot; CHICHEN BUILDING CHICHEN BUILDING CHICHEN 1&#39;rzA DESCRIPTION&quot; preregcivic—ncrv&#39;lc GUILDS&quot; ME COLOSSEUM&quot; BUILDING COLOSSEUM&quot; BUILDING COLOSSEUM DESCRIPTION&quot; CONSTRUCTION&quot; COLOSSUS&quot; BUILDING COLOSSUS&quot; BUILDING COLOSSUS DESCRIPTION&quot; SHIPBUILDING&quot; FORBIDDEN cl&#39;l%&#39;&quot; BUILDING FORBIDDEN cl&#39;l&quot;l&#39;&quot; BUILDING FORBIDDEN cl&#39;l%&#39; DESCRIPTION&quot; PRINTING&quot; cost:&quot;&#39; GREAT LIBRARY&quot; BUILDING GREAT LIBRARY&quot; BUILDING GREAT LIBRARY DESCRIPTION&quot; preregcivic—ncrv&#39;lc RECORDED HISTORY&quot; GREAT LIGHTHOUSE&quot; BUILDING GREAT LIGHTHOUSE&quot; BUILDING GREAT LIGHTHOUSE DESCRIPTION&quot; CELESTIAL GREAT ZIMBA_BiE&quot; BUILDING GREAT ZIMBABV,E&quot; BUILDING GREAT ZIMBABV,E DESCRIPTION&quot; BANKING&quot; HAGIA SOPHIA&quot; BUILDING HAGIA SOPHIA&quot; BUILDING HAGIA SOPHIA DESCRIPTION&quot; EDUCATION&quot; HANGING GARDENS&quot; BUILDING HANGING GARDENS&quot; BUILDING HANGING GARDENS DESCRIPTION&quot; IRRIGATION&quot; MAHABODHI TEMPLE&quot; BUILDING MAHABODHI TEMPLE&quot; BUILDING MAHABODHI TEMPLE DESCRIPTION&quot; preregcivic—ncrv&#39;lc THEOLOGY&#39; Lac BUILDING Lac BUILDING DRAY-A &#39;240&quot; Maxi&#39;) PETRA&quot; BUILDING PETRA&quot; BUILDING PETRA DESCRIPTION&quot; MATHEMATICS&quot; cost:&quot; 240&quot; MaxWozIdInstances—&quot;: PYRAMIDS&quot; BUILDING PYRAMIDS&quot; BUILDING PYRAMIDS DESCRIPTION&quot; MASONRY&quot; STONEHENGE&quot; BUILDING STONEHENGE&quot; BUILDING STONEHENGE DESCRIPTION&quot; ASTROLOGY&quot; TAJ MAHAL&quot; BUILDING TAJ MAHAL&quot; BUILDING TAJ MAHAL DESCRIPTION&quot; preregcivic—ncrv&#39;lc HUMANISM&quot; TENOCHTITIÄN&quot; BUILDING TENOCHTITIÄN&quot; BUILDING TENOCHTITIÄN DESCRIPTION&quot; MILITARY TAcT1csn cost: TERRACOTTA ARMY&quot; BUILDING TERRACOTTA ARMY&quot; BUILDING TERRACOTTA ARMY DESCRIPTION&quot; ENGINEERING&quot; ARSENAL&quot; BUILDING ARSENAL&quot; BUILDING ARSENAL DESCRIPTION&quot; ASSEMBLY " width="1152" height="498" /></p>

<p>We specifically care about the <strong>BuildingType</strong> of the tag, which is the name that the game will be looking for when trying to figure out how to display the wonder. So in our case it's <em><strong>&quot;BUILDING_ORACLE&quot;</strong></em>.</p>


<p>3.- Adding your Wonder Movie Asset to a package:</p>

<p>Now we need to make sure that the wonder we created is added into the wonder movie .XLP file so that the game can use it. Open the Asset Editor, and open <strong>WonderMovie.xlp</strong>. In this file we need to add a new entry for your wonder movie. So in the Entries section, click the 'Add Existing' button, and select your wonder movie asset in the browser.</p>

<p><img src="BuildingsProcess/media/image204.png" alt="Machine generated alternative text: se &#39;tor - Edit View Window ma I n TER Mountain Base.mtl TER Mountain G.tex GameLighting.artdef WonderMovies.atdef Landmarks.atdef Entity Name Wonde r Movies.xlp Library_Construction movie Library_Construction movie Library Construction movie Library_Construction movie Library_Construction movie Library_Construction movie Library_Construction movie Library_Construction movie Library_Construction movie Library_Construction movie Library Construction movie Library_Construction movie Module Name Package Name XLP Class Entries Add Existing B RARY WonderMovie Wonder Movies Wonder Movie WON WON WON WON WON WON WON WON WON WON WON WON Great G reat Great G reat Great G reat Great G reat G reat G reat Great G reat BUILDING BUILDING BUILDING *BUILDING BUILDING BUILDING BUILDING BUILDING BUILDING BUILDING BUILDING ALHAMBRA CHICHEN ITZA COLOSSEUM COLOSSUS FORBIDDEN CITY GREAT LIGHTHOUSE GREAT ZIMBABWE HAGIA SOPHIA HANGING GARDENS MAHABODHI TEMPLE MONT ST MICHEL " width="807" height="427" /></p>

<p>You can change the name of the entry if you want and then save the change to the XLP file.</p>

<p>4.- Hooking up the XLP entry to the Wonder Movies ArtDef:</p>

<p>Still in the Asset Editor, you need to open <strong>WonderMovie.artdef</strong>. You need to add an entry for the wonder to the WonderMovie list, so click on WonderMovie (1) and then go to 'File &gt; Add Element' (2).</p>


<p><img src="BuildingsProcess/media/image205.png" alt="Machine generated alternative text: AssetEditor - D. Edit View Window TER Mountain Base.mtl TER Mountain Alt Definition Template WonderMovie .&#39;.,&#39;orcerMovie G. tex GameLighting.artdef AssetEditor - D: Window Ctrl Ctrl* Ctrl* Ctrl Ctrl* Edit Won View Undo Redo Copy Paste Delete y x v in G.tex GameLighting.artdef EAT LIBRARY ALHAMBRA CHICHEN ITZA COLOSSEUM COLOSSUS FORBIDDEN CITY GREAT LIGHTHOUSE GREAT ZIMBABWE HAGIA SOPHIA HANGING GARDENS MAHABOOHI TEMPLE MONT ST MICHEL ORACL POTALA PETRA STONEHENGE MAHAL TENOCHTITLAN TERRACOTTA ARMY VENETIAN ARSENAL Delete Ctrl*A aulLOI BUILDING BUILDING BUILDING BUILDING BUILDING BUILDING BUILDING BUILDING BUILDING BUILDING BUILDING BUILDING BUILDING BUILDING BUILDING BUILDING BUILDING BUILDING BUILDING BUILDING Select All Add Element Keyboard Shortcuts Load or Save Settings... Reload Project Config Preferences... MAHABOOHI TEMPLE MONT ST MICHEL ORACL POTALA PETRA STONEHENGE MAHAL TENOCHTITLAN TERRACOTTA ARMY VENETIAN ARSENAL a ILOING BUILDING BUILDING BUILDING BUILDING BUILDING BUILDING BUILDING BUILDING BUILDING BUILDING " width="645" height="489" /></p>

<p>The new entry will have a name like WonderMovie1, you need to change the name to the BuildingType that we got from step 1. In our case, the name needs to be <em><strong>BUILDING_ORACLE</strong></em>. Then Click on the arrow on the left of the entry to expand it, and select the Asset that belongs to the entry. Here we need to assign the wonder movie asset that we set up in the XLP file.</p>

<p>Save the ArtDef and you're done.</p>

<p>5.- Looking at it in the game</p>

<p>In order to see your wonder asset in the game, first it needs to be cooked. In order to cook the Asset, right-click the AssetCloud icon on your System Tray, and click on <strong>'Cook Local Assets… &gt; XLP…'</strong>. In the browser dialog, you need to select the XLP where we added the wonder movie, so select <strong>WonderMovie.xlp.</strong></p>

<p><img src="BuildingsProcess/media/image206.png" alt="Machine generated alternative text: Current Project: Cl&#39;,6 Content Tools Sync... Submit... Revet... Select Project... Use Local Tools Enable Notifications Settings... Main View... New Only Rebuild Database All Assets Cook Local Assets... 9:36 AM " width="432" height="360" /></p>

<p>Give it a few moments, and you should see a little bubble on the System Tray telling that the cooking has completed. Now you can load the game and plop down your wonder and it should play the animation</p>


</div> <!-- panel body --> 
</div> <!-- panel -->

<div class="panel panel-primary" id="ColorKey">
<div class="panel-heading">
<div class="panel-title">ColorKey
</div>
</div>
<div class="panel-body">

<p>Color Keys</p>
<p>ColorKeys are not technically Assets, they are just loose entities (specifically textures) that are used by the game directly.</p>

<p>Viewing Color Keys in Game</p>
<p>We now apply a color key to the worldview.  By default, it is turned off.  To turn it on, enter ‘colorkey’ &lt;xxx&gt; in the console, where &lt;xxx&gt; is the name of the color key you want.   To turn it back off, just type ‘colorkey’</p>
<p>To see a list of the available color key names, type ‘colorkey listnames’</p>

<p>Creating Color Keys</p>
<p>Step 0:  Capture a screenshot from the game using the console.   ‘screenshot colorkey’ or ‘screenshot colorkey noui’ </p>

<p><img src="ColorKey/media/image1.jpg" alt="C:\0F89CE25\D7DEA720-039D-4E38-9029-D41134FF7220_files\image001.jpg" width="538" height="279" /></p>

<p>This will create a screenshot with a color table embedded in it.  Open the screenshot file in photoshop.  Do whatever you want to it.  Anything that you do to the image</p>
<p>Will be reflected in the color table, as long as it is done to the entire image and not a subset of it.  Save the screenshot someplace in artdev so you can find it later.</p>

<p>Step 1:  Import the texture into the asset cloud</p>

<p>Open asset editor.   File-&gt;New.  You will be asked to pick an Entity type.  Choose texture.   Follow directions below:</p>

<ul>
<li><p>1. Select ‘ColorKey’ from the drop down</p></li>
<li><p>2. Browse to the desired file</p></li>
<li><p>3. If the file is a PSD, select the appropriate group here</p></li>
</ul>

<p><img src="ColorKey/media/image2.png" width="624" height="276" /></p>



<p>Step 2:  Add the cloud texture to the color key package</p>

<p>Open Package -&gt; ColorKeys.XLP.  (Located in &lt;YOUR_PERFORCE_ROOT&gt;/Civ6/pantry/XLPs)   Follow directions on image below to add the Colorkey to the XLP</p>


<ul>
<li><p>1. Click the ‘add existing’ button</p></li>
<li><p>2. The Entry ID is a name by which the engine will refer to the color key. By default it’s the same name as the ColorKey, but you can change it if you want.</p></li>
<li><p>3. File-&gt;Save your file and then File-&gt;Cook. Your ColorKey is now ready to use.</p></li>
</ul>
<p><img src="ColorKey/media/image3.png" width="622" height="397" /></p>

<p>Step 3:  Iterating on it</p>
<p>         Open asset editor.  File-&gt;Open.  Open the colorkey that you want to change.    File-&gt;Reimport will reimport the texture from the original source file (assuming it can find it).  If the source file is checked into perforce under artdev, other people will be able to reimport it if they have synced.    If you have both the Colorkey texture and XLP open, the tools will do an automatic re-cook when a color key is re-imported.  If you also have the game open, it will hotload.    If any of the above do not occur, please let the tools team know.</p>

<p>Step 4: At this point The color key can now be called up by artdefs. Currently the ScreenWashEffects, and the GameLighting artdefs can take colorkeys to be used in the game.</p>
</div> <!-- panel body --> 
</div> <!-- panel -->

<div class="panel panel-primary" id="DataDocumentation">
<div class="panel-heading">
<div class="panel-title">DataDocumentation
</div>
</div>
<div class="panel-body">

<p><span id="1" class="anchor"></span></p>
<p>Data documentation</p>
<p>Madrid</p>
<p>Exported on Feb 08, 2019</p>
<p><span id="scroll-bookmark-1" class="anchor"></span>Modders (and your co-workers) need help understanding how our data works. Please go through the following list and write something about each class you know something about.<br />
Keep in mind these docs should be targetting someone who doesn’t know our tech. For assets and art entities its good to know what other entities they are used with and how ArtDefs refer to them.<br />
For ArtDefs and XLPs it’s nice to know what systems use them and how.</p>
<p>We are trying to put enough detail in these docs so the modders can answer questions like, if I want to add a building what data do I need to modify?</p>
<h1 id="assets">Assets</h1>
<table>
<thead>
<tr class="header">
<th>Asset Class</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>CityBlock</td>
<td>Placed around cities and districts in the form of procedural filler. Considered to be a &quot;Landmark&quot;. For process, consult Buildings Process.</td>
</tr>
<tr class="even">
<td>Landmark</td>
<td>Used to be used by everything, now only used by DynamicGeometry for splined geometry and towers.</td>
</tr>
<tr class="odd">
<td>Leader</td>
<td></td>
</tr>
<tr class="even">
<td>RouteDoodad</td>
<td>Placed along roads according to certain rules, currently only supports bridges. Considered to be a &quot;Landmark&quot;.</td>
</tr>
<tr class="odd">
<td>StrategicView_DirectedAsset<span id="scroll-bookmark-3" class="anchor"></span></td>
<td>Represents StrategicView assets that are placed along a tile (hex) edge and therefore need 12 permutations (6 edges of a tile times two fog-of-war states, visible and revealed). The permutations are cook parameters (<a href="#scroll-bookmark-4">StrategicView_Sprite</a> textures) and are named following compass directions, i.e. North-East Revealed, North-East Visible, East Revealed, East Visible, South-East Revealed, etc.) Examples used in game are bridges and cliffs. The <a href="#scroll-bookmark-5">StrategicVIew.artdef</a>'s TerrainBlends, Features, and Improvements collections reference directed asset XLP entries.</td>
</tr>
<tr class="even">
<td>StrategicView_Route<span id="scroll-bookmark-6" class="anchor"></span></td>
<td><p>Represents StrategicView roads, which connect the middle points of each tile (hex) edge. Because the roads can be mirrored and in most cases pass through the tile center, only 8 permutations (4 road segments times two fog-of-war states, visible and revealed) are required. The four road segments are:</p>
<ul>
<li>
<p>north-west to north-east tile edge,</p>
</li>
<li>
<p>north-east to east tile edge,</p>
</li>
<li>
<p>north-west tile edge to tile center, and</p>
</li>
<li>
<p>west tile edge to tile center.</p>
</li>
</ul>
<p>Examples used in game are roads. The <a href="#scroll-bookmark-5">StrategicVIew.artdef</a>'s Routes collection references route XLP entries.</p></td>
</tr>
<tr class="odd">
<td>StrategicView_TerrainBlend<span id="scroll-bookmark-7" class="anchor"></span></td>
<td>Represents a StrategicView terrain blend containing 70 cook parameters that can be filled with 17, 31 or 70 textures representing the different terrain blend categories (see <a href="https://hub.take2games.com/display/FXSMadrid/Terrain+Overview">StrategicView Terrain Overview</a> and the <strong>Base game's Art OneNote's StrategicView → Generating Terrain Blends section</strong>). The <a href="#scroll-bookmark-5">StrategicVIew.artdef</a>'s TerrainBlends collection references terrain blend XLP entries.</td>
</tr>
<tr class="even">
<td>StrategicView_TerrainBlendCorners<span id="scroll-bookmark-8" class="anchor"></span></td>
<td>Represents the shared terrain blend corners containing 4 cook parameters ((see <a href="https://hub.take2games.com/display/FXSMadrid/Terrain+Overview">StrategicView Terrain Overview</a> and the <strong>Base game's Art OneNote's StrategicView → Generating Terrain Blends section</strong>). The <a href="#scroll-bookmark-5">StrategicVIew.artdef</a>'s TerrainBlendCorners collection references terrain blend corner XLP entries. It is unlikely that you should need to create or modify any terrain blend corner assets.</td>
</tr>
<tr class="odd">
<td>TerrainElementAsset</td>
<td>Assets that represent</td>
</tr>
<tr class="even">
<td>TileBase</td>
<td>Placed as districts, buildings, improvements, etc. Can be attached to other TileBase assets. Considered to be a &quot;Landmark&quot;. For process, consult Buildings Process.</td>
</tr>
<tr class="odd">
<td>UILensAsset</td>
<td>Describes which lens layers to turn on/off for a given &quot;lens&quot;.</td>
</tr>
<tr class="even">
<td>Unit</td>
<td></td>
</tr>
<tr class="odd">
<td>VFX</td>
<td>Represents assets that are managed by the visual effect system or that can be spawned by the particle effect system. It is not required that a VFX asset have a dsg, geometry, animations, or particle efffects.</td>
</tr>
<tr class="even">
<td>WonderMovie</td>
<td><p>Represents assets that are used to represent world wonders in the game. These assets usually have WonderMovie geometry class and camera information from the WonderMovieCamera geometry class. Typically, the camera and base geometry come from the same 3DS Max file, but are in different hierarchies. Geometry from the DecalGeometry asset class may also be added to this asset as well. DecalGeometry added directly to the WonderMovie asset will always be visible when the asset is placed down in game. Additionally, attachment geometry (from the TileBase asset class) can be added to the WonderMovie asset. The attachment geometry (as well as any decals associated with it) will only be visible if the attachment point geometry associated with the attachment point is visible (as defined by the WonderMovie asset state) and the attachment point itself is visible (as defined by the reveal animation visibility). Also note that attachments with a connection type of ROAD will be added as connections points immediately when the asset is placed in game (regardless of the visibility of the attachment point that it is associated with).</p>
<p>Note that wonder movie assets do not require an animation or camera animation in order to be placeable in game; however, at least a base geometry is require in order to be functional.</p>
<p>Visual Progress Change During Construction - While the wonder is being built, the amount of build progress that it has achieved is normalized and used to sample the visibility track associated with its reveal animation in order to determine what geometry should be displayed. In addition, the visibility associated with attachment point bones is used to only show visual effects on attachment points associated with visible bones. This attachment point visibility information is important because it allows the construction animation to loop and cull out the calling of visual effects on invisible bones.</p>
<p>The following information can be used to determine the state that the wonder asset will be in when it is placed down in game:</p>
<ul>
<li>
<p>Before the wonder reveal:</p>

<ul>
<li>
<p>Asset State: UNWORKED (same for TileBase and all DecalGeometry)</p>
</li>
<li>
<p>DSG State: ANY → CONSTRUCTION (TileBase: ANY → UNWORKED)</p>
</li>
</ul></li>
<li>
<p>During the wonder reveal:</p>

<ul>
<li>
<p>Asset State: UNWORKED (same for TileBase and all DecalGeometry)</p>
</li>
<li>
<p>DSG State: ANY → REVEAL (TileBase: ANY → CONSTRUCTION)</p>
</li>
</ul></li>
<li>
<p>After the wonder reveal:</p>

<ul>
<li>
<p>Asset State: WORKED (same for TileBase and all DecalGeometry)</p>
</li>
<li>
<p>DSG State: ANY → WORKED (TileBase: ANY → WORKED)</p>
</li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>
<h1 id="materials">Materials</h1>
<table>
<thead>
<tr class="header">
<th>Material Class</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>BurnMaterial</td>
<td><p>The Burn material causes an existing material to appear burnt. It contains a set of textures to override the material textures in burnt regions, and a set of parameters which control the procedural noise which is used to blend between the burnt and non-burnt materials. Any asset with a burn material will have the procedural burn effect applied.</p>
<p>The procedural burn effect also depends on a number of asset-level parameters, which are specified as cook parameters for CityBlock and Landmark assets. These parameters are:</p>
<ul>
<li>
<p>GradientScale: Controls the speed at which the burn effect blends in. Higher scales result in sharper transitions from burnt to unburnt.</p>
</li>
<li>
<p>BurnEdgeBlend:</p>
</li>
<li>
<p>BurnHeight: Controls the height from the base of the asset at which the burn effect starts blending in</p>
</li>
</ul></td>
</tr>
<tr class="even">
<td>DecalMaterial</td>
<td>Material used for decals placed on the terrain.</td>
</tr>
<tr class="odd">
<td>FOWLineDrawing</td>
<td><p>This material controls the types of FOW strokes which will be drawn for the mesh edges on the geometry. The FOW material can be used to disable wing strokes, fin strokes, or both. The default FOWLineDrawing material draws both stroke types. A common usage of the FOW material is to disable FOW strokes on alpha-tested geometry such as wheat. This is necessary to prevent the outlines of the base geometry from being drawn.</p>
<p>You can also prevent geometry from appearing in FOW by omitting the material. If the material is null, then the geometry is completely invisible in FOW.</p>
<p>For more information, see the documentation for the 'LandmarkModel' geometry class.</p></td>
</tr>
<tr class="even">
<td>Landmark</td>
<td>Material used for all assets considered to be 'Landmarks'.</td>
</tr>
<tr class="odd">
<td>Leader</td>
<td></td>
</tr>
<tr class="even">
<td>Leader_Cloth</td>
<td></td>
</tr>
<tr class="odd">
<td>Leader_Glass</td>
<td></td>
</tr>
<tr class="even">
<td>Leader_Hair</td>
<td></td>
</tr>
<tr class="odd">
<td>Leader_Matte</td>
<td></td>
</tr>
<tr class="even">
<td>Leader_Skin</td>
<td></td>
</tr>
<tr class="odd">
<td>RiverWater</td>
<td>Simplified variation of the water material which is used on rivers.</td>
</tr>
<tr class="even">
<td>SnowMaterial</td>
<td>The snow material is a placeholder. If a snow material is assigned to a triangle group, it will have the procedural snow effect. Otherwise, it will not. The settings from the procedural snow shader, if present, are specified at the asset level.</td>
</tr>
<tr class="odd">
<td>TerrainElement</td>
<td>A local hand-built region of terrain that is blended into the procedural terrain.</td>
</tr>
<tr class="even">
<td>TerrainMaterial</td>
<td>Terrain material used by either TerrainElement or procedural terrain layer.</td>
</tr>
<tr class="odd">
<td>UILensMaterial</td>
<td>Simple material used on UI lens model assets, such as the movement ring.</td>
</tr>
<tr class="even">
<td>Unit</td>
<td></td>
</tr>
<tr class="odd">
<td>VFXModel</td>
<td>Represents the more basic version of the material used for VFX related content.</td>
</tr>
<tr class="even">
<td>VFXModel_FX</td>
<td>Represents the more advanced version of the material used for VFX related content. This material contains additional features such as multiple texture layers, uv scrolling, and alpha mode selection.</td>
</tr>
<tr class="odd">
<td>Water</td>
<td>Material controls for water materials used by oceans, shallows, lakes, and natural wonders.</td>
</tr>
<tr class="even">
<td>WaveMaterial</td>
<td>Material which specifies a texture atlas for coastal waves. The wave atlas is treated as a greyscale image. Only the Red channel is used.</td>
</tr>
</tbody>
</table>
<h1 id="geometry">Geometry</h1>
<table>
<thead>
<tr class="header">
<th>Geometry Class</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>DecalGeometry</td>
<td>Represents the class of geometry that can be used for terrain decals.</td>
</tr>
<tr class="even">
<td>LandmarkModel</td>
<td><p>Represents the class of geometry used for buildings, clutter, city blocks, and other such elements. The LandmarkModel geometry class may be visible in FOW. Landmark models in FOW will render with their BaseColor map, mixed in with a parchment texture. They will also render 'strokes' on mesh edges.</p>
<p>There are two types of FOW strokes:</p>
<ul>
<li>
<p>Wing Strokes: The purpose of a wing stroke is to highlight important features on a model, such as sharp corners and roof lines. Wing strokes are generated in the following circumstances:</p>

<ul>
<li>
<p>On edges in which connect to only one triangle</p>
</li>
<li>
<p>On edges which connect to 3 or more triangles (&quot;pin-wheels&quot;)</p>
</li>
<li>
<p>On edges with two triangles, where the angle between triangles exceeds a given threshold.</p>
</li>
</ul></li>
</ul>
<ul>
<li>
<p>Fin Strokes: Fin strokes are generated for every edge in the mesh which connects two triangles. The purpose of the fin stroke is to highlight the silhouettes of the model. Fin strokes are not rendered unless the edge is a silhouette, meaning that one triangle is back-facing and the other front facing.</p>
</li>
</ul>
<p>The FOWLineDrawing material controls the types of strokes which are rendered (wings or fins), while the geometry class defines parameters which control stroke placement:</p>
<ul>
<li>
<p>FOWForceThreshold: FOW strokes are &quot;forced&quot; (always drawn) on edges where the angle between the incident faces is larger than this value</p>
</li>
<li>
<p>FOWFlatThreshold: FOW strokes are never drawn on edges where the angle between the incident faces is less than or equal to this value. This test is used to prevent spurious edges from appearing between co-planar polygons.</p>
</li>
</ul></td>
</tr>
<tr class="odd">
<td>LandmarkObstructionProfile</td>
<td>Indicates an area, usually on a TileBase asset, that cannot be occupied by other assets. Must be XY planar, the Z coordinate of every vertex must be the same.</td>
</tr>
<tr class="even">
<td>Leader_ShadowVolume</td>
<td></td>
</tr>
<tr class="odd">
<td>UILensModel</td>
<td></td>
</tr>
<tr class="even">
<td>Unit</td>
<td></td>
</tr>
<tr class="odd">
<td>VFXModel</td>
<td>Represents the class of geometry that can be added to VFX related content. In the game and AssetEditor, when VFX assets are placed they will be placed in the Default asset state.</td>
</tr>
<tr class="even">
<td>WonderMovieCamera</td>
<td>Represents the class of geometry that can be used to represent a camera for wonder related content.</td>
</tr>
<tr class="odd">
<td>WonderMovieModel</td>
<td><p>Represents the class of geometry that can be used to represent the base skeleton/mesh for wonder related content.</p>
<p>Additional Export Information - Be sure that objects with visibility information are uniquely named; otherwise, the system will not be able to properly acquire the visibility information. Also, in order to export visibility for bones in 3DS Max, you will need to create a mesh with visibility and then set the “Export as Bone” option on those meshes within the Model Manager.</p></td>
</tr>
</tbody>
</table>
<h1 id="animation">Animation</h1>
<table>
<thead>
<tr class="header">
<th>Animation Class</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Landmark</td>
<td>Class of animations that can be added to any asset considered to be a 'Landmark'.</td>
</tr>
<tr class="even">
<td>Leader</td>
<td></td>
</tr>
<tr class="odd">
<td>Unit</td>
<td></td>
</tr>
<tr class="even">
<td>VFX</td>
<td>Represents the class of animation that can be added to VFX related content.</td>
</tr>
<tr class="odd">
<td>WonderMovie</td>
<td>Represents the class of animation that can be added to wonder related content.</td>
</tr>
</tbody>
</table>
<h1 id="dsg">DSG</h1>
<table>
<thead>
<tr class="header">
<th>DSG Class</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Clutter</td>
<td></td>
</tr>
<tr class="even">
<td>Landmark</td>
<td>Class of state graph that can be used with any asset considered to be a 'Landmark'.</td>
</tr>
<tr class="odd">
<td>LeaderDSG</td>
<td></td>
</tr>
<tr class="even">
<td>TerrainElementAsset</td>
<td>Class of state graph that can be used with any asset considered to be a 'TerrainElementAsset'</td>
</tr>
<tr class="odd">
<td>Unit</td>
<td></td>
</tr>
<tr class="even">
<td>VFX</td>
<td>Represents the class of state graph that can be added to VFX related context. In the game and AssetEditor, when VFX assets are placed they will have the ANY to IDLE state graph transition applied.</td>
</tr>
<tr class="odd">
<td>WonderMovie</td>
<td>Represents the class of state graph that can be added to wonder related content.</td>
</tr>
</tbody>
</table>
<h1 id="texture">Texture</h1>
<table>
<thead>
<tr class="header">
<th>Texture Class</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>ColorKey</td>
<td>ColorKey textures are used to implement tabulated color correction. To generate a colorkey, you must first take a special screenshot using the in-game debug console. Open the console and type 'screenshot colorkey'. This will generate an image file in your screenshots directory containing a game screenshot and an embedded color table. You can then color-correct the resulting image, and import it using the asset editor. The asset cooker will extract the color table from the imported image and discard the rest.</td>
</tr>
<tr class="even">
<td>Decal_BaseColor</td>
<td>This texture class defines decal material base color. The base color is used to scale diffuse lighting. It is an sRGB color image with alpha.</td>
</tr>
<tr class="odd">
<td>Decal_FOWColor</td>
<td>This texture class defines decal material FOW color. When the terrain is in FOW this texture is used to directly set the color for the terrain with no lighting. It is an sRGB color image with alpha.</td>
</tr>
<tr class="even">
<td>Decal_Heightmap</td>
<td>This texture class defines decal material detail height data to blend into the terrain before the normal map is generated. It is a linear texture where the red channel is the height and the alpha channel is the blend.</td>
</tr>
<tr class="odd">
<td>Decal_Spec</td>
<td>This texture class defines decal material gloss. White pixels are shiny, black pixels are dull. This is a linear value which encodes GGX roughness. The Civ6 engine uses a GGX approximation based on a pair of Beckman lobes which are filtered using CLEAN mapping to avoid specular loss in the exceedingly common case of minified textures. The specular results should appear similar to GGX but may not produce a 1 to 1 match.</td>
</tr>
<tr class="even">
<td>FOW</td>
<td>This texture class is used for FOW parchment and hatch textures.</td>
</tr>
<tr class="odd">
<td>FOWGreyscale</td>
<td>A greyscale FOW texture with only one color channel. This may also be used for parchment and hatch textures.</td>
</tr>
<tr class="even">
<td>FOWSprite</td>
<td>This texture class is used for FOW sprites.</td>
</tr>
<tr class="odd">
<td>Generic_AO</td>
<td>This texture class is used for AO textures. It is a greyscale image interpreted as a linear value by the shader.</td>
</tr>
<tr class="even">
<td>Generic_BaseColor</td>
<td>This texture class is used for base color. The base color is used to scale diffuse lighting. On metal surfaces, diffuse lighting is disabled, and the base color scales specular lighting instead. The basecolor map is an sRGB color image.</td>
</tr>
<tr class="odd">
<td>Generic_BurnMap</td>
<td>This texture class defines an alternate base color map which is blended with the base color for the procedural burn effect. It is an sRGB color image which is blended with the base color after conversion to linear color space.</td>
</tr>
<tr class="even">
<td>Generic_Emissive</td>
<td>This texture class is used for emissive surfaces like lit windows. It is an sRGB color image. The emissive color is added verbatim to the shading result AFTER conversion into linear color space.</td>
</tr>
<tr class="odd">
<td>Generic_Gloss</td>
<td>This texture class is used for gloss. White pixels are shiny, black pixels are dull. This is a linear value which encodes GGX roughness. The Civ6 engine uses a GGX approximation based on a pair of Beckman lobes which are filtered using CLEAN mapping to avoid specular loss in the exceedingly common case of minified textures. The specular results should appear similar to GGX but may not produce a 1 to 1 match.</td>
</tr>
<tr class="even">
<td>Generic_LightMap</td>
<td>This texture class is used for pre-computed global illumination, which is supported for building textures. It is an sRGB color image which is modulated by base color after conversion to linear space.</td>
</tr>
<tr class="odd">
<td>Generic_Metalness</td>
<td>This texture class is used to mark areas of the surface as being metallic. It is a greyscale image which is interpreted as a linear value by the shader.</td>
</tr>
<tr class="even">
<td>Generic_Normal</td>
<td>This is a normal map. It will be post-processed by the asset cooker to produce a CLEAN map.</td>
</tr>
<tr class="odd">
<td>Generic_OPAC</td>
<td>This is an opacity map. It is a greyscale image interpretted as a linear value by the shader. Civ6 uses screendoor transparency based on MSAA coverage mask export, so the number of available opacity levels is proportional to the MSAA level which the user has selected in the graphics options. In the limit case, when MSAA is disabled, this technique degrades to classical alpha testing. Therefore, high contrast maps with blended edges are the most effective. Mid-tones and subtle patterns will generally not resolve well.</td>
</tr>
<tr class="even">
<td>Generic_TintMask</td>
<td>This texture class is used to blend between the base color and a &quot;tint color&quot;, which is defined externally to the asset. It is a greyscale image which is interpreted as a linear value by the shader. The unit material also supports a translucency mode, which allows for effects such as back lighting and subsurface scattering on sails and such like. In translucency mode, the tint mask is re-purposed as a translucency mask.</td>
</tr>
<tr class="odd">
<td>Leader_Anisotropy</td>
<td></td>
</tr>
<tr class="even">
<td>Leader_AO</td>
<td></td>
</tr>
<tr class="odd">
<td>Leader_BaseColor</td>
<td></td>
</tr>
<tr class="even">
<td>Leader_BlurWidth</td>
<td></td>
</tr>
<tr class="odd">
<td>Leader_Fallback</td>
<td></td>
</tr>
<tr class="even">
<td>Leader_FilmGrain</td>
<td></td>
</tr>
<tr class="odd">
<td>Leader_Fuzz</td>
<td></td>
</tr>
<tr class="even">
<td>Leader_Gloss</td>
<td></td>
</tr>
<tr class="odd">
<td>Leader_Metalness</td>
<td></td>
</tr>
<tr class="even">
<td>Leader_Normal</td>
<td></td>
</tr>
<tr class="odd">
<td>Leader_OPAC</td>
<td></td>
</tr>
<tr class="even">
<td>Leader_Tangent</td>
<td></td>
</tr>
<tr class="odd">
<td>Leader_Tint</td>
<td></td>
</tr>
<tr class="even">
<td>Leader_Translucency</td>
<td></td>
</tr>
<tr class="odd">
<td>Overlay</td>
<td>Textures used by the culture borders, movement lenses, reticules, and various other in-game overlays.</td>
</tr>
<tr class="even">
<td>SkyboxTexture2D</td>
<td>Textures used as &quot;skyboxes&quot;. This is the background texture which is visible through the top and bottom of the world map. Textures of this type are cooked into the 'SkyboxTexture' XLP.</td>
</tr>
<tr class="odd">
<td>StrategicView_CultureBorder<span id="scroll-bookmark-14" class="anchor"></span></td>
<td>A 2D, 256x256, RGBA8 texture representing the culture-border mask used in <a href="#scroll-bookmark-7">StrategicView_TerrainBlend</a> assets.</td>
</tr>
<tr class="even">
<td>StrategicView_Riverbank<span id="scroll-bookmark-15" class="anchor"></span></td>
<td>A 2D, 256x256, RGBA8 texture representing the riverbank and coastline mask used in <a href="#scroll-bookmark-7">StrategicView_TerrainBlend</a> assets.</td>
</tr>
<tr class="odd">
<td>StrategicView_Sprite<span id="scroll-bookmark-4" class="anchor"></span></td>
<td>A 2D, RGBA8 texture of variable size (4x4 - 4096x4096) representing any sprites (features, improvements, buildings, etc.) used in the StrategicView. Mostly referenced through <a href="#scroll-bookmark-16">StrategicView_Sprite</a> XLP entries in <a href="#scroll-bookmark-5">StrategicVIew.artdef</a>'s various collections. See the <strong>Base game's Art OneNote's StrategicView → How to Get Art into the Strategic View → &quot;Photoshop File Organization for Sprites and Terrain Types&quot; and &quot;Importing New Sprites and Terrain Types into the Asset Cloud&quot; sections</strong>.</td>
</tr>
<tr class="even">
<td>StrategicView_TerrainBlend<span id="scroll-bookmark-17" class="anchor"></span></td>
<td>A 2D, 256x256, RGBA8 texture representing the terrain blend mask used in <a href="#scroll-bookmark-7">StrategicView_TerrainBlend</a> assets.</td>
</tr>
<tr class="odd">
<td>StrategicView_TerrainType<span id="scroll-bookmark-18" class="anchor"></span></td>
<td>A 2D, RGBA8 texture of variable size (4x4 - 4096x4096) representing the terrain type (grass, plains, snow, etc.). Mostly referenced through <a href="#scroll-bookmark-19">StrategicView_TerrainType</a> XLP entries in <a href="#scroll-bookmark-5">StrategicVIew.artdef</a>'s TerrainType collection.</td>
</tr>
<tr class="even">
<td>Terrain_BaseColor</td>
<td>This texture class defines terrain material base color. The base color is used to scale diffuse lighting. It is an sRGB color image.</td>
</tr>
<tr class="odd">
<td>Terrain_FOWColor</td>
<td>This texture class defines terrain material FOW color. When the terrain is in FOW this texture is used to directly set the color for the terrain with no lighting. It is an sRGB color image.</td>
</tr>
<tr class="even">
<td>Terrain_Fuzz</td>
<td></td>
</tr>
<tr class="odd">
<td>Terrain_Heightmap</td>
<td>This texture class defines terrain material detail height data used to generate the normal map. It is a linear texture where the red channel is the height and black is lower, white is higher.</td>
</tr>
<tr class="even">
<td>Terrain_Spec</td>
<td>This texture class defines terrain material gloss. White pixels are shiny, black pixels are dull. This is a linear value which encodes GGX roughness. The Civ6 engine uses a GGX approximation based on a pair of Beckman lobes which are filtered using CLEAN mapping to avoid specular loss in the exceedingly common case of minified textures. The specular results should appear similar to GGX but may not produce a 1 to 1 match.</td>
</tr>
<tr class="odd">
<td>TerrainElementBlendmap</td>
<td>This texture class defines a blendmap used to drive blending of a TerrainElementHeightmap.</td>
</tr>
<tr class="even">
<td>TerrainElementHeightmap</td>
<td>This texture class defines a heightmap used to define the height of the terrain geometry.</td>
</tr>
<tr class="odd">
<td>TerrainElementIDMap</td>
<td>This texture class defines which terrain materials should be drawn in a specific region of terrain. It is a linear texture with alpha, where the alpha channel is used to identify the material to use for each pixel. The alpha channel must be set to a valid AlphaIdentifier (see TerrainMaterial) or 0 to leave the existing material.</td>
</tr>
<tr class="even">
<td>TerrainElementNoise2D</td>
<td>This texture class defines a noise texture used in some of the procedurally generated terrain passes. It is a linear texture with noise in the red and green channels.</td>
</tr>
<tr class="odd">
<td>UserInterface<span id="scroll-bookmark-20" class="anchor"></span></td>
<td><p>UI Textures can be encoded in two different ways:</p>
<ul>
<li>
<p>Scalable: the texture is stored in an atlas, using the TexturePadding and IsStandalone parameters to control how it is fit in with other textures. This format is ideal for textures that need to rotate or scale higher than double their original resolution.</p>
</li>
<li>
<p>Compressed: the texture is block compressed, dramatically reducing the memory footprint, especially on textures with large regions of a repeating pattern. This format can only do point and bilinear filtering, so textures that need to rotate/scale large amounts should be marked as scalable.</p>
</li>
</ul></td>
</tr>
<tr class="even">
<td>VFXParticle_BaseColor</td>
<td>Color map for VFX texture assets.</td>
</tr>
<tr class="odd">
<td>VFXParticle_Mask</td>
<td>Greyscale map used by the VFXModel_FX material for layer masking.</td>
</tr>
<tr class="even">
<td>VFXParticle_Ramp</td>
<td>Color ramp used by the VFXModel_FX material for blending color over lifetime. This is a 1D texture, only the top row of pixels is used.</td>
</tr>
<tr class="odd">
<td>Water_Color</td>
<td>THIS TEXTURE CLASS IS NO LONGER USED. IT IS DECLARED IN THE PROJECT CONFIG BUT NEVER REFERENCED. DELETE IT!</td>
</tr>
<tr class="even">
<td>WaterDensityMap</td>
<td><p>This map controls how quickly light is absorbed or attenuated at different water depths. It is a one-dimensional texture, only the top row of pixels will be used. Left is at the water surface, right as at the depth specified by the &quot;DensityMapRange&quot; parameter (depths lower than this are clamped). You should set the DensityMapRange based on the degree of fine control you need/want for a particular water type.</p>
<p>High density values will make objects look like the inverted color. This means that a solid blue map will cause the underwater objects to appear yellow, because no blue light is reaching them. The further underwater they are, the yellower they will appear. The color channels are multiplied by the alpha channel to give the actual value of the density map. Color can be used to controle hue, and alpha intensity</p></td>
</tr>
</tbody>
</table>
<h1 id="behaviors">Behaviors</h1>
<table>
<thead>
<tr class="header">
<th>Behavior Class</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Unit</td>
<td></td>
</tr>
</tbody>
</table>
<h1 id="particle-effects">Particle Effects</h1>
<table>
<thead>
<tr class="header">
<th>Particle Class</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>FireFXParticle</td>
<td>This class is for particles using the new FireFX scripting system. For documentation on understanding the scripting language go <a href="https://hub.take2games.com/display/FXSMadrid/Understanding+FireFX+Scripts">here</a></td>
</tr>
<tr class="even">
<td>VFXParticle</td>
<td>Represents a class of particle effect that can be added to VFX related content.</td>
</tr>
</tbody>
</table>
<h1 id="lights-analytic">Lights (ANALYTIC)</h1>
<table>
<thead>
<tr class="header">
<th>Light (ANALYTIC) Class</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Generic_PointLight</td>
<td>Represents a class of a point light. This class exposes various properties that allow users to define the way that a light affects the scene and surrounding objects.</td>
</tr>
<tr class="even">
<td>Generic_SpotLight</td>
<td></td>
</tr>
</tbody>
</table>
<h1 id="lights-environment">Lights (ENVIRONMENT)</h1>
<table>
<thead>
<tr class="header">
<th>Light (ENV) Class</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>GameEnvironment</td>
<td>Game environment lights are referenced by 'GameEnvironment' light rigs.</td>
</tr>
<tr class="even">
<td>LeaderEnvironment</td>
<td></td>
</tr>
</tbody>
</table>
<h1 id="light-rigs">Light Rigs</h1>
<table>
<thead>
<tr class="header">
<th>Light Rig Class</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>GameEnvironment</td>
<td>'GameEnvironment' light rigs are referenced by the time of day art def. The time of day system defines a blend between different environment lights over time.</td>
</tr>
<tr class="even">
<td>LeaderEnvironment</td>
<td></td>
</tr>
</tbody>
</table>
<h1 id="xlp">XLP</h1>
<table>
<thead>
<tr class="header">
<th>XLP Class</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>CameraAnimation</td>
<td></td>
</tr>
<tr class="even">
<td>CityBuildings</td>
<td>Contains CityBlock assets.</td>
</tr>
<tr class="odd">
<td>ColorKey</td>
<td>This package contains all of the cooked color keys, which are available for color correction.</td>
</tr>
<tr class="even">
<td>DynamicGeometry</td>
<td>Contains Landmark Assets used by Dynamic Geometry system.</td>
</tr>
<tr class="odd">
<td>FireFX</td>
<td></td>
</tr>
<tr class="even">
<td>FOWSprite</td>
<td>Contains FOW sprite textures.</td>
</tr>
<tr class="odd">
<td>FOWTexture</td>
<td>Contains global FOW textures such as hatch patterns and parchments.</td>
</tr>
<tr class="even">
<td>GameLighting</td>
<td>Contains cooked game environment light rights.</td>
</tr>
<tr class="odd">
<td>Landmark</td>
<td>Contains Landmark Assets used by nobody in particular.</td>
</tr>
<tr class="even">
<td>Leader</td>
<td></td>
</tr>
<tr class="odd">
<td>LeaderFallback</td>
<td></td>
</tr>
<tr class="even">
<td>LeaderLighting</td>
<td></td>
</tr>
<tr class="odd">
<td>Light</td>
<td>References assets created with the Light asset class. It is expected that the entry name and entry value fields will be the same name. This is necessary in order for the Light assets to be correctly referenced by other assets through Light triggers. The LT_Warning asset is the warning asset for Lights (looks a cyan spot light). The LT_Warning asset will appear in game (in non-Final Release builds) when a Light trigger is fired on an asset, but there is no Light asset in an cooked xlp with a name that corresponds to the Light triggers asset name.</td>
</tr>
<tr class="even">
<td>OverlayTexture</td>
<td>This package contains cooked overlay textures which are used by various in-game UI elements.</td>
</tr>
<tr class="odd">
<td>RouteDecalMaterial</td>
<td>Contains decal materials used by procedural routes.</td>
</tr>
<tr class="even">
<td>RouteDoodad</td>
<td>Contains RouteDoodad assets used by procedural routes.</td>
</tr>
<tr class="odd">
<td>SkyBoxTexture</td>
<td>This package contains cooked skybox textures which may be used as background images.</td>
</tr>
<tr class="even">
<td>StrategicView_DirectedAsset<span id="scroll-bookmark-27" class="anchor"></span></td>
<td>References all <a href="#scroll-bookmark-3">StrategicView_DirectedAssets</a> that are used by the game. This includes bridges and cliffs. The TerrainBlends, Features, and Improvements collections in <a href="#scroll-bookmark-5">StrategicView.artdef</a> reference directed assets XLP entries in addition to the default sprite texture XLP entries.</td>
</tr>
<tr class="odd">
<td>StrategicView_Route<span id="scroll-bookmark-28" class="anchor"></span></td>
<td>References all <a href="#scroll-bookmark-6">StrategicView_Route</a> assets that are used by the game. The Routes collection in <a href="#scroll-bookmark-5">StrategicView.artdef</a> references route XLP entries.</td>
</tr>
<tr class="even">
<td>StrategicView_Sprite<span id="scroll-bookmark-16" class="anchor"></span></td>
<td>References <a href="#scroll-bookmark-4">StrategicView_Sprite</a> textures that are used by the game. There are several BLPs using this class, e.g. StrategicView_Features, StrategicView_Districts, etc. Most collections in <a href="#scroll-bookmark-5">StrategicView.artdef</a> reference sprite XLP entries. See the <strong>Base game's Art OneNote's StrategicView → How to Get Art into the Strategic View → &quot;Photoshop File Organization for Sprites and Terrain Types&quot; and &quot;Importing New Sprites and Terrain Types into the Asset Cloud&quot; sections</strong>.</td>
</tr>
<tr class="odd">
<td>StrategicView_TerrainBlend<span id="scroll-bookmark-29" class="anchor"></span></td>
<td>References <a href="#scroll-bookmark-7">StrategicView_TerrainBlend</a> assets that are used by the game. The TerrainBlends collection in <a href="#scroll-bookmark-5">StrategicView.artdef</a> references terrain blend XLP entries.</td>
</tr>
<tr class="even">
<td>StrategicView_TerrainBlendCorners<span id="scroll-bookmark-30" class="anchor"></span></td>
<td>References <a href="#scroll-bookmark-8">StrategicView_TerrainBlendCorners</a> assets that used used by the game. The TerrainBlendCorners collection in <a href="#scroll-bookmark-5">StrategicView.artdef</a> references terrain blend corners XLP entries.</td>
</tr>
<tr class="odd">
<td>StrategicView_TerrainType<span id="scroll-bookmark-19" class="anchor"></span></td>
<td>References <a href="#scroll-bookmark-18">StrategicView_TerrainType</a> textures that are used by the game. The TerrainTypes collection in <a href="#scroll-bookmark-5">StrategicView.artdef</a> references terrain type XLP entries.</td>
</tr>
<tr class="even">
<td>TerrainAsset</td>
<td></td>
</tr>
<tr class="odd">
<td>TerrainElement</td>
<td></td>
</tr>
<tr class="even">
<td>TerrainMaterial</td>
<td></td>
</tr>
<tr class="odd">
<td>TileBase</td>
<td>Contains TileBase assets.</td>
</tr>
<tr class="even">
<td>UILensAsset</td>
<td></td>
</tr>
<tr class="odd">
<td>UITexture</td>
<td>This package type contains references to <a href="#scroll-bookmark-20">UserInterface</a> textures used by the game's UI</td>
</tr>
<tr class="even">
<td>Unit</td>
<td></td>
</tr>
<tr class="odd">
<td>VFX</td>
<td>References assets created with the VFX asset class. It is expected that the entry name and entry value fields will be the same name. This is necessary in order for the VFX assets to be correctly referenced by other assets through VFX Asset triggers. The FX_Warning asset is the warning asset for VFX (looks like a fountain of yellow yield sign icons). The FX_Warning asset will appear in game (in non-Final Release builds) when a VFX Asset trigger is fired on an asset, but there is no VFX asset in any cooked xlp with a name that corresponds to the VFX Asset triggers asset name.</td>
</tr>
<tr class="even">
<td>Water</td>
<td>Contains cooked water materials which are referenced by art definitions.</td>
</tr>
<tr class="odd">
<td>Wave</td>
<td>Contains cooked wave materials which are referenced by art definitions.</td>
</tr>
<tr class="even">
<td>WonderMovie</td>
<td>References assets created with the WonderMovie asset class.</td>
</tr>
</tbody>
</table>
<h1 id="artdefs">ArtDefs</h1>
<table>
<thead>
<tr class="header">
<th>ArtDef Class</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Appeal</td>
<td><p>Binds ranges of hex 'Appeal' values to specific names that may be referenced by other artdefs.</p>
<p>Contains Game-Dependent Content.</p></td>
</tr>
<tr class="even">
<td>Buildings<span id="scroll-bookmark-32" class="anchor"></span></td>
<td><p>Binds building names to usable assets for various systems.</p>
<p>Contains Game-Dependent Content. &quot;Building&quot; element names must be identical to &quot;type&quot; attribute in corresponding game XML entries.</p>
<p>The StrategicView property creates an association between BuildStates and entries in <a href="#scroll-bookmark-5">StrategicView.artdef</a>'s Buildings collection.</p>
<p>The BuildStates collection contains valid build states for buildings and have to match the game's hard-coded values.</p>
<p>The BuildingChains contains named collections that are referenced by entries in <a href="#scroll-bookmark-5">StrategicView.artdef</a>'s Buildings collection. A BuildingChain encodes the progression of district → building level 1 → building level 2 → building level 3 (e.g. Science District → Library → University → Research Center).</p>
<p>While the WorldView draws the district and all buildings in it (in their potentially pillaged states), the StrategicView only draws the most recent (or most recently pillaged) district / building. To accomplish this it needs to know the order in which the districts / buildings appear and be able to move up and down (in case of pillaging) the list.</p>
<p>Note that within a level, specialty items (i.e. civilization-specific districts or buildings) should come after &quot;normal&quot; items, because the game goes through the elements of a level in reverse order and uses the first one it finds.</p>
<p>Also note that DLC and mod versions of this ArtDef append their new elements to the end of each level and overwrite elements only if they are named identically.</p></td>
</tr>
<tr class="odd">
<td>Camera</td>
<td><p>Defines configuration settings for the in game camera. Each entry in the camera artdef is a block of settings, and supports editing the following:</p>
<ul>
<li>
<p>FOV, Tilt, and Altitude, as functions of zoom level</p>
</li>
<li>
<p>Atmospheric fog parameters, as functions of zoom level</p>
</li>
<li>
<p>Near and Far clip distances</p>
</li>
<li>
<p>Bloom and exposure parameters</p>
</li>
</ul>
<p>The DEFAULT_CAMERA entry is used by default. There is currently no way to override the camera configuration without using the in-game console.</p></td>
</tr>
<tr class="even">
<td>Cities</td>
<td>Binds eras from the <a href="#scroll-bookmark-33">Eras.artdef</a> to entries in <a href="#scroll-bookmark-5">StrategicView.artdef</a>'s Cities collection.</td>
</tr>
<tr class="odd">
<td>CityGenerators</td>
<td>Defines procedural generation parameters and asset lists that CityGen uses to create the procedural 'City Center' districts and small filler buildings around nearby disticts.</td>
</tr>
<tr class="even">
<td>Civilizations</td>
<td><p>Source for all artdefs that must refer to a civilization.</p>
<p>Contains Game-Dependent Content. &quot;Civilization&quot; element names must be identical to &quot;type&quot; attribute in corresponding game XML entries.</p></td>
</tr>
<tr class="odd">
<td>Clutter</td>
<td>Defines a set of clutter assets for randomly scattered models.</td>
</tr>
<tr class="even">
<td>Cultures</td>
<td>Groups Civilizations for ease of reference in other artdefs. Why add 15 entries, when you can add one entry and one culture?</td>
</tr>
<tr class="odd">
<td>Districts</td>
<td><p>Binds district names to usable assets for various systems.</p>
<p>Contains Game-Dependent Content. &quot;District&quot; element names must be identical to &quot;type&quot; attribute in corresponding game XML entries.</p>
<p>The StrategicView property creates an association between BuildStates and entries in <a href="#scroll-bookmark-5">StrategicView.artdef</a>'s Districts collection.</p>
<p>The BuildStates collection contains valid build states for districts and have to match the game's hard-coded values.</p></td>
</tr>
<tr class="even">
<td>DynamicGeo</td>
<td>Defines &quot;Walls&quot;: sets of dynamic geometry assets with metadata that allows them to be used in game.</td>
</tr>
<tr class="odd">
<td>Eras<span id="scroll-bookmark-33" class="anchor"></span></td>
<td><p>Binds era names to usable assets for various systems.</p>
<p>Binds groups of eras to specific ArtEra names that can be referenced by other artdefs.</p>
<p>Contains Game-Dependent Content. &quot;Era&quot; element names must be identical to &quot;type&quot; attribute in corresponding game XML entries.</p></td>
</tr>
<tr class="even">
<td>Farms</td>
<td>Defines the sets of asset tiles used by the farm system.</td>
</tr>
<tr class="odd">
<td>Features</td>
<td><p>Binds feature names to usable assets for various systems.</p>
<p>Contains Game-Dependent Content. &quot;Feature&quot; element names must be identical to &quot;type&quot; attribute in corresponding game XML entries.</p>
<p>The StrategicView property creates an association between Shapes and entries in <a href="#scroll-bookmark-5">StrategicView.artdef</a>'s Features collection. Shapes can be:</p>
<ul>
<li>
<p>1Dot (one tile),</p>
</li>
<li>
<p>2Dash (two tiles horizontal),</p>
</li>
<li>
<p>2Dash_East (two tiles horizontal with the east tile being water),</p>
</li>
<li>
<p>2Dash_West (two tiles horizontal with the west tile being water),</p>
</li>
<li>
<p>2ForwardSlash (two tiles diagonal left-to-right),</p>
</li>
<li>
<p>2ForwardSlash_NorthEast (two tiles diagonal left-to-right with the north-east tile being water),</p>
</li>
<li>
<p>2ForwardSlash_SouthWest (two tiles diagonal left-to-right with the south-west tile being water),</p>
</li>
<li>
<p>2Backslash (two tiles diagonal right-to-left),</p>
</li>
<li>
<p>2Backslash_SouthEast (two tiles diagonal right-to-left with the south-east tile being water),</p>
</li>
<li>
<p>2Backslash_NorthWest (two tiles diagonal right-to-left with the north-west tile being water),</p>
</li>
<li>
<p>3Dash (three tiles horizontal),</p>
</li>
<li>
<p>3ForwardSlash (three tiles diagonal left-to-right),</p>
</li>
<li>
<p>3Backslash (three tiles diagonal right-to-left),</p>
</li>
<li>
<p>3V_North (three tiles in an A-shape, i.e. two tiles in bottom row and one tile in top row),</p>
</li>
<li>
<p>3V_NorthEast (three tiles in a V-shape with the bottom tile's west neighbor being water),</p>
</li>
<li>
<p>3V_SouthEast (three tiles in an A-shape with the top tile's west neighbor being water),</p>
</li>
<li>
<p>3V_South (three tiles in a V-shape, i.e. one tile in the bottom row and two tiles in the top row),</p>
</li>
<li>
<p>3V_SouthWest (three tiles in an A-shape with the top tile's east neighbor being water),</p>
</li>
<li>
<p>3V_NorthWest (three tiles in a V-shape with the bottom tile's east neighbor being water),</p>
</li>
<li>
<p>4Z (four tiles in a Z-shape, i.e. two rows of two with the top row offset to the left),</p>
</li>
<li>
<p>4S (four tiles in an S-shape, i.e. two rows of two with the top row offset to the right),</p>
</li>
<li>
<p>4Diamond (four tiles in a diamond shape, i.e. one tile in the bottom row, two tiles in the middle row, and one tile in the top row),</p>
</li>
<li>
<p>4Tail_NorthEast (four tiles, three in the bottom row one in the top row, with the three bottom tiles pointing north-east),</p>
</li>
<li>
<p>4Tail_East (four tiles, three in the bottom row one in the top row, with the three bottom tiles pointing east),</p>
</li>
<li>
<p>4Tail_SouthEast (four tiles, three in the bottom row one in the top row, with the three bottom tiles pointing south-east),</p>
</li>
<li>
<p>4Tail_SouthWest (four tiles, three in the bottom row one in the top row, with the three bottom tiles pointing south-west),</p>
</li>
<li>
<p>4Tail_West (four tiles, three in the bottom row one in the top row, with the three bottom tiles pointing west),</p>
</li>
<li>
<p>4Tail_NorthWest (four tiles, three in the bottom row one in the top row, with the three bottom tiles pointing north-west),</p>
</li>
<li>
<p>6Dash (six tiles horizontal),</p>
</li>
<li>
<p>6ForwardSlash (six tiles diagonal, left-to-right), and</p>
</li>
<li>
<p>6Backslash (six tiles diagonal, right-to-left).</p>
</li>
</ul>
<p>(Any order mentioned above is in game coordinates, which go from lower-left to upper-right in row-order.)</p></td>
</tr>
<tr class="even">
<td>FOWConfig</td>
<td><p>Defines FOW configuration. The FOW configuration is a laundry list of global controls which govern the appearance of the fogged areas. It also defines the placement rules for the various sprites which are scattered throughout the full-fog and mid-fog.</p>
<p>The FOW artdef references textures cooked into the FOWSprites and FOWTextures xlps</p></td>
</tr>
<tr class="odd">
<td>GamePropertyRanges</td>
<td></td>
</tr>
<tr class="even">
<td>GenericObjectBLPs</td>
<td></td>
</tr>
<tr class="odd">
<td>GoodyHuts</td>
<td></td>
</tr>
<tr class="even">
<td>GraphicsTweaks</td>
<td>Contains various knobs and switches for low-level control over graphics settings.</td>
</tr>
<tr class="odd">
<td>Improvements</td>
<td><p>Binds improvement names to usable assets for various systems.</p>
<p>Contains Game-Dependent Content. &quot;Improvement&quot; element names must be identical to &quot;type&quot; attribute in corresponding game XML entries.</p>
<p>The StrategicView property creates an association between BuildStates and entries in <a href="#scroll-bookmark-5">StrategicView.artdef</a>'s Improvements collection.</p>
<p>The BuildStates collection contains valid build states for improvements and have to match the game's hard-coded values.</p></td>
</tr>
<tr class="even">
<td>Landmarks</td>
<td>Contains a large amount of metadata describing Districts, the Buildings inside of them, the assets that make up both, and the relationship each has with the other. Also describes 'Landmarks', which are mostly Tile Improvements, with some Resources and Features sprinkled in. Abandon hope all ye who enter here</td>
</tr>
<tr class="odd">
<td>LeaderFallback</td>
<td></td>
</tr>
<tr class="even">
<td>Leaders</td>
<td></td>
</tr>
<tr class="odd">
<td>Lenses</td>
<td></td>
</tr>
<tr class="even">
<td>Minimap</td>
<td></td>
</tr>
<tr class="odd">
<td>Overlay</td>
<td></td>
</tr>
<tr class="even">
<td>Resources</td>
<td><p>Binds resource names to usable assets for various systems.</p>
<p>Contains Game-Dependent Content. &quot;Resource&quot; element names must be identical to &quot;type&quot; attribute in corresponding game XML entries.</p></td>
</tr>
<tr class="odd">
<td>Routes</td>
<td><p>Binds resource names to usable assets for various systems.</p>
<p>Contains Game-Dependent Content. &quot;Route&quot; element names must be identical to &quot;type&quot; attribute in corresponding game XML entries.</p>
<p>The StrategicView property creates an association between BuildStates and entries in <a href="#scroll-bookmark-5">StrategicView.artdef</a>'s Routes collection.</p>
<p>The BuildStates collection contains valid build states for routes and have to match the game's hard-coded values.</p></td>
</tr>
<tr class="even">
<td>ScriptedArtSelector</td>
<td></td>
</tr>
<tr class="odd">
<td>SkyBox</td>
<td>Allows for overriding the background texture.</td>
</tr>
<tr class="even">
<td>StrategicView<span id="scroll-bookmark-5" class="anchor"></span></td>
<td><p>Controls all drawable content in the StrategicView. Most drawable content requires two fog-of-war states: revealed (aka mid-fog) and visible. Because of this, most drawable content in the StrategicView.artdef is first grouped into &quot;entries&quot; (e.g. FeatureEntries, ImprovementEntries, BuildingEntries, etc.), which are then grouped into the actual drawable &quot;elements&quot; (e.g. Features, Improvements, Buildings, etc.).</p>
<p><em>Entries</em> group references to texture XLP entries with draw-specific meta information (such as which part of the textures to draw).</p>
<p><em>Elements</em> group multiple entries together and add usage-specific meta information (such as where and how the entries are supposed to be drawn on the map).</p>
<p><span id="scroll-bookmark-34" class="anchor"></span>An entry (found in any *Entries collection) consists of the following:</p>
<ul>
<li>
<p>Visible_XLPEntry,</p>
</li>
<li>
<p>Visible_TopLeft,</p>
</li>
<li>
<p>Visible_BottomRight,</p>
</li>
<li>
<p>Revealed_XLPEntry,</p>
</li>
<li>
<p>Revealed_TopLeft, and</p>
</li>
<li>
<p>Revealed_Bottom_Right.</p>
</li>
</ul>
<p>Visible_XLPEntry and Revealed_XLPEntry are XLP references to the visible and revealed textures that represent the drawable content..</p>
<p>Visible_TopLeft and Revealed_TopLeft are 2D coordinates representing the top-left corner (in pixels) of the area of the texture that represents the visible and revealed drawable content.</p>
<p>Visible_BottomRight and Revealed_BottomRight are 2D coordinates representing the bottom-right corner (in pixels) of the area of the texture that represents the visible and revealed drawable content.</p>
<p>The *_TopLeft and *_BottomRight 2D coordinates allow you to create atlassed textures containing multiple sprites in a single image and have each ArtDef entry reference only a small rectangular part of that image. If both the *_TopLeft and *_BottomRight 2D coordinates are identical the whole image is drawn.</p>
<p><span id="scroll-bookmark-35" class="anchor"></span>An element (found in any other collection except for Properties, PositionSets, PlacementRules, TerrainBlends, and TerrainBlendCorners) consists of the following:</p>
<ul>
<li>
<p>PositionSet,</p>
</li>
<li>
<p>PlacementRule,</p>
</li>
<li>
<p>Render,</p>
</li>
<li>
<p>TileCount, and</p>
</li>
<li>
<p>Entries.</p>
</li>
</ul>
<p>A PositionSet is an ArtDef reference to an entry in the PositionSet collection. This entry determines where the drawable content is placed within a tile.</p>
<p>A PlacementRule is an ArtDef reference to an entry in the PlacementRules collection. This entry determines how the PositionSet values are mapped to the individual entries.</p>
<p>The Render flag is a boolean value that determines whether the sprite will be drawn on screen. This is useful for things like the Palace or Walls, which are drawn in the WorldView but are shown as UI elements only in the StrategicView.</p>
<p>TileCount determines how many in-game tiles will be covered by the entries referenced in the Entries collection. Depending on the selected PlacementRule, this number may or may not need to be equal to the number of elements in the Entries collection.</p>
<p>Entries is a sub-collection of ArtDef references to an entry in the corresponding *Entries collection. This entry represents the actual visible and revealed textures that will be rendered.</p>
<p>StrategicView.artdef contains the following collections:</p>
<ul>
<li>
<p>Properties contain generic values that apply to the whole StrategicView, e.g. the color of coastlines and river water.</p>
</li>
<li>
<p>PositionSets contain named collections of 2D coordinates that determine where within the hex something will be drawn. The coordinate system's origin (0.0, 0.0) is aligned with the hex center. The right hex boundary is located at (0.5, 0.0) while the left hex boundary is located at (-0.5, 0.0). The top hex vertex is located at (0.0, 0.57) and the bottom hex vertex is located at (0.0, -0.57).</p>
</li>
<li>
<p>PlacementRules are an enumeration of known identifiers that tell the engine how to map the 2D coordinates from a PositionSet to a collection of texture entries. The following values are supported:</p>

<ul>
<li>
<p>Centered takes the first texture entry and centers it around the first entry of the PositionSet.</p>
</li>
<li>
<p>Centered_NotScaled Same as Centered in terms of placement but it does not squish the sprite in vertical direction.</p>
</li>
<li>
<p>AtEdges_NotScaled takes the first texture entry and places it on the hex edges as provided in 2_Edges PositionSet.</p>
</li>
<li>
<p>Centered_NotScaled_Animate Same as Centered_NotScaled and has some sort of simple lerp animation.</p>
</li>
<li>
<p>Centered_Random takes a random texture entry and centers it around the first entry of the PositionSet.</p>
</li>
<li>
<p>GreatWall is used by the Great Wall improvement and combines one texture entry (tower) with one directed asset (wall pieces in different directions)</p>
</li>
<li>
<p>MultipleEntriesPerTile Used by yield icons where each tile can have multiple texture entries of same UI Lens type</p>
</li>
<li>
<p>OneEntryPerTile is used by multi-tile natural wonders and it places each texture entry on a separate tile.</p>
</li>
</ul></li>
<li>
<p>TerrainBlends contain references to XLP entries of <a href="#scroll-bookmark-7">StrategicView_TerrainBlend</a> assets and optionally a <a href="#scroll-bookmark-3">StrategicView_DirectedAsset</a> for cliffs (since cliffs have to match the coastline determined by the terrain blend).</p>
</li>
<li>
<p>TerrainBlendCorners contain references to XLP entries of <a href="#scroll-bookmark-8">StrategicView_TerrainBlendCorners</a> assets.</p>
</li>
<li>
<p>TerrainSpriteEntries are <a href="#scroll-bookmark-34">entries</a> containing references to XLP entries of <a href="#scroll-bookmark-4">StrategicView_Sprite</a> textures that are referenced by TerrainSprites.</p>
</li>
<li>
<p>TerrainSprites are <a href="#scroll-bookmark-35">elements</a> referencing TerrainSpriteEntries that contain terrain-related textures that can overlap surrounding tiles (as opposed to <a href="#scroll-bookmark-18">StrategicView_TerrainType</a> textures in the TerrainTypes collection, which are drawn only within the borders of the tile). Examples including mountains and hills.</p>
</li>
<li>
<p>TerrainTypes contain a category and in-line (i.e. not referenced) <a href="#scroll-bookmark-34">entry</a> containing references to XLP entries of <a href="#scroll-bookmark-18">StrategicView_TerrainType</a> textures. The category can be one of Hills, Mountains, Coast, Ocean, and Default (everything else). The game applies different rules to each category. Additionally, each inline entry can contain a reference to a TerrainSprite. (For example, &quot;Mountains&quot; is a TerrainType, which has a background texture that fills the tile up to its borders, and references a &quot;Mountains&quot; TerrainSprite, which has the actual mountain texture that overlaps the tile borders.)</p>
</li>
</ul>
<ul>
<li>
<p>FeatureEntries are <a href="#scroll-bookmark-34">entries</a> containing references to XLP entries of <a href="#scroll-bookmark-4">StrategicView_Sprite</a> textures that are referenced by Features.</p>
</li>
<li>
<p>Features are <a href="#scroll-bookmark-35">elements</a> referencing FeatureEntries that contain in-game features (ice, jungle, etc.) and natural wonders (Crater Lake, Mount Everest, etc.). Additionally, Features can reference <a href="#scroll-bookmark-3">StrategicView_DirectedAssets</a> (for cliff-based natural wonders like the Cliffs of Dover) and contain a RenderTerrainSprite checkbox and a TerrainTypeOverride list. The RenderTerrainSprite checkbox determines whether the terrain sprite of the underlying game tile will be drawn underneath the feature or not. The TerrainTypeOverride list allows the game to override the underlying terrain type for lake-like natural wonders. (An implementation side-effect of lakes is that their terrain type implicitly changes to coast. In StrategicView, the lake textures have their own coastlines, so the game has to create a non-coast terrain type to fill in the gaps between the tile borders and the lake coastlines baked into the texture. This list allows you to influence which terrain types are created.)</p>
</li>
<li>
<p>Routes contain two references to XLP entries, one roads (<a href="#scroll-bookmark-6">StrategicView_Route</a> assets) and one for bridges (<a href="#scroll-bookmark-3">StrategicView_DirectedAssets</a> assets).</p>
</li>
<li>
<p>ImprovementEntries are <a href="#scroll-bookmark-34">entries</a> containing references to XLP entries of <a href="#scroll-bookmark-4">StrategicView_Sprite</a> textures that are referenced by Improvements.</p>
</li>
<li>
<p>Improvements are <a href="#scroll-bookmark-35">elements</a> referencing ImprovementEntries that contain in-game improvements (farms, mines, etc.). Additionally, Improvements can reference <a href="#scroll-bookmark-3">StrategicView_DirectedAssets</a> for special-case improvements like The Greal Wall.</p>
</li>
<li>
<p>DistrictEntries are <a href="#scroll-bookmark-34">entries</a> containing references to XLP entries of <a href="#scroll-bookmark-4">StrategicView_Sprite</a> textures that are referenced by Districts.</p>
</li>
<li>
<p>Districs are <a href="#scroll-bookmark-35">elements</a> referencing DistrictEntries that contain in-game districts (science, faith, etc.).</p>
</li>
<li>
<p>BuildingEntries are <a href="#scroll-bookmark-34">entries</a> containing references to XLP entries of <a href="#scroll-bookmark-4">StrategicView_Sprite</a> textures that are referenced by Buildings.</p>
</li>
<li>
<p>Buildings are <a href="#scroll-bookmark-35">elements</a> referencing BuildingEntries that contain in-game buildings (library, market, etc.). Additionally, Buildings contain a reference to a BuildingChain entry in <a href="#scroll-bookmark-32">Buildings.artdef</a>.</p>
</li>
<li>
<p>CityEntries are <a href="#scroll-bookmark-34">entries</a> containing references to XLP entries of <a href="#scroll-bookmark-4">StrategicView_Sprite</a> textures that are referenced by Cities.</p>
</li>
<li>
<p>Cities are <a href="#scroll-bookmark-35">elements</a> referencing CityEntries that contain in-game cities in their various eras.</p>
</li>
<li>
<p>ParkEntries are <a href="#scroll-bookmark-34">entries</a> containing references to XLP entries of <a href="#scroll-bookmark-4">StrategicView_Sprite</a> textures that are referenced by Parks.</p>
</li>
<li>
<p>Parks are <a href="#scroll-bookmark-35">elements</a> referencing ParkEntries that contain in-game national parks.</p>
</li>
<li>
<p>EffectEntries are <a href="#scroll-bookmark-34">entries</a> containing references to XLP entries of <a href="#scroll-bookmark-4">StrategicView_Sprite</a> textures that are referenced by Effects.</p>
</li>
<li>
<p>Effects are <a href="#scroll-bookmark-35">elements</a> referencing EffectEntries that contain in-game effects (e.g. fallout).</p>
</li>
<li>
<p>UILensEntries are <a href="#scroll-bookmark-34">entries</a> containing references to XLP entries of <a href="#scroll-bookmark-4">StrategicView_Sprite</a> textures that are referenced by UILenses.</p>
</li>
<li>
<p>UILenses are <a href="#scroll-bookmark-35">elements</a> referencing UILensEntries that contain in-game UI Lens Textures.</p>
</li>
</ul></td>
</tr>
<tr class="odd">
<td>TerrainMaterialSet</td>
<td></td>
</tr>
<tr class="even">
<td>TerrainStyle</td>
<td><p>Controls for the procedural terrain layers.</p>
<p>RidgelineMountain: Controls the look of the procedural ridgeline mountains.</p>
<p>StandardHills: Controls the look for hills for the basic terrain types. These hills are controlled with TerrainElement heightmaps that are blended into the terrain.</p>
<p>DuneDesertHills: Controls the desert hills, which are procedurally generated sand dunes.</p>
<p>StandardCoastline: Controls the appearance of the procedural coastlines in the game.</p>
<p>StandardRiver: Controls the appearance of the procedural rivers in the game, as well as a list of TerrainElement entries used for river sources and the Clutter entry used for the randomly scattered river assets.</p>
<p>StandardFlat: Controls the look of flat terrain types in the game. Flat terrain consists of terrain material as well as TerrainElement for subtle height variation.</p>
<p>StandardOcean: Controls the look of the procedural ocean.</p>
<p>StandardIceShelf: Controls the look for the procedural ice shelf around ice terrain tiles.</p>
<p>DesertMountain: Controls the look of the new desert mountain style. Delete this entry to have all mountains use the RidgelineMountain style.</p>
<p>NaturalWonders: List of entries that define natural wonder assets, including the TerrainAsset, TerrainElement, and water style settings. The TerrainElement for natural wonders is required to have either 512 square textures (to cover a single hex) or 1024 square textures (to cover a larger region). The two diagrams below show how these two size textures will line up to hexes in the game. The entries in the Pattern group allow you to define certain properties for hexes 1 - 6, and the game will automatically rotate the asset if require to ensure it lines up properly. These properties are:</p>
<ol style="list-style-type: decimal">
<li>
<p>BlockingHexN - This natural wonder fills this hex, blocking and overriding the procedural terrain. By default hex 0 (the center hex) is blocking.</p>
</li>
<li>
<p>TerrainTypeN - This natural wonder asset requires special conditions to line up properly, such as being next to water in a specific direction.</p>
</li>
</ol>
<p><img src="DataDocumentation/media/image1.jpeg" alt="/download/attachments/152437570/TerrainElementTemplate_Small.jpg?version=1&amp;modificationDate=1498249375480&amp;api=v2" width="249" height="249" /></p>
<p><img src="DataDocumentation/media/image2.jpeg" alt="/download/attachments/152437570/TerrainElementTemplate_Medium.jpg?version=1&amp;modificationDate=1498249713867&amp;api=v2" width="396" height="396" /></p>
<p>MaterialSet: List of terrain materials that are referenced by the TerrainElementIDMap entry of a TerrainElement in the NaturalWonders list. If you do not put the material in this list, the game will not load it and the black error error material will be used.</p></td>
</tr>
<tr class="odd">
<td>Terrains</td>
<td><p>Binds resource names to usable assets for various systems.</p>
<p>Contains Game-Dependent Content. &quot;Terrain&quot; element names must be identical to &quot;type&quot; attribute in corresponding game XML entries.The StrategicView property references entries in <a href="#scroll-bookmark-5">StrategicView.artdef</a>'s TerrainTypes collection.</p></td>
</tr>
<tr class="even">
<td>TimeOfDay</td>
<td><p>Controls the time of day system. The TimeOfDay setting named 'DEFAULT_LIGHTING' is used most of the time. The setting named 'WONDER_TOD' is used when a wonder movie is active. The engine and wonder movies will set time of day using a value between 0 and 24 (midnight to midnight). The time of day system provides the following controls, all of which can be animated over time:</p>
<ul>
<li>
<p>Blending environment lights over time: The 'CubeLights' collection defines a set of GameEnvironment light rigs to be used for image-based lighting, and a weight curve to be applied over time to each light. The weight curve can be used to adjust the influence of a given light over time (for example, fading it out at night). The engine supports up to 8 simultaneous non-zero weights.</p>
</li>
<li>
<p>Animating the sun direction: The SunAzimuth, SunTilt, SunZenith, and SunColor controls all control the behavior of the sun as a function of time of day.</p>
</li>
<li>
<p>Turning lightmaps and emission maps off over time: The 'LightMapWeight' curve specifies a scale factor that is applied to all light maps and emission maps in the shaders. Among other things, this can be used to turn emissive window lights on and off at night time.</p>
</li>
<li>
<p>Exposure: This is a camera exposure control which can be animated over time of day. Exposure is measured in f-stops.</p>
</li>
<li>
<p>Color Keys correction time: The color key system is under the control of the time of day system. The 'ColorKeys' collection specifies a set of color keys and a weight curve, similar to the environment lights. The engine supports up to 2 simultaneously active color keys.</p>
</li>
</ul></td>
</tr>
<tr class="odd">
<td>UIPreview</td>
<td></td>
</tr>
<tr class="even">
<td>UnitActivities</td>
<td></td>
</tr>
<tr class="odd">
<td>UnitOperations</td>
<td></td>
</tr>
<tr class="even">
<td>Units</td>
<td></td>
</tr>
<tr class="odd">
<td>UserInterfaceBLPs</td>
<td></td>
</tr>
<tr class="even">
<td>VFX</td>
<td>Contains information about globally named visual effects. The visual effects within the NormalVFX collection are typically referenced directly from the game (by name) when particular game conditions occur. These visual effects can also be referenced by assets via ArtDef triggers. The WeaponVFX, TerrainVFX, and MaterialVFX collections contain tables that represent the type of visual effect that should be displayed for each of the named elements when a particular weapon is used, terrain/feature type is hit, or material is encountered. WeaponVFX, TerrainVFX, and MaterialVFX collections are typically referenced by ArtDef triggers on units and the game's unit system takes care of ensuring that the appropriate context for each collection is supplied in order to correctly select the visual effect to be displayed (these typically occur during combat). Note that the DEFAULT entry within the WeaponVFX, TerrainVFX, and MaterialVFX collections will be used in the event that an appropriate match is not found within the named element's table.</td>
</tr>
<tr class="odd">
<td>WaterMaterials</td>
<td></td>
</tr>
<tr class="even">
<td>WaterSettings</td>
<td><p>Provides global controls for the appearance of river and ocean water. This includes:</p>
<ul>
<li>
<p>Specifying the water materials used around ice, and in oceans, lakes, and rivers.</p>
</li>
<li>
<p>Controlling the procedural haze effect which is applied around coastlines.</p>
</li>
<li>
<p>Specifying global visual settings for the water such as specular power, reflectivity. Certain values are specified globally, rather than in the individual materials, in order to guarantee a consistent water appearance.</p>
</li>
</ul></td>
</tr>
<tr class="odd">
<td>WaveSettings</td>
<td>Various controls and tweaks for the coastal waves.</td>
</tr>
<tr class="even">
<td>WonderMovie</td>
<td>Contains information for each world wonder that can be displayed by the game. Additionally, special buildings such as the small, medium, and large rockets are also represented as wonders. When creating visual representations for buildings, the wonder artdef is checked for the building before checking the buildings artdef.</td>
</tr>
<tr class="odd">
<td>WorldViewRoutes</td>
<td>Defines materials and models to be used when creating procedural roads in the World View (NOT the Strategic View!). Additionally, defines some parameters that control for shape and formation of procedural roads.</td>
</tr>
</tbody>
</table>
</div> <!-- panel body --> 
</div> <!-- panel -->

<div class="panel panel-primary" id="Geometry">
<div class="panel-heading">
<div class="panel-title">Geometry
</div>
</div>
<div class="panel-body">

<p>Geometry (.geo)</p>
<p>Geometry files contain the 3D data used for units, buildings, leaders, etc. Currently we support importing geometry directly from 3DSMax and Maya</p>

<p>Structure of a Geometry File</p>

<p>Geometry files are organized in a very specific way that the engine relies on to be able to set up assets</p>


<ul>
<li>
<p>.Geo File</p>

<ul>
<li>
<p>Model</p>

<ul>
<li>
<p>Mesh</p>

<ul>
<li>
<p>Triangle Group</p>
</li>
</ul></li>
<li>
<p>Mesh</p>

<ul>
<li>
<p>Triangle Group</p>
</li>
</ul></li>
<li>
<p>Mesh</p>

<ul>
<li>
<p>Triangle Group</p>
</li>
<li>
<p>Triangle Group</p>
</li>
</ul></li>
<li>
<p>Mesh</p>

<ul>
<li>
<p>Triangle Group</p>
</li>
</ul></li>
</ul></li>
</ul></li>
</ul>


<p>So every Geo File contains only a single Model, which is the logical grouping of all the Meshes in the Geo file, and each Mesh file can have any number of Triangle groups. When orienting a mesh, keep in mind that the pivot of the mesh will be set to 0,0,0 on export. This means that any desired offsets will have to be added to the mesh itself.<img src="Geometry/media/image1.png" width="613" height="402" /></p>

<p>However, any child objects of the top mesh in the hierarchy will retain their pivot offsets.</p>

<p>Using the Asset Editor</p>

<ul>
<li>
<p>In the Asset Editor go to 'File &gt; New' and select Geometry from the list.</p>
</li>
</ul>


<p><img src="Geometry/media/image2.png" width="619" height="496" /></p>


<ul>
<li>
<p>In the Class Name dropdown select the class that you want (1). It can be tricky to change the class for entities after they are created, so try to make sure you have the correct class.</p>
</li>
</ul>

<p><img src="Geometry/media/image3.png" width="622" height="408" /></p>

<ul>
<li>
<p>Click on the line for '<em><strong>Source File Path</strong></em>' (2), and browse to the Max or Maya file that has your geometry.</p>
</li>
</ul>

<ul>
<li>
<p>When you select your file, the editor will parse the file and find which models are available for export. This will fill out the '<em><strong>Source Object</strong></em>' dropdown (3) with all the available models for you to pick from, so click the dropdown and select the model object that you want.</p>
</li>
</ul>

<ul>
<li>
<p>The '<em><strong>Name</strong></em>' (4)of the geometry will get set automatically to the name of the source object, but you can change it to whatever you want before saving.</p>
</li>
</ul>

<ul>
<li>
<p>Go to &quot;<em><strong>File &gt; Save</strong></em>&quot; and you're done.</p>
</li>
</ul>

</div> <!-- panel body --> 
</div> <!-- panel -->

<div class="panel panel-primary" id="IconXML">
<div class="panel-heading">
<div class="panel-title">IconXML
</div>
</div>
<div class="panel-body">

<h1 id="icon-packages-and-icon-xml-creation">Icon Packages and Icon XML Creation</h1>
<p><span id="scroll-bookmark-1" class="anchor"></span>Adding icons is a multi-step process, certain steps can be skipped if a project or icon file(s) have been setup. Steps are the following:</p>
<ol style="list-style-type: decimal">
<li><p>Create Icon Package(s)</p></li>
<li><p>Add Icon Package(s) to project</p></li>
<li><p>Edit Icon XML for icon entries.</p></li>
</ol>
<h1 id="create-icon-packages">1. Create Icon Package(s)</h1>
<p>Open up <strong>AssetEditor</strong> and either open the existing Icons.xlp or create a new XLP by selecting File &gt; New &gt; &quot;XLP&quot; (under packages).</p>
<p><img src="IconXML/media/image1.png" alt="/download/attachments/161288176/image2018-4-16_13-36-16.png?version=1&amp;modificationDate=1523900176160&amp;api=v2" width="523" height="366" /></p>
<p>Under the Entries list, choose the &quot;Add New&quot; icon to map an Icon file to a package name. The mapping of names is usually the same asset name as file name.</p>
<p><img src="IconXML/media/image2.png" alt="/download/attachments/161288176/image2018-4-16_13-41-22.png?version=1&amp;modificationDate=1523900482953&amp;api=v2" width="566" height="548" /></p>
<p>Above here, the XP1_UnitActions80 EntryID is mapped the XP1_UnitActions80.dds file.</p>
<p>(The indexing for XP1_UnitActions80 icons are setup <em>in Expansion1_Icons_UnitActions.xml</em> explained in step 3.)</p>
<h1 id="add-icon-packages-to-project">2. Add Icon Package(s) to project</h1>
<p>Open up <strong>Project Builder</strong> and choose from the File menu &quot;Game Art Specification&quot; for that project.</p>
<p>For the base game this is in <em>$\Civ6\pantry\Civ6.Art.xml</em></p>
<p>For XP1 this is in <em>$\Civ6\DLC\Expansion1\pantry\Expansion1.Art.xml</em></p>
<p>For XP2 this is in <em>$\Civ6\DLC\Expansion2\pantry\Expansion2.Art.xml</em></p>
<p><img src="IconXML/media/image3.png" width="565" height="424" /></p>
<p>In the Libraries section, press &quot;Add...&quot; or select the existing &quot;UITexture&quot; Library. A list of packages will show up on the right:</p>
<p><img src="IconXML/media/image4.png" width="565" height="342" /></p>
<p>Click the right-most &quot;Add...&quot; next to &quot;Packages&quot; and select the new XLPs.</p>
<h1 id="edit-the-icon-xml-for-icon-entires">3. Edit the Icon XML for icon entires</h1>
<h2 id="step-by-step-guide">Step-by-step guide</h2>
<ol style="list-style-type: decimal">
<li><p>In the <strong>IconTextureAtlases</strong> section of the corresponding XML file, add an entry that maps from <strong>texture asset name</strong> (from package) to <strong>atlas name</strong>. This file may not exist, and will have to be created and then have its <strong>IconTextureAtlases</strong> section defined. You can map multiple textures of different resolutions to the same atlas name. The correct size will be chosen automatically based on the UI control size.</p></li>
</ol>
<p>Example -</p>
<table>
<tbody>
<tr class="odd">
<td>&lt;IconTextureAtlases&gt;<br />
&lt;Row Name=&quot;ICON_ATLAS_POTTERY&quot; IconSize=&quot;32&quot; Filename=&quot;TechPottery32&quot;/&gt;<br />
&lt;Row Name=&quot;ICON_ATLAS_POTTERY&quot; Iconsize=&quot;48&quot; Filename=&quot;TechPottery48&quot;/&gt;<br />
&lt;/IconTextureAtlases&gt;</td>
</tr>
</tbody>
</table>
<p>Example with hand atlased texture -</p>
<table>
<tbody>
<tr class="odd">
<td>&lt;IconTextureAtlases&gt;<br />
&lt;Row Name=&quot;ICON_ATLAS_TECH&quot; IconSize=&quot;32&quot; IconsPerRow=&quot;8&quot; IconsPerColumn=&quot;8&quot; Filename=&quot;Tech32&quot;/&gt;<br />
&lt;Row Name=&quot;ICON_ATLAS_TECH&quot; IconSize=&quot;48&quot; IconsPerRow=&quot;8&quot; IconsPerColumn=&quot;8&quot; Filename=&quot;Tech48&quot;/&gt;<br />
&lt;/IconTextureAtlases&gt;</td>
</tr>
</tbody>
</table>
<p>2. In the <strong>IconDefinitions</strong> section, add an entry that maps <strong>atlas name</strong> to <strong>icon name</strong>. If the icon is hand atlased, you need to specify the atlas location <strong>index</strong>. The icon name is what is used to get the correct texture in the UI.</p>
<p>Example -</p>
<table>
<tbody>
<tr class="odd">
<td>&lt;IconDefinitions&gt;<br />
&lt;Row Name=&quot;ICON_TECH_POTTERY&quot; Atlas=&quot;ICON_ATLAS_POTTERY&quot;/&gt;<br />
&lt;/IconDefinitions&gt;</td>
</tr>
</tbody>
</table>
<p>Example with hand atlased texture -</p>
<table>
<tbody>
<tr class="odd">
<td>&lt;IconDefinitions&gt;<br />
&lt;Row Name=&quot;ICON_TECH_MINING&quot; Index=&quot;2&quot; Atlas=&quot;ICON_ATLAS_TECH&quot;/&gt;<br />
&lt;/IconDefinitions&gt;</td>
</tr>
</tbody>
</table>
</div> <!-- panel body --> 
</div> <!-- panel -->

<div class="panel panel-primary" id="Iteration">
<div class="panel-heading">
<div class="panel-title">Iteration
</div>
</div>
<div class="panel-body">

<p>Iterating on an Entity</p>
<p>Once you've imported an entity into the Asset cloud, there are a few ways of updating it if you make changes to the original source file</p>

<p>File Watches</p>

<p>Whenever you open an entity in the Asset Editor, it creates a file watch on the corresponding source file, so that if you have the instance open in the editor it will attempt to reimport the entity every time it detects a change in the source file. It will also place a watch on any entities that compose the one you have open, so if you open an Asset, it will place file watches on all the entities that compose it.</p>

<p>You can see a list of all the File Watches in the Asset Editor by looking at the File Watches Tab which by default is at the bottom of the editor. If it's not there, you need to enable it by going to <strong>Window &gt; File Watches</strong></p>

<p><img src="Iteration/media/image1.jpg" alt="Machine generated alternative text: AssetEditor - D:XprojectsXBALW-AGOULD Civ6 mainXCiv6Xpa Edit View Window Lig hting_ P robe.geo Basic Name Class Name Desc ri pticn C ategorization Tags Groups Source Source File Path Source Object Imported Time Exported Ti me Data Data Files File Watches Unit Path (I items) Unit items) D:XprojectsXBALW-AGOULD Civ6 1/1/0001 AM 1/1/0001 AM Relative Path Lig hting_P robe.gr2 GR2 CIVE mainlCIvBpantryXGeomethesXLighting_Probegeo D AprojectsXBALW-AGOLlLD CIVE main* DevXLjghtingXHeIper ObjectsXLjghting Probe.max " width="576" height="481" /></p>


<p>Manual Reimport:</p>

<p>Sometimes if the File watch doesn't successfully detect your change, or if you made a change to your source file without the entity open in the tools.</p>
<p>You have two options:</p>

<ol style="list-style-type: lower-alpha">
<li>
<p>Open the Entity that you need to reimport and go to '<em><strong>File &gt; Import</strong></em>' (CTRL + SHIFT +I), or hit the Import button on the top toolbar</p>
</li>
</ol>

<p><img src="Iteration/media/image2.png" alt="Machine generated alternative text: AssetEditor - Edit D:XprojectsXBALW-AGOULD Civ6_mainXCiv6NpantryNGeometriesX16 Scouts.geo View Window tilebases.xlp 16 Scouts Unit en Source file 16_Scouts.geo Asset Pr. 16 Scouts.ast* Basic Name Class Name Desc ri pticn " width="576" height="163" /></p>


<ol style="list-style-type: lower-alpha">
<li>
<p>If the Entity you are trying to reimport is being referenced by another Asset or Entity, find where the entity is being referenced, and there will usually be a button to reimport it somewhere near by:</p>
</li>
</ol>



<ol style="list-style-type: lower-roman">
<li>
<p><img src="Iteration/media/image3.png" alt="Machine generated alternative text: Categorization (I items) items) Tags Groups Mesh O Unit Animations chments A Group Particles Behaviors Material v State " width="576" height="354" /></p>
</li>
</ol>

<p><em>For Geometries, Animations and Particles in an Asset the button is here</em></p>


<ol style="list-style-type: lower-roman">
<li>
<p><img src="Iteration/media/image4.png" alt="Machine generated alternative text: Groups o Unit -0 items) (128128) Black Base_CoIor (2048x2048) Material Test Linear Gradient (512x512) Cook Parameters Value 3aseCcIcr Gloss Metal ness Normal Seperate_AO TintMask " width="576" height="324" /></p>
</li>
</ol>

<p>For Cook Parameters (which can be any kind of entity) the button is here</p>





</div> <!-- panel body --> 
</div> <!-- panel -->

<div class="panel panel-primary" id="MappingToGameCore">
<div class="panel-heading">
<div class="panel-title">MappingToGameCore
</div>
</div>
<div class="panel-body">

<p>Mapping GameCore IDs to ArtDef Entries</p>
<p>GameCore uses database IDs (row numbers) to reference features, resources, improvements, districts, buildings, and units. So when the player builds something GameCore asks the engine to draw &quot;improvement 14.&quot; Depending on the version of the game, which DLCs, expansion packs, or mods are loaded, &quot;improvement 14&quot; can refer to different assets. The engine provides a <strong>translation layer</strong>, commonly referred to as Xref, which translates &quot;improvement 14&quot; into a specific ArtDef entry. A missing entry in the translation layer will cause the asset to not show up (and trigger a red data error), even if a corresponding ArtDef entry exists on the engine side.</p>

<p>GameCore Database IDs</p>
<p>The GameCore database that contains all features, resources, improvement, districts, buildings, and units is created from XML files located in //civ6/main/Civ6/game/assets/Gameplay/Data/… The XML files correspond each to an asset category:</p>

<ul>
<li>
<p>Buildings.xml,</p>
</li>
<li>
<p>Districts.xml,</p>
</li>
<li>
<p>Features.xml,</p>
</li>
<li>
<p>Improvements.xml,</p>
</li>
<li>
<p>Resources.xml,</p>
</li>
<li>
<p>Terrains.xml, and</p>
</li>
<li>
<p>Units.xml.</p>
</li>
</ul>

<p>You should never edit these files, but by looking at the entries in the &lt;Types&gt; element you can see what &quot;things&quot; GameCore can ask for in each category. <strong>Each of these entries must correspond to an entry in the Xref ArtDef!</strong></p>

<p>Xref ArtDefs</p>
<p>The engine's translation layer is implemented via ArtDef files in //civ6/main/Civ6/game/ArtDefs/… You will find an Xref ArtDef file for each one of the GameCore database XMLs:</p>

<ul>
<li>
<p>Buildings.artdef,</p>
</li>
<li>
<p>Districts.artdef,</p>
</li>
<li>
<p>Features.artdef,</p>
</li>
<li>
<p>Improvements.artdef,</p>
</li>
<li>
<p>Resources.artdef,</p>
</li>
<li>
<p>Terrains.artdef, and</p>
</li>
<li>
<p>Units.artdef.</p>
</li>
</ul>

<p>Each of the ArtDef files contains a single collection with entries named exactly like the &lt;Types&gt; element entries in the GameCore XMLs. Any misspellings or missing entries will cause the engine to not find the entry GameCore requested and not render it.</p>

<p>An entry in the Xref ArtDef contains multiple parameters, usually Audio and StrategicView (WorldView will be added later). These parameters are names of entries in other ArtDef files - in the case of the StrategicView it's StrategicView.artdef.</p>

<p><strong>It is up to the art department to ensure that all GameCore database IDs are represented in their respective Xref ArtDef files and that the ArtDef entries are referencing valid names of type-specific ArtDef entries!</strong></p>

<p>For example, if Features.xml contains FEATURE_FLOODPLAINS, then Features.artdef must contain an entry called FEATURE_FLOODPLAINS whose StrategicView parameter references the Floodplains entry within StrategicView.artdef.</p>
</div> <!-- panel body --> 
</div> <!-- panel -->

<div class="panel panel-primary" id="PackagingAssets">
<div class="panel-heading">
<div class="panel-title">PackagingAssets
</div>
</div>
<div class="panel-body">

<p>Packaging Assets</p>
<p>Once you have created an asset (or free-standing entity, e.g. texture) you will need to package it in order for the engine to be able to load it.</p>

<p>The engine cannot load loose files. All assets and entities have to be &quot;cooked&quot; into a <strong>Binary Library Package (BLP)</strong>, which is a binary file format that contains processed art data organized for fast loading during engine startup.</p>

<p><strong>ModBuddy</strong> contains the <strong>Cooker</strong>, which is a tool that takes assets and entities from your Mod, processes them according to the game configuration file, and writes the results to a platform-specific file (i.e. a Windows BLP won't work on iOS and vice versa).</p>

<p>The Cooker uses an <strong>XML Library Package (XLP)</strong> file to determine which assets and entities are part of a single BLP. The XLP file lists assets and entities from the Asset Cloud and assigns them identifiers (names). The engine as well as the remaining tools refer only to these identifiers, not the actual asset and entity names from the Asset Cloud.</p>

<p>Editing XLPs</p>

<p>In order to get a new art asset (or entity) into the game you will have to first package it:</p>
<ul>
<li>
<p>Open the Asset Editor.</p>
</li>
<li>
<p>Most XLP files should already be created for you, so click the <strong>Open an Existing XLP Document</strong> button and select the XLP you wish to edit.</p>
</li>
</ul>


<p><img src="PackagingAssets/media/image1.png" width="341" height="192" /></p>


<ul>
<li>
<p>If you cannot find an appropriate XLP document talk with your lead to ensure that a new BLP is the appropriate place for your new assets.</p>
</li>
</ul>
<ul>
<li>
<p>In the XLP click either the <strong>Add Existing</strong> button (if the asset or entity you want to add already exists in the Asset Cloud) or the <strong>Add New</strong> button (if the asset or entity you want to add does not yet exist in the Asset Cloud).</p>
</li>
</ul>


<p><img src="PackagingAssets/media/image2.png" width="624" height="504" /></p>


<ul>
<li>
<p>When you click the Add Existing button a new <strong>Asset Browser</strong> window pops up and allows you to select an asset or entity from the Asset Cloud.</p>

<ul>
<li>
<p>The Asset Editor may ask you for confirmation that you wish to check out the XLP file from Perforce, which you should do.</p>
</li>
<li>
<p>The newly added entry in the XLP will use the asset's or entity's name by default, which you may want to change.</p>
</li>
</ul></li>
<li>
<p>Once you have added all assets or entities you wish to add to the game to the XLP file be sure to <strong>save</strong> it and then navigate to <strong>File &gt; Cook</strong> to update the BLP with your newly added changes.</p>

<ul>
<li>
<p>Pay attention to the Output window at the bottom to make sure the cook completed successfully.</p>
</li>
</ul></li>
</ul>

<p>Creating New XLPs:</p>

<p>In most cases you probably want to use an XLP that already exists that is part of the system you're working on, but there are a couple of reasons you might want to create a new XLP:</p>
<ul>
<li>
<p>You might want to break apart the Entity packages into logical groups (i.e. you might have a separate for assets for a certain Era) for organizational purposes</p>
</li>
<li>
<p>If you want to add content that is specific to a Game Mod or Expansion</p>
</li>
<li>
<p>The system you're working in requires BLPs to be separated in such a way that they can be individually loaded (Like the leader system, which only loads the BLPs for leaders that are in your game)</p>
</li>
</ul>
</div> <!-- panel body --> 
</div> <!-- panel -->

<div class="panel panel-primary" id="ParticleEffects">
<div class="panel-heading">
<div class="panel-title">ParticleEffects
</div>
</div>
<div class="panel-body">

<p>Particle Effects (.ptl)</p>
<p>Thursday, April 09, 2015</p>
<p>3:14 PM</p>
<p>Particle effects consist of the barebones data that is used by Fork to simulate the procedural animation of a particle system.</p>

<p>Currently the engine is using Fork for its particle system so you must create your particle system in Fork's Particle Studio before bringing it into the engine.</p>

<p>Using the Asset Editor</p>

<ul>
<li>
<p>In the Asset Editor go to 'File &gt; New' and select ParticleEffect from the list.</p>
</li>
</ul>


<p><img src="ParticleEffects/media/image1.png" alt="Machine generated alternative text: aa Pick the file type to create Tenure Analytic Light File Type Entities Animation Environment I_jght Behavior Packages Material " width="453" height="323" /></p>


<ul>
<li>
<p>In the Class Name dropdown select the class that you want (1). Right now all VFX are using just the one 'VFXParticle' Class, but more classes might be created later on.</p>
</li>
</ul>


<p><img src="ParticleEffects/media/image2.png" alt="Machine generated alternative text: AssetEditor - D. Edit View Window Open Source file VT Particle Effect.peb FT Particle Effect.ptr Basic Name Class Name Desc ri pticn C ategorization Tags Groups Source Source File Path Source Object Imported Time Exported Ti me Data Data Files Cook Parameters Value FT Particle Effect VFXParticle (I items) VFXParticle items) Path D:XprojectsXBALW-AGOULD Civ6 mainXArtDevXFunctionaITest 1/1/0001 AM 1/1/0001 AM Relative Path FT Particle Effect.psb FT Particle Effect Texture " width="576" height="531" /></p>

<p>-Click on the line for 'Source File Path', and browse to the .PEB file for your particle effect.</p>

<p>-Once you pick the source file, the 'Cook Parameters' tab will get filled out with the slots for all the textures and model that are used in your effect. If those entities already exist in the cloud, then they will get automatically assigned (3). If they don't exist you will have to create them by clicking the 'Add New' button (4) for each slot and importing the corresponding entity. Go here for further instructions on that.</p>


<ul>
<li>
<p>The '<em><strong>Name</strong></em>' (5)of the Particle Effect will get set automatically to the name of the source file, but you can change it to whatever you want before saving.</p>
</li>
</ul>



<ul>
<li>
<p>Go to &quot;<em><strong>File &gt; Save</strong></em>&quot; and you're done.</p>
</li>
</ul>



</div> <!-- panel body --> 
</div> <!-- panel -->

<div class="panel panel-primary" id="ParticleEffectsWorkflow">
<div class="panel-heading">
<div class="panel-title">ParticleEffectsWorkflow
</div>
</div>
<div class="panel-body">

<p>Simplified Particle workflow</p>
<p>Monday, September 14, 2015</p>
<p>1:49 PM</p>

<p>Since Particle effect Assets are fairly straight forward, the process of creating one will probably the same (Until you start doing more complex effects that combine multiple Particle effects, meshes, and animations).</p>

<p>You must still create your particle effect in Fork like you would normmally, but once you are ready to bring it into the engine follow these steps:</p>


<ol style="list-style-type: decimal">
<li>
<p>Ensure that the Asset Cloud is running</p>
</li>
<li>
<p>Open AssetEditor</p>
</li>
<li>
<p>File &gt; New &gt; Asset</p>
</li>
<li>
<p>Select ‘VFX’ Class Name</p>
</li>
<li>
<p>Select ‘Particles’ tab</p>
</li>
<li>
<p>Click ‘Add New’ tool strip button within ‘Particles’ tab to launch the Mini Importer</p>
</li>
<li>
<p>Click the ‘+ Add Source File…’ and navigate to the desired .peb file and click ‘<em><strong>OK</strong></em>’</p>
</li>
<li>
<p>Ensure that the .peb file selected appears within the text box within the Mini Importer and is checked. And click ‘Import’</p>

<ol style="list-style-type: lower-alpha">
<li>
<p>If you are re-importing the .peb file you need to ensure that the ‘<em><strong>Check Out</strong></em>’ button is checked</p>

<ol style="list-style-type: lower-roman">
<li>
<p>Alternatively, if you are reimporting a .peb file, you can simply select the item within the ‘Particles’ tab and click the ‘Reimport’ tool strip button (it looks like the recycling sign).</p>
</li>
</ol></li>
</ol></li>
</ol>

<p><img src="ParticleEffectsWorkflow/media/image1.png" alt="Machine generated alternative text: Cook Params Geometries Filter: Reimport Particle Name FX Cam fire2 Attac h ments Animations Pa rticles Behaviors " width="394" height="184" /></p>


<ol style="list-style-type: decimal">
<li>
<p>Within the Asset Previewer (Window &gt; Asset Previewer) you should see your see particle effect play at least once.</p>

<ol style="list-style-type: lower-alpha">
<li>
<p>NOTE: That the tools team is looking into a bug where particle effects do not play when first added (mentioned above) and so you’ll need to click the ‘Recook’ button in the top left within the ‘Global Previewer Info’ section in order to see your changes.</p>
</li>
</ol></li>
</ol>
<ol style="list-style-type: decimal">
<li>
<p>If the particle effect looks correct within the ‘Asset Previewer’ then all that’s left to do is tweak the cook parameters within the ‘Cook Params’ section to your desired values. If the particle effect does not look correct (typically because of unbound textures), then you’ll need to open the .ptl file via this button:</p>
</li>
</ol>

<p><img src="ParticleEffectsWorkflow/media/image2.jpg" alt="C:\6C2B1625\956122A8-36E4-41EE-B78C-8956EA84A4D0_files\image002.jpg" width="615" height="233" /></p>


<ol style="list-style-type: decimal">
<li>
<p>Within the .ptl document, you’ll want to take a look at the cook parameters and import any textures that are not bound. Because the tool automatically binds textures that have been imported previously, any unbound textures are new textures that need to be bound. You can bind the textures quickly using the below button and navigating to the named texture within your ArtDev directory:</p>
</li>
</ol>

<p><img src="ParticleEffectsWorkflow/media/image3.jpg" alt="C:\6C2B1625\956122A8-36E4-41EE-B78C-8956EA84A4D0_files\image003.jpg" width="612" height="148" /></p>


<ol style="list-style-type: decimal">
<li>
<p>After all textures have been bound, your vfx asset should now look correct. After this point, you should you should be able to save both your .ptl and save your vfx asset to a new name (and you should be free to close the .ptl – you can re-open it later if you need to bind additional textures, but otherwise, you don’t need to keep it open).</p>
</li>
<li>
<p>You can then go ahead and open the VFX.xlp and add the new asset there or you can open the particle effect in particle studio and tweak it further (using the tools hotload functionality to capture changes or reimporting manually).</p>
</li>
<li>
<p>After you get things to where you’d like them, save all modified documents.</p>
</li>
<li>
<p>If you’d like to see your changes in the game, you just need to ensure that you added your assets to the VFX.xlp and cooked the VFX.xlp (right-click Asset Cloud &gt; Cook Local Assets… &gt; Files… &gt; VFX.xlp). Launch the game and you can use the Asset Preview tab within the FireTuner2 to plop down your vfx in the game.</p>
</li>
</ol>
</div> <!-- panel body --> 
</div> <!-- panel -->

<div class="panel panel-primary" id="TerrainBounceLighting">
<div class="panel-heading">
<div class="panel-title">TerrainBounceLighting
</div>
</div>
<div class="panel-body">

<h1 id="terrain-bounce-lighting">Terrain Bounce Lighting</h1>
<p><span id="scroll-bookmark-1" class="anchor"></span><strong>Overview</strong></p>
<p><img src="TerrainBounceLighting/media/image1.png" alt="/download/attachments/59081138/image2015-10-19%2011%3A42%3A24.png?version=1&amp;modificationDate=1445269408300&amp;api=v2" width="434" height="249" /> <img src="TerrainBounceLighting/media/image2.png" alt="/download/attachments/59081138/image2015-10-19%2011%3A42%3A31.png?version=1&amp;modificationDate=1445269408300&amp;api=v2" width="434" height="249" /></p>
<p>We have the ability to do a crude approximation of bounced lighting of the directional light off of the terrain to help seat models onto the terrain. For visual inspection, this feature can be toggled via the “shaders bounce” console command. Each hex has a representative color that is calculated as a composite of artist supplied colors for terrain type, feature type and improvement type. These values are specified in the ArtDef for each of these different types. The field should be under &quot;Lighting&quot; and then &quot;BounceColor&quot;.</p>
<p><img src="TerrainBounceLighting/media/image3.png" alt="/download/attachments/59081138/image2015-10-19%2011%3A42%3A51.png?version=1&amp;modificationDate=1445269408283&amp;api=v2" width="359" height="249" /></p>
<p><strong>Layering</strong></p>
<p><strong><br />
</strong></p>
<p><img src="TerrainBounceLighting/media/image4.png" alt="/download/attachments/59081138/image2015-10-19%2011%3A43%3A17.png?version=1&amp;modificationDate=1445269408253&amp;api=v2" width="305" height="249" /></p>
<p>Some types also have a &quot;BounceAlpha&quot; which specifies how much that layer should override the layers under it. This feature can be used to:</p>
<p>1) <strong>Blend in the color of a feature</strong> - E.g. Shifting the color towards water color for marshland/flood plains, accounting for dirt decal placed under goody huts</p>
<p>2) <strong>Simulate ambient occlusion</strong> - Having a forest ramp down the bounce color of the terrain type makes sense</p>
<p><strong>Calculating Lighting</strong></p>
<p>The bounce lighting is simulated as a light source below the unit. The final bounce lighting color is the final hex color multiplied with the directional light color. The angle of the sun is also taken into account so that the effect is dimmed as the sun reaches the horizon. The effect also fades out vertically from the bottom of the model so large models that penetrate the terrain significantly may look strange as the falloff doesn’t follow the terrain surface</p>
</div> <!-- panel body --> 
</div> <!-- panel -->

<div class="panel panel-primary" id="TerrainOverview">
<div class="panel-heading">
<div class="panel-title">TerrainOverview
</div>
</div>
<div class="panel-body">

<p><span id="1" class="anchor"></span></p>
<p>Terrain Overview</p>
<p>Madrid</p>
<p>Exported on Jun 30, 2017</p>
<p><span id="scroll-bookmark-1" class="anchor"></span>The Strategic View uses a modified version of <em>offset blending</em> to render most of its terrain-based elements (i.e. terrain blending and the rendering of rivers, coastlines, the hex grid, and culture borders). Offset blending uses a <em>blend grid</em> to position all render elements. The blend grid is separate hex grid that is offset from the game grid by half a hex on both the Cartesian X and Y axes. In addition, where the game grid’s odd rows are offset along the positive Cartesian X axis, the blend grid’s odd rows are offset along the negative Cartesian Y axis. (Compare the game and blend grid’s plot [0, 1] in Figure 1.)</p>
<p>Figure 1 Figure 1: The game hex grid (black) and the blend hex grid (grey).</p>
<p><img src="TerrainOverview/media/image1.png" alt="Figure 1: The game hex grid (black) and the blend hex grid (grey)." width="566" height="452" /></p>
<p>Each blend hex overlaps three game hexes and conversely each game hex contains parts of three different blend hexes. (Game hex [1, 1] consists of blend hexes [1, 2], [2, 2], and [2, 1] in Figure 1.) The animated GIF in Figure 2 depicts the relationship between the blend hexes and the game hexes.</p>
<p>Figure 2 Figure 2: The relationship between the game grid and the blend grid.</p>
<p><img src="TerrainOverview/media/image2.png" alt="Figure 2: The relationship between the game grid and the blend grid." width="408" height="400" /></p>
<p>Because of this both sides of the edge between game hexes are contained within a single blend hex. This ensures that the blends between different terrain textures will always line up perfectly. The only drawback is that the blends from different blend textures have to line up at three of the hex’s six points (2, 6, and 10 o’clock).</p>
<p>In order to render the terrain system needs six textures:</p>
<ol style="list-style-type: decimal">
<li><p>the Terrain Blend Texture,</p></li>
<li><p>the Terrain Diffuse Texture covering the lower-right (red) part of the blend hex,</p></li>
<li><p>the Terrain Diffuse Texture covering the lower-left (green) part of the blend hex,</p></li>
<li><p>the Terrain Diffuse Texture covering the top (blue) part of the blend hex,</p></li>
<li><p>the Coastline / Riverbank Texture, and</p></li>
<li><p>the Culture Border / Hex Grid Texture.</p></li>
</ol>
<p>Unless noted otherwise the textures are all 256x256 uncompressed DDS files (8.8.8.8. ARGB 32 bpp | unsigned).</p>
<h1 id="terrain-blend-texture">Terrain Blend Texture</h1>
<p>The Terrain Blend Texture determines where each of the three Terrain Diffuse Textures gets rendered. The texture uses the red channel to place Terrain Diffuse Texture 1, the green channel to place Terrain Diffuse Texture 2, and the blue channel to place Terrain Diffuse Texture 3. The alpha channel is used to render the actual hex shape and prevent the rendering quads from visibly overlapping.</p>
<p>An example texture using straight lines to separate the three diffuse textures can be seen in Figure 3. A more advanced blending texture can be seen in Figure 4.)</p>
<p><img src="TerrainOverview/media/image3.png" alt="/download/attachments/166105140/image2017-6-14_10-33-35.png?version=1&amp;modificationDate=1497450815060&amp;api=v2" width="255" height="255" /><img src="TerrainOverview/media/image4.png" alt="/download/attachments/166105140/image2017-6-14_10-34-0.png?version=1&amp;modificationDate=1497450840313&amp;api=v2" width="255" height="255" /></p>
<table>
<thead>
<tr class="header">
<th><strong>Channels</strong></th>
<th><strong>Description</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>R</td>
<td>Bottom-right (red) terrain diffuse texture will be drawn here.</td>
</tr>
<tr class="even">
<td>G</td>
<td>Bottom-left (green) terrain diffuse texture will be drawn here.</td>
</tr>
<tr class="odd">
<td>B</td>
<td>Top (blue) terrain diffuse texture will be drawn here.</td>
</tr>
<tr class="even">
<td>A</td>
<td>Hex shape visibility to prevent quad overlap.</td>
</tr>
</tbody>
</table>
<h1 id="terrain-diffuse-textures">Terrain Diffuse Textures</h1>
<p>The three Terrain Diffuse Textures provide color information for the different terrain types. Ideally they are hex-tileable, i.e. each of the six hex edges matches its opposite edge perfectly.</p>
<p><img src="TerrainOverview/media/image5.png" alt="/download/attachments/166105140/image2017-6-14_10-47-35.png?version=1&amp;modificationDate=1497451655923&amp;api=v2" width="255" height="255" /><img src="TerrainOverview/media/image6.png" alt="/download/attachments/166105140/image2017-6-14_10-47-50.png?version=1&amp;modificationDate=1497451670440&amp;api=v2" width="255" height="255" /></p>
<table>
<thead>
<tr class="header">
<th><strong>Channels</strong></th>
<th><strong>Description</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>R, G , B</td>
<td>Diffuse color information for the terrain type.</td>
</tr>
<tr class="even">
<td>A</td>
<td>No information</td>
</tr>
</tbody>
</table>
<h1 id="the-coastline-riverbank-texture">The Coastline / Riverbank Texture</h1>
<p>The Coastline / Riverbank Texture stores the luminance information for the lines that represent the coastlines and the riverbanks as well as the placement information for the coastal outline / river water. Since the color will be superimposed on top of the terrain blending the location within the texture needs to only roughly follow the terrain blend.</p>
<p>The luminance information is expressed in nine (9) different layers stored in three (3) separate permutation textures:</p>
<ol style="list-style-type: decimal">
<li><p>right inside coastline / riverbank (stored in the first texture’s red channel),</p></li>
<li><p>right outside coastline / riverbank (stored in the first texture’s green channel),</p></li>
<li><p>left inside coastline / riverbank (stored in the second texture’s red channel),</p></li>
<li><p>left outside coastline / riverbank (stored in the second texture’s green channel),</p></li>
<li><p>top inside coastline / riverbank (stored in the third texture’s red channel),</p></li>
<li><p>top outside coastline / riverbank (stored in the third texture’s green channel),</p></li>
<li><p>left-corner dot coastline / riverbank (stored in the first texture’s blue channel),</p></li>
<li><p>right-corner dot coastline / riverbank (stored in the second texture’s blue channel), and</p></li>
<li><p>bottom-corner dot coastline / riverbank (stored in the third texture’s blue channel).</p></li>
</ol>
<p>The direction (right / left) describes which way the coastlines / riverbanks are turning – right means turning towards 2 o’clock, left means turning towards 10 o’clock. Inside / outside describes where the coastline / riverbank is placed in relationship to its respective terrain blend – inside means the coastline / riverbank overlaps the terrain blend, outside means it overlaps the remaining two terrain blends. The dot is required to connect combinations of coastlines / riverbanks that extend into neighboring blend hexes, e.g. two left inside coastlines / riverbanks arranged diagonally. The dots can most likely be authored once and reused.</p>
<p><img src="TerrainOverview/media/image7.png" alt="/download/attachments/166105140/image2017-6-14_10-50-46.png?version=1&amp;modificationDate=1497451846160&amp;api=v2" width="201" height="201" /><img src="TerrainOverview/media/image8.png" alt="/download/attachments/166105140/image2017-6-14_10-51-18.png?version=1&amp;modificationDate=1497451878663&amp;api=v2" width="201" height="201" /><img src="TerrainOverview/media/image9.png" alt="/download/attachments/166105140/image2017-6-14_10-51-53.png?version=1&amp;modificationDate=1497451913287&amp;api=v2" width="201" height="201" /></p>
<p>In addition to the luminance information for the coastline / riverbank lines the Coastline / Riverbank Texture stores placement information for the coastal outline / river water in the alpha channel of each of the three textures.</p>
<p><img src="TerrainOverview/media/image10.png" alt="/download/attachments/166105140/image2017-6-14_10-52-52.png?version=1&amp;modificationDate=1497451972350&amp;api=v2" width="201" height="201" /><img src="TerrainOverview/media/image11.png" alt="/download/attachments/166105140/image2017-6-14_10-53-26.png?version=1&amp;modificationDate=1497452006633&amp;api=v2" width="201" height="201" /><img src="TerrainOverview/media/image12.png" alt="/download/attachments/166105140/image2017-6-14_10-53-55.png?version=1&amp;modificationDate=1497452035463&amp;api=v2" width="201" height="201" /></p>
<p>Rivers can start in one of six directions within a blend hex (see Figure 13). Special variations of the Coastline / Riverbank Texture provide the luminance information for these cases and just like the dots can most likely be authored once and reused.</p>
<p>Figure 3 Figure 13: River source flow directions.</p>
<p><img src="TerrainOverview/media/image13.png" alt="Figure 13: River source flow directions." width="255" height="255" /></p>
<p>Unfortunately since the coastal outline needs to be wider than the river water area, the coastline textures and river textures cannot be shared.</p>
<table>
<thead>
<tr class="header">
<th><strong>Channels</strong></th>
<th><strong>Description</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>R</td>
<td>Inside coastline / riverbank luminance information.</td>
</tr>
<tr class="even">
<td>G</td>
<td>Outside coastline / riverbank luminance information.</td>
</tr>
<tr class="odd">
<td>B</td>
<td>Dot coastline / riverbank luminance information.</td>
</tr>
<tr class="even">
<td>A</td>
<td>Coastal outline / river water placement.</td>
</tr>
</tbody>
</table>
<h1 id="culture-border-hex-grid-texture">Culture Border / Hex Grid Texture</h1>
<p>The Culture Border / Hex Grid Texture stores the luminance (or possibly gradient lookup) information for culture borders as well as the hex grid luminance information. Since the color will be superimposed on top of the terrain blending or the coastlines / riverbanks the location within the texture needs to exactly match one of the previous two textures.</p>
<p>The luminance / gradient lookup information is expressed in nine (9) different layers stored in three (3) separate permutation textures:</p>
<ol style="list-style-type: decimal">
<li><p>right inside culture border (stored in the first texture’s red channel),</p></li>
<li><p>right outside culture border (stored in the first texture’s green channel),</p></li>
<li><p>left inside culture border (stored in the second texture’s red channel),</p></li>
<li><p>left outside culture border (stored in the second texture’s green channel),</p></li>
<li><p>top inside culture border (stored in the third texture’s red channel),</p></li>
<li><p>top outside culture border (stored in the third texture’s green channel),</p></li>
<li><p>left-corner dot culture border (stored in the first texture’s blue channel),</p></li>
<li><p>right-corner dot culture border (stored in the second texture’s blue channel), and</p></li>
<li><p>bottom-corner dot culture border (stored in the third texture’s blue channel).</p></li>
</ol>
<p>The direction (right / left) describes which way culture border is turning – right means turning towards 2 o’clock, left means turning towards 10 o’clock. Inside / outside describes where the culture border is placed in relationship to its respective terrain blend – inside means the culture border overlaps the terrain blend, outside means it overlaps the remaining two terrain blends. The dot is required to connect combinations of culture borders that extend into neighboring blend hexes, e.g. two left inside culture borders arranged diagonally. The dots can most likely be authored once and reused.</p>
<p><img src="TerrainOverview/media/image14.png" alt="/download/attachments/166105140/image2017-6-14_11-0-29.png?version=1&amp;modificationDate=1497452429657&amp;api=v2" width="201" height="201" /><img src="TerrainOverview/media/image15.png" alt="/download/attachments/166105140/image2017-6-14_11-1-4.png?version=1&amp;modificationDate=1497452464283&amp;api=v2" width="201" height="201" /><img src="TerrainOverview/media/image16.png" alt="/download/attachments/166105140/image2017-6-14_11-1-32.png?version=1&amp;modificationDate=1497452492237&amp;api=v2" width="201" height="201" /></p>
<p>In addition to the luminance / gradient lookup information for the culture border the Culture Border / Hex Grid Texture stores the hex grid luminance information in the alpha channel of each of the three textures.</p>
<p>Figure 4 Figure 17: Hex grid luminance information.</p>
<p><img src="TerrainOverview/media/image17.png" alt="Figure 17: Hex grid luminance information." width="255" height="255" /></p>
<p>The Culture Border / Hex Grid Texture is tightly coupled to either the terrain blend shapes of the Terrain Blend Texture or the coastline / riverbank shapes of the Coastline / Riverbank Texture and cannot therefore be associated with both of them at the same time.</p>
<table>
<thead>
<tr class="header">
<th><strong>Channels</strong></th>
<th><strong>Description</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>R</td>
<td>Inside culture border luminance / gradient lookup information.</td>
</tr>
<tr class="even">
<td>G</td>
<td>Outside culture border luminance / gradient lookup information.</td>
</tr>
<tr class="odd">
<td>B</td>
<td>Dot culture border luminance / gradient lookup information.</td>
</tr>
<tr class="even">
<td>A</td>
<td>Hex grid luminance information.</td>
</tr>
</tbody>
</table>
<h1 id="authoring-and-runtime">Authoring and Runtime</h1>
<p>(For a detailed walk-through of how to author the terrain blend textures see the Base game's Art OneNote, StrategicView, Generating Terrain Blends.)</p>
<p>Each terrain blend (with or without corresponding coastline / riverbank) is authored in a single PSD file with many layers. The export process takes care of encoding the layers in different texture channels and assigns them to textures. The cooker then creates all possible permutations of coastlines, riverbanks, and culture borders and stores all of them as separate entries in the BLP. At runtime the engine simply selects the appropriate BLP entry based on the procedurally generated terrain.</p>
<p>In the table below the Group column specifies which layers have to present for a terrain blend PSD to be valid:</p>
<ul>
<li><p>Base represents a terrain blend that can be applied to any blend tile that has no river banks, sources or coastlines present.</p></li>
<li><p>Channel must include all Base layers in addition to its own and represents a terrain blend that can be applied to a tile that has either coastlines or river banks, but no sources, in addition to any blend tiles that Base can be applied to.</p></li>
<li><p>Source must include all Base and Channel layers in addition to its own and represents the full terrain blend that can be applied to any blend tile, including one with river sources.</p></li>
</ul>
<table>
<thead>
<tr class="header">
<th>Group</th>
<th>Layer</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Base</td>
<td>TerrainBlend</td>
</tr>
<tr class="even">
<td></td>
<td>CultureBorder_Right</td>
</tr>
<tr class="odd">
<td></td>
<td>CultureBorder_Left</td>
</tr>
<tr class="even">
<td></td>
<td>CultureBorder_Top</td>
</tr>
<tr class="odd">
<td></td>
<td>RiverbankCorners_CultureBorder_RightBottom</td>
</tr>
<tr class="even">
<td></td>
<td>RiverbankCorners_CultureBorder_RightTop</td>
</tr>
<tr class="odd">
<td></td>
<td>RiverbankCorners_CultureBorder_RightTopAndBottom</td>
</tr>
<tr class="even">
<td></td>
<td>RiverbankCorners_CultureBorder_LeftBottom</td>
</tr>
<tr class="odd">
<td></td>
<td>RiverbankCorners_CultureBorder_LeftTop</td>
</tr>
<tr class="even">
<td></td>
<td>RiverbankCorners_CultureBorder_LeftTopAndBottom</td>
</tr>
<tr class="odd">
<td></td>
<td>RiverbankCorners_CultureBorder_TopLeft</td>
</tr>
<tr class="even">
<td></td>
<td>RiverbankCorners_CultureBorder_TopRight</td>
</tr>
<tr class="odd">
<td></td>
<td>RiverbankCorners_CultureBorder_TopRightAndLeft</td>
</tr>
<tr class="even">
<td>Channel</td>
<td>RiverbankChannelRight_ChannelBottomThin</td>
</tr>
<tr class="odd">
<td></td>
<td>RiverbankChannelRight_ChannelBottomThin_CultureBorder_Left</td>
</tr>
<tr class="even">
<td></td>
<td>RiverbankChannelRight_ChannelBottomThin_CultureBorder_Right</td>
</tr>
<tr class="odd">
<td></td>
<td>RiverbankChannelRight_ChannelBottomThin_CultureBorder_Top</td>
</tr>
<tr class="even">
<td></td>
<td>RiverbankChannelRight_ChannelBottomFat</td>
</tr>
<tr class="odd">
<td></td>
<td>RiverbankChannelLeft_ChannelBottomThin</td>
</tr>
<tr class="even">
<td></td>
<td>RiverbankChannelLeft_ChannelBottomThin_CultureBorder_Left</td>
</tr>
<tr class="odd">
<td></td>
<td>RiverbankChannelLeft_ChannelBottomThin_CultureBorder_Right</td>
</tr>
<tr class="even">
<td></td>
<td>RiverbankChannelLeft_ChannelBottomThin_CultureBorder_Top</td>
</tr>
<tr class="odd">
<td></td>
<td>RiverbankChannelLeft_ChannelBottomFat</td>
</tr>
<tr class="even">
<td></td>
<td>RiverbankChannelRight_ChannelLeft</td>
</tr>
<tr class="odd">
<td></td>
<td>RiverbankChannelRight_ChannelLeft_CultureBorder_Left</td>
</tr>
<tr class="even">
<td></td>
<td>RiverbankChannelRight_ChannelLeft_CultureBorder_Right</td>
</tr>
<tr class="odd">
<td></td>
<td>RiverbankChannelRight_ChannelLeft_CultureBorder_Top</td>
</tr>
<tr class="even">
<td>Source</td>
<td>RiverbankSourceRight</td>
</tr>
<tr class="odd">
<td></td>
<td>RiverbankSourceRight_CultureBorder_Right</td>
</tr>
<tr class="even">
<td></td>
<td>RiverbankSourceRight_CultureBorder_Top</td>
</tr>
<tr class="odd">
<td></td>
<td>RiverbankSourceRight_ChannelBottomThin</td>
</tr>
<tr class="even">
<td></td>
<td>RiverbankSourceRight_ChannelBottomThin_CultureBorder_Right</td>
</tr>
<tr class="odd">
<td></td>
<td>RiverbankSourceRight_ChannelBottomThin_CultureBorder_Top</td>
</tr>
<tr class="even">
<td></td>
<td>RiverbankSourceRight_ChannelBottomFat</td>
</tr>
<tr class="odd">
<td></td>
<td>RiverbankSourceRight_ChannelLeft_ChannelBottomThin</td>
</tr>
<tr class="even">
<td></td>
<td>RiverbankSourceRight_ChannelLeft_ChannelBottomThin_CultureBorder_Top</td>
</tr>
<tr class="odd">
<td></td>
<td>RiverbankSourceRight_ChannelLeft_ChannelBottomFat</td>
</tr>
<tr class="even">
<td></td>
<td>RiverbankSourceRight_ChannelLeft</td>
</tr>
<tr class="odd">
<td></td>
<td>RiverbankSourceRight_ChannelLeft_CultureBorder_Right</td>
</tr>
<tr class="even">
<td></td>
<td>RiverbankSourceRight_SourceLeft_ChannelBottomThin</td>
</tr>
<tr class="odd">
<td></td>
<td>RiverbankSourceRight_SourceLeft_ChannelBottomThin_CultureBorder_Left</td>
</tr>
<tr class="even">
<td></td>
<td>RiverbankSourceRight_SourceLeft_ChannelBottomThin_CultureBorder_Top</td>
</tr>
<tr class="odd">
<td></td>
<td>RiverbankSourceRight_SourceLeft_ChannelBottomFat</td>
</tr>
<tr class="even">
<td></td>
<td>RiverbankSourceRight_SourceBottom_ChannelLeft</td>
</tr>
<tr class="odd">
<td></td>
<td>RiverbankSourceRight_SourceBottom_ChannelLeft_CultureBorder_Left</td>
</tr>
<tr class="even">
<td></td>
<td>RiverbankSourceRight_SourceBottom_ChannelLeft_CultureBorder_Right</td>
</tr>
<tr class="odd">
<td></td>
<td>RiverbankSourceLeft</td>
</tr>
<tr class="even">
<td></td>
<td>RiverbankSourceLeft_CultureBorder_Left</td>
</tr>
<tr class="odd">
<td></td>
<td>RiverbankSourceLeft_CultureBorder_Top</td>
</tr>
<tr class="even">
<td></td>
<td>RiverbankSourceLeft_ChannelRight_ChannelBottomThin</td>
</tr>
<tr class="odd">
<td></td>
<td>RiverbankSourceLeft_ChannelRight_ChannelBottomThin_CultureBorder_Top</td>
</tr>
<tr class="even">
<td></td>
<td>RiverbankSourceLeft_ChannelRight_ChannelBottomFat</td>
</tr>
<tr class="odd">
<td></td>
<td>RiverbankSourceLeft_ChannelBottomThin</td>
</tr>
<tr class="even">
<td></td>
<td>RiverbankSourceLeft_ChannelBottomThin_CultureBorder_Top</td>
</tr>
<tr class="odd">
<td></td>
<td>RiverbankSourceLeft_ChannelBottomFat</td>
</tr>
<tr class="even">
<td></td>
<td>RiverbankSourceLeft_ChannelRight</td>
</tr>
<tr class="odd">
<td></td>
<td>RiverbankSourceLeft_ChannelRight_CultureBorder_Left</td>
</tr>
<tr class="even">
<td></td>
<td>RiverbankSourceLeft_SourceBottom_ChannelRight</td>
</tr>
<tr class="odd">
<td></td>
<td>RiverbankSourceLeft_SourceBottom_ChannelRight_CultureBorder_Left</td>
</tr>
<tr class="even">
<td></td>
<td>RiverbankSourceLeft_SourceBottom_ChannelRight_CultureBorder_Right</td>
</tr>
<tr class="odd">
<td></td>
<td>RiverbankSourceBottom_Thin</td>
</tr>
<tr class="even">
<td></td>
<td>RiverbankSourceBottom_Thin_CultureBorder_Left</td>
</tr>
<tr class="odd">
<td></td>
<td>RiverbankSourceBottom_Thin_CultureBorder_Right</td>
</tr>
<tr class="even">
<td></td>
<td>RiverbankSourceBottom_Fat</td>
</tr>
<tr class="odd">
<td></td>
<td>RiverbankSourceBottom_ChannelRight</td>
</tr>
<tr class="even">
<td></td>
<td>RiverbankSourceBottom_ChannelRight_CultureBorder_Left</td>
</tr>
<tr class="odd">
<td></td>
<td>RiverbankSourceBottom_ChannelLeft</td>
</tr>
<tr class="even">
<td></td>
<td>RiverbankSourceBottom_ChannelLeft_CultureBorder_Right</td>
</tr>
<tr class="odd">
<td></td>
<td>RiverbankSourceBottom_ChannelRight_ChannelLeft</td>
</tr>
<tr class="even">
<td></td>
<td>RiverbankSourceRight_SourceLeft_SourceBottom</td>
</tr>
</tbody>
</table>
<p>Additionally, the following four textures are part of a separate terrain blend corners PSD, because they do not depend on the individual terrain blends:</p>
<table>
<thead>
<tr class="header">
<th>Corners</th>
<th>CultureBorderCorners_All</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td>RiverbankCorners_All</td>
</tr>
<tr class="even">
<td></td>
<td>RiverbankWaterCorners_All</td>
</tr>
<tr class="odd">
<td></td>
<td>RiverbankCorners_CultureBorder_All</td>
</tr>
</tbody>
</table>
</div> <!-- panel body --> 
</div> <!-- panel -->

<div class="panel panel-primary" id="Texture">
<div class="panel-heading">
<div class="panel-title">Texture
</div>
</div>
<div class="panel-body">

<p>Texture (.tex)</p>
<p>Texture are the entities that represent pixel data, these are used for the different maps in a material, or they can be used for UI, or as sprites in the strategic view layer.</p>

<p>The engine currently supports two different source formats for creating Textures: TGA, and PSD. You can create textures using either the Asset Editor (one at a time) or using the Asset Importer (many at once as long as they come from the same source file).</p>

<p>Using the Asset Editor</p>
<p>The Asset Editor allows you to create one texture at a time by first creating the entity and then selecting the texture class and other parameters.</p>

<p>From TGA</p>
<ul>
<li>
<p>In the Asset Editor, go to <strong>File &gt; New</strong></p>
</li>
<li>
<p>You'll be prompted to pick what type of file you'd like to create. Pick <strong>Texture</strong>, and hit <strong>OK</strong></p>
</li>
</ul>


<p><img src="Texture/media/image1.png" width="624" height="477" /></p>

<ul>
<li>
<p>Now you need to pick the Class for the texture you're creating by selecting it from the <strong>ClassName</strong> dropdown</p>
</li>
</ul>


<p><img src="Texture/media/image2.png" width="624" height="439" /></p>


<ul>
<li>
<p>Now you need to assign your source file to the texture, so click on the <strong>Source File Path</strong> line and the browse button will appear. click the and it will bring up a browser where you can navigate to your .tga file</p>
</li>
</ul>


<p><img src="Texture/media/image3.png" width="622" height="394" /></p>


<ul>
<li>
<p>Once you pick a source file, you'll see the <strong>Name</strong> of the Texture change to match the name of the source file, it will also attempt to import the source file at this point.</p>
</li>
<li>
<p>If you want you can change the <strong>Name</strong> of the texture to whatever you want</p>
</li>
<li>
<p>At the bottom of the window you can also tweak the Texture's Export Settings</p>
</li>
<li>
<p>Finally you need to save your Texture by going to <strong>File &gt; Save</strong></p>
</li>
</ul>
</div> <!-- panel body --> 
</div> <!-- panel -->

<div class="panel panel-primary" id="TextureExportSettings">
<div class="panel-heading">
<div class="panel-title">TextureExportSettings
</div>
</div>
<div class="panel-body">

<p>Texture Export Settings</p>
<p>Thursday, April 09, 2015</p>
<p>12:19 PM</p>

<p>Pixel Format:</p>

<p>This is the actual Texture data format that will get exported and used in the engine. This is decided by the engineer that defined the class and is not modifiable at the import stage</p>


<p>Filter Type:</p>

<p>This is the algorithm that the cooker will use to generate the texture mip maps. Unfortunately it can be tricky to pick the right filter to use because they all have different performance characteristics that depend heavily on the type of content in the image (Some are better for texture with a lot of small details, while others are good for textures with sharp straight edges). The full discussion of what filter to use is beyond the scope of this documentation, but feel free to discuss it with your local graphics engineer if you're interested. By default we use the Box filter which will tend to make things look a bit blurrier at a distance, but it's very fast to compute, and does not tend to produce visual artifacts at a distance.</p>


<p>Sample From Top:</p>

<p>This is used to tell the Mip map generation step to calculate every mip based on the highest resolution rather than the mip step before it. Enabling it will generally produce slightly better results, but can become extremely slow to compute if the texture is large (over 1k per size)</p>


<p>Export Mode:</p>

<p>This lets you pick between the default texture export and mip generation or use the mips set up manually in the source file</p>
<p><img src="TextureExportSettings/media/image1.png" alt="Machine generated alternative text: " width="442" height="221" /></p>
<p><em>This is how your source file how to look like when setting up manual mips.</em></p>


<p>Use Mips:</p>

<p>I'm not sure what this does…</p>


<p>Number of Manual Mips:</p>

<p>If you've only created a certain number of mip levels manually you can set that number here.</p>


<p>Complete Mip Chain:</p>

<p>If you generated all the mips levels manually check this box, otherwise it will use the <strong>Number of Manual Mips</strong></p>


<p>Value Clamp Max/Min:</p>

<p>This sets the maximum and minimum values that are allowed inside the texture, and it will clamp any pixels that go beyond those</p>


<p>Scale:</p>

<p>This lets you override the pixel size at which the texture will be exported (If you authored your texture at a really large size, but you don't mind it being scaled down before getting into the cloud)</p>



</div> <!-- panel body --> 
</div> <!-- panel -->

<div class="panel panel-primary" id="The%20Life%20of%20a%20Leader">
<div class="panel-heading">
<div class="panel-title">The Life of a Leader
</div>
</div>
<div class="panel-body">

<p><img src="The Life of a Leader/media/image1.png" width="585" height="391" /></p>
<p>Leaders make up arguably the most expensive aspects of Civ VI. Whether it be through the months it takes to create a fully animated leader, or the complexities of the different cultural costumes, Leaders are a challenge. Within this paper we hope to document the process of creating one of these guys the best we know how.<br />
<br />
To begin the creation of such a complicated moving piece, we start like most other concepts in game development: a conversation.</p>
<p><strong>The Kick Off:<br />
</strong><br />
Once we have the idea of who the civilization is and who the leader for the civ will be, we sit down as a team and go over any and all ideas for production. During this time a rough sketch from concept (or a few) may be presented, and we discuss any and all ideas modeling and animation might have for this leader.</p>
<p><img src="The Life of a Leader/media/image2.jpeg" /></p>
<p>The concept ref folder is very important. This is a folder of images collected by concept and is used throughout the pipeline. Within this folder are general cultural notes on clothing, color, and alternative pieces of props and items that modeling can sort through</p>
<p><img src="The Life of a Leader/media/image3.png" alt="C:\Users\mkean\AppData\Local\Microsoft\Windows\INetCache\Content.Word\Capture2.png" width="317" height="245" /></p>
<p><strong>Voice Work:</strong></p>
<p>An incredibly important aspect of the pipeline often left towards the end is the VO recording of the leader dialogue. Once we have a personality established and an understanding of the general look of the culture, the writers go and begin assembling the script that the leader will say. The hope in this is that modeling will begin with the line recorded so that we hit the 3D part of the pipeline with all the information we need.</p>
<p>It is important to note here that design is set on the VO lines to be recorded. There should be no lines recorded that design is no longer considering or are ambivalent on. This way, down the pipeline, no time is wasted reviewing and choosing between lines that are not even an option.</p>
<p><img src="The Life of a Leader/media/image4.jpeg" width="297" height="416" /></p>
<p><strong>Concept: </strong></p>
<p>Once the meeting is over, concept and modeling meet to discuss the next step forward. The usual next step is for concept to begin blocking the more final ideas.</p>
<p>When audition VO is recorded, Animation will start shooting test reference to explore ways in which the Leader might move and behave. This will help inform Concept as they finalize their ideas.</p>
<p>Once we really start to jive on where the concept is going it is presented for final feedback. Usually this is the hand-off stage, a place where modeling can begin. Here modeling deems if there is everything they need (or at least a good chunk of it there), to begin and if there might be any red flags. At this point we should all be on board with the general idea of who this leader is.</p>
<p><img src="The Life of a Leader/media/image5.jpeg" width="358" height="427" /></p>
<p><strong>Final Concept?</strong></p>
<p>Though we try not to go back to 2D sketches very often, there are chances that concept will continue to refine ideas found within the concept, or attempt new color pallet ideas.</p>
<p>Modeling can pull from the new ideas if need be or use them to try out different versions of the final leader textures.</p>
<p>Also, at times, paint overs will be required for the block-in to feel right, these tend to become the base for more final drawings later on.</p>
<p><img src="The Life of a Leader/media/image6.png" width="235" height="274" /></p>
<p><strong>Modeling:</strong><br />
<br />
Starting with one of the base meshes we use for the leaders, modeling begins to block in a sculpt for which we can give rough feedback on. This block in usually includes a facial pass and a rough estimate of the forms of the clothing. We can begin to break things down here. We decide a bunch of things at this stage as well, like whether or not to use marvelous designer for the clothing, and how much will be done with substance. Usually at the point, during the translation of 2D to 3D the red flags will appear. Concept usually gets pinged again and we go back and forth a bit, but only if there is difficulties in the translation. Modeling attempts to have most forms blocked in rough. Better to have and not need than to miss something.</p>
<p>Once we are good with the blocking we begin the process of the final high poly. This is the stage in which the models become bit more realized. Within Zbrush we attempt to give some material definition in the sculpt itself (not too much as most of the heavy lifting will be done in substance) and clean up any gummy forms. Things are broken out and separated. The modeler begins to think about the low poly form and how he or she will retopo the pieces for the low poly.<br />
<br />
Within this section are a many smaller tasks that don’t always happen on all the leaders. If marvelous designer was used, we then go in a cleanup those meshes, as they are usually triangulated and at a much high fidelity than what we can realistically render. One of the things we find is baked in wrinkles don’t look very good if they do not move. If the character has a lot of hard surface pieces (armor), then we begin to separate those out, and figure which parts will be separate or not.</p>
<p><img src="The Life of a Leader/media/image7.png" /></p>
<p>Once we are happy with the high poly we begin the process of generating the lowpoly model. Though software may differ to retopologize, we generally either use topogun or Maya to model on top of the high poly.</p>
<p><img src="The Life of a Leader/media/image8.png" alt="C:\Users\mkean\AppData\Local\Microsoft\Windows\INetCache\Content.Word\Capture.png" width="282" height="360" /></p>
<p>Items that may be mirrored and elements of UVing are thought about. Many times a back and forth is created between the high poly and low poly, reprojecting and adjusting the mesh to generate the cleanest model we can.</p>
<p><img src="The Life of a Leader/media/image9.png" alt="C:\Users\mkean\AppData\Local\Microsoft\Windows\INetCache\Content.Word\Capture2.png" width="228" height="228" /><img src="The Life of a Leader/media/image10.png" alt="C:\Users\mkean\AppData\Local\Microsoft\Windows\INetCache\Content.Word\Capture2.png" width="225" height="219" /></p>
<p>Using a program like UV layout, we quickly jump back and forth between it and Maya, adjusting meshes as we go to get the cleanest UV’s as we can. UVs are done in a linear fashion</p>
<p>The reasoning here is that any and all stretching will be due to the mesh itself will not be noticeable. Also our texture pipeline deals mostly in tiling textures, so they tend to apply better when a linear UV is present.</p>
<p>Once the UVs are done and packed, we throw a Texel texture on there to makes sure everything is around the same density. I say around, because we do cheat at times cramming more detail into items we deem to be POI’s (points of interests). Any POI tends to get a little more Texel resolution.</p>
<p>We make our way over to marmoset where we begin our first HUB program. In our pipeline the art resources are captured into two HUB programs:</p>
<p>Marmoset for all highpoly and lowpoly bake meshes</p>
<p>Substance for all textures and source textures.</p>
<p>This keeps things clean and creates a “living pipeline”.</p>
<p>By this we mean that everything in marmoset is live-linked to the source assets location on the drive, so if that updates so does the marmoset scene, and that in turn cranks out a normal map in real-time, that is then pumped back into substance…etc. etc. Basically each adjustment we make can trickle through the texture pipeline with relative ease, though that’s not always the case.</p>
<p><img src="The Life of a Leader/media/image11.png" /></p>
<p>Baking In marmoset is easy, and is one of the few programs (outside of Maya and substance) that the modeling team is hard locked into using. Bake consistency is everything, and being able to rely on the same kind of normal quality and Ambient occlusion quality (the two maps we bake) makes everything down the line that much easier. After grouping the high polys and the low polys in their respective groups it’s as simple as clicking “Bake” and then adjusting the automated cage mesh and normal skew using the brushed provided to create a clean bake.</p>
<p><img src="The Life of a Leader/media/image12.png" alt="C:\Users\mkean\AppData\Local\Microsoft\Windows\INetCache\Content.Word\screenshot054.png" width="343" height="397" /></p>
<p>Continuing the modeling pipeline, we plug into substance the low poly and all the source textures we created (normal and AO) and use substance’s internal map converter to create the other maps need. Its cleaner this way, and smart materials assume these maps to be created in this fashion. Then it’s a generic substance workflow in which we are blocking in materials based on concept, and adjusting materials as we need them to be adjusted as ideas hit us. Because we have the civ tech shader inside of painter, this allows us to live a bit inside of substance before we make our way into the engine.</p>
<p><img src="The Life of a Leader/media/image13.png" /></p>
<p>Using our premade civtech export preset, we export our textures after we have blocked them in a bit. After that we load up the asset editor and create a leader asset in the engine. This consists of us selecting the asset type and importing the geometry from Maya into the scene. Then we create a shader for the skin and clothing.</p>
<p>Once modeling sets this all up, we begin to go back and forth between the engine and substance, as all textures update live and can be iterated on fairly easily.</p>
<p>The leaders have two shader types for clothing, a cloth shader and an all-purpose uber-shader for everything else. The mesh definitions for these shaders are done in Maya, by assigning a material to the mesh. Each material in Maya is read as a material group and therefore able to have a material assigned to it.</p>
<p>This leads us to a textured version that is ready for initial feedback.</p>
<p><img src="The Life of a Leader/media/image14.png" /></p>
<p><strong>Animation:</strong></p>
<p>Final VO has been recorded by now. Animators choose the lines they will use. Animators re-synch with writers and designers on VO choices. These VO lines and deliveries inform the animators on how to pose the leader in their base set.</p>
<p><strong>Poses to test:</strong></p>
<p>Arms across the chest, arms down by their sides, and hands clasped in front to check proportions and to make sure the Leader can look relaxed. This can result in model change requests</p>
<p><img src="The Life of a Leader/media/image15.jpeg" alt="TestPoses" width="519" height="251" /></p>
<p>IK and FK switches with props, the torso twists and folds, foot roll, and finger skinning. We do a thorough investigation of every control on the body. Making a fist, facial poses, and mouth shapes. We need to see that the character can make a convincing O, M, and T shape, puff their cheeks, and close their eyes. We want to see that the eyebrows can make appealing shapes.</p>
<p><img src="The Life of a Leader/media/image16.jpeg" alt="Tshape" width="153" height="93" /><img src="The Life of a Leader/media/image17.jpeg" alt="Mshape" width="148" height="95" /><img src="The Life of a Leader/media/image18.jpeg" alt="OShape" width="135" height="94" /><img src="The Life of a Leader/media/image19.jpeg" alt="Eyebrows" width="154" height="94" /></p>
<p>Animation starts to create and evaluate base idle poses with a functional rig. [happy, neutral, unhappy].</p>
<p><img src="The Life of a Leader/media/image20.png" /></p>
<p>This is massively informative for a few reasons, such as seeing how the poses react to basic lighting and seeing how the proportions of the character hold up. Around this time, we all meet up and take a look at the poses and discuss changes that need to happen. As stated before, at time this includes modeling changes, as well as rig and weighting adjustments. Rigging and modeling might get another round of notes to finalize the rig.</p>
<p>Lighting does an initial pass here with the base poses.</p>
<p><img src="The Life of a Leader/media/image21.png" width="279" height="235" /></p>
<p>The animator shoots reference video of VO lines and Base set using chosen idle poses. Acting choices are made and approved by Animation Lead.</p>
<p><strong>Blocking</strong></p>
<p>Blocking is when the animator picks their main poses out that describe the acting. They time these poses out approximately. While doing this process discoveries can be made about the limitations and differences between the rig compared to what the reference does. This is the part of the process where we can make big acting changes and timing changes. We can go back and re-shoot reference if needed.</p>
<p>Blocking passes can be in stepped mode or splined and smooth. The thing that makes them a blocking pass is that they lack the detail that a polished pass has. There may be some facial poses but not all. The points at which hands switch from IK to FK may NOT be smoothed. All we need to glean from the blocking pass is the animator’s intent.</p>
<p><strong>Splining</strong></p>
<p>After the animator has an approved blocking pass they go on to add in the detail. The lip synch is added, switches are smooth out, and hitches are cleaned up. Timing is tightened. If the blocking pass was in stepped mode the animator changes over to smooth splined. More transitional poses are added to better describe actions.</p>
<p><strong>Polish</strong></p>
<p>Now the animation is smooth and has everything it needs to make sense and be workable. What it lacks is the fine tuning. In the polish pass we take another visit to the eyes, the pupils, the eyebrows. We add in fine eye movements. We take another pass on the fingers to make sure all contact points feel believable. We make everything feel like butter</p>
<p><strong>Testing in Editor and Game</strong></p>
<p>Throughout animation process animation tests animations out in asset editor and game. This makes sure we are seeing the true aim of their eyes, spot issues with compression and blending. Keep up to date and see what changes the other departments have been making to the character and make sure those changes are working well.</p>
<p>Meanwhile…materials begin to finalize. Lighting continues to be adjusted. We do not animate and texture to a lighting set up, rather the lighting set up is created to what we make.</p>
<p><strong>Stitching</strong></p>
<p>When multiple animators have worked on one character that requires dynamics, stitching is required.</p>
<p>This allows for dynamics to be done on the entire string of animations together and provides a massive time savings.</p>
<p><img src="The Life of a Leader/media/image22.png" width="385" height="288" /></p>
<p>As animation gets closer to being ready for feedback we begin a cycle of adjustments and model tweaks. Usually the animation lead and modeling lead sit down and fine tune things. Modeling gives notes on how they intended things to look, and animation has a more clear presentation with what they intend to do with the character.<br />
<br />
With animation going along, lighting begins its process, blocking in something that works with the idle poses. It will continue to be revised as the animations and materials begin to finalize. We do not animate and texture to a lighting set up, rather the lighting set up is created to what we make.</p>
<p>To stitch, animation uses RedNine to bring all animations for VO into one VO file and all animations for the Base set into one Base Set file.</p>
<p>Once the stitching happens, all large form animation changes halt and small form facial and hand tweaks continue. Material work from modeling happens as well, but at this point most modeling tweaks halt, and become on request only. Animators work only in the stitched file to make tweaks.</p>
<p>In Civ none of the dynamic items (cloth, necklaces, etc) are done in realtime. We must bake out simulations done within Maya.</p>
<p>Audio can start a pass of sound effects now. Animation and dynamics are mostly tied down.<br />
<br />
Finally, we begin the final polish stages. As Dynamics get finalized, we begin to review how it all fits together. Lighting gets tweaked to the backgrounds (intensity) and we start to lay in the final material tweaks and such. Final bug lists get cleared and hopefully if all is said and done correctly we should be left with a leader scene that doesn’t clash with what we did on the base game.</p>
<p>Audio can now completely have at it now to drive it home.</p>
</div> <!-- panel body --> 
</div> <!-- panel -->

<div class="panel panel-primary" id="TileBase">
<div class="panel-heading">
<div class="panel-title">TileBase
</div>
</div>
<div class="panel-body">

<p>Tile Base</p>
<p>Monday, March 30, 2015</p>
<p>3:54 PM</p>
<p>The Tilebases in Civ 6 have a pretty complex pipeline in order to support the procedural building placement, as well as model and material sharing. Each Tilebase is built out of a Base asset which has attachment point where other Tilebase assets get slotted into in the game.</p>

<p><img src="TileBase/media/image1.png" alt="Machine generated alternative text: chm Point Attachment Asset (i.e.Tent 01) Base Asset (i.e. Encampment) chm Attachment Asset (i.e.Tent 01) Attachment Asset (i.e.Tent 01) Poin Attachment Asset (i.e.Tent 01) " width="550" height="279" /></p>
<p>Following is a set of step to build a Tilebase asset. This is not the only way to build one, but this should explain all the pieces required and from there you can build them in the way that suits the needs of the Tilebase you are building</p>

<p>Prescribed Steps to build a Tilebase:</p>

<p>Step 1: Build your Max scene file:</p>
<p>Build your Max File. The Max scene should be composed of the pieces that the Tilebase is built from, and then copies of those objects, where each copy is named the same thing as the initial piece with a number added at the end. All the object copies should be parented under a root bone that is named the name of the Base Asset (Talk to your lead about what the naming conventions are). Here is an example of what your Max scene should look like:</p>

<p><img src="TileBase/media/image2.png" alt="Machine generated alternative text: Select Display Edit Name Houseoos House007 LamppostOOI Lamppost002 Lamppost003 PineTreeOOI PineTree003 PineTree004 PineTreeoos PineTree006 PineTree007 PineTreeoog PineTreeOIO PineTreeSmaIOOI PineTreeSma11002 PineTreesma11003 PineTreeSma11004 PineTreeSma11005 PineTreesma11007 PineTreeSma11008 PineTreeSmaIIOOg House Lamppost PineTree PineTreeSmaII Workspace: Default (Perspective) (Realistic) These will become the attachment points of the Base Asset where the Attachment Assets will slot into These will become the Attachment Assets Autodesk 3 cls Max 2015 Tilebase_SampIeA55et.max 0/0 This will become the Base Asset " width="691" height="579" /></p>

<p>Note: Keep in mind that the engine will try to help you by automatically assigning material to your assets if the name of the material assigned to them in Max/Maya matches the name of a compatible material in the Asset Cloud.</p>

<p>Once you have your scene laid out the way you want, you need to run the <strong>'TileBase Cleanup'</strong> script that will convert all the object copies into Points with the same name so that they get imported as bones into the engine rather than as meshes:</p>



<ul>
<li>
<p>Select the Root Bone/Point that has all the piece copies parented to it</p>
</li>
<li>
<p>Run the '<strong>TileBase Cleanup</strong>' script which is under '<strong>Civ 6 Tools</strong>' (the image shows one way to get to the script)</p>
</li>
<li>
<p><img src="TileBase/media/image3.png" alt="Machine generated alternative text: 10 Tilebase Cleanup Do Cleanup Undo Cleanup Utilibes Sets More... Asset ar owser Perspective Match Collapse Color Clipboard Measure MO bon Capture Rese t XF orm Flight Studio (c) MAX Script Open Listener New Script Open Script Run Script Utilities Civ S Tools Civ 6 Tools Amma bon Manager Model Manager Clean Scene TileBase Cleanup Close " width="318" height="639" /></p>
</li>
<li>
<p>Click the '<strong>Do Cleanup</strong>' button in the tool's dialog box.</p>
</li>
<li>
<p>You will see a Point appear at the position of every object under the root.</p>
</li>
<li>
<p>Save your Max file, it's ready to be imported into the engine.</p>
</li>
</ul>

<p>Create an asset for each model in the Max File:</p>
<p>We have a script that will automatically turn each model in you Max file into an asset. Go to '<em><strong>File &gt; Run Script</strong></em>' and load the script &quot;<em><strong>C:\Program Files\Civ6\Asset Cloud - Civ6\AssetEditor\Scripts\Create_Assets_From_Source_File.py</strong></em>&quot;. The script will bring up a prompt asking for what asset class should the Assets be, select &quot;<strong>TileBase</strong>&quot; and click <strong>'OK'</strong></p>

<p><img src="TileBase/media/image4.png" alt="Machine generated alternative text: Please Pick the Asset Class to use This script wil create individual assets for each root model in one or more Max/Maya Please pick the classfor the assets you want to creatæ ASSET CLASS T,1eBase " width="276" height="195" /></p>

<p>Then you'll be prompter by the Mini importer dialog. Click the &quot;<em><strong>+ Add Source File…</strong></em>&quot; button and navigate to your Max file in the file browser. The mini importer will then show you a list of all the models that it found in your Max file. By default it sets all of the to import, but if there is a model that you don't want to import then click on the checkbox to the left of it to disable the import for it. Each model will also show a dropdown on the right indicating what geometry class it should be. 3D models should be &quot;<em><strong>LandmarkModel</strong></em>&quot; and decal models should be set to &quot;<em><strong>DecalGeometry</strong></em>&quot;. There is a dropdown at the top of the dialog that will let you assign a geometry class to all the models at once, simply pick the class from the dropdown and click the '<em><strong>Apply to Selected</strong></em>' button</p>

<p><img src="TileBase/media/image5.png" alt="Machine generated alternative text: Mini Importer Entity Type: Geometry LandmarkWodeI Entity Nanne Sort by Name Select/DeseIect All house pineTree PineTreeSma City La m p zost I + Add Source File... Apply ta Selected Entity Class: Check Out All LandmarkModeI LandmarkModeI LandmarkModeI LandmarkModeI LandmarkModeI Impart. Cancel " width="403" height="388" /></p>

<p>Depending on how may models are in your Max files this could take up to a couple of minutes, but once it's done it will prompt you to add the newly created Assets to an XLP. Click 'Yes Please…' and pick the XLP that you want to add your assets to. For now the tilebases are being added into the 'tilebases.xlp' file (check with your lead if you're unsure about this). Click 'Yes' when getting prompted to check-out the XLP file and then save the XLP file.</p>

<p>Create Attachment points on the base Asset:</p>
<p>Open up the base asset that was created by the script by going to '<em><strong>File &gt; Open Entity</strong></em>' and finding your asset, selecting it in the browser and clicking '<em><strong>OK</strong></em>'.</p>
<p>Select the Attachments tab, and click the button to 'Add Attachment Points to all Bones'. This will automatically create an attachment point for every Bone/Point in the Base Asset (these were the bones that were created by the 'TileBase Cleanup' script in Max).</p>

<p><img src="TileBase/media/image6.png" alt="Machine generated alternative text: Landmarks.aftdef tilebases.xlp (I items) Lamp Post. ast City.ast* Properties Name Class Name Desc ri pticn C ity Tile Base Particles C ategorization Tags Groups o Tile Base items) Geomet ries Attachments Cook Pa rams 0 001 Animations Filter: Add Attachment Points to all Bones Attachment Point Name A Model Instance " width="426" height="523" /></p>

<p>Once the attachment points are created, save your Asset. You can test that the Attachment points and Attachment Assets by going to the Knobs on the right, selecting the tab for the asset (The one that has the same name as your asset followed by &quot;_0&quot;) and click on the &quot;<em><strong>Attach by name</strong></em>&quot; which will slot in the Asset into their corresponding attachment points.</p>

<p><img src="TileBase/media/image7.png" alt="Machine generated alternative text: Global Previewer Info Module Landmark Base Lighting Values Knobs Reset Camera Reset Lighting H ide Skybox Reset Camera Reset Lighting City_o DefaultGameEnviro.. I Add Asset ktach By Name Attachment Point HouseOOI PineTreeS mallOOI PineTreeSma11002 PineTreeS ma11003 Pi neTreeSma 11004 PineTreeS ma11005 PineT rees ma 11007 PineT rees ma 11008 PineTreeS mal 1009 Attac hed Asset " width="576" height="285" /></p>

<p>This does not actually do the connection of the attachments, it's only to preview the attachments. The actual attachment hookups are done in the Landmarks.artdef file.</p>

<p>Hooking up the Attachment Assets to the Base Asset:</p>

<p>The Landmarks.artdef file is where the attachment are associated with the base asset .This information is stored in the artdef because it's possible to have the same Base asset have multiple different sets of attachments. For example Mines will probably use the same base asset, but have different mineral attachment assets associated with the different resource types it could be built on top of.</p>

<p>Because many of the Tilebase Assets have dozens of attachments setting up all the connections by hand can take a significant chunk of time, so there's a script that will automate that step for you. Go to '<em><strong>File &gt; Run Script</strong></em>' and load the script &quot;<em><strong>C:\Program Files\Civ6\Asset Cloud - Civ6\AssetEditor\Scripts\Create_District_Base.py</strong></em>&quot;. This will bring up a dialog prompt showing you a list of all the Assets in the tilebases.xlp file. Pick the Base Asset that you created before from the list and click '<em><strong>OK</strong></em>'. This will open up the Ladnmarks.artdef file for you and create the tilebase entry with all the attachments.</p>

<p><img src="TileBase/media/image8.png" alt="Machine generated alternative text: BLP Entry Browser Name CityCent er_ Lg _ Test CityCenter Sm Test CityCent er_Test Asset Path DIS DIS DIS DIS DIS DIS DIS DIS DIS DIS DIS DIS DIS DIS DIS DIS DIS CTY AW CTY AW CItyCenter Sm Test CTY AW CItyCenter_Test DIS DIS DIS DIS DIS DIS DIS DIS DIS DIS DIS DIS DIS DIS Ancient Ancient Ancient Ancient Ancient Ancient Ancient Cross flag Lg aller Sm Banner Sm Filler Stone Patch Wood Ancient Ancient Ancient Ancient Ancient Ancient Ancient Cross flag Lg aller Sm Banner Sm Filler Stone Patch Wood CM p CM p CM p CM p CM p CM p CM p CM p CM p CM p CM p CM p CM p CM p Ancient Base 01 Ancient Base 02 Ancient _ Lg Filler Ancient Base 01 Ancient Base 02 Ancient Lg Filler Base Classical Base Industrial Classical Base Classical Base _ Temp _ Temp 02 Base Classical Base Industrial Classical Base Classical Base _ Temp _ Temp 01 02 " width="523" height="466" /></p>

<p>As with the previous script, the more pieces there are associated with the Asset, the longer the script will take to process, but in the worst case it'll take a minute or so. You'll get a message box telling you the process was completed so that you know when it's done. Makse sure to Save the Landmarks.artdef file after the script is done.</p>

<p>Hook up the Asset into the game:</p>
<p>This process will be slightly different whether you are hooking up a Improvement/Landmark or a District.</p>

<p><strong>Landmark</strong>:</p>

<p>If you don't have it open, you need to open the Landmarks.artdef file. On the left there's a tree list of the different entries that the game is using, expand the &quot;<em><strong>Landmarks</strong></em>&quot; list by clicking on the arrow to the left.</p>

<p><img src="TileBase/media/image9.png" alt="Machine generated alternative text: AssetEditor - D. Edit View Landma rtdef* Alt Definition Template Landmarks Districts DEFAULT Window Open Source fil M M M M M M M CAMP CAMP CHATEAU FARM FISHING BOATS GOODY HUT LUMBER MILL MINE OFFSHORE OIL RIG OIL WEL PASTURE PLANTATION QUARRY STEPWEL ZIGGURAT Dis trictGenerators Tileaase Her08uiIdingTags Res ourceTags Cul tureTags EraTags UsageTags Globals CITY GL08ALS " width="430" height="549" /></p>

<p>This will show you a list of the entries that are currently being used by the game. If the Asset you are working on doesn't have an entry for it yet you'll need to set it up. The instructions on hooking up an artdef entry to a gameplay element are here: Mapping GameCore IDs to ArtDef Entries. If you need help setting it up ask your lead or the pertinent programmer that's working on your system.</p>
<p>If the entry that you need is already there, expand it out and you'll see an entry under that called '<em><strong>Eras</strong></em>'. Click on the '<em><strong>Eras</strong></em>' entry (1), and on the right you'll a grid that maps the tilebase you just created with a specific era. If the Era you need is already there, just click on the '<em><strong>Ref_LandmarkBase</strong></em>' item and it will show you a dropdown where you can pick the tilebase that you created in the last step (2). If the Era that you need is not in the list, click the Add Element button on the top toolbar (3). This will add a new element to the grid, and you can set the 'Tag_Era' for it from the dropdown of available Eras and then assign the tilebase.</p>

<p><img src="TileBase/media/image10.png" alt="Machine generated alternative text: AssetEditor - D:XprojectsXBALW-AGOULD Civ6 mainXCiv6Xpantry%ArtDefsXLandmarks.artdeff File Edit View Window Landma rtdef* Alt Definition Template Landmarks Open Source file Ref Landmark3ase VIL Tribal Thatch 01 v I Tag Era DEFAULT Filter: Name CAMP Erasl Districts Landmarks DEFAULT M M M M M M M CAMP CHATEAU FARM CMP CMP CMP CMP CMP CMP Ancient Base 01 Ancient Base 02 Base Classical Temp Base Industrial Temp Classical Base 01 Classical Base 02 FISHING BOATS GOODY HUT LUMBER ILL MINE OFFSHORE OIL RIG OIL WEL PASTURE PLANTATION QUARRY STEPWEL ZIGGURAT Dis trictGenerators Tileaase Her08uiIdingTags Res ourceTags Cul tureTags EraTags UsageTags Globals CITY GL08ALS " width="576" height="606" /></p>


<p><strong>District</strong>:</p>

<p>If you don't have it open, you need to open the Landmarks.artdef file. On the left there's a tree list of the different entries that the game is using, expand the &quot;<em><strong>Landmarks</strong></em>&quot; list by clicking on the arrow to the left.</p>

<p><img src="TileBase/media/image11.png" alt="Machine generated alternative text: AssetEditor - D:XprojectsXBALW-AGOULD Civ6 mainXCiv6Xpa File Edit View Window Landma rtdef* Alt Definition Template Landmarks C.i3trict3 ACROPOLIS AERODROME AQUEDUCT CAMPUS CITY CENTER COMMERCIAL HUB ENCAMPMENT ENTERTAINMENT cot, HARBOR HOLY SITE INDUSTRIAL ZONE MBANZA NEIGHBORHOOD SPACEPORT THEATER DEFAULT DISTRICT DISTRICT DISTRICT DISTRICT DISTRICT DISTRICT DISTRICT DISTRICT DISTRICT DISTRICT DISTRICT DISTRICT DISTRICT DISTRICT DISTRICT DISTRICT Landmarks Dis trictGenerators Tileaase Her08uiIdingTags Res ourceTags Cul tureTags EraTags UsageTags Globals CITY GL08ALS " width="385" height="694" /></p>

<p>his will show you a list of the entries that are currently being used by the game. If the Asset you are working on doesn't have an entry for it yet you'll need to set it up. The instructions on hooking up an artdef entry to a gameplay element are here: Mapping GameCore IDs to ArtDef Entries. If you need help setting it up ask your lead or the pertinent programmer that's working on your system.</p>
<p>If the entry that you need is already there, expand it out and you'll see an entry under that called '<em><strong>BaseVariants</strong></em>'. Click on the '<em><strong>BaseVariants</strong></em>' entry (1), and on the right you'll a grid that maps the tilebase you just created with a specific era, culture, and set of Hero Buildings. If the Era/Culture/HeroBuilding combination you need is already there, just click on the '<em><strong>Ref_DistrictBase</strong></em>' item and it will show you a dropdown where you can pick the tilebase that you created in the last step (2). If the combination that you need is not in the list, click the Add Element button on the top toolbar (3). This will add a new element to the grid, and you can set the Era/Culture/HeroBuidling for it from the dropdowns available and then assign the tilebase.</p>

<p><img src="TileBase/media/image12.png" alt="Machine generated alternative text: AssetEditor - D:XprojectsXBALW-AGOULD Civ6 mainXCiv6Xpantry%ArtDefsXLandmarks.artdef File Edit View Window Open Source file Landmarks.artdef tilebas Alt Definition Template Landmarks Districts Tag Era DEFAULT DEFAULT DEFAULT MCDERN ARTERA MODERN ARTERA MODERN ARTERA_MODERN Tag Culture DEFAULT DEFAULT DEFAULT DEFAULT Ref District3ase DIS HBR Base Classical 01 DIS HBR Base Classical 02 DIS HBR Base Classical (B DIS 01 Filter: Name BaseVariantsOOI BaseVariants002 Var iants003 3aseVariantsDDS BaseVariants006 BaseVar iants007 Set Herc3uiIdings EMPTY LIGHTHOUSE LIGHTHOUSE SHIPYARD LIGHTHOUSE LIGHTHOUSE, SHIPYARD HTHOUSE SHIHARD. SEAPOR ACROPOLIS AERODROME AQUEDUCT CAMPUS CITY CENTER COMMERCIAL HUB ENCAMPMENT ENTERTAINMENT cot, HARBOR DEFAULT DISTRICT DISTRICT DISTRICT DISTRICT DISTRICT DISTRICT DISTRICT DISTRICT DISTRICT DISTRICT City CMP CMP CMP CMP CMP CMP Ancient Base 01 Ancient Base 02 Base Classical Temp Base Industrial Temp Classical Base 01 Classical Base 02 BaseVariants Bull dingVariants C:&#39; BuildingSets DISTRICT DISTRICT DISTRICT DISTRICT DISTRICT DISTRICT Landmarks HOLY SITE INDUSTRIAL ZONE MBANZA NEIGHBORHOOD SPACEPORT THEATER Dis trictGenerators Tileaase Her08uiIdingTags Res ourceTags Cul tureTags EraTags UsageTags Globals CITY GL08ALS " width="576" height="412" /></p>


<p>Save the artdef file once you're doing hooking up your asset. To see it in the game, you have to Cook the tilebases.xlp and then load up the game and build the tilebase you just added.</p>

<p>Check everything in:</p>

<p>Once you've verified that the tilebase is working in your asset the way you expect, you can either do that through Perforce directly or you can use the Asset Cloud</p>
</div> <!-- panel body --> 
</div> <!-- panel -->

<div class="panel panel-primary" id="UnitPreviewingScript">
<div class="panel-heading">
<div class="panel-title">UnitPreviewingScript
</div>
</div>
<div class="panel-body">

<h1 id="civ-6-unit-previewing-script">Civ 6 Unit Previewing Script</h1>
<p><span id="scroll-bookmark-1" class="anchor"></span>This is how to load a Unit from the game with Culture Variants and props into the Asset Editor</p>
<p>From the asset Editor Top Menus select File\Run Script</p>
<p>Select Preview_Unit.py in the ..\Steam\steamapps\common\Sid Meier's Civilization VI SDK\AssetModTools\AssetEditor\Scripts directory</p>
<p><img src="UnitPreviewingScript/media/image1.png" width="565" height="442" /></p>
<p>Select your UNIT in the 'Pick the Unit' popup and click OK button</p>
<p><img src="UnitPreviewingScript/media/image2.png" alt="/download/attachments/267366110/image2018-8-29_13-12-36.png?version=1&amp;modificationDate=1535563264137&amp;api=v2" width="327" height="231" /></p>
<p>Select your CULTURE in the 'Pick the Culture' popup and click OK button</p>
<p><img src="UnitPreviewingScript/media/image3.png" alt="/download/attachments/267366110/image2018-8-29_13-13-9.png?version=1&amp;modificationDate=1535563264120&amp;api=v2" width="324" height="231" /></p>
<p>This will open the Unit_Bins.artdef, Units.artdef and a random Armor Asset of the unit you picked.</p>
<p>This also Attaches a Hat, Weapon, Head\Hair combo and body based off of the variations defined for unit and Culture.</p>
<p>Here is the example for Redcoat\European</p>
<table>
<tbody>
<tr class="odd">
<td><img src="UnitPreviewingScript/media/image4.png" alt="/download/attachments/267366110/image2018-8-29_13-13-57.png?version=1&amp;modificationDate=1535563264103&amp;api=v2" width="283" height="126" /></td>
<td><img src="UnitPreviewingScript/media/image5.png" alt="/download/attachments/267366110/image2018-8-29_13-14-41.png?version=1&amp;modificationDate=1535563264090&amp;api=v2" width="135" height="249" /></td>
</tr>
</tbody>
</table>
<p><strong>*** NOTE ***</strong> Cultural Skin color tinting will not be represented here. An example is that African and Middle Eastern bodies will only show up in the default Pink skin color. BUT the actual Head will be pulled from the defined set of Cultural Heads for that culture, but just not the right skin color. Below shows the correct Head for an African Archer ... just not the correct skin color.</p>
<table>
<tbody>
<tr class="odd">
<td><img src="UnitPreviewingScript/media/image6.png" alt="/download/attachments/267366110/image2018-8-29_16-15-12.png?version=1&amp;modificationDate=1535573712693&amp;api=v2" width="141" height="13" /></td>
<td><img src="UnitPreviewingScript/media/image7.png" alt="/download/attachments/267366110/image2018-8-29_16-14-21.png?version=1&amp;modificationDate=1535573661457&amp;api=v2" width="132" height="109" /></td>
<td></td>
<td></td>
</tr>
</tbody>
</table>
<p>Oddly in the right-hand side Archer unit tab under its <em>TRANSFORM</em> tab is where you can change the tint color. Tint is always White as a default. <strong>BUT</strong> that's not all ... It tints the Head, Boday and the Armor. <strong>NOT</strong> the hands</p>
<table>
<tbody>
<tr class="odd">
<td><img src="UnitPreviewingScript/media/image8.png" alt="/download/attachments/267366110/image2018-8-29_16-23-48.png?version=1&amp;modificationDate=1535574228177&amp;api=v2" width="283" height="128" /></td>
<td><img src="UnitPreviewingScript/media/image9.png" alt="/download/attachments/267366110/image2018-8-29_16-26-4.png?version=1&amp;modificationDate=1535574364447&amp;api=v2" width="211" height="400" /></td>
</tr>
</tbody>
</table>
<p><strong>OK</strong></p>
<p>Now if you want to edit this unit's Timeline you will need to open its Behavior. In this case it is the Redcoat.bhv</p>
<table>
<tbody>
<tr class="odd">
<td><img src="UnitPreviewingScript/media/image10.png" alt="/download/attachments/267366110/image2018-8-29_13-17-34.png?version=1&amp;modificationDate=1535563264090&amp;api=v2" width="283" height="247" /></td>
<td><img src="UnitPreviewingScript/media/image11.png" alt="/download/attachments/267366110/image2018-8-29_13-17-43.png?version=1&amp;modificationDate=1535563264057&amp;api=v2" width="195" height="318" /></td>
</tr>
</tbody>
</table>
<p>Once that is loaded you can edit the timeline while the bhv is selected. Plus play the animations.</p>
<p>Have at it!</p>
</div> <!-- panel body --> 
</div> <!-- panel -->

<div class="panel panel-primary" id="World%20Builder">
<div class="panel-heading">
<div class="panel-title">World Builder
</div>
</div>
<div class="panel-body">

<p><span id="scroll-bookmark-1" class="anchor"></span><img src="World Builder/media/image1.png" alt="_scroll_external\attachments\image2018-6-6_15-55-19-806c77b8608b72aed5a3181a425630c744adee755cf1dbce003a6f7396c1ec69.png" width="566" height="317" /></p>
<p>How to use the Tiled Importer for World Builder </p>
<ol style="list-style-type: decimal">
<li><p>Open Tiled Editor and open up a new map (File -&gt; New -&gt; New Map)</p></li>
</ol>

<p><img src="World Builder/media/image2.png" alt="_scroll_external\attachments\image2018-6-5_16-27-20-f6115e54a7ccc71bb38e8cd13e510d433cd1aedb83c32634e556ed062241c8b6.png" width="413" height="249" /></p>

<ol style="list-style-type: decimal">
<li><p>Choose a Hexagonal map, for tile layer format, choose CSV and render order right down</p></li>
<li><p>Under map size, you may set any dimensions you like, but staying close to existing Civ map dimensions is probably best.</p>
<ol style="list-style-type: lower-alpha">
<li><p>Duel: 44 tiles wide by 26 tiles high</p></li>
<li><p>Tiny: 60 tiles wide by 38 tiles high</p></li>
<li><p>Small: 74 tiles wide by 46 tiles high</p></li>
<li><p>Standard: 84 tiles wide by 54 tiles high</p></li>
<li><p>Large: 96 tiles wide by 60 tiles high</p></li>
<li><p>Huge: 106 tiles wide by 66 tiles high</p></li>
</ol></li>
<li><p>Under Tile size, choose Width: 32px Height: 64px</p></li>
</ol>

<p><img src="World Builder/media/image3.png" alt="_scroll_external\attachments\image2018-7-23_16-16-44-82ef751efb1b4df764abe1866e95a73100f63a42b25a6c6199416028b606bae1.png" width="357" height="372" /></p>

<ol style="list-style-type: decimal">
<li><p>Use Tiled's File→Open function to load the tilesets for each layer you're going to use.  They are currently in Examples/WorldBuilder Tiled Importing.</p></li>
<li><p>Under Map -&gt; Properties: </p>
<ul>
<li><p>Hexagonal (Staggered) </p></li>
<li><p>Tile Width: 32</p></li>
<li><p>Tile Height 64</p></li>
<li><p>Stagger Axis: Y</p></li>
<li><p>Stagger Index: Even</p></li>
<li><p>Tile Layer Format: XML</p></li>
<li><p>Tile Render Order: &quot;Right Down&quot; or &quot;Right Up&quot; will work.  The importer can tell which is which and flip the map accordingly.</p></li>
</ul></li>
</ol>

<p><img src="World Builder/media/image4.png" alt="_scroll_external\attachments\image2018-6-6_15-50-53-5f28629fc6414da6b74787a778576bcc441ac991562fd17962236e30002ccde3.png" width="285" height="291" /></p>

<ol style="list-style-type: decimal">
<li><p>Layers can be a mix of tile layers and object layers.  Object layers are necessary for some types because they allow you to define per-tile parameters that are passed to the importer.</p></li>
<li><p>In order from the top to the bottom of the layer list, the layers must be: Rivers, Buildings, Districts, Cities, Continents, Improvements, Resources, Features, and Terrain.</p>
<ol style="list-style-type: lower-alpha">
<li><p>Terrain must be a tile layer and you should always define all of the tiles on the terrain layer.  The Bucket Fill tool can be useful to set the whole map to a base type.</p></li>
<li><p>You don't have to have all layers in a given map for it to import successfully, but all of the layers below the highest one you have must exist.  For instance, if you want to place improvements on terrain, you must still have resources and features layers.  Just don't place anything on them.</p></li>
<li><p>Features can be a tile layer or an object layer.  Unused hexes do not need to be filled in.</p></li>
<li><p>Resources should be an object layer.  After you place each resource, click the &quot;+&quot; at the bottom of the Properties column and add a custom property &quot;number&quot; of type &quot;int&quot;.  Then set the value to represent the amount of that resource present in that hex.</p></li>
<li><p>Improvements should be an object layer.  As with resources, add a custom property named &quot;player&quot; of type &quot;int&quot;.  This value sets which civ the improvement will belong to.</p></li>
<li><p>Continents should be a tile layer currently.  The tiles for them represent, in order: Africa, Amasia, America, Antarctica, Arctica, Asia, AsiaAmerica, Atlantica, Atlantis, Australia, Avalonia, Azania, Baltica, Cimmeria, Columbia, Congo Craton, EurAmerica, Europe, Gondwana, Kalaharia, Kazakhstania, Kernorland, Kumari Kandam, LaurAsia, Laurentia, Lemuria, Mu, Nena, North America, Novopangea, Nuna, Oceana, Pangaea, Pangaea Ultima, Pannotia, Rodinia, Siberia, South America, Australis, Ur, Vaalbara, Vendia, and Zelandia. </p></li>
<li><p>Cities can be a tile layer or an object layer.  In both cases, the tiles are 1-16 representing up to 16 players in a game.  TIle 1 here is the same as &quot;player 0&quot; in the Improvements layer, 2 is the same as &quot;1&quot;, and so on.</p>
<ol style="list-style-type: lower-roman">
<li><p>If you make this an object layer, you can add a custom parameter named &quot;spawn&quot; of type Bool.  This will show as a checkbox in the list of parameters, and if you check it, this will be the spawn point for the player rather than generating a city on the spot.</p></li>
</ol></li>
<li><p>Districts should be an object layer with a &quot;player&quot; custom parameter</p></li>
<li><p>Buildings should be an object layer with a &quot;player&quot; custom parameter.</p></li>
<li><p>Rivers should be an object layer with a custom parameter named &quot;direction&quot; of type String.  Valid values are &quot;NE&quot;, &quot;E&quot;, &quot;SE&quot;, &quot;SW&quot;, 'W&quot;, or &quot;NW&quot;.  TODO: what does this parameter mean?</p></li>
<li><p>To set up parameters:</p>
<ol style="list-style-type: lower-roman">
<li><p>Click here:<br />
<img src="World Builder/media/image5.png" alt="_scroll_external\attachments\image2018-7-26_16-21-29-681b577720210f3bf085ba8de004e7208e374b2613575a829b618b1ae9e13ce2.png" width="446" height="342" /></p></li>
<li><p>Which brings up this: <img src="World Builder/media/image6.png" alt="_scroll_external\attachments\image2018-7-26_16-23-59-11d86b1413e07a024a686f73c2aa8609783f9c190f05bd7434e499ecf18d49fb.png" width="314" height="109" /></p></li>
<li><p>Enter the name in the text field and set the type with the drop-down <img src="World Builder/media/image7.png" alt="_scroll_external\attachments\image2018-7-26_16-27-27-d2e0ec31bbffe7d88f9c2b88188a2743a6468510816c4c46a7f7ecb0d0804860.png" width="415" height="192" /></p></li>
<li><p>The new parameter will appear in the left-hand column as shown where you may set the value.Buildings should be an object layer with a &quot;player&quot; custom parameter.</p></li>
</ol></li>
</ol></li>
<li><p>Each layer must only use tiles from one tileset.  If you use more than one the behavior of the importer is not guaranteed to be correct.</p></li>
<li><p>Save file as tmx.</p></li>
<li><p>In Civ VI-&gt;Additional Content-&gt;World Builder choose &quot;Import Map&quot;.</p>
<ol style="list-style-type: lower-alpha">
<li><p><img src="World Builder/media/image8.png" alt="_scroll_external\attachments\image2018-6-25_9-58-38-ce921c1f7b19efb11e6e68a5606dece4cfe609f3b9b2f36990d4f251114e0817.png" width="329" height="213" /></p></li>
</ol></li>
<li><p>The &quot;Advanced Setup&quot; screen will appear, minus the map size options.   Pick the number of players for your map and the specific teams if you want them to be particular civs, as well as any rules changes.</p></li>
<li><p>Click the &quot;Import Map&quot; button and the Civ file browser will appear, with extra buttons for full drive navigation to anywhere on your computer.  Choose a map and WorldBuilder will load with the selected map.</p></li>
<li><p>When you're finished viewing/fine-tuning in WorldBuilder, press Esc to bring up the menu and click the &quot;Save Game&quot; button to save a game with your map.</p></li>
</ol>
</div> <!-- panel body --> 
</div> <!-- panel -->

<div class="panel panel-primary" id="FireFX%5CEmitter%20Properties">
<div class="panel-heading">
<div class="panel-title">Emitter Properties
</div>
</div>
<div class="panel-body">

<h1 id="emitter-properties">Emitter Properties</h1>
<p><span id="scroll-bookmark-1" class="anchor"></span>These are all the emitter properties that can be assigned to a given emitter. This properties must be defined at compile time (they cannot be changed at run-time based using script logic).</p>
<p>The syntax for properties is the keyword &quot;property&quot;, followed by the property identifier, followed by the equals (=) sign, followed by the value. For example:</p>
<table>
<tbody>
<tr class="odd">
<td>
<p>property blend_type = alpha<br />
<br />
<br />
geometry_type = [none, quad_rotated, quad_aligned, quad_fixed, string_aligned, string_fixed]</p>
</td>
</tr>
</tbody>
</table>
<p>Default is 'none'.</p>
<p>Only valid on emitters that have a sim block.</p>
<p>Description: Determines the geometry type of the emitter.</p>
<table>
<tbody>
<tr class="odd">
<td>
<p>material_type = [none, quad_unlit, string_unlit, quad_unlit_masked, string_unlit_masked, quad_unlit_distorted, string_unlit_distorted]</p>
</td>
</tr>
</tbody>
</table>
<p>Default is 'none'.</p>
<p>Only valid on emitters that have a sim block.</p>
<p>Description: DEPRECATED: use combination of other material properties instead.</p>
<table>
<tbody>
<tr class="odd">
<td>
<p>blend_type = [none, alpha, additive]</p>
</td>
</tr>
</tbody>
</table>
<p>Default is 'none'.</p>
<p>Only valid on emitters that have a sim block.</p>
<p>Description: Sets the blend mode for the particle.</p>
<table>
<tbody>
<tr class="odd">
<td>
<p>distorted = [true,false]</p>
</td>
</tr>
</tbody>
</table>
<p>Default is 'false'.</p>
<p>Only valid on emitters that have a sim block.</p>
<p>Description: Enable distortion texture slot.</p>
<table>
<tbody>
<tr class="odd">
<td>
<p>masked = [true,false]</p>
</td>
</tr>
</tbody>
</table>
<p>Default is 'false'.</p>
<p>Only valid on emitters that have a sim block.</p>
<p>Description: Enable mask texture slot.</p>
<table>
<tbody>
<tr class="odd">
<td>
<p>normalmap = [true,false]</p>
</td>
</tr>
</tbody>
</table>
<p>Default is 'false'.</p>
<p>Only valid on emitters that have a sim block.</p>
<p>Description: Enable NormalMap texture slot. Only used if directional lighting is enabled.</p>
<table>
<tbody>
<tr class="odd">
<td>
<p>material_lighting = [none, directional, non_directional]</p>
</td>
</tr>
</tbody>
</table>
<p>Default is 'none'.</p>
<p>Only valid on emitters that have a sim block.</p>
<p>Description: Set the lighting mode for the particle.</p>
<table>
<tbody>
<tr class="odd">
<td>
<p>sort_order = [emit_order, reverse_emit_order]</p>
</td>
</tr>
</tbody>
</table>
<p>Default is 'emit_order'.</p>
<p>Only valid on emitters that have a sim block.</p>
<p>Description: Set the sort mode for particles emitter by this emitter.</p>
<table>
<tbody>
<tr class="odd">
<td>
<p>priority = [Integer in the interval [0, 256)]</p>
</td>
</tr>
</tbody>
</table>
<p>Default is 0.</p>
<p>Only valid on emitters that have a sim block.</p>
<p>Description: Determines the rendering order of emitters within the same tree. Lower priority emitters render before higher priority emitters.</p>
<table>
<tbody>
<tr class="odd">
<td>
<p>layer = [opaque, blended, underwater, overblended, overlay, primary]</p>
</td>
</tr>
</tbody>
</table>
<p>Default is 'primary'.</p>
<p>Only valid on emitters that have a sim block.</p>
<p>Description: Layer to render the emitter into.</p>
<table>
<tbody>
<tr class="odd">
<td>
<p>callbacks = [true,false]</p>
</td>
</tr>
</tbody>
</table>
<p>Default is 'false'.</p>
<p>Description: Enable callbacks for emitter lifetime events. This is expensive, so only enable it if you really need the callbacks.</p>
<table>
<tbody>
<tr class="odd">
<td>
<p>shadows = [true,false]</p>
</td>
</tr>
</tbody>
</table>
<p>Default is 'true'.</p>
<p>Only valid on emitters that have a sim block.</p>
<p>Description: Enable shadow casting by this emitter. Not available in the Overlay layer, or with Additive blend mode.</p>
</div> <!-- panel body --> 
</div> <!-- panel -->

<div class="panel panel-primary" id="FireFX%5CFireFX%20UI%20Backend">
<div class="panel-heading">
<div class="panel-title">FireFX UI Backend
</div>
</div>
<div class="panel-body">

<h1 id="firefx-ui-backend-design">FireFX UI Backend Design</h1>
<p><span id="scroll-bookmark-1" class="anchor"></span>The way that the UI maps to the FireFX script will be through code injection where the user can select blocks which map to code blocks that get combined</p>
<p>Tags are used to indicate sections that contain code, or sections where that code should be injected into</p>
<p>&lt; &gt; tags represent a section where code should be copied into that matches the tags identifier</p>
<p>[ ] tags represent the identifier for the following block of code that should be copied into a section defined by a matching tag</p>
<p>Code should be copied in order from top to bottom</p>
<p>When copying code into a section, any identical lines of code (white space should be ignored for comparison) should not get duplicated and only the first one should remain.</p>
<h1 id="block-types">Block types:</h1>
<p>Property blocks: These blocks are unique for each emitter and can define several different code blocks where each code block is mapped to an Enum entry that the user can pick from the UI. There might be additional block parameter meta data for description, tooltips, etc. Different options may or may not also expose UI parameters for the user to pick (not yet clear, but we should assume that we’ll need to).</p>
<p>This blocks are used to defined emitter properties, and also write out the appropriate exports that make the property valid. These blocks will also usually initialize critical variables that will be modified by other blocks. These are usually variables that need to be fed to the exports, for things like Position or Color.</p>
<p>Example:</p>
<p>Code Block 1 Property blocks example 1</p>
<table>
<tbody>
<tr class="odd">
<td>
<p>Description = &quot;This is determines the way that the particles are blended on the screen (Mesh particles determine their own blending based on their material)&quot;<br />
# Property blocks have a UI exposed enum, where each one then maps to a code block<br />
<br />
<br />
#This is the first possible code block, and should be the default when added to an emitter<br />
Enum1: &quot;additive&quot;<br />
<br />
[PARTICLE_GLOBAL]<br />
varying color p_color;<br />
varying float p_alpha;<br />
<br />
[PARTICLE_SPAWN]<br />
p_color = color(1,1,1);<br />
p_alpha = 0;<br />
<br />
[PARTICLE_PROPERTIES]<br />
property geometry_type = quad_rotated;<br />
<br />
[PARTICLE_RENDER]<br />
export( &quot;COLOR&quot;, p_color);<br />
export( &quot;ALPHA&quot;, p_alpha);</p>
</td>
</tr>
</tbody>
</table>
<p>Code Block 2 Property blocks example 2</p>
<table>
<tbody>
<tr class="odd">
<td>
<p># The code block is mutually exclusive from the first<br />
Enum2: &quot;alpha&quot;<br />
<br />
[PARTICLE_GLOBAL]<br />
varying color p_color;<br />
varying float p_alpha;<br />
<br />
[PARTICLE_SPAWN]<br />
p_color = color(1,1,1);<br />
p_alpha = 0;<br />
<br />
[PARTICLE_PROPERTIES]<br />
property geometry_type = quad_rotated;<br />
<br />
[PARTICLE_RENDER]<br />
export( &quot;COLOR&quot;, p_color);<br />
export( &quot;ALPHA&quot;, p_alpha);</p>
</td>
</tr>
</tbody>
</table>
<p>Particle logic blocks: This is the most common type of block that will compose the meat of the logic for the particles. These blocks will only contain one block of code, and additional metadata to indicate the type of block, it’s uniqueness, other logic block prerequisites, and UI exposures.</p>
<p>Example:</p>
<p>Code Block 3 Particle Logic Blocks</p>
<table>
<tbody>
<tr class="odd">
<td>
<p># Flag for indicating whether this block has to be unique across a group of blocks within an emitter (only one lifetime block allowed per emitter)<br />
Block_Type = SpawnRate<br />
Unique = True<br />
<br />
# Flag indicating that this block needs other types of blocks to be present to function,<br />
Before = none<br />
After = none<br />
Anywhere = none<br />
<br />
# Description to be placed somewhere in the UI for users<br />
Description = &quot;Particles will spawn at a constant rate of N particles per second&quot;<br />
<br />
# This is the section that describes the variables exposed to the UI. This need to describe UI string for the variable, variable name (this is the identifier in the code that will get replaced with the user driven value), type, range, tooltip, and default.<br />
# Eventually there might be UI hints available to tell the tools which control to use when displaying<br />
[UI: Particles per second, name: PARTICLE_RATE, float, range:0,1000000, default: 10]<br />
[UI: Initial Particle burst, name: PARTICLE_BURST, float, range:0,1000000, default: 0]<br />
[UI: Emitter life, name: EMITTER_LIFE, float, range:-1,1000000, default: -1]<br />
[UI: Delay Min, name: DELAY_MIN, float, range:-1,1000000, default: 0]<br />
[UI: Delay Max, name: DELAY_MAX, float, range:-1,1000000, default: 0]<br />
<br />
# This section then gets converted into code and merged<br />
[INCLUDES]<br />
<br />
[PARTICLE_GLOBAL]<br />
<br />
[PARTICLE_SPAWN]<br />
<br />
[PARTICLE_SPAWN_ARGUMENTS]<br />
(<br />
&lt;PARTICLE_SPAWN_ARGUMENTS_ADDITIONAL&gt;<br />
float in_age<br />
)<br />
<br />
[PARTICLE_SIM]<br />
<br />
[PARTICLE_PROPERTIES]<br />
<br />
[RENDER]<br />
<br />
<br />
[EMITTER_GLOBAL]<br />
varying float p_age;<br />
varying float p_inv_lifetime;<br />
<br />
[EMITTER_SPAWN]<br />
p_inv_lifetime = (EMITTER_LIFE &gt; 0)? 1.0 / EMITTER_LIFE : 0;<br />
p_age = 0.0;<br />
<br />
emit_count(&quot;EMITTER_NAME&quot; + &quot;_particle&quot;, PARTICLE_RATE)<br />
{<br />
&lt;PARTICLE_SPAWN_PARAMETERS&gt;<br />
export(&quot;in_age&quot;,p_age);<br />
};<br />
<br />
[EMITTER_SIM]<br />
emit_rate(&quot;EMITTER_NAME&quot; + &quot;_particle&quot;, PARTICLE_RATE)<br />
{<br />
&lt;PARTICLE_SPAWN_PARAMETERS&gt;<br />
export(&quot;in_age&quot;,p_age);<br />
};<br />
p_age = p_age + delta_time() * p_inv_lifetime;<br />
kill(p_age &gt; 1);</p>
</td>
</tr>
</tbody>
</table>
<p>Blank emitter block: This block gets automatically generated behind the scene for every emitter. It has no User exposures (except for the name), and is just generated to provide the structure for other blocks to build into. The “EMITTER_NAME+_particle” bit just indicates that that line should contain the name of the emitter with the “_particle” suffix.</p>
<p>Code Block 4 Blank emitter block</p>
<table>
<tbody>
<tr class="odd">
<td>
<p>#Blank emitter<br />
<br />
[PARTICLES]<br />
emitter EMITTER_NAME+_particle<br />
{<br />
&lt;PARTICLE_GLOBAL&gt;<br />
SPAWN<br />
&lt;PARTICLE_SPAWN_ARGUMENTS&gt;<br />
{<br />
&lt;PARTICLE_SPAWN&gt;<br />
}<br />
SIM<br />
{<br />
&lt;PARTICLE_SIM&gt;<br />
}<br />
<br />
&lt;PARTICLE_PROPERTIES&gt;<br />
<br />
RENDER<br />
{<br />
&lt;PARTICLE_RENDER&gt;<br />
}<br />
}<br />
<br />
[EMITTERS]<br />
emitter EMITTER_NAME<br />
{<br />
&lt;EMITTER_GLOBAL&gt;<br />
SPAWN<br />
{<br />
&lt;EMITTER_SPAWN&gt;<br />
}<br />
SIM<br />
{<br />
&lt;EMITTER_SIM&gt;<br />
}<br />
<br />
&lt;EMITTER_PROPERTIES&gt;<br />
<br />
RENDER<br />
{<br />
&lt;EMITTER_RENDER&gt;<br />
}<br />
}<br />
<br />
[GROUP_SPAWN]<br />
emit_count( &quot;EMITTER_NAME&quot;, 1 );</p>
</td>
</tr>
</tbody>
</table>
<p>Blank group block: Similar to the blank emitter block, this is just an internal structural block of code for the rest of the code to inject into. There is only one group block per effect, and is the first block that gets used and all other block go into:</p>
<p>Code Block 5 Blank group block</p>
<table>
<tbody>
<tr class="odd">
<td>
<p>&lt;INCLUDES&gt;<br />
<br />
&lt;PARTICLES&gt;<br />
<br />
&lt;EMITTERS&gt;<br />
<br />
<br />
group PARTICLE_SYSTEM_NAME<br />
{<br />
SPAWN<br />
{<br />
&lt;GROUP_SPAWN&gt;<br />
}<br />
SIM<br />
{<br />
&lt;GROUP_SIM&gt;<br />
}<br />
}</p>
</td>
</tr>
</tbody>
</table>
<p>Two special cases:</p>
<p>Template Emitter block: These are highly optimized emitter blocks that are self-contained and just expose a few parameters to the user, but cannot have any other blocks added to them. Internally however it should function very much like a regular Emitter Logic Block, that just gets injected directly into the Group Block.</p>
<p>The main purpose of these blocks is to encompass common use cases, but not used for high volume effects.</p>
<p>Template Effects: This is a case where there is a very optimized emitter that should be shared for high volume effects. Like the Template Emitter, this only exposes a handful of parameters and cannot have additional blocks added to it. Unlike it though, the way that this is expressed internally is slightly different. This will probably be implemented as a special Group Block that gets injected into an existing shared FireFX file so that all the effects that use this template can be compiled together.</p>
<h1 id="injection-order">Injection order:</h1>
<p>So the order in which block should be combined is:</p>
<p>Each <strong>Blank Emitter Block</strong> emitter block should get all its <strong>Property Blocks</strong> injected into it in order. Then it should get all its Particle Logic Blocks injected into it in order.</p>
<p>Then each finished <strong>Emitter Block</strong> should get injected into the <strong>Blank Group</strong> Block in order.</p>
<p>When injecting the code, any lines of code that are identical to a line that already exists (ignoring white space) should be ignored.</p>
<h1 id="section"> </h1>
<h1 id="types-and-ui-controls">Types and UI controls:</h1>
<p>Float (with an optional 3D Scale Gizmo, 3D Radius Gizmo, or Greyscale color picker)</p>
<p>Float2</p>
<p>Float3</p>
<p>Float4 (With an optional 3D Rotation Gizmo)</p>
<p>Color (With an HDR color picker, or at least a SRGB color picker)</p>
<p>Point2D (With a 2D Position Gizmo, maybe?)</p>
<p>Point3D (With a 3D Position Gizmo)</p>
<p>Int (maps to an equivalent float)</p>
<p>Bool (true = 1, false = 0)</p>
<p>String ( for referencing other emitters, though automatic Enum generation for existing emitters would be even better)</p>
<p>Spline selector (Scope to be determined, but we need some way for the user to be able to specify a 1D function either from a preset of functions, or as a custom spline)</p>
<p>Code block (This would allow the user to type in code snippets)</p>
<p>Example usage:</p>
<p>In the example directory there are a handful of example blocks that should generate the Output.txt script if all the defaults are used, and the Particle System name was “Root” and the Emitter name was “CenterGlowWhite”</p>
</div> <!-- panel body --> 
</div> <!-- panel -->

<div class="panel panel-primary" id="FireFX%5CUnderstanding%20FireFX%20Scripts">
<div class="panel-heading">
<div class="panel-title">Understanding FireFX Scripts
</div>
</div>
<div class="panel-body">

<h1 id="understanding-firefx-scripts">Understanding FireFX Scripts</h1>
<p><span id="scroll-bookmark-1" class="anchor"></span>FireFX is a language for expressing the motion and rendering of particles, or particle-like things.<br />
The language is based heavily on C for it's structure and syntax, so this documentation might gloss over some syntax details. This documentation also assumes the readers has some experience programming but should cover everything needed to get you writing your own scripts. If you find any gaps in documentation, please fill them or ask someone else to do so.<br />
One script file can contain the logic for multiple different particles. Each particle is broken up into a chunk of code that defines the initial conditions and simulation logic for a single particle. It also has code to then feed certain outputs back to the engine so that the engine that define how to render the particle.<br />
One thing to note is that FireFX doesn't make any distinction between a particle and a particle emitter. All particles can emit other particles (we'll go into the syntax later), so the terms emitter and particle will be used interchangeably in this document.<br />
A very bare bones particle script would look something like this:</p>
<p>Code Block 1 Simple Script</p>
<table>
<tbody>
<tr class="odd">
<td>
<p>group My_First_Particle<br />
{<br />
SPAWN<br />
{<br />
}<br />
<br />
SIM<br />
{<br />
}<br />
property geometry_type = quad_rotated;<br />
property blend_type = additive;<br />
<br />
RENDER<br />
{<br />
export( &quot;BASECOLOR_UV&quot;, float4(0,0,1,1) );<br />
export( &quot;SCALE&quot;, float2(15, 5 ));<br />
export( &quot;ROTATION&quot;, 0 );<br />
export( &quot;POSITION&quot;, float3(0,0,0));<br />
export( &quot;COLOR&quot;, float3(1,1,1));<br />
export( &quot;ALPHA&quot;, 1);<br />
}<br />
}</p>
</td>
</tr>
</tbody>
</table>
<p>The first line is composed to two parts. The Keyword &quot;group&quot; is used to indicate that this an entry point for the script file, followed by an identifier of your choice, in this case &quot;My_First_Particle&quot;. All particle systems must define a Group which is the starting code for that particle system. A script file may define multiple groups in it, but only one can be used by a particle system at a time.<br />
The code for the Group must then be contained within pair of curly braces.<br />
Inside the Group there are 4 sections, the SPAWN code, the SIM code, the properties, and the RENDER code. This particle isn't defining any spawn or simulation logic, so those sections are empty. The properties section lets you set a handful of engine specific properties that are fixed for each particle that tell the engine what to do with the data that the particle system is going to give it. For a full list of all the properties go here (<a href="https://hub.firaxis.com/display/FXSMadrid/Emitter+Properties" class="uri">https://hub.firaxis.com/display/FXSMadrid/Emitter+Properties</a>). Finally the Render section has several lines, where each line is feeding a labeled export back to the engine telling it how to render this particle.<br />
In Civ 6, this particle will look something like this:</p>
<p><img src="FireFX\Understanding FireFX Scripts/media/image1.png" alt="/download/attachments/304711043/worddav2d5a38bf2b5f2bf75d9e2dafbdad3254.png?version=1&amp;modificationDate=1549399541090&amp;api=v2" width="357" height="386" /></p>
<p>Not much to look at right now, but the language allows for expressing much more complex particle systems.</p>
<h1 id="variables-and-types">Variables and types:</h1>
<p>Things get much more interesting once you start using variables rather than fixed values for driving particle behavior. FireFX currently only supports floating point math, so the only variable types that are available are just groupings of floats:<br />
float, number ( a single float)<br />
float2, point2d (two floats)<br />
flaot3, point3d, color (three floats)<br />
float4 (four floats)<br />
There are two scopes that variables can exist in: varying and local. A &quot;varying&quot; variable is persistent through the whole life of a particle, and is accessible anywhere within the particle's code. This allows you to initialize the variable in the spawn block, and modify it every frame in the sim block and use it in the render block. Varying variables, also called &quot;varyings&quot;, must be defined outside of any of the particle's blocks.<br />
The syntax for a varying variable is the keyword &quot;varying&quot;, followed by the variable type, followed by the name or identifier you want to use followed by a semi-colon. For example:</p>
<table>
<tbody>
<tr class="odd">
<td>
<p>group My_Particle<br />
{<br />
varying float silly_variable;<br />
SPAWN<br />
{<br />
silly_variable = 3;<br />
}<br />
SIM<br />
{<br />
silly_variable = silly_variable + 1;<br />
}<br />
property geometry_type = quad_rotated;<br />
property blend_type = additive;<br />
RENDER<br />
{<br />
export( &quot;BASECOLOR_UV&quot;, float4(0,0,1,1) );<br />
export( &quot;SCALE&quot;, float2(15, 5 ));<br />
export( &quot;ROTATION&quot;, silly_variable );<br />
export( &quot;POSITION&quot;, float3(0,0,0));<br />
export( &quot;COLOR&quot;, float3(1,1,1));<br />
export( &quot;ALPHA&quot;, 1);<br />
}<br />
}</p>
</td>
</tr>
</tbody>
</table>
<p>This particle has a variable called &quot;silly_variable&quot;, it is initialized to the value of 3 in the spawn block, and then the variable is increased by one every time the sim block runs (more on that later). The variable is then output in the render block as the ROTATION value for the particle. This would produce a quickly spinning particle:</p>
<p><img src="FireFX\Understanding FireFX Scripts/media/image2.png" alt="/download/attachments/304711043/worddav444314236a06fa123f12a2daf114a66d.png?version=1&amp;modificationDate=1549399541153&amp;api=v2" width="336" height="300" /></p>
<p>On the other hand, a &quot;local&quot; variable only exists within the scope of one of the blocks in the particle, and immediately disposed of when that block ends. Local variables are used to temporarily store values within a block and are mostly useful to just make your code more readable or to calculate a value once and reuse it several times in the same block. Local variables within the sim block get re-initialized every time the sim block runs, so the data does not persist across iterations of the block. Local variables in the spawn block are not accessible in the sim block, however local variables in the sim block are accessible in the render block. Internally, the sim block and the render block are merged into one, so that you can more easily pass sim data into the render step.<br />
The syntax for local variables is similar to varyings. Local variables must be defined inside the block they are going to be used in. use the keyword &quot;local&quot; followed by the type, followed by the variable name, followed by a semi colon. You can also initialize the variable in the same line as you define it the way you might expect.</p>
<table>
<tbody>
<tr class="odd">
<td>
<p>group My_Particle<br />
{<br />
varying float silly_variable;<br />
SPAWN<br />
{<br />
silly_variable = 3;<br />
}<br />
SIM<br />
{<br />
silly_variable = silly_variable + 1;<br />
local float output_rotation = silly_variable / 10;<br />
local float3 output_position;<br />
output_position = float3(0,0, silly_variable / 5);<br />
}<br />
property geometry_type = quad_rotated;<br />
property blend_type = additive;<br />
RENDER<br />
{<br />
export( &quot;BASECOLOR_UV&quot;, float4(0,0,1,1) );<br />
export( &quot;SCALE&quot;, float2(15, 5 ));<br />
export( &quot;ROTATION&quot;, output_rotation );<br />
export( &quot;POSITION&quot;, output_position);<br />
export( &quot;COLOR&quot;, float3(1,1,1));<br />
export( &quot;ALPHA&quot;, 1);<br />
}<br />
}</p>
</td>
</tr>
</tbody>
</table>
<p>In this example you can see that in the Sim block we created two local variables &quot;output_rotation&quot; and &quot;output_position&quot; which are recalculated every time the Sim loop runs. The two variables are then used in the Render as exports to control the rendering behavior. In this case you could do the calculation for these variables in-line with the export function, but that can get messy once your calculations are more involved.<br />
NOTE: As a rule of thumb, a bit more math is always preferable to using more varyings. Memory tends to be much slower to access that just recalculating a value every frame. Also, CivTech games tend to be more limited by memory than by CPU performance.</p>
<h1 id="spawn">Spawn:</h1>
<p>The Spawn block is the first bit of code executed as soon as a particle is instantiated. The Spawn Block only ever gets executed once per particle and is guaranteed to fully execute before any of the code in the Sim block happens. The Spawn block is where you initialize any varyings that you are going in your particle, and it's also where you handle any of the particle's Spawn parameters (more on Spawn parameters later).</p>
<h1 id="sim">Sim:</h1>
<p>The Sim block is where you define the behavior of a particles through time. The Sim block gets run once per frame for every particle. The only way to pass data from one frame to the next is using varyings, since every local variable will get re-initialized every frame. Also remember that you are writing the logic for a single particle which has no information about other particles.<br />
Since the Sim code is run once per frame, it means that the Sim block is frame-rate dependent, and you should program accordingly. To help you with that there is a helpful system function delta_time() which returns the number of seconds since the last frame. So wherever possible you should write your particle logic relative to the result from that function. For example:</p>
<table>
<tbody>
<tr class="odd">
<td>
<p>group My_Particle<br />
{<br />
varying float3 particle_position;<br />
SPAWN<br />
{<br />
particle_position = float3(0,0,0);<br />
}<br />
SIM<br />
{<br />
local float3 particle_velocity = float3(15,0,0);<br />
particle_position = particle_position + particle_velocity * delta_time();<br />
}<br />
property geometry_type = quad_rotated;<br />
property blend_type = additive;<br />
RENDER<br />
{<br />
export( &quot;BASECOLOR_UV&quot;, float4(0,0,1,1) );<br />
export( &quot;SCALE&quot;, float2(15, 5 ));<br />
export( &quot;ROTATION&quot;, 0 );<br />
export( &quot;POSITION&quot;, particle_position);<br />
export( &quot;COLOR&quot;, float3(1,1,1));<br />
export( &quot;ALPHA&quot;, 1);<br />
}<br />
}</p>
</td>
</tr>
</tbody>
</table>
<p>In this example you can see that we set an initial position in the Spawn block, and then in the Sim block we're changing the position using a velocity. If we just added the velocity value every frame without multiplying it by the delta_time value the particle would move twice as fast if the game was running at 60 FPS than if it was running at 30 FPS.</p>
<h1 id="properties">Properties:</h1>
<p>Every particle program has a set of particle properties which are used to tell the engine what to do with the data that the program is going to export. A particle's properties are fixed at compile time and cannot be changed at runtime. Some properties require certain exports to be filled out. For example the &quot;quad_rotated&quot; property for the &quot;geometry_type&quot; requires the program to export a &quot;ROTATION&quot; value.<br />
Most of the properties have default values which are the most common based on traditional particle effects. So, if you don't specify a property the default value will be used.<br />
For more information on which properties are available, and what are their possible values and required exports go here (<a href="https://hub.firaxis.com/display/FXSMadrid/Emitter+Properties" class="uri">https://hub.firaxis.com/display/FXSMadrid/Emitter+Properties</a><em>)</em>.<br />
Each property can only be set once per particle program.</p>
<h1 id="exports">Exports:</h1>
<p>The exports in your program are ultimately the most important part. You can think of the exports as the actual output of the particle program back to the engine. Which exports you need to fill out is dependent on the Properties of the particle program whether explicit or implicit (which would be any properties you don't pick values for which would get their defaults).<br />
You can fill out exports that you are not required based on the selected properties and that program will still compile but the exported data will be ignored. This can be useful if you're trying to iterate by changing what properties you are using so you can just export valid data into all the required exports. Otherwise you must remember to change your exports every time you change a program's properties.</p>
<table>
<tbody>
<tr class="odd">
<td>
<p>property geometry_type = quad_rotated;<br />
//property geometry_type = quad_aligned;<br />
property blend_type = additive;<br />
RENDER<br />
{<br />
export( &quot;BASECOLOR_UV&quot;, float4(0,0,1,1) );<br />
export( &quot;SCALE&quot;, float2(15, 5 ));<br />
export( &quot;ROTATION&quot;, 0 );<br />
export( &quot;TANGENT&quot;, float3(0,1,0) );<br />
export( &quot;POSITION&quot;, particle_position);<br />
export( &quot;COLOR&quot;, float3(1,1,1));<br />
export( &quot;ALPHA&quot;, 1);<br />
}</p>
</td>
</tr>
</tbody>
</table>
<p>The example shows that you can export the &quot;ROTATION&quot; and &quot;TANGENT&quot; values, even though they are required exclusively for the &quot;quad_rotated&quot; and &quot;quad_aligned&quot; properties respectively. That way you could easily try out the different geometry types by just swapping the comments in the properties section.</p>
<h1 id="emitting-particles">Emitting particles:</h1>
<table>
<tbody>
<tr class="odd">
<td>
<p>Up until this point we've been writing logic for a single particle which is not particularly interesting. In FireFX every particle can emit other particles at any point. You need to two things to be able to emit a particle, a particle definition, and an emit statement.<br />
A Particle definition has the same syntax as a group, the only difference is that you use the keyword &quot;emitter&quot; instead. So for example here is a very basic particle definition:<br />
emitter My_Particle<br />
\{<br />
SPAWN<br />
\{<br />
\}<br />
\\<br />
SIM<br />
\{<br />
\}<br />
\\<br />
property geometry_type = quad_rotated;<br />
property blend_type = additive;<br />
\\<br />
RENDER<br />
\{<br />
export( &quot;BASECOLOR_UV&quot;, float4(0,0,1,1) );<br />
export( &quot;SCALE&quot;, float2(15, 5 ));<br />
export( &quot;ROTATION&quot;, 0 );<br />
export( &quot;POSITION&quot;, float3(0,0,0));<br />
export( &quot;COLOR&quot;, float3(1,1,1));<br />
export( &quot;ALPHA&quot;, 1);<br />
\}<br />
\}<br />
You can then have your particle system emit particles of this type using an emit statement as follows:<br />
group My_Particle_System<br />
\{<br />
SPAWN<br />
\{<br />
emit_count(&quot;My_Particle&quot;, 7);<br />
\}<br />
\}<br />
This group will then emit seven particles of the type &quot;My_Particle&quot; as soon as it is spawned. There are two emit functions, emit_count() and emit_rate(), with the following syntax:<br />
emit_count(&quot;\[name of the emitter to emit\]&quot;, \[number of particles to emit\]);<br />
emit_rate(&quot;\[name of the emitter to emit\]&quot;, \[number of particles to emit per second\], \[Min number to emit, optional\]);<br />
the first one will immediately emit exactly that number of particles on that frame, while the second will emit however many particles in that frame as it needs to try to maintain the emission rate passed in. So if you are running at 30 frames per second, and you have an emit rate of 10 particles per second, it will emit a particle approximately once every third frame.<br />
The emit_count() function can be used in both the Spawn, and the Sim block of a particle, while the emit_rate() function can only be used in the Sim block since that's the only place it makes sense.<br />
Any particle can emit other particle at any point with a few exceptions:</p>
</td>
</tr>
</tbody>
</table>
<ul>
<li><p>An emitter cannot emit other groups, you can only emit emitters</p></li>
<li><p>An emitter cannot emit emitters of the same type as itself</p></li>
<li><p>An emitter cannot emit emitters that would cause a cyclic dependency</p></li>
<li><p>An emitter can only emit an emitter type once per frame. So you can't call the emit function multiple times in a block with the same emitter type. But you can emit any number of different emitters in a frame</p></li>
</ul>
<h2 id="emit-spawn-parameters">Emit Spawn Parameters:</h2>
<p>The emit functions also allow you to pass arbitrary data into a particle when emitting it using the following syntax:</p>
<table>
<tbody>
<tr class="odd">
<td>
<p>emit_count(&quot;\[particle name\]&quot;, \[number of particles to emit\])</p>
</td>
</tr>
</tbody>
</table>
<h1 id="section">{</h1>
<table>
<tbody>
<tr class="odd">
<td>
<p>export(&quot;\[Parameter name 1\]&quot;, \[Parameter value 1\] );</p>
</td>
</tr>
</tbody>
</table>
<table>
<tbody>
<tr class="odd">
<td>
<p>export(&quot;\[Parameter name 2\]&quot;, \[Parameter value 2\] );</p>
</td>
</tr>
</tbody>
</table>
<h1 id="section-1">…</h1>
<table>
<tbody>
<tr class="odd">
<td>
<p>export(&quot;\[Parameter name n\]&quot;, \[Parameter value n\] );</p>
</td>
</tr>
</tbody>
</table>
<h1 id="section-2">};</h1>
<table>
<tbody>
<tr class="odd">
<td>
<p>\\<br />
When the particles get emitted, those parameters will get passed into them by matching up the parameter names to input parameters that the particles themselves define. Each particle can define what parameters it expects as either required or optional. You can pass in parameters that a particle is not expecting but they won't be used for anything. The order of the parameters does not matter since they are matched up by name. Any Spawn parameters that are exposed by an emitter that are not optional have to be passed in.<br />
An emitter defines the expected Spawn parameters as a set of function arguments on its Spawn block:<br />
group My_Particle<br />
\{<br />
SPAWN(\[Parameter type\] \[Parameter name 1\],<br />
\[Parameter type\] \[Parameter name 2\],<br />
…,<br />
\[Parameter type\] \[Parameter name n\]<br />
)<br />
\{<br />
…<br />
\}<br />
\}<br />
The Spawn parameters are then available as variables within the Spawn block, and will be initialized to the value that got passed in at the time the particle is emitted.<br />
For example:<br />
group My_Particle_System<br />
\{<br />
SPAWN<br />
\{<br />
emit_count(&quot;My_Particle&quot;, 1)<br />
\{<br />
export(&quot;minimum_size&quot;, 5 );<br />
export(&quot;maximum_size&quot;, 10 );<br />
\};<br />
\}<br />
\}<br />
emitter My_Particle<br />
\{<br />
varying float size;<br />
\\<br />
SPAWN( float minimum_size,<br />
float maximum_size<br />
)<br />
\{<br />
size = mix(minimum_size, maximum_size, random());<br />
\}<br />
\\<br />
property geometry_type = quad_rotated;<br />
property blend_type = additive;<br />
\\<br />
RENDER<br />
\{<br />
export( &quot;BASECOLOR_UV&quot;, float4(0,0,1,1) );<br />
export( &quot;SCALE&quot;, float2(size, size ));<br />
export( &quot;ROTATION&quot;, 0 );<br />
export( &quot;POSITION&quot;, float3(0,0,0));<br />
export( &quot;COLOR&quot;, float3(1,1,1));<br />
export( &quot;ALPHA&quot;, 1);<br />
\}<br />
\\<br />
\}<br />
\\<br />
In this example, the group is emitting a single particle that expects two parameters: &quot;minimum_size&quot; and &quot;maximum_size&quot;. The particle then uses the mix() function (which linearly interpolates between two values using an interpolant value that goes from 0 to 1) and the random() function (which generates a pseudo random value form 0 to 1) to randomly pick a value between those two values and use that as the size of the particle.<br />
\\<br />
To define an emitter's Spawn parameter as optional add an equal sign (=) after the parameter name followed by the default value. If the parameter is not passed into the emit function, then the default value is used. Something like this:<br />
\\<br />
…<br />
SPAWN( float minimum_size = 1)<br />
…<br />
\\</p>
</td>
</tr>
</tbody>
</table>
<h1 id="killing-particles">Killing particles:</h1>
<p>Killing a particle allows you to stop the execution of a given particle. To kill a particle you must use the kill() function. The function takes a comparison expression, and the particle will get killed if the comparison evaluates to true.</p>
<table>
<tbody>
<tr class="odd">
<td>
<p>group My_Particle<br />
{<br />
varying float time;<br />
SPAWN<br />
{<br />
time = 0;<br />
}<br />
SIM<br />
{<br />
time = time + delta_time();<br />
kill(time &gt; 3);<br />
}<br />
property geometry_type = quad_rotated;<br />
property blend_type = additive;<br />
RENDER<br />
{<br />
export( &quot;BASECOLOR_UV&quot;, float4(0,0,1,1) );<br />
export( &quot;SCALE&quot;, float2(15, 5 ));<br />
export( &quot;ROTATION&quot;, 0 );<br />
export( &quot;POSITION&quot;, float3(0,0,0));<br />
export( &quot;COLOR&quot;, float3(1,1,1));<br />
export( &quot;ALPHA&quot;, 1);<br />
}<br />
}</p>
</td>
</tr>
</tbody>
</table>
<p>This example shows a particle with a time variable that keeps track of how long the particle has been alive. The kill() statement then checks if the time variable is greater than 3, and if it is then it will kill the particle. Effectively this makes the particle exist for three seconds and then disappear.<br />
The kill statement will get executed at the location that it is in the script, so if a particle is killed it will not execute any lines of code that come after the kill statement. This is especially important for emit calls being done on the frame that the particle will be killed. If you want the particles to be emitted before the particle is killed, then those calls need to be before the kill() statement.<br />
Note: particles that are no longer being managed by some system in the game will eventually be killed after 10 seconds to avoid flooding the game with particles that weren't killed.</p>
<h1 id="flow-control">Flow control:</h1>
<p>FireFX does not support any kind of traditional flow control like &quot;if&quot; or &quot;for&quot; statements. The closest thing that is currently available is a ternary selector operator with the following syntax:<br />
(conditional expression)? expression1 : expression2<br />
If the conditional expression is true, then the operator returns the first expression, and if the condition is false then the second condition is returned.<br />
You can use this to mask out certain behavior based on whether a condition is true. For example:</p>
<table>
<tbody>
<tr class="odd">
<td>
<p>group My_Particle<br />
{<br />
varying float3 particle_position;<br />
varying float time;<br />
SPAWN<br />
{<br />
time = 0;<br />
particle_position = float3(0,0,0);<br />
}<br />
SIM<br />
{<br />
time = time + delta_time();<br />
local float velocity_mask = (time &lt; 5)? 1 : 0;<br />
local float3 particle_velocity = float3(15,0,0) * velocity_mask;<br />
particle_position = particle_position + particle_velocity * delta_time();<br />
}<br />
property geometry_type = quad_rotated;<br />
property blend_type = additive;<br />
RENDER<br />
{<br />
export( &quot;BASECOLOR_UV&quot;, float4(0,0,1,1) );<br />
export( &quot;SCALE&quot;, float2(15, 5 ));<br />
export( &quot;ROTATION&quot;, 0 );<br />
export( &quot;POSITION&quot;, particle_position);<br />
export( &quot;COLOR&quot;, float3(1,1,1));<br />
export( &quot;ALPHA&quot;, 1);<br />
}<br />
}</p>
</td>
</tr>
</tbody>
</table>
<p>This example shows a particle that keeps track of how long it's been alive, and then masks whether to apply a velocity to it if the time elapsed is less than 5.</p>
<h1 id="includes-and-defines">Includes and defines:</h1>
<p>The FireFX scripting system includes a c-style preprocessing step that lets you do things like have Include files and define directives.<br />
Include files let you write libraries of script functions that are frequently used. Includes must be done in the outermost scope of the script file, grouped together at the top of the file for readability.<span id="scroll-bookmark-15" class="anchor"></span> Syntax is: Pound symbol (#) followed by the keyword &quot;include&quot; followed by the name of the file to be included in quotations:<br />
#include &quot;Math.FXH&quot;<br />
Defines let you define commonly used constants readable names and simple functions to be inlined. The define syntax is a little more complicated and will not be covered here. You can look up the syntax for C style preprocessor on the webs.</p>
<h1 id="system-functions">System functions:</h1>
<p>Here's a few of the more common system functions:<br />
hash(float x): return a pseudo random value between 0 to 1 that is deterministic based on the input float. So if you give it the same input number you'll get the same random number back.<br />
max(float a, float b): returns the highest of the two values a or b.<br />
min(float a, float b): returns the lowest of the two values a or b.<br />
sin(float angle): returns the sine of he given input angle. Input angle expected in radians.<br />
cos(float angle): returns the cosine of he given input angle. Input angle expected in radians.<br />
floor(float x): returns the nearest integer value to the input number rounded down.<br />
ceil(float x): returns the nearest integer value to the input number rounded up.<br />
frac(float x): returns the fractional component of the input number<br />
mix(float a, float b, float time): return the linearly interpolated value between a and b using the value t as the time from zero to one. So if t = 0 then it will return a, if t = 1 it will return b, and t = 0.5 will return a value half way between a and b.</p>
<h2 id="spawn-specific">Spawn specific:</h2>
<p>This functions can only be used in the Spawn block of a program<br />
random(): returns a pseudo random between 0 and 1.<br />
index(): returns the index of the particle within the system. Each particle in a system is given an ordered index value based on spawn order (the first particle emitted has index 0, the next one has index 1, and so forth). Each emitter in a system has its own set of indices each starting at index 0.<br />
instance_id(): returns a unique identifier number for the entire effect instance, and all of its particles.</p>
<h2 id="sim-specific">Sim specific:</h2>
<p>This functions can only be used in the Sim block of a program<br />
delta_time(): returns the time in seconds that has elapsed since the last frame.</p>
<h1 id="best-practices">Best Practices:</h1>
<p>Following are some best practices and paradigms that should help you create scripts that are efficient and easy to understand.</p>
<h2 id="particle-age">Particle age:</h2>
<p>Divisions are relatively expensive (compared to multiplications and additions), so we try to avoid doing them wherever possible. Having a normalized age value (from zero to one) for a particle is a very common use case. If you know the lifetime of the particle at the Spawn of a particle you can calculate the reciprocal, and then use that to keep your age as a normalized value using only one division in the Spawn block:</p>
<table>
<tbody>
<tr class="odd">
<td>
<p>group My_Particle<br />
{<br />
varying float age;<br />
varying float inverse_lifetime;<br />
SPAWN<br />
{<br />
age = 0;<br />
local float lifetime = random() * 10;<br />
inverse_lifetime = 1 / lifetime;<br />
}<br />
SIM<br />
{<br />
age = age + delta_time() * inverse_lifetime;<br />
kill(age &gt; 1);<br />
}<br />
property geometry_type = quad_rotated;<br />
property blend_type = additive;<br />
RENDER<br />
{<br />
export( &quot;BASECOLOR_UV&quot;, float4(0,0,1,1) );<br />
export( &quot;SCALE&quot;, float2(5, 5 ) * (1-age));<br />
export( &quot;ROTATION&quot;, 0 );<br />
export( &quot;POSITION&quot;, float3(0,0,0));<br />
export( &quot;COLOR&quot;, float3(1,1,1));<br />
export( &quot;ALPHA&quot;, 1);<br />
}<br />
}</p>
</td>
</tr>
</tbody>
</table>
<p>In this example the &quot;age&quot; value will start at 0 in the Spawn, and will become 1 at the particle's &quot;lifetime&quot; value which is randomly calculated in the Spawn block.</p>
<h2 id="tweens-and-shaping-functions">Tweens and shaping functions:</h2>
<h2 id="forces-and-integration">Forces and integration:</h2>
<h2 id="terrain-collision">Terrain collision:</h2>
<h2 id="world-and-local-spaces">World and local spaces:</h2>
<h2 id="flipbooks">Flipbooks:</h2>
</div> <!-- panel body --> 
</div> <!-- panel -->

<div class="panel panel-primary" id="Forge%20UI%5CDebug%20Features">
<div class="panel-heading">
<div class="panel-title">Debug Features
</div>
</div>
<div class="panel-body">

<p>UI Debug Features</p>
<p>Friday, December 19, 2014</p>
<p>11:20</p>

<p><strong>Debug XML Attribute</strong></p>

<p>All controls derive from &lt;Container&gt; (in code this is &quot;ControlBase&quot;) and on &lt;Container&gt; is a special attribute: &quot;d&quot;, which stands for &quot;debug&quot;. When certain values are put into &quot;d&quot; it will display appropriate debug information for the control, and in some cases it's children.</p>

<p><strong>Attributes Values 1,2,3,4,5,6 and *</strong></p>
<p>Fast control bounds coloring based on which number is used or picks a random color if * is used.</p>

<p><strong>Attribute Value +</strong></p>
<p>Using a plus (&quot;+&quot;) will tell ForgeUI to cascade whatever debug values are set on this control to its children.</p>

<p><strong>Attribute Value id</strong></p>
<p>If the lowercase letters &quot;id&quot; appears, then the identifier (if any) will be displayed in text in the upper left region of the control. Mousing over the text will display a tooltip (using the default style) of the control path.</p>




<p><strong>Examples:</strong></p>
<p>An example of using the &quot;d&quot; attribute for debugging.</p>


<p>Set d to a number 1,2,3,4,5 or 6</p>
<p>e.g., <strong>d=”1”</strong></p>
<p>&lt;Container   Anchor=&quot;R,T&quot; Size=&quot;512,1&quot; &gt;</p>
<p>      &lt;Image Anchor=&quot;R,T&quot; Size=&quot;119,119&quot; Texture=&quot;HUDBackingCorner.dds&quot; <strong>d=&quot;1&quot;</strong> /&gt;</p>
<p>      &lt;!-- etc... --&gt;</p>
<p><img src="Forge UI\Debug Features/media/image1.png" alt="C:\0FAAA085\222AE316-8AD0-43BE-AD7A-3B0A13BF93FC_files\image001.png" width="490" height="154" /></p>


<p> e.g, <strong>d=”6”</strong></p>
<p>&lt;Container   Anchor=&quot;R,T&quot; Size=&quot;512,1&quot; &gt;</p>
<p>      &lt;Image Anchor=&quot;R,T&quot; Size=&quot;119,119&quot; Texture=&quot;HUDBackingCorner.dds&quot; <strong>d=&quot;6&quot;</strong> /&gt;</p>
<p>      &lt;!-- etc... --&gt;</p>
<p><img src="Forge UI\Debug Features/media/image2.png" alt="C:\0FAAA085\222AE316-8AD0-43BE-AD7A-3B0A13BF93FC_files\image002.png" width="490" height="151" /></p>


<p>Set d to a number and add a plus (“+”) afterward to cascade to children.</p>
<p>e.g., <strong>d=”6+”</strong></p>
<p>&lt;Container   Anchor=&quot;R,T&quot; Size=&quot;512,1&quot; <strong>d=&quot;6+&quot;</strong> &gt;</p>
<p>      &lt;Image Anchor=&quot;R,T&quot; Size=&quot;119,119&quot; Texture=&quot;HUDBackingCorner.dds&quot; /&gt;</p>
<p>      &lt;!-- etc... --&gt;</p>
<p><img src="Forge UI\Debug Features/media/image3.png" alt="C:\0FAAA085\222AE316-8AD0-43BE-AD7A-3B0A13BF93FC_files\image003.png" width="490" height="166" /></p>


<p>Or instead of number just use an asterisk (“*”) and ForgeUI will cycle through 12 random colors:</p>
<p>e.g., <strong>d=”*+”</strong></p>
<p>&lt;Container   Anchor=&quot;R,T&quot; Size=&quot;512,1&quot; <strong>d=&quot;*+&quot;</strong> &gt;</p>
<p>      &lt;Image Anchor=&quot;R,T&quot; Size=&quot;119,119&quot; Texture=&quot;HUDBackingCorner.dds&quot; /&gt;</p>
<p>      &lt;!-- etc... --&gt;</p>
<p><img src="Forge UI\Debug Features/media/image4.png" alt="C:\0FAAA085\222AE316-8AD0-43BE-AD7A-3B0A13BF93FC_files\image004.png" width="490" height="178" /></p>



<p>e.g., <strong>d=”id”</strong></p>
<p>&lt;Container  ID=&quot;CultureArea&quot;    Anchor=&quot;R,T&quot; Offset=&quot;100,0&quot; Size=&quot;100,140&quot; <strong>d=”id”</strong>&gt;</p>
<p>  &lt;Image                        Anchor=&quot;L,T&quot; Offset=&quot;3,20&quot;  Size=&quot;71,79&quot;   Texture=&quot;TopBarRingCulture.dds&quot;&gt;</p>
<p>    &lt;Meter  ID=&quot;CultureMeter&quot;   Anchor=&quot;L,T&quot; Offset=&quot;7,17&quot;  Size=&quot;56,56&quot;   Texture=&quot;HUDTopBarCultureMeter.dds&quot; /&gt;</p>
<p>  &lt;/Image&gt;</p>
<p>&lt;/Container&gt;</p>
<p><img src="Forge UI\Debug Features/media/image5.jpg" alt="cid:image001.png@01D01AF0.32FBA450" width="702" height="150" /></p>

<p>Mouse over the text:</p>
<p><img src="Forge UI\Debug Features/media/image6.jpg" alt="cid:image002.png@01D01AF0.32FBA450" width="700" height="151" /></p>


<p>e.g., <strong>d=”id+”</strong></p>
<p>&lt;Container  ID=&quot;CultureArea&quot;    Anchor=&quot;R,T&quot; Offset=&quot;100,0&quot; Size=&quot;100,140&quot; <strong>d=”id+”</strong>&gt;</p>
<p>  &lt;Image                        Anchor=&quot;L,T&quot; Offset=&quot;3,20&quot;  Size=&quot;71,79&quot;   Texture=&quot;TopBarRingCulture.dds&quot;&gt;</p>
<p>    &lt;Meter  ID=&quot;CultureMeter&quot;   Anchor=&quot;L,T&quot; Offset=&quot;7,17&quot;  Size=&quot;56,56&quot;   Texture=&quot;HUDTopBarCultureMeter.dds&quot; /&gt;</p>
<p>  &lt;/Image&gt;</p>
<p>&lt;/Container&gt;</p>
<p><img src="Forge UI\Debug Features/media/image7.jpg" alt="cid:image003.png@01D01AF0.32FBA450" width="706" height="151" /></p>



<p>Combining IDs with coloring, and cascading:</p>
<p>e.g., <strong>d=”id*+”</strong></p>
<p>&lt;Container  ID=&quot;CultureArea&quot;    Anchor=&quot;R,T&quot; Offset=&quot;100,0&quot; Size=&quot;100,140&quot; <strong>d=”id*+”</strong>&gt;</p>
<p>  &lt;Image                        Anchor=&quot;L,T&quot; Offset=&quot;3,20&quot;  Size=&quot;71,79&quot;   Texture=&quot;TopBarRingCulture.dds&quot;&gt;</p>
<p>    &lt;Meter  ID=&quot;CultureMeter&quot;   Anchor=&quot;L,T&quot; Offset=&quot;7,17&quot;  Size=&quot;56,56&quot;   Texture=&quot;HUDTopBarCultureMeter.dds&quot; /&gt;</p>
<p>  &lt;/Image&gt;</p>
<p>&lt;/Container&gt;</p>
<p><img src="Forge UI\Debug Features/media/image8.jpg" alt="cid:image004.png@01D01B7B.A5DD3750" width="493" height="192" /></p>




</div> <!-- panel body --> 
</div> <!-- panel -->

<div class="panel panel-primary" id="Forge%20UI%5CLUA%20Conventions">
<div class="panel-heading">
<div class="panel-title">LUA Conventions
</div>
</div>
<div class="panel-body">

<p>LUA Conventions</p>

<p>The below conventions are highly recommended to those writing LUA script which are for Forge.</p>

<p>Use Havokscript type qualifiers</p>
<p>Havokscript offers an extension to LUA where variables can be defined as taking a type (number, string, boolean, ifunction, table).  When possible, use a strongly typed define to potential reap the Havokscript benefits of: preventing invalid types to be assigned, faster execution, less memory.</p>

<p><em>Example</em></p>
<p>local numPlayers     :number = 0;</p>
<p>local isReady        :boolean = false;</p>
<p>local data           :table = {};</p>
<p>local callback       :ifunction = nil;</p>


<p>Naming LUA variables</p>
<p>Scope</p>
<p><strong>Use “m_” to prefix variables scoped to a file.</strong></p>
<p>At a glance shows meaningful scope of a variable and helps to prevent function vs file name collisions.</p>

<p><em>Example:</em></p>
<p>local m_currentPlayer;</p>

<p><strong>Use “g_” to prefix variables of global scope.</strong></p>
<p>Variables without “<strong>local</strong>” that are accessible globally (when included) have their scope known with “g_”.</p>

<p><em>Example:</em></p>
<p>g_debugColor :number  = 0x3344ffee;</p>

<p>Constant Naming</p>
<table>
<thead>
<tr class="header">
<th><strong>Prefix</strong></th>
<th><strong>Suffix</strong></th>
<th><strong>Type</strong></th>
<th><strong>Example</strong></th>
<th><strong>Description</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>COLOR_</td>
<td> </td>
<td>number</td>
<td>COLOR_FILTERED_NOT</td>
<td>ABGR color number.</td>
</tr>
<tr class="even">
<td>m_debug</td>
<td> </td>
<td>*</td>
<td>m_debugOutputInfo</td>
<td>A setting for some debugging feature.</td>
</tr>
<tr class="odd">
<td>PIC_</td>
<td> </td>
<td>string</td>
<td>PIC_MARKER_PLAYER</td>
<td>Name of a texture (either loose .DDS or ID in BLP)</td>
</tr>
<tr class="even">
<td>SIZE_</td>
<td>_X</td>
<td>number</td>
<td>SIZE_MIN_SPEC_X</td>
<td>Size in pixels for a width.</td>
</tr>
<tr class="odd">
<td>SIZE_</td>
<td>_Y</td>
<td>number</td>
<td>SIZE_MIN_SPEC_Y</td>
<td>Size in pixels for a height.</td>
</tr>
<tr class="even">
<td>TXT_</td>
<td> </td>
<td>string</td>
<td>TXT_TO_BOOST</td>
<td>A constant localized string that has been obtained via Locale.Lookup()</td>
</tr>
</tbody>
</table>

<p>Variable Naming</p>
<table>
<thead>
<tr class="header">
<th><strong>Prefix</strong></th>
<th><strong>Suffix</strong></th>
<th><strong>Type</strong></th>
<th><strong>Example</strong></th>
<th><strong>Description</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>cached</td>
<td> </td>
<td>*</td>
<td>m_cachedPathUnit</td>
<td>A check value that is used locally to prevent extraneous computations and/or C++ calls.</td>
</tr>
<tr class="even">
<td>e</td>
<td> </td>
<td>number</td>
<td>m_ePlayer</td>
<td>A C++ enumeration (typically 0 based, with -1 being invalid)</td>
</tr>
<tr class="odd">
<td>k</td>
<td> </td>
<td>table</td>
<td>m_kFilters</td>
<td>Generic LUA table.</td>
</tr>
<tr class="even">
<td>k</td>
<td>IM</td>
<td>table</td>
<td>m_kEraLabelIM</td>
<td>Table acting as an Instance Manager (helper for dynamically creating instances of controls for use in a pooled structure.)</td>
</tr>
<tr class="odd">
<td>m_</td>
<td> </td>
<td> </td>
<td> </td>
<td> </td>
</tr>
<tr class="even">
<td>max</td>
<td> </td>
<td>number</td>
<td>m_maxColumns</td>
<td>Highest number for a range of values.</td>
</tr>
<tr class="odd">
<td>min</td>
<td> </td>
<td>number</td>
<td>m_minMoves</td>
<td>Lowest number for a range of values.</td>
</tr>
<tr class="even">
<td>p</td>
<td> </td>
<td>table</td>
<td>pInputStruct</td>
<td>Table created from C++ (likely has C++ method calls off of it)</td>
</tr>
<tr class="odd">
<td>is</td>
<td> </td>
<td>boolean</td>
<td>isHandled</td>
<td>Generic boolean</td>
</tr>
<tr class="even">
<td>ui</td>
<td> </td>
<td>table</td>
<td>m_uiEraLabels</td>
<td>Table that holds references to UI controls created dynamically.</td>
</tr>
<tr class="odd">
<td> </td>
<td>Control</td>
<td>table</td>
<td>civTextControl</td>
<td>A UI control instance</td>
</tr>
</tbody>
</table>

<p>Function Naming</p>
<p>Functions should be in PascalCase; where the first letter of each word is capitalized; avoiding underscores unless part of a group of similarly called functions.</p>
<table>
<thead>
<tr class="header">
<th><strong>Prefix</strong></th>
<th><strong>Suffix</strong></th>
<th><strong>Example</strong></th>
<th><strong>Description</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>On</td>
<td> </td>
<td>OnPlayerElected</td>
<td>Function which acts as an Event, LUAEvent, or UI callback.</td>
</tr>
</tbody>
</table>


<p>Define an Initialize function</p>
<p>The equivalent of a CTOR for a LUA context, is having an “Initialize” function, defined near the bottom of the file and executed on context load.</p>
<p>This is useful when initialization off of the file scope may be difficult to determine, especially if it occurs across many lines and the file is particularly large.</p>

<p><em>Example:</em></p>
<p>function Initialize()</p>
<p>    -- Do setup stuff</p>
<p>end</p>
<p>Initialize();</p>


<p>Place UI callback linkages in Initialize()</p>
<p>Formally UI events linkages were defined immediately after the function they call. This made it more difficult to determine what callbacks were wired up to XML.</p>

<p><em>Example:</em></p>
<p>function OnExitButtonPressed()</p>
<p>    ExitScreen();</p>
<p>end</p>

<p>function Initialize()</p>
<p>Controls.ExitButton:RegisterCallback( Mouse.eLClick, OnExitButtonPressed);</p>
<p>end</p>


<p>Event Registering</p>
<p>Place broadcast callbacks at the bottom of the file in an “Events” section in Initialize().</p>
<p>These events are either raised by other files (LuaEvents), or the C++ side, and they broadcast so there may be more than one listener, even in the same file.</p>

<p><em>Example:</em></p>
<p>function Initialize()</p>
<p>    -- Events</p>
<p>    ContextPtr:SetInitHandler( OnContextInitialize );</p>
<p>    ContextPtr:SetRefreshHandler( OnRefresh );</p>
<p>    Events.CitySelectionChanged.Add( OnCitySelectionChanged );</p>
<p>   Events.LocalPlayerTurnBegin.Add( OnLocalPlayerTurnBegin );</p>
<p>Events.UnitOperationsCleared.Add( OnUnitOperationsCleared );</p>
<p>LuaEvent.TestPanel_AllSectionsClosed.Add( OnAllSectionsClosed );</p>
<p>end</p>


<p>LUAEvents</p>
<p>Name based on the context from where its raised</p>
<p>In order to know who may be raising a LUA event, name the event based on the context that raises it.</p>
<p>If the same event could be raised from two different contexts, the event should either be considered to be moved into the engine or they should be broken out as 2 separate LUA events. </p>

<p>This mitigates the confusion as to which LUA event is being raised from where in terms of logic being applied to the UI and simplifies debugging LUA event based issues.</p>

<p><em>Example:</em></p>
<p>LuaEvent.ActionPanel_OpenChooseResearch();  -- Raised from ActionPanel.lua for any listeners</p>

<p>Only pass simple types</p>
<p>Only strings, numbers, and booleans should be passed as arguments to a LUAEvent. A table can be passed as well, as long as it's not a table returned from the game engine nor a table that, somewhere, holds a game engine object. This includes UI objects.</p>

<p>On first glance it would appear to work but it's dangerous in that when the LUA context, which received the event, is working on the complex type passed in, it's possible for the owning context to have already deleted the backing to the object.</p>

<p>e.g., A button control, that was passed across contexts, will be working fine then all of a sudden become invalid when it's owning context cleans up.</p>


<p>Include Files</p>
<p>Any included files will have all contents copied into the local context. For this reason, include files should minimize any local variables and state utilized in them as this will increase size and could create potential name conflicts.</p>

</div> <!-- panel body --> 
</div> <!-- panel -->

<div class="panel panel-primary" id="Forge%20UI%5CLUA%20Input">
<div class="panel-heading">
<div class="panel-title">LUA Input
</div>
</div>
<div class="panel-body">

<p>LUA Input</p>
<p>Wednesday, April 08, 2015</p>
<p>9:53</p>

<p>To receive input in a LUA context, set a function to be a callback handler.</p>

<p>The handler function should return <strong>true</strong> if the input was handled.</p>
<p>The handler function should return <strong>false</strong> if the input was not handled or it was handled but should be considered by other inputs.</p>

<p>Once input is marked as handled (<strong>true</strong>), no other controls (or contexts) within that <strong><em>root</em></strong> context will receive input. But other controls/contexts within other <strong><em>root</em></strong> contexts will receive a chance to handle the input, despite if it was marked has handled (<strong>true</strong>) in a different root context.</p>
<p><em>(NOTE: Root contexts are set via C++, chances are you are working within a single root context.)</em></p>

<p>Only one input handler callback can be set per context.</p>

<p>There are two types of handlers that can receive input.</p>

<p><strong>Simple Handler</strong></p>
<p>The simple handler will callback when input occurs passing in 3 parameters:</p>
<p><strong>function InputHandler( uiMsg, wParam, lParam )</strong></p>

<p>The uiMsg will be the type of input (keyboard, mouse, pointer, etc…), wParam and lParam will be values that have meaning, based on the type of input that comes in.</p>

<p>To set the handler call <strong>SetInputHandler()</strong> on the context, passing in the name of function to receive input.</p>
<p>ContextPtr:SetInputHandler( InputHandler );</p>

<p><strong>Example</strong></p>
<p>function InputHandler( uiMsg, wParam, lParam )</p>
<p>if (uiMsg==KeyEvents.KeyDown) then</p>
<p>if (wParam==Keys.VK_ESCAPE) then</p>
<p>OnBack();</p>
<p>return true;</p>
<p>end</p>
<p>end</p>

<p>if (uiMsg==MouseEvents.MouseMove) then        </p>
<p>InspectWhatsBelowTheCursor();</p>
<p>return true;</p>
<p>end</p>
<p>return false;</p>

<p>end</p>
<p>ContextPtr:SetInputHandler( InputHandler );</p>

<p><strong>Extended Handler</strong></p>
<p>The extended handler works almost the same as the simple handler except that it receives a single parameter which is a table of input information:</p>
<p><strong>function InputHandler( inputStruct )</strong></p>


<p>The <strong>inputStruct</strong> is the same one as &quot;<strong>InputStruct</strong>&quot; defined in ForgeUI. It allows for detailed querying of the input through various functions.</p>

<p>To set the input handler:</p>
<table>
<tbody>
<tr class="odd">
<td>ContextPtr:SetInputHandler(</td>
<td>InputHandler, true );</td>
</tr>
</tbody>
</table>

<p><strong>InputStruct</strong> functions include:</p>

<table>
<thead>
<tr class="header">
<th><strong>Function</strong></th>
<th><strong>Returns</strong></th>
<th><strong>Description</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>GetFlags</td>
<td>number</td>
<td>Return the low level bit-flags the input system is using.</td>
</tr>
<tr class="even">
<td>GetKey</td>
<td>number</td>
<td>Obtain the AppHost key code.</td>
</tr>
<tr class="odd">
<td>GetMessageType</td>
<td>number</td>
<td><p>The type of input message contained in this instance of the structure.</p>
<p>Values include:</p>

<p>KeyEvents.KeyDown</p>
<p>KeyEvents.KeyUp</p>
<p>MouseEvents.LButtonDown</p>
<p>MouseEvents.LButtonDoubleClick</p>
<p>MouseEvents.LButtonUp</p>
<p>MouseEvents.MButtonDown</p>
<p>MouseEvents.MButtonDoubleClick</p>
<p>MouseEvents.MButtonUp</p>
<p>MouseEvents.PointerDown</p>
<p>MouseEvents.PointerUp</p>
<p>MouseEvents.RButtonDown</p>
<p>MouseEvents.RButtonDoubleClick</p>
<p>MouseEvents.RButtonUp</p>
</td>
</tr>
<tr class="even">
<td>GetMouseDX</td>
<td>number</td>
<td>Obtain the horizontal delta for the mouse since the last frame of input.</td>
</tr>
<tr class="odd">
<td>GetMouseDY</td>
<td>number</td>
<td>Obtain the vertical delta for the mouse since the last frame of input.</td>
</tr>
<tr class="even">
<td>GetTouchID</td>
<td>number</td>
<td>The unique ID associate with this touch generating an event.</td>
</tr>
<tr class="odd">
<td>GetWheel</td>
<td>number</td>
<td>Get mouse wheel value</td>
</tr>
<tr class="even">
<td>GetX</td>
<td>number</td>
<td>Horizontal coordinate for this mouse or touch event.</td>
</tr>
<tr class="odd">
<td>GetY</td>
<td>number</td>
<td>Vertical coordinate for this mouse or touch event.</td>
</tr>
<tr class="even">
<td>IsShiftDown</td>
<td>bool</td>
<td>Is the shift key held down?</td>
</tr>
<tr class="odd">
<td>IsControlDown</td>
<td>bool</td>
<td>Is the control key held down?</td>
</tr>
<tr class="even">
<td>IsLButtonDown</td>
<td>bool</td>
<td>Is the left mouse button (or touch equivalent) down?</td>
</tr>
<tr class="odd">
<td>IsRButtonDown</td>
<td>bool</td>
<td>Is the right mouse button down?</td>
</tr>
<tr class="even">
<td>IsMButtonDown</td>
<td>bool</td>
<td>Is the middle mouse button (commonly the mouse wheel) down?</td>
</tr>
<tr class="odd">
<td>IsAnyButtonDown</td>
<td>bool</td>
<td>Is the left, right, or middle mouse button down?</td>
</tr>
</tbody>
</table>



<p><strong>Example</strong></p>
<p>function KeyHandler( key:number )</p>

<p>if (key == Keys.VK_ESCAPE) then Close(); return true; end</p>
<p>return false;</p>

<p>end</p>
<p>function InputHandler( inputStruct:table )</p>

<p>local uiMsg = inputStruct:GetMessageType();</p>
<p>if (uiMsg == KeyEvents.KeyDown) then return KeyHandler( inputStruct:GetKey() ); end;</p>
<p>return false;</p>

<p>end</p>
<p>ContextPtr:SetInputHandler( InputHandler, true );</p>
</div> <!-- panel body --> 
</div> <!-- panel -->

<div class="panel panel-primary" id="Forge%20UI%5CLUA%20Reference">
<div class="panel-heading">
<div class="panel-title">LUA Reference
</div>
</div>
<div class="panel-body">

<p>LUA Reference</p>
<p>Wednesday, October 08, 2014</p>
<p>3:12 PM</p>

<p>Common attributes of a control can be changed and edited during runtime using specific methods in LUA. For example, changing the size of a window, showing or hiding it, changing its screen location, etc. can all be done in this manner.</p>

<p><em>Examples:</em></p>
<p>Controls.MyControl:SetSizeVal(width, height);</p>
<p>Controls.MyControl:SetHide(false);</p>


<p><strong>Control Operations</strong></p>

<p><strong>ContextPtr:LookUpControl( path )</strong></p>
<p>Looks up a control based on it's placement in the UI control tree. If found returns the control itself; otherwise returns NIL.</p>
<p>The path uses forward slashes (&quot;/&quot;) between contexts and controls in the tree.</p>
<p>If the context being used has to step up the tree, from where it's at, two dots (&quot;..&quot;) can be used to jump up to the parent.</p>
<p>Wildcards via an asterisk (&quot;*&quot;) can be used anywhere in the path except for the controls name. If there are more than two controls with the same name, the first control found with a matching name will be returned. When possible, avoid wildcard lookups, as they can be expensive.</p>

<p><strong>Examples:</strong></p>
<p>local a = ContextPtr:LookUpControl(&quot;/FrontEnd/FrontEndPopup/CloseButton&quot;); -- Start at root</p>
<p>local b = ContextPtr:LookUpControl(&quot;../FrontEndPopup/CloseButton&quot;); -- Go up one level from current context</p>
<p>local c = ContextPtr:LookUpControl(&quot;/FrontEnd/*/CloseButton&quot;); -- Use a wildcard for a child context</p>
<p>local d = ContextPtr:LookUpControl(&quot;*/FrontEndPopup/CloseButton&quot;); -- Use a wildcard from the root contexts</p>
<p>local e = ContextPtr:LookUpControl(&quot;*/*/CloseButton&quot;); -- Multiple wildcards from the root contexts</p>
<p>local f = ContextPtr:LookUpControl(&quot;../FrontEndPopup/*&quot;); -- NOT LEGAL, wildcards cannot be used for a control name</p>


<p><strong>String Operators:</strong></p>
<p>Commands that, when placed in a string, will result in special behavior.</p>

<table>
<thead>
<tr class="header">
<th><strong>[NEWLINE]</strong></th>
<th>inserts a carriage return into a string.</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>[COLOR:ColorName] text string you want to color [ENDCOLOR]</strong></td>
<td>to dynamically set the color of a string of text to something other than the default. 'ColorName' is the name of the color defined in the project color atlas.</td>
</tr>
<tr class="even">
<td><strong>[ICON_name]</strong></td>
<td>Pulls out a graphic &quot;icon&quot; from the Text Icon Atlas and inserts it into the text field.</td>
</tr>
</tbody>
</table>


<p><strong>Text and Localization</strong></p>

<p><strong>LocalizeAndSetText() </strong></p>
<p>Localize then set the text string on a control.</p>

<p><strong>SetToolTipString(&quot;myString&quot;) </strong></p>
<p>Set the text for the tooltip of the control.</p>

<p><strong>SetText(&quot;mystring&quot;)</strong></p>
<p>Set the text on a control.</p>

<p><strong>LocalizeAndSetToolTip(&quot;MY_TEXT_KEY&quot;) </strong></p>
<p>Localize then set the text for the tooltip of the control.</p>

<p><strong>Locale.Lookup(&quot;MY_TEXT_KEY&quot;)</strong></p>
<p>Convert the text key to its localized equivalent.</p>


<p><strong>Tutorial Manager</strong></p>

<p><strong>UITutorialManager:ShowControlsByID(&quot;triggerID&quot;)</strong></p>
<p>Turn on a control (or series of controls) that are listening for a certain trigger ID.</p>

<p><strong>UITutorialManager:HideControlsByID(&quot;triggerID&quot;)</strong></p>
<p>Turn off a control (or series of controls) that are listening for a certain trigger ID.</p>

<p><strong>UITutorialManager:HideAll()</strong></p>
<p>Turn off any/all tutorial controls.</p>

<p><strong>UITutorialManager:AddControlToAlwaysReceiveInput( control );</strong></p>
<p>Set a control to always be active (essentially ignore tutorial calls)</p>

</div> <!-- panel body --> 
</div> <!-- panel -->

<div class="panel panel-primary" id="Forge%20UI%5CReference%20Guide">
<div class="panel-heading">
<div class="panel-title">Reference Guide
</div>
</div>
<div class="panel-body">

<p><span id="1" class="anchor"></span></p>
<p>Reference Guide</p>
<p>Madrid</p>
<p>Exported on Jul 26, 2017</p>
<h1 id="controls">Controls</h1>
<p>A 'Control' is the smallest discrete UI component, such as a button or a text box. ForgeUI has the following control types:</p>
<h2 id="layout-controls">Layout Controls</h2>
<h3 id="container">Container</h3>
<p>The Container is the most basic control in ForgeUI. All other controls inherit from it. It is useful for making a group of other controls that can be modified together.</p>
<h3 id="group">Group</h3>
<p>Similar to container, but allows clipping</p>
<h3 id="tabcontrol">TabControl</h3>
<p>A control that allows for switching between different panels by clicking tabs</p>
<h3 id="scrollpanel">ScrollPanel</h3>
<p>A container that allows its children to be moved with a scrollbar, and clips children that are out of range</p>
<h3 id="worldanchor">WorldAnchor</h3>
<p>A control that is tied to a position in the 3D world</p>
<h3 id="stack">Stack</h3>
<p>A container that arranges its children in order, based on the position of the previous child. Stacks can arrange their children linearly or in a 2D grid</p>
<p><img src="Forge UI\Reference Guide/media/image1.png" alt="/download/attachments/168854679/stack.png?version=1&amp;modificationDate=1498673892670&amp;api=v2" width="531" height="109" /></p>
<h2 id="context-controls">Context Controls</h2>
<h3 id="context">Context</h3>
<p>A control containing controls specified in an XML file</p>
<h3 id="luacontext">LuaContext</h3>
<p>A Context that is backed by a Lua program</p>
<h2 id="animation-controls">Animation Controls</h2>
<h3 id="scrollanim">ScrollAnim</h3>
<p>An animated scrolling texture</p>
<h3 id="flipanim">FlipAnim</h3>
<p>A flip-book animation control</p>
<h3 id="slideanim">SlideAnim</h3>
<p>A container that allows for sliding its children across the screen</p>
<h3 id="alphaanim">AlphaAnim</h3>
<p>A container that allows for animating the transparency of its children</p>
<h2 id="visual-controls">Visual Controls</h2>
<h3 id="line">Line</h3>
<p>A control that draws a line segment between two points</p>
<h3 id="box-colorbox">Box / ColorBox</h3>
<p>A rectangular control that is filled with a single color</p>
<h3 id="bar">Bar</h3>
<p>A progress bar that uses solid colors</p>
<h3 id="texturebar">TextureBar</h3>
<p>A progress bar that uses a texture</p>
<h3 id="meter">Meter</h3>
<p>Rotating circular progress bar</p>
<h3 id="image">Image</h3>
<p>A control that contains an arbitrary texture</p>
<h3 id="grid">Grid</h3>
<p>A 9-slice image, where a texture is mapped to a 3x3 grid. This allows for the texture to stretch only the middle regions while the edges and corners remain uniform</p>
<p><img src="Forge UI\Reference Guide/media/image2.png" alt="/download/attachments/168854679/grid.png?version=1&amp;modificationDate=1498673727463&amp;api=v2" width="413" height="214" /></p>
<h3 id="label">Label</h3>
<p>A control that contains arbitrary text</p>
<h3 id="movie">Movie</h3>
<p>A control that can play a video (encoded with Bink)</p>
<h3 id="render">Render</h3>
<p>A control to draw a texture generated by the game</p>
<h3 id="graph">Graph</h3>
<p>A line graph, capable of displaying arbitrary data</p>
<h2 id="interactive-controls">Interactive Controls</h2>
<h3 id="button">Button</h3>
<p>A simple button with a solid color background</p>
<h3 id="boxbutton">BoxButton</h3>
<p>A button with a solid color background</p>
<h3 id="textbutton">TextButton</h3>
<p>A button with text on it</p>
<h3 id="gridbutton">GridButton</h3>
<p>A button with a 9-grid texture background</p>
<h3 id="editbox">EditBox</h3>
<p>A text box that allows the user to edit the text directly</p>
<h3 id="listbox">ListBox</h3>
<p>A control containing a list of entries</p>
<h3 id="multiselectlistbox">MultiSelectListBox</h3>
<p>A control that allows for selecting any number of options that are available</p>
<h3 id="checkbox">CheckBox</h3>
<p>A type of button with only 2 states</p>
<h3 id="radiobutton">RadioButton</h3>
<p>A button with only 2 states, where only one can be active at a time</p>
<h3 id="slider">Slider</h3>
<p>A control that allows the user to select a value with a slider e.g. volume</p>
<h3 id="pulldown">PullDown</h3>
<p>A drop-down box that can have multiple options within it</p>
<h3 id="simplepulldown">SimplePullDown</h3>
<p>Simplified (but less adaptable) version of PullDown</p>
<h3 id="drag">Drag</h3>
<p>A control that can be dragged with the mouse</p>
<h2 id="miscellaneous">Miscellaneous</h2>
<h3 id="tween">Tween</h3>
<h3 id="include">Include</h3>
<p>Includes the contents of an xml file into the existing context. It's mostly used to include instances shared by multiple contexts.</p>
<h3 id="makeinstance">MakeInstance</h3>
<p>Creates an instance of an object; similar to calling <strong>ContextPtr:BuildInstanceForControl</strong>. If the ID attribute is defined, you can access the instance via Controls table.</p>
<h3 id="tooltiptype">ToolTipType</h3>
<h3 id="tutorial">Tutorial</h3>
<h1 id="attributes">Attributes</h1>
<p>Each control can have the following attributes to initialize them, some controls have additional attributes that can only be used with that control type</p>
<table>
<thead>
<tr class="header">
<th>Attribute</th>
<th>Description</th>
<th>Examples</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Size<span id="scroll-bookmark-80" class="anchor"></span></td>
<td><p>The size of the control. The size can be specified as one of the following:</p>
<ul>
<li>
<p>number: the absolute size of the control in pixels</p>
</li>
<li>
<p>parent[+/-number]: size is relative to the parent control (top-level controls use the screen resolution)</p>
</li>
<li>
<p>auto: size is relative to the region taken up by children</p>
</li>
</ul>
<p><em>Note: 'full' has been deprecated, use 'parent' instead</em></p></td>
<td>Size=&quot;parent-16, parent&quot;<br />
Size=&quot;1920, auto&quot;</td>
</tr>
<tr class="even">
<td>Offset</td>
<td>the position relative to the parent</td>
<td>Offset=&quot;16, 0&quot;</td>
</tr>
<tr class="odd">
<td>ClampSize</td>
<td>whether to limit the control's size to its parent's size. Can be 1, 0, True, False, Vertical, or Horizontal</td>
<td>ClampSize=&quot;1&quot;<br />
ClampSize=&quot;False&quot;<br />
ClampSize=&quot;Vertical&quot;</td>
</tr>
<tr class="even">
<td>InnerPadding</td>
<td>The amount of padding used when a child uses parent sizing</td>
<td>InnerPadding=8,0&quot;</td>
</tr>
<tr class="odd">
<td>MinSize</td>
<td>The minimum size of this control when calculating auto size</td>
<td>MinSize=&quot;32, 32&quot;</td>
</tr>
<tr class="even">
<td>Anchor</td>
<td><p>Which edge of the parent to anchor to:<br />
X axis can be: L, C, or R (left, center, or right respectively)<br />
Y axis can be: T, C, or B (top, center, or bottom respectively)</p>
<p><img src="Forge UI\Reference Guide/media/image3.png" alt="/download/attachments/168854679/anchor.png?version=1&amp;modificationDate=1498672831210&amp;api=v2" width="298" height="249" /></p></td>
<td>Anchor=&quot;C,C&quot;<br />
Anchor=&quot;R,B&quot;</td>
</tr>
<tr class="odd">
<td>AnchorSide</td>
<td><p>Whether to anchor on the inside or outside of the parent: I=Inside, O=Outside</p>
<p><img src="Forge UI\Reference Guide/media/image4.png" alt="/download/attachments/168854679/anchorside.png?version=1&amp;modificationDate=1498672869350&amp;api=v2" width="351" height="86" /></p></td>
<td>AnchorSide=&quot;I,O&quot;</td>
</tr>
<tr class="even">
<td>Color</td>
<td><p>The color to use for this control (unused by several control types)</p>
<p>RGBA values range from 0-255, alpha is optional.</p>
<p>A color name will use the values defined in Civ6_ColorAtlas.xml</p></td>
<td>Color=&quot;206,218,225,255&quot;<br />
Color=&quot;255,255,255&quot;<br />
Color=&quot;White&quot;<br />
Color=&quot;Black,128&quot;</td>
</tr>
<tr class="odd">
<td>ID</td>
<td>The ID used to refer to this control in lua</td>
<td>ID=&quot;Foo&quot;</td>
</tr>
<tr class="even">
<td>Hidden</td>
<td>Whether this control is currently visible</td>
<td>Hidden=&quot;1&quot;</td>
</tr>
<tr class="odd">
<td>NeedsMouseOver</td>
<td>Whether this control should be notified when the mouse hovers over it</td>
<td>NeedsMouseOver=&quot;0&quot;</td>
</tr>
<tr class="even">
<td>NoClip</td>
<td>Whether to ignore clipping</td>
<td>NoClip=&quot;1&quot;</td>
</tr>
<tr class="odd">
<td>GlobalUpdate</td>
<td>Whether to update this control even when it isn't visible</td>
<td>GlobalUpdate=&quot;0&quot;</td>
</tr>
<tr class="even">
<td>ConsumeMouse<br />
ConsumeAllMouse</td>
<td>Whether this control consumes all mouse actions</td>
<td>ConsumeMouseButton=&quot;1&quot;</td>
</tr>
<tr class="odd">
<td>ConsumeMouseButton</td>
<td>Whether mouse clicks are consumed by this control</td>
<td>ConsumeMouseButton=&quot;0&quot;</td>
</tr>
<tr class="even">
<td>ConsumeMouseOver</td>
<td>Whether mouse movement is consumed by this control</td>
<td>ConsumeMouseOver=&quot;1&quot;</td>
</tr>
<tr class="odd">
<td>ConsumeMouseWheel</td>
<td>Whether mouse wheel movement is consumed by this control</td>
<td>ConsumeMouseWheel=&quot;0&quot;</td>
</tr>
<tr class="even">
<td>ModalBlocksInput</td>
<td>Whether this control allows input through while it is modal</td>
<td>ModalBlocksInput=&quot;1&quot;</td>
</tr>
<tr class="odd">
<td>Disabled</td>
<td>Whether this control is in a disabled state</td>
<td>ModalBlocksInput=&quot;0&quot;</td>
</tr>
<tr class="even">
<td>AutoSize</td>
<td><em>deprecated, use 'auto' in the Size attribute</em></td>
<td>AutoSize=&quot;Vertical&quot;</td>
</tr>
<tr class="odd">
<td>AutoSizePadding<br />
SizePadding</td>
<td>The border around children to add when auto size is calculated</td>
<td>AutoSizePadding=&quot;16, 0&quot;</td>
</tr>
<tr class="even">
<td>Padding</td>
<td><em>deprecated, same as AutoSizePadding and SizePadding</em></td>
<td>Padding=&quot;32, 32&quot;</td>
</tr>
<tr class="odd">
<td>Alpha</td>
<td>The opacity of this control and its children</td>
<td>Alpha=&quot;0.3&quot;</td>
</tr>
<tr class="even">
<td>ToolTip</td>
<td>The text to show when the mouse is hovering over this control</td>
<td>ToolTip=&quot;Foo&quot;</td>
</tr>
<tr class="odd">
<td>ToolTipType</td>
<td>The type of panel to use when showing the tool tip</td>
<td>ToolTipType=&quot;CivTooltip&quot;</td>
</tr>
<tr class="even">
<td>ShowOnMouseOver<br />
HideOnMouseOver<br />
ShowOnMouseOut</td>
<td>Whether to show or hide this control when the mouse moves</td>
<td>ShowOnMouseOver=&quot;1&quot;</td>
</tr>
<tr class="odd">
<td>debug<br />
d</td>
<td>* highlights the control with a random colored rectangle<br />
# sets the debug tag</td>
<td>d=&quot;*&quot;<br />
d=&quot;#2&quot;</td>
</tr>
</tbody>
</table>
<h1 id="lua">Lua</h1>
<p>The controls defined in a LuaContext can be controlled via Lua. To refer to a named control, use the namespace 'Controls' e.g. Controls.Background would be a control with the ID 'Background'</p>
<p>All controls have the following exposed methods, certain controls have additional methods that can only be used with that control type:</p>
<table>
<thead>
<tr class="header">
<th>Method</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>SetOffset</td>
<td>sets the control's offset to the specified value, which is a 2D vector</td>
</tr>
<tr class="even">
<td>SetOffsetX</td>
<td>sets the control's X offset to the specified float value</td>
</tr>
<tr class="odd">
<td>SetOffsetY</td>
<td>sets the control's Y offset to the specified float value</td>
</tr>
<tr class="even">
<td>SetOffsetVal</td>
<td>sets the control's offset to the specified X, Y float values</td>
</tr>
<tr class="odd">
<td>GetOffsetX</td>
<td>returns the X offset of this control</td>
</tr>
<tr class="even">
<td>GetOffsetY</td>
<td>returns the Y offset of this control</td>
</tr>
<tr class="odd">
<td>GetOffsetVal</td>
<td>returns both the X and Y offsets of this control</td>
</tr>
<tr class="even">
<td>GetScreenOffset</td>
<td>returns the offset from the top left corner of the screen</td>
</tr>
<tr class="odd">
<td>SetAnchor</td>
<td>anchors the control based on the specified comma-delimited string</td>
</tr>
<tr class="even">
<td>SetAllChildrenVisible</td>
<td>shows/hides all children based on the boolean argument</td>
</tr>
<tr class="odd">
<td>SetHide</td>
<td>sets the controls visibility based on the specified boolean value</td>
</tr>
<tr class="even">
<td>SetShow</td>
<td>sets the controls visibility based on the specified boolean value</td>
</tr>
<tr class="odd">
<td>SetNoClip</td>
<td>enables/disables clipping based on the specified boolean value</td>
</tr>
<tr class="even">
<td>IsHidden</td>
<td>returns whether the control is invisible</td>
</tr>
<tr class="odd">
<td>IsVisible</td>
<td>returns whether the control is visible</td>
</tr>
<tr class="even">
<td>GetNumChildren</td>
<td>returns the number of children the control has</td>
</tr>
<tr class="odd">
<td>GetChildren</td>
<td>returns a table containing all the children of this control</td>
</tr>
<tr class="even">
<td>ReprocessAnchoring</td>
<td>forces the control to update its position and size relative to its parent</td>
</tr>
<tr class="odd">
<td>GetSizeX</td>
<td>returns the width of the control<br />
<em>note: it is suggested to use relative sizing as much as possible instead of manually sizing controls in lua</em></td>
</tr>
<tr class="even">
<td>GetSizeY</td>
<td>returns the height of the control<br />
<em>note: it is suggested to use relative sizing as much as possible instead of manually sizing controls in lua</em></td>
</tr>
<tr class="odd">
<td>GetSizeVal</td>
<td>returns both the width and height of the control<br />
<em>note: it is suggested to use relative sizing as much as possible instead of manually sizing controls in lua</em></td>
</tr>
<tr class="even">
<td>SetSize</td>
<td>sets the size of the control to the specified value, which is a 2D vector</td>
</tr>
<tr class="odd">
<td>SetSizeX</td>
<td>sets the width of the control to the specified float value</td>
</tr>
<tr class="even">
<td>SetSizeY</td>
<td>sets the height of the control to the specified float value</td>
</tr>
<tr class="odd">
<td>SetSizeVal</td>
<td>sets the width and height of the control to the specified X, Y float values</td>
</tr>
<tr class="even">
<td>DoAutoSize</td>
<td>forces the control to resize based on its children</td>
</tr>
<tr class="odd">
<td>GetParentRelativeSizeX</td>
<td>returns the X modifier this control uses when calculating parent sizing</td>
</tr>
<tr class="even">
<td>GetParentRelativeSizeY</td>
<td>returns the Y modifier this control uses when calculating parent sizing</td>
</tr>
<tr class="odd">
<td>GetParentRelativeSizeVal</td>
<td>returns both the X and Y modifiers this control uses when calculating parent sizing</td>
</tr>
<tr class="even">
<td>SetParentRelativeSize</td>
<td>sets the modifier used when calculating parent sizing to the specified value, which is a 2D vector</td>
</tr>
<tr class="odd">
<td>SetParentRelativeSizeX</td>
<td>sets the X modifier used when calculating parent sizing to the specified float</td>
</tr>
<tr class="even">
<td>SetParentRelativeSizeY</td>
<td>sets the Y modifier used when calculating parent sizing to the specified float</td>
</tr>
<tr class="odd">
<td>SetParentRelativeSizeVal</td>
<td>sets the modifiers used when calculating parent sizing to the specified X, Y float values</td>
</tr>
<tr class="even">
<td>GetParentRelativeOffset</td>
<td>returns the X and Y offset from the anchor position</td>
</tr>
<tr class="odd">
<td>SetColor</td>
<td>sets the color of this control, can be a table containing r, g, b values, a single integer encoding an rgb color, or separate rgb values</td>
</tr>
<tr class="even">
<td>SetColorByName</td>
<td>sets the color to the named color in the Civ6_ColorAtlas.xml file</td>
</tr>
<tr class="odd">
<td>SetAlpha</td>
<td>sets the control's opacity to the specified float value</td>
</tr>
<tr class="even">
<td>GetAlpha</td>
<td>returns the control's opacity</td>
</tr>
<tr class="odd">
<td>SortChildren</td>
<td>sort the children with the specified lua comparator function</td>
</tr>
<tr class="even">
<td>AddChildAtIndex</td>
<td>adds the specified control as a child at the specified ordinal, lower indices are rendered first, essentially 'behind' the higher indices</td>
</tr>
<tr class="odd">
<td>BranchResetAnimation</td>
<td>recursively reset any animations for this control and its children</td>
</tr>
<tr class="even">
<td>SetID</td>
<td>sets the name of this control to the specified string<br />
<em>note: does not change the values in the Controls namespace</em></td>
</tr>
<tr class="odd">
<td>GetID</td>
<td>returns the specified name of this control</td>
</tr>
<tr class="even">
<td>SetDisabled</td>
<td>enables/disable the control based on the boolean argument</td>
</tr>
<tr class="odd">
<td>IsDisabled</td>
<td>returns whether the control is disabled</td>
</tr>
<tr class="even">
<td>SetEnabled</td>
<td>enables/disable the control based on the boolean argument</td>
</tr>
<tr class="odd">
<td>IsEnabled</td>
<td>returns whether the control is enabled</td>
</tr>
<tr class="even">
<td>SetModal</td>
<td>sets the control to modal based on the boolean argument</td>
</tr>
<tr class="odd">
<td>IsModal</td>
<td>returns whether the control is in a modal state</td>
</tr>
<tr class="even">
<td>SetTag</td>
<td>sets the tag to the specified integer, useful for debugging</td>
</tr>
<tr class="odd">
<td>GetTag</td>
<td>gets the specified debug tag</td>
</tr>
<tr class="even">
<td>CalculateVisibilityBox</td>
<td>force the control to update its visibility box</td>
</tr>
<tr class="odd">
<td>SetToolTipCallback</td>
<td>set a lua function to be called when the tooltip is shown</td>
</tr>
<tr class="even">
<td>ClearToolTipCallback</td>
<td>remove the tooltip callback function</td>
</tr>
<tr class="odd">
<td>IsToolTipEnabled</td>
<td>returns whether there is a tooltip active for this control</td>
</tr>
<tr class="even">
<td>EnableToolTip</td>
<td>enables/disables the tooltip based on a boolean argument</td>
</tr>
<tr class="odd">
<td>SetToolTipType</td>
<td>sets the type of tooltip to a defined ToolTipType</td>
</tr>
<tr class="even">
<td>SetToolTipString</td>
<td>sets the string shown in the tooltip</td>
</tr>
<tr class="odd">
<td>LocalizeAndSetToolTip</td>
<td>sets the string shown in the tooltip after looking up the localized string</td>
</tr>
<tr class="even">
<td>GetToolTipString</td>
<td>returns the string shown in the tooltip</td>
</tr>
<tr class="odd">
<td>ChangeParent</td>
<td>change the parent of this control</td>
</tr>
<tr class="even">
<td>GetParent</td>
<td>returns the parent of this control</td>
</tr>
<tr class="odd">
<td>GetParentByType</td>
<td>recurse up the tree and find the first parent with the specified type</td>
</tr>
<tr class="even">
<td>GetParentByID</td>
<td>recurse up the tree and find the first parent with the specified name</td>
</tr>
<tr class="odd">
<td>Reparent</td>
<td>reattach this control to its parent, causing it to be at the last index</td>
</tr>
<tr class="even">
<td>HasMouseOver</td>
<td>returns whether the mouse is currently over this control</td>
</tr>
<tr class="odd">
<td>DestroyChild<br />
ReleaseChild</td>
<td>releases the specified child control</td>
</tr>
<tr class="even">
<td>SetConsumeMouseOver</td>
<td>enables/disables consuming mouse over input based on the specified boolean value</td>
</tr>
<tr class="odd">
<td>SetConsumeMouseButton</td>
<td>enables/disables consuming mouse click input based on the specified boolean value</td>
</tr>
<tr class="even">
<td>SetConsumeMouseWheel</td>
<td>enables/disables consuming mouse wheel input based on the specified boolean value</td>
</tr>
<tr class="odd">
<td>GetConsumeMouseOver</td>
<td>returns whether this control consumes mouse movement</td>
</tr>
<tr class="even">
<td>GetConsumeMouseButton</td>
<td>returns whether this control consumes mouse clicks</td>
</tr>
<tr class="odd">
<td>GetConsumeMouseWheel</td>
<td>returns whether this control consumes mouse wheel movement</td>
</tr>
<tr class="even">
<td>DestroyAllChildren</td>
<td>destroys all children of this control</td>
</tr>
<tr class="odd">
<td>RegisterMouseEnterCallback</td>
<td>set the function called when the mouse enters this control's bounding box</td>
</tr>
<tr class="even">
<td>RegisterMouseExitCallback</td>
<td>set the function called when the mouse exits this control's bounding box</td>
</tr>
<tr class="odd">
<td>RegisterMouseOverCallback</td>
<td>set the function called when the mouse is moved within this control's bounding box</td>
</tr>
<tr class="even">
<td>RegisterWhenShown</td>
<td>set the function called when the this control becomes visible</td>
</tr>
<tr class="odd">
<td>RegisterWhenHidden</td>
<td>set the function called when the this control becomes hidden</td>
</tr>
<tr class="even">
<td>ClearMouseEnterCallback</td>
<td>clear the function called when the mouse enters this control's bounding box</td>
</tr>
<tr class="odd">
<td>ClearMouseExitCallback</td>
<td>clear the function called when the mouse exits this control's bounding box</td>
</tr>
<tr class="even">
<td>ClearMouseOverCallback</td>
<td>clear the function called when the mouse is moved within this control's bounding box</td>
</tr>
</tbody>
</table>
</div> <!-- panel body --> 
</div> <!-- panel -->

<div class="panel panel-primary" id="Forge%20UI%5CControls%5CAlphaAnim">
<div class="panel-heading">
<div class="panel-title">AlphaAnim
</div>
</div>
<div class="panel-body">

<p><strong>&lt;AlphaAnim&gt;</strong></p>
<p>Friday, February 21, 2014</p>
<p>3:04 PM</p>
<p>Used to animate the alpha value of the control and all of its children.</p>

<p><strong>AlphaBegin</strong> - Alpha value to start at (float: 0.0 - 1.0)</p>
<p><strong> </strong></p>
<p><strong>AlphaEnd</strong> - Alpha value to end at (float: 0.0 - 1.0)</p>
<p><strong> </strong></p>
<p><strong>Texture</strong> - Optional texture</p>

<p>For additional controls see: <em>Animation</em></p>

<p><strong>LUA Methods</strong></p>

<table>
<thead>
<tr class="header">
<th><strong>Function</strong></th>
<th><strong>Returns</strong></th>
<th><strong>Arguments</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>SetTexture</strong></td>
<td>bool</td>
<td>string</td>
</tr>
<tr class="even">
<td><strong>SetTextureOffset</strong></td>
<td>void</td>
<td>FGXVector2</td>
</tr>
<tr class="odd">
<td><strong>SetTextureOffsetVal</strong></td>
<td>void</td>
<td>float x, float y</td>
</tr>
<tr class="even">
<td><strong>SetSize</strong></td>
<td>void</td>
<td>FGXVector2</td>
</tr>
<tr class="odd">
<td><strong>SetSizeVal</strong></td>
<td>void</td>
<td>float x, float y</td>
</tr>
</tbody>
</table>

<p>For Common LUA animation methods, see: <em>LUA Animation Methods</em></p>
</div> <!-- panel body --> 
</div> <!-- panel -->

<div class="panel panel-primary" id="Forge%20UI%5CControls%5CBar">
<div class="panel-heading">
<div class="panel-title">Bar
</div>
</div>
<div class="panel-body">

<p><strong>&lt;Bar&gt;</strong></p>
<p>Friday, February 21, 2014</p>
<p>3:05 PM</p>

<p>Progress bar control made of a solid color. For a bitmapped version see: <em>&lt;TextureBar&gt;</em></p>

<p><strong>XML</strong></p>
<table>
<thead>
<tr class="header">
<th><strong>Attribute</strong></th>
<th><strong>Type</strong></th>
<th><strong>Details</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>FGColor</td>
<td>String</td>
<td>The red, green, blue and (optional) alpha values to apply to the meter texture. (Default is white with full alpha e.g., &quot;255,255,255,255);</td>
</tr>
<tr class="even">
<td>BGColor</td>
<td>String</td>
<td> </td>
</tr>
<tr class="odd">
<td>Direction</td>
<td>String</td>
<td>In which way does the bar fill: <strong>&quot;Up&quot; &quot;Down&quot; &quot;Left&quot; &quot;Right&quot;</strong></td>
</tr>
<tr class="even">
<td>Percent</td>
<td>Number</td>
<td>Start value of the bar, by default this is 0.</td>
</tr>
<tr class="odd">
<td>Speed</td>
<td>Number</td>
<td>(default: &quot;<strong>0</strong>&quot;) What speed to animate the fill. If 0, no animation; immediately set percentage.</td>
</tr>
</tbody>
</table>


<p><strong>LUA Functions</strong></p>
<table>
<thead>
<tr class="header">
<th><strong>Function</strong></th>
<th><strong>Returns</strong></th>
<th><strong>Arguments</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>SetPercent</strong></td>
<td><strong>n/a</strong></td>
<td><strong>float</strong>, 0.0 - 1.0 percent of the texture bar that is displayed (filled)</td>
</tr>
<tr class="even">
<td><strong>SetShadowPercent</strong></td>
<td><strong>n/a</strong></td>
<td><strong>float</strong>, 0.0-1.0 percent of texture used as a 'drop shadow'</td>
</tr>
<tr class="odd">
<td><strong>SetAnimationSpeed</strong></td>
<td><strong>n/a</strong></td>
<td><strong>float</strong>, 0 to animation speed where 0 is none</td>
</tr>
</tbody>
</table>
</div> <!-- panel body --> 
</div> <!-- panel -->

<div class="panel panel-primary" id="Forge%20UI%5CControls%5CBox">
<div class="panel-heading">
<div class="panel-title">Box
</div>
</div>
<div class="panel-body">

<p><strong>&lt;Box&gt;</strong></p>
<p>Friday, February 21, 2014</p>
<p>2:21 PM</p>

<p>Box of solid color. (Also &lt;ColorBox&gt; but that is deprecated.)</p>

<p>For an empty region, use <strong>&lt;Container&gt;</strong> instead.</p>

<p><strong>XML</strong></p>
<table>
<thead>
<tr class="header">
<th><strong>Attribute</strong></th>
<th><strong>Type</strong></th>
<th><strong>Details</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Color</td>
<td>String</td>
<td>Values (0-255) for red, green, blue, and (optionally) alpha, separated by commas. e.g., an orange color: &quot;255,128,0,200&quot;</td>
</tr>
</tbody>
</table>

<p><strong>LUA Functions</strong></p>
<table>
<thead>
<tr class="header">
<th><strong>Function</strong></th>
<th><strong>Returns</strong></th>
<th><strong>Arguments</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>SetColor</strong></td>
<td><strong>n/a</strong></td>
<td><strong>uint</strong>, Either a single ABGR or RGBA value to represent the red, green, blue, and alpha values. By default uses ABGR. This can be changed to RGBA if the ForgeUI manager is called once at startup with <strong>SetColorFormatRGBA(true)</strong>.</td>
</tr>
</tbody>
</table>
</div> <!-- panel body --> 
</div> <!-- panel -->

<div class="panel panel-primary" id="Forge%20UI%5CControls%5CBoxButton">
<div class="panel-heading">
<div class="panel-title">BoxButton
</div>
</div>
<div class="panel-body">

<p><strong>&lt;BoxButton&gt;</strong></p>
<p>Friday, February 21, 2014</p>
<p>4:49 PM</p>

<p>Button control which is a rectangle of color only.</p>

<p><strong>XML</strong></p>

<p>No unique XML attributes, see <em>&lt;Button&gt;</em></p>


<p><strong>Example</strong></p>

<p>&lt;BoxButton ID=&quot;MySoothingButton&quot; Color=&quot;10,255,30,200&quot; Size=300,100 /&gt;</p>

</div> <!-- panel body --> 
</div> <!-- panel -->

<div class="panel panel-primary" id="Forge%20UI%5CControls%5CButton">
<div class="panel-heading">
<div class="panel-title">Button
</div>
</div>
<div class="panel-body">

<p>&lt;Button&gt;</p>
<p>Friday, February 21, 2014</p>
<p>4:43 PM</p>

<p>Simple button control using a texture map.</p>

<p>When the button state changes, we offset vertically down the texture according to the StateOffsetIncrement value in following order:</p>
<ol style="list-style-type: decimal">
<li>
<p>Normal</p>
</li>
<li>
<p>MouseOver</p>
</li>
<li>
<p>ButtonDown</p>
</li>
<li>
<p>Disabled.</p>
</li>
</ol>



<p>If no StateOffsetIncrement is specified, we assume to be moving by the y-size of the control (There are very few cases where this would not be appropriate, so StateOffsetIncrement is usually not necessary).</p>

<p><strong>XML</strong></p>
<table>
<thead>
<tr class="header">
<th><strong>Texture</strong></th>
<th>File to use for the texture</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>TextureOffset</strong></td>
<td>Offset within the texture</td>
</tr>
<tr class="even">
<td><strong>States</strong></td>
<td><p>(default 7) The number of states on a button. Valid values are 2,4,5,7, and 8. The states are:</p>
<p>1=up, 2=over, 3=down, 4=disabled, 5=selected, 6=selected over, 7=selected down, 8=8 selected disabled</p></td>
</tr>
<tr class="odd">
<td><strong>StateOffsetIncrement</strong></td>
<td>How far to offset the texture for state changes. If this is not specified, it is assumed to offset by the y-size of the control.</td>
</tr>
<tr class="even">
<td><strong>NoStateChange</strong></td>
<td>Flag that indicates that the texture should not be offset when state changes</td>
</tr>
<tr class="odd">
<td><strong>Sampler</strong></td>
<td>The sampler type to use to sample the texture. All images default to a point sampler, but we may specify &quot;Linear&quot; here if we want a non-point-sampled texture.</td>
</tr>
<tr class="even">
<td><strong>String</strong></td>
<td>Text to appear on the button.</td>
</tr>
<tr class="odd">
<td><strong>ToolTip</strong></td>
<td>Tool tip string</td>
</tr>
<tr class="even">
<td><strong>TextAnchor</strong></td>
<td>Anchoring flag for the text.</td>
</tr>
<tr class="odd">
<td><strong>TextOffset</strong></td>
<td>X,Y offset value for the text.</td>
</tr>
<tr class="even">
<td><strong>Color</strong></td>
<td>RGB tint for the button.</td>
</tr>
<tr class="odd">
<td><strong>DisabledCallbacks</strong></td>
<td>Triggers input callbacks when disabled.</td>
</tr>
</tbody>
</table>
<p><strong> </strong></p>


<p><strong>LUA Methods</strong></p>
<table>
<thead>
<tr class="header">
<th><strong>Function</strong></th>
<th><strong>Returns</strong></th>
<th><strong>Arguments</strong></th>
<th><strong>Description</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>ClearCallback</strong></td>
<td>void</td>
<td> </td>
<td>Clear the registered callback function.</td>
</tr>
<tr class="even">
<td><strong>GetVoid1</strong></td>
<td>void</td>
<td> </td>
<td> </td>
</tr>
<tr class="odd">
<td><strong>GetVoid2</strong></td>
<td>void</td>
<td> </td>
<td> </td>
</tr>
<tr class="even">
<td><strong>IsTrackingLeftMouseButton</strong></td>
<td>bool</td>
<td> </td>
<td> </td>
</tr>
<tr class="odd">
<td><strong>IsTrackingRightMouseButton</strong></td>
<td>bool</td>
<td> </td>
<td> </td>
</tr>
<tr class="even">
<td><strong>IsTrackingMiddleMouseButton</strong></td>
<td>bool</td>
<td> </td>
<td> </td>
</tr>
<tr class="odd">
<td><strong>IsTrackingTouch</strong></td>
<td>bool</td>
<td> </td>
<td> </td>
</tr>
<tr class="even">
<td><strong>RegisterCallback</strong></td>
<td>void</td>
<td>state, function</td>
<td><p>Sets a LUA function to receive callbacks. State may be one of:</p>

<p>eLClick</p>
<p>eRClick</p>
<p>eMClick</p>
<p>eLDbClick</p>
<p>eRDblClick</p>
<p>eMDblClick</p>
<p>eTap</p>
<p>eDblTap</p>
<p>eWheel</p>
<p>eMouseEnter</p>
<p>eMouseExit</p>
</td>
</tr>
<tr class="odd">
<td><strong>ReceiveCallbacksIfDisabled</strong></td>
<td>void</td>
<td>bool</td>
<td>Sets whether input callbacks trigger when disabled.</td>
</tr>
<tr class="even">
<td><strong>SetDisabled</strong></td>
<td>void</td>
<td>bool</td>
<td>Sets button to be in &quot;Disabled&quot; (note: from ControlBase)</td>
</tr>
<tr class="odd">
<td><strong>SetSelected</strong></td>
<td>void</td>
<td>bool</td>
<td>Sets button to be in &quot;Selected Mode&quot;</td>
</tr>
<tr class="even">
<td><strong>SetVoid1</strong></td>
<td>void</td>
<td>bool/string/number</td>
<td>Set a value to be used in a return call.</td>
</tr>
<tr class="odd">
<td><strong>SetVoid2</strong></td>
<td>void</td>
<td>bool/string/number</td>
<td>Set a value to be used in a return call.</td>
</tr>
<tr class="even">
<td><strong>SetVoids</strong></td>
<td>void</td>
<td>x2 bool/string/number</td>
<td>Set both of the values to be used in a return call.</td>
</tr>
</tbody>
</table>

<p><strong> </strong></p>
<p><strong> </strong></p>
<p><strong> </strong></p>
</div> <!-- panel body --> 
</div> <!-- panel -->

<div class="panel panel-primary" id="Forge%20UI%5CControls%5CCheckBox">
<div class="panel-heading">
<div class="panel-title">CheckBox
</div>
</div>
<div class="panel-body">

<p>&lt;CheckBox&gt;</p>
<p>Friday, February 21, 2014</p>
<p>4:58 PM</p>

<p>The check box control consists of a normal button with an overlaid <strong>CheckTexture</strong> and a text button label which can be clicked.</p>

<p>The size and position control the check box and the text button is positioned relative to the check box.</p>

<p>All attributes are passed through to the inherent TextButton control which itself builds from the inherent Text control. As such the attributes listed below are either common to be set or unique to checkboxes but there are additional attribute that can be set (e.g., “Font”, “NormalColor”, etc…)</p>

<table>
<thead>
<tr class="header">
<th><strong>Attribute</strong></th>
<th><strong>Details</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>BoxOnLeft</strong></td>
<td>Replaces “<strong>TextAnchor</strong>”, if true places the box on the left of the text button, instead of to the right.</td>
</tr>
<tr class="even">
<td><strong>ButtonSize</strong></td>
<td><strong>Required</strong> Size of the check button itself.</td>
</tr>
<tr class="odd">
<td><strong>ButtonTexture</strong></td>
<td><strong>Required</strong> Texture to use for the button</td>
</tr>
<tr class="even">
<td><strong>CheckColor</strong></td>
<td>A color to tint the checked image.</td>
</tr>
<tr class="odd">
<td><strong>CheckOffset</strong></td>
<td>Coordinate for positioning the check over the button.</td>
</tr>
<tr class="even">
<td><strong>CheckSize</strong></td>
<td>Size of the check texture.</td>
</tr>
<tr class="odd">
<td><strong>CheckTexture</strong></td>
<td>Texture to use as the check mark.</td>
</tr>
<tr class="even">
<td><strong>CheckTextureOffset</strong></td>
<td>Offset into the check texture.</td>
</tr>
<tr class="odd">
<td><strong>IsChecked</strong></td>
<td>Flag indicating the box should start checked</td>
</tr>
<tr class="even">
<td><strong>String</strong></td>
<td>Set the label</td>
</tr>
<tr class="odd">
<td><strong><del>TextAnchor</del></strong></td>
<td><del>DEPRECATED Anchor flag for the TextButton</del></td>
</tr>
<tr class="even">
<td><strong>TextButtonData</strong></td>
<td>All of the tags used for the TextButton control are used here to describe the text button portion of the check box</td>
</tr>
<tr class="odd">
<td><strong>TextOffset</strong></td>
<td>Offset of the TextButton portion from the check button</td>
</tr>
<tr class="even">
<td><strong>UnCheckColor</strong></td>
<td>A color to tint the image used in the uncheck state</td>
</tr>
<tr class="odd">
<td><strong>UnCheckOffset</strong></td>
<td>Same as CheckOffset but for the UnCheckTexture</td>
</tr>
<tr class="even">
<td><strong>UnCheckSize</strong></td>
<td>Same as CheckSize but for the UnCheckTexture</td>
</tr>
<tr class="odd">
<td><strong>UnCheckTexture</strong></td>
<td>A texture to show on top of the button when unchecked</td>
</tr>
<tr class="even">
<td><strong>UnCheckTextureOffset</strong></td>
<td>Same as CheckTextureOffset but for the UnCheckTexture</td>
</tr>
<tr class="odd">
<td><strong>UseSelectedTextures</strong></td>
<td>The button of the checkbox has &quot;selected&quot; states (for normal, over, and down) which should be used when checked.</td>
</tr>
</tbody>
</table>
</div> <!-- panel body --> 
</div> <!-- panel -->

<div class="panel panel-primary" id="Forge%20UI%5CControls%5CContainer">
<div class="panel-heading">
<div class="panel-title">Container
</div>
</div>
<div class="panel-body">

<p>&lt;Container&gt;</p>
<p>Friday, February 21, 2014</p>
<p>1:50 PM</p>

<p>The <strong>&lt;Container&gt;</strong> is the most basic control in the system. All other controls extend this and so all of these tags are usable on all other controls. It is most useful for making a group of controls that can be shown/hidden easily. It is likely more useful to the UI Programmer than the UI Artist.</p>

<p>Class name ControlBase.</p>


<p><strong>XML</strong></p>
<table>
<thead>
<tr class="header">
<th><strong>Attributed</strong></th>
<th><strong>Details</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>Alpha</strong></td>
<td>A 0-1 value used for the alpha for this control AND all of its children.</td>
</tr>
<tr class="even">
<td><strong>Anchor</strong></td>
<td>Where on its parent this control is attached.</td>
</tr>
<tr class="odd">
<td><strong>AnchorSide</strong></td>
<td>Whether the control is attached to the Inside or Outside of its parent (in X and Y).</td>
</tr>
<tr class="even">
<td><strong>AutoSize</strong></td>
<td><p>0, 1, V or H. If 1 control will completely autosize. If 0 it won't at all.</p>
<p>If V will only autosize vertically.</p>
<p>If H will only autosize horizontally.</p>
<p>Autosizing is based on the total size of its children. This will only happen at load time. If the children are changing sizes, the programmer must call DoAutoSize() at runtime.</p></td>
</tr>
<tr class="odd">
<td><strong>AutoSizePadding</strong></td>
<td>The amount of padding in X,Y to add when doing the AutoSize calculation. Formally “<strong>Padding</strong>”.</td>
</tr>
<tr class="even">
<td><strong>Color</strong></td>
<td>What color this control should be. The scale is 0-255, can include an alpha channel, and can use a named color. This is not used for all control types and only affects this control, not its children.</td>
</tr>
<tr class="odd">
<td><strong>ConsumeAllMouse</strong></td>
<td>Flag to indicate that this control should consume all mouse events that happen while it is being moused-over.</td>
</tr>
<tr class="even">
<td><strong>ConsumeMouseButton</strong></td>
<td>Flag to indicate that this control should consume mouse button events that happen while it is being moused-over.</td>
</tr>
<tr class="odd">
<td><strong>ConsumeMouseOver</strong></td>
<td>Flag to indicate that this control should consume mouse move events that happen while it is being moused-over.</td>
</tr>
<tr class="even">
<td><strong>ConsumeMouseWheel</strong></td>
<td>Flag to indicate that this control should consume mouse wheel events that happen while it is being moused-over.</td>
</tr>
<tr class="odd">
<td><strong>d</strong></td>
<td>1-6, or &quot;*&quot; and an optional &quot;+&quot;. Set debug flags. 1-6 will set a color. &quot;*&quot; will pick a random color. &quot;+&quot; will cascade to child controls. This attribute is purposely lowercase and a single letter so a author can add/remove quickly.</td>
</tr>
<tr class="even">
<td><strong>Disabled</strong></td>
<td>Flag to indicate that this control is disabled and should not get mouseover state or be clickable.</td>
</tr>
<tr class="odd">
<td><strong>GlobalUpdate</strong></td>
<td>Programmer flag. Used to make controls receive update ticks even when invisible.</td>
</tr>
<tr class="even">
<td><strong>Hidden</strong></td>
<td>Whether this control (and all of its children) should be drawn.</td>
</tr>
<tr class="odd">
<td><strong>HideOnMouseOver</strong></td>
<td>Flag to indicate that this control should only be visible when its parent is NOT being moused-over.</td>
</tr>
<tr class="even">
<td><strong>ID</strong></td>
<td>The controls name. Used by the programmer to work with this control at runtime. This value must be unique.</td>
</tr>
<tr class="odd">
<td><strong>InnerOffset</strong></td>
<td>Used with AutoSize</td>
</tr>
<tr class="even">
<td><strong>InnerPadding</strong></td>
<td>Used with AutoSize</td>
</tr>
<tr class="odd">
<td><strong>NeedsMouseOver</strong></td>
<td>Programmer flag. Indicates that the control needs mouse information.</td>
</tr>
<tr class="even">
<td><strong>NoClip</strong></td>
<td>Flag to indicate that this control is not affected when put inside of a scroll panel.</td>
</tr>
<tr class="odd">
<td><strong>Offset</strong></td>
<td>How far away from the anchor point the control is.</td>
</tr>
<tr class="even">
<td><strong>ShowOnMouseOver</strong></td>
<td>Flag to indicate that this control should only be visible when its parent is being moused-over.</td>
</tr>
<tr class="odd">
<td><strong>ShowOnMouseOut</strong></td>
<td>Similar to HideOnMouseOver but will not show the contents when first visible. Best utilized for mouse out animations.</td>
</tr>
<tr class="even">
<td><strong>Size</strong></td>
<td>The size on screen in pixels.</td>
</tr>
<tr class="odd">
<td><strong>SizePadding</strong></td>
<td>Alt name for “<strong>AutoSizePadding</strong>” (see above).</td>
</tr>
<tr class="even">
<td><strong>ToolTip</strong></td>
<td>Simple tooltip text string when mousing over this control.</td>
</tr>
<tr class="odd">
<td><strong>ToolTipType</strong></td>
<td>Name of a complex tool tip type to use when mousing over this control.</td>
</tr>
<tr class="even">
<td><strong>TutorialActive</strong></td>
<td>This control, and its children, will show on top of the tutorial overlay and be responsive to input. Essentially, when a tutorial is on, this control continues to behave as it normally would.</td>
</tr>
</tbody>
</table>

<p><strong>LUA</strong></p>
<table>
<thead>
<tr class="header">
<th><strong>Function</strong></th>
<th><strong>Returns</strong></th>
<th><strong>Arguments</strong></th>
<th><strong>Description</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>RegisterMouseEnterCallback</strong></td>
<td> </td>
<td> </td>
<td> </td>
</tr>
<tr class="even">
<td><strong>RegisterMouseExitCallback</strong></td>
<td> </td>
<td> </td>
<td> </td>
</tr>
<tr class="odd">
<td><strong>RegisterMouseOverCallback</strong></td>
<td> </td>
<td> </td>
<td> </td>
</tr>
<tr class="even">
<td><strong><del>(RegisterWhenClippedCallback)</del></strong></td>
<td>float</td>
<td>void</td>
<td>WARNING! This is per-frame and likely the most expensive of any LUA operation. You will hurt performance by using this and it's very likely this function will go away. Don't use it.</td>
</tr>
<tr class="odd">
<td><strong>RegisterWhenShown</strong></td>
<td> </td>
<td> </td>
<td> </td>
</tr>
<tr class="even">
<td><strong>RegisterWhenHidden</strong></td>
<td> </td>
<td> </td>
<td> </td>
</tr>
<tr class="odd">
<td><strong>SetColorByName</strong></td>
<td>void</td>
<td>string</td>
<td>Sets the color of the control based on a name from the color atlas.</td>
</tr>
<tr class="even">
<td><strong>SetHide</strong></td>
<td>void</td>
<td>bool</td>
<td> </td>
</tr>
<tr class="odd">
<td><strong>SetOffsetVal</strong></td>
<td>void</td>
<td>float x, float y</td>
<td> </td>
</tr>
<tr class="even">
<td><strong>GetOffsetVal</strong></td>
<td>float x, float y</td>
<td>..</td>
<td> </td>
</tr>
<tr class="odd">
<td><strong>SetSizeVal</strong></td>
<td>void</td>
<td>float x, float y</td>
<td> </td>
</tr>
<tr class="even">
<td><strong>GetSizeVal</strong></td>
<td>float x, float y</td>
<td>..</td>
<td> </td>
</tr>
<tr class="odd">
<td><strong>SetAnchor</strong></td>
<td>void</td>
<td>String - See <em>'Anchor'</em> attribute</td>
<td> </td>
</tr>
<tr class="even">
<td><strong>SetDisabled</strong></td>
<td>void</td>
<td>bool</td>
<td> </td>
</tr>
<tr class="odd">
<td><strong>SetHide</strong></td>
<td>void</td>
<td>bool</td>
<td> </td>
</tr>
<tr class="even">
<td><strong>SetSizeX</strong></td>
<td>void</td>
<td>float</td>
<td> </td>
</tr>
<tr class="odd">
<td><strong>SetSizeY</strong></td>
<td>void</td>
<td>float</td>
<td> </td>
</tr>
<tr class="even">
<td><strong>GetSizeX</strong></td>
<td>float</td>
<td>..</td>
<td> </td>
</tr>
<tr class="odd">
<td><strong>GetSizeY</strong></td>
<td>float</td>
<td>..</td>
<td> </td>
</tr>
<tr class="even">
<td><strong>SetOffsetX</strong></td>
<td>void</td>
<td>float</td>
<td> </td>
</tr>
<tr class="odd">
<td><strong>SetOffsetY</strong></td>
<td>void</td>
<td>float</td>
<td> </td>
</tr>
<tr class="even">
<td><strong>GetOffsetX</strong></td>
<td>float</td>
<td>..</td>
<td> </td>
</tr>
<tr class="odd">
<td><strong>GetOffsetY</strong></td>
<td>float</td>
<td>..</td>
<td> </td>
</tr>
</tbody>
</table>
</div> <!-- panel body --> 
</div> <!-- panel -->

<div class="panel panel-primary" id="Forge%20UI%5CControls%5CContext">
<div class="panel-heading">
<div class="panel-title">Context
</div>
</div>
<div class="panel-body">

<p>&lt;Context&gt;</p>
<p>Friday, February 21, 2014</p>
<p>5:08 PM</p>

<p>Control to load a new .XML file of controls.</p>
<p>This is also frequently the top level XML tag for a file; it's used differently based on where it's used.</p>

<p>When not the top level tag of the file, the following attributes are allowed:</p>
<table>
<thead>
<tr class="header">
<th><strong>Attribute</strong></th>
<th><strong>Details</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>FileName</strong></td>
<td>Name of the xml file to load (without the .xml extension)</td>
</tr>
</tbody>
</table>


<p>When it is the top level of a file these attributes can be used:</p>
<table>
<thead>
<tr class="header">
<th><strong>Attribute</strong></th>
<th><strong>Details</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>Layer</strong></td>
<td>(optional) Name of what rendering layer to draw on. Typically a game engine will be setup with named layers such as &quot;Debug&quot; or &quot;Modal&quot;. If the attribute is omitted, all contents will be rendered to the default rending layer.<br />
This should NOT be used for Z-order sorting UI as there are a limited # of layers, and typically the only reason a UI elements needs to be on a specific layer is because a shader effect is being applied to the default layer. (e.g., Bluring out the game and UI when a pop-up occurs; the pop-up will be on a special &quot;Modal&quot; layer so the shader isn't applied to it, but all UI on the default layer will be blurred.)</td>
</tr>
</tbody>
</table>
</div> <!-- panel body --> 
</div> <!-- panel -->

<div class="panel panel-primary" id="Forge%20UI%5CControls%5CDragPanel">
<div class="panel-heading">
<div class="panel-title">DragPanel
</div>
</div>
<div class="panel-body">

<p><strong>&lt;DragPanel&gt;</strong></p>
<p>Friday, February 21, 2014</p>
<p>2:23 PM</p>

<p>Panel that allows moving by gaining focus (e.g., holding the mouse down) and then dragging to a new position to reveal content clipped off of the top and bottom, left and right, or all 4 sides.</p>

<table>
<thead>
<tr class="header">
<th><strong>Attribute</strong></th>
<th><strong>Details</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>Horizontal</strong></td>
<td>(t/f, t default) Allow dragged scrolling in the horizontal axis.</td>
</tr>
<tr class="even">
<td><strong>Vertical</strong></td>
<td>(t/f, t default) Allow dragged scrolling in the vertical axis.</td>
</tr>
<tr class="odd">
<td><strong>ZoomMax</strong></td>
<td>Maximum zoom value sent to control / LUA.</td>
</tr>
<tr class="even">
<td><strong>ZoomMin</strong></td>
<td>Minimum zoom value sent to control / LUA.</td>
</tr>
<tr class="odd">
<td><strong>ZoomStep</strong></td>
<td>Increments of zooming via equivalent mouse wheel click.</td>
</tr>
</tbody>
</table>
</div> <!-- panel body --> 
</div> <!-- panel -->

<div class="panel panel-primary" id="Forge%20UI%5CControls%5CEditBox">
<div class="panel-heading">
<div class="panel-title">EditBox
</div>
</div>
<div class="panel-body">

<p><strong>&lt;EditBox&gt;</strong></p>
<p>Friday, February 21, 2014</p>
<p>2:25 PM</p>
<p>Control for user entered text.</p>

<table>
<thead>
<tr class="header">
<th><strong>Attribute</strong></th>
<th><strong>5</strong></th>
<th><strong>F</strong></th>
<th><strong>Details</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>CallOnChar</strong></td>
<td>Y</td>
<td>?</td>
<td> </td>
</tr>
<tr class="even">
<td><strong>ColorSet</strong></td>
<td>-</td>
<td>Y</td>
<td>The name of the colorset to use.</td>
</tr>
<tr class="odd">
<td><strong>CursorColor</strong></td>
<td>Y</td>
<td>Y</td>
<td>Color of the cursor</td>
</tr>
<tr class="even">
<td><strong>EditMode</strong></td>
<td>Y</td>
<td>Y</td>
<td><p>Flag to indicate this is for editing an existing string rather than entering a new string.</p>
<p>EditMode caches the existing string when it takes focus and will restore the cached version if the esc button is pressed.</p>
<p>EditMode also automatically calls the commit callback when the EditBox loses focus.</p></td>
</tr>
<tr class="odd">
<td><strong>FocusStop</strong></td>
<td>Y</td>
<td>Y</td>
<td> </td>
</tr>
<tr class="even">
<td><strong>Font</strong></td>
<td>-</td>
<td>Y</td>
<td>The name of the font to use for this control.</td>
</tr>
<tr class="odd">
<td><strong>FontSize</strong></td>
<td>-</td>
<td>Y</td>
<td>The point size of the font to use.</td>
</tr>
<tr class="even">
<td><strong>FontStyle</strong></td>
<td>-</td>
<td>Y</td>
<td>The name of the font style to use. Valid styles are: <strong>&quot;Shadow&quot;, &quot;Glow&quot;, &quot;Stroke&quot;</strong></td>
</tr>
<tr class="odd">
<td><strong>HighlightColor</strong></td>
<td>Y</td>
<td>Y</td>
<td>Color of the text highlight</td>
</tr>
<tr class="even">
<td><strong>KeepFocus</strong></td>
<td>Y</td>
<td>Y</td>
<td>Flag to indicate this control should keep focus after the user enters text.</td>
</tr>
<tr class="odd">
<td><strong>MaxLength</strong></td>
<td>Y</td>
<td>Y</td>
<td>Maximum number of characters which can be entered.</td>
</tr>
<tr class="even">
<td><strong>NumberInput</strong></td>
<td>Y</td>
<td>Y</td>
<td>Flag to indicate this entry box is only for numbers.</td>
</tr>
<tr class="odd">
<td><strong>Obscure</strong></td>
<td>Y</td>
<td>Y</td>
<td>Instead of showing what is entered, use a replacement character.</td>
</tr>
<tr class="even">
<td><strong>HighlightOnFocus</strong></td>
<td>?</td>
<td>?</td>
<td>Automatically highlight all the text in the edit box when the box gets focus. Useful for text that should be copy/paste.</td>
</tr>
</tbody>
</table>
</div> <!-- panel body --> 
</div> <!-- panel -->

<div class="panel panel-primary" id="Forge%20UI%5CControls%5CFlipAnim">
<div class="panel-heading">
<div class="panel-title">FlipAnim
</div>
</div>
<div class="panel-body">

<p>&lt;FlipAnim&gt;</p>
<p>Friday, February 21, 2014</p>
<p>3:02 PM</p>

<p>Flipbook animation. Moves by steps through a texture.</p>

<p><strong>FrameCount</strong> - Total number of frames in the animation.</p>
<p><strong> </strong></p>
<p><strong>Texture</strong> - Filename of the texture to flip through.</p>
<p><strong> </strong></p>
<p><strong>Columns</strong> - Number of columns of animation in the texture before wrapping</p>

<p>Civ5: StepSize, MaskTexture</p>

<p>For additional controls see: <em>Animation</em></p>

<p><strong>LUA Methods</strong></p>

<table>
<thead>
<tr class="header">
<th><strong>Function</strong></th>
<th><strong>Returns</strong></th>
<th><strong>Arguments</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>SetFrame</strong></td>
<td>bool</td>
<td>Int</td>
</tr>
</tbody>
</table>

<p>For Common LUA animation methods, see: <em>LUA Animation Methods</em></p>

</div> <!-- panel body --> 
</div> <!-- panel -->

<div class="panel panel-primary" id="Forge%20UI%5CControls%5CGrid">
<div class="panel-heading">
<div class="panel-title">Grid
</div>
</div>
<div class="panel-body">

<p><strong>&lt;Grid&gt;</strong></p>
<p>Friday, February 21, 2014</p>
<p>2:27 PM</p>

<p>Textured, 9-slicable, dynamically sized control.</p>

<table>
<thead>
<tr class="header">
<th><strong>Attribute</strong></th>
<th><strong>Details</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>NoStateChange</strong></td>
<td>Flag that indicates that the texture should not be offset when used as a button</td>
</tr>
<tr class="even">
<td><strong>StateOffsetIncrement</strong></td>
<td>How far to offset the texture for state changes when used as a button</td>
</tr>
<tr class="odd">
<td><strong>Texture</strong></td>
<td>Filename of the texture to build the grid from</td>
</tr>
<tr class="even">
<td><strong>SliceStart</strong></td>
<td>(optional) The x,y coordinates where a particular texture starts in an image sheet. If the entire image IS the texture, then this can be omitted. Default 0,0.</td>
</tr>
<tr class="odd">
<td><strong>SliceCorner</strong></td>
<td>An x,y offset from the start of the texture where to begin the 9-slicing.</td>
</tr>
<tr class="even">
<td><strong>SliceSize</strong></td>
<td>Width and height of the actual 9 slice. (aka: Size of the center rectangle in the grid.) Default: 1,1.</td>
</tr>
<tr class="odd">
<td><strong>SliceTextureSize</strong></td>
<td>The width and height of the image from the texture. If omitted, assumes cutting is symmetrical.</td>
</tr>
</tbody>
</table>

<p><img src="Forge UI\Controls\Grid/media/image1.png" alt="SliceStart SliceCorner SlicerSize SliceTextureSize" width="466" height="245" /></p>


</div> <!-- panel body --> 
</div> <!-- panel -->

<div class="panel panel-primary" id="Forge%20UI%5CControls%5CGridButton">
<div class="panel-heading">
<div class="panel-title">GridButton
</div>
</div>
<div class="panel-body">

<p>&lt;GridButton&gt;</p>
<p>Friday, February 21, 2014</p>
<p>2:33 PM</p>

<p>A Button control which uses a <strong>Grid</strong> to allow the size to be flexible, and may contain an optional text field. Grid specific data is specified by a sub-control called <strong>&lt;GridData&gt;</strong> which contains all of the normal control data for a GridControl. For state changes, we offset into the texture by the <strong>StateOffsetIncrement</strong> value in the GridData.</p>

<p><strong>Child Tags</strong></p>
<p><strong>&lt;GridData&gt;</strong> - Sub control with the details of the grid to use. See <em>&lt;Grid&gt;</em> for details.</p>

<p><strong>XML</strong></p>
<table>
<thead>
<tr class="header">
<th><strong>Attribute</strong></th>
<th><strong>Details</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>Color</strong></td>
<td>What color to set the grid vertices to use.</td>
</tr>
<tr class="even">
<td><strong>ColorSet</strong></td>
<td>Color set to utilize.</td>
</tr>
<tr class="odd">
<td><strong>Font</strong></td>
<td>The name of the font to use for this control.</td>
</tr>
<tr class="even">
<td><strong>FontSize</strong></td>
<td>The point size of the font to use</td>
</tr>
<tr class="odd">
<td><strong>FontStyle</strong></td>
<td>The name of the font style to use. Valid styles are: <strong>&quot;Shadow&quot;, &quot;Glow&quot;, &quot;Stroke&quot;</strong></td>
</tr>
<tr class="even">
<td><strong>SelectedTextColor</strong></td>
<td>The color of text to use when in a &quot;selected&quot; state.</td>
</tr>
<tr class="odd">
<td><strong>TextAnchor</strong></td>
<td>Anchoring within the grid. (Default is centered, e.g., “C,C”).</td>
</tr>
<tr class="even">
<td><strong>TextColor</strong></td>
<td>Color to set the text, use to override the general &quot;Color&quot; tag that effects the button's vertices as well as the text color.</td>
</tr>
<tr class="odd">
<td><strong>TextOffset</strong></td>
<td>Offset (in pixels) for the text.</td>
</tr>
<tr class="even">
<td><strong>String</strong></td>
<td>Contents of a text label. (Default is blank.)</td>
</tr>
<tr class="odd">
<td><strong>ToolTip</strong></td>
<td>Tool tip string</td>
</tr>
</tbody>
</table>


<p><strong>LUA Methods</strong></p>
<p>All the methods in &lt;Button&gt; as well as:</p>

<table>
<thead>
<tr class="header">
<th><strong>Function</strong></th>
<th><strong>Returns</strong></th>
<th><strong>Arguments</strong></th>
<th><strong>Description</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>DoAutoSize</strong></td>
<td>void</td>
<td>bool</td>
<td>Perform an auto size</td>
</tr>
<tr class="even">
<td><strong>GetText</strong></td>
<td>bool</td>
<td> </td>
<td>Obtain text in the child text control</td>
</tr>
<tr class="odd">
<td><strong>GetTextControl</strong></td>
<td>bool</td>
<td> </td>
<td>Obtain the child text control</td>
</tr>
<tr class="even">
<td><strong>LocalizeAndSetText</strong></td>
<td>bool</td>
<td> </td>
<td>Set the text of the text control after going through the localizer system.</td>
</tr>
<tr class="odd">
<td><strong>SetSizeToText</strong></td>
<td>void</td>
<td>width, height</td>
<td>Set the backing grid of the button to the size of the text field inside of it, with additional width and height padding.</td>
</tr>
<tr class="even">
<td><strong>SetSizeVal</strong></td>
<td>void</td>
<td>width, height</td>
<td>Override to set the size by value.</td>
</tr>
<tr class="odd">
<td><strong>SetText</strong></td>
<td>void</td>
<td> </td>
<td>Set the text of the text control</td>
</tr>
<tr class="even">
<td><strong>SetTextureOffset</strong></td>
<td>void</td>
<td> </td>
<td>Clear the registered callback function.</td>
</tr>
<tr class="odd">
<td><strong>SetTextureOffsetVal</strong></td>
<td>void</td>
<td> </td>
<td>Set an offset of the grid.</td>
</tr>
</tbody>
</table>

</div> <!-- panel body --> 
</div> <!-- panel -->

<div class="panel panel-primary" id="Forge%20UI%5CControls%5CImage">
<div class="panel-heading">
<div class="panel-title">Image
</div>
</div>
<div class="panel-body">

<p><strong>&lt;Image&gt;</strong></p>
<p>Friday, February 21, 2014</p>
<p>2:35 PM</p>
<p>The &lt;Image&gt; control is used to display a texture.</p>

<p><strong>XML</strong></p>
<table>
<thead>
<tr class="header">
<th><strong>Attribute</strong></th>
<th><strong>Details</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>ColorSpace</strong></td>
<td>(default: &quot;<strong>RGB&quot;</strong>, &quot;Linear&quot;) Set this to &quot;linear&quot; if rendering a linear texture onto the quad (e.g., using it as a Render Target)</td>
</tr>
<tr class="even">
<td><strong>FlipX</strong></td>
<td>Horizontally flip the image</td>
</tr>
<tr class="odd">
<td><strong>FlipY</strong></td>
<td>Vertically flip the image</td>
</tr>
<tr class="even">
<td><strong>Icon</strong></td>
<td>Calls the icon manager to obtain the icon specified.</td>
</tr>
<tr class="odd">
<td><strong>IconSize</strong></td>
<td>Specifies the width and height of the icon.</td>
</tr>
<tr class="even">
<td><strong>MaskTexture</strong></td>
<td>The filename of a texture to use as an alpha mask.</td>
</tr>
<tr class="odd">
<td><strong>MaskTextureOffset</strong></td>
<td>The x,y offset (in pixels) into the mask texture.</td>
</tr>
<tr class="even">
<td><strong>NormalizedQuad</strong></td>
<td>Programmer flag. Indicates that there is not a 1:1 ratio of pixels:texels</td>
</tr>
<tr class="odd">
<td><strong>Sampler</strong></td>
<td>Set this to &quot;Linear&quot; if you're scaling a block compressed image. It will try.</td>
</tr>
<tr class="even">
<td><strong>Rotate</strong></td>
<td>Rotate the texture on the quad (degrees) Note: In the current implementation, stretching will occur as the quad itself is not rotate.</td>
</tr>
<tr class="odd">
<td><strong>Scale</strong></td>
<td>Uniformly scale up the texture by a multiplier. (e.g., “1.5” will scale it up 150%.)</td>
</tr>
<tr class="even">
<td><strong>Size</strong></td>
<td>(Inherited from <strong>Container</strong>) Specify a size for this control; the texture will take up a portion (or all of it). This attribute is only ignored if the stretch mode is set to auto.</td>
</tr>
<tr class="odd">
<td><strong>StretchMode</strong></td>
<td><p>How to stretch the texture; one of the following values:</p>
<p><strong>None, Uniform, Fill, Tile, TileX, TileY, UniformToFill, Auto</strong></p></td>
</tr>
<tr class="even">
<td><strong>Texture</strong></td>
<td>The filename of the texture to use.</td>
</tr>
<tr class="odd">
<td><strong>TextureOffset</strong></td>
<td>The x,y offset (in pixels) into the texture for where to start drawing.</td>
</tr>
<tr class="even">
<td><strong>TextureOffsetUV</strong></td>
<td>The offset into the texture in UV coordinates.</td>
</tr>
<tr class="odd">
<td><strong>TextureSizeUV</strong></td>
<td>The size in floating-point UV texture coordinates to make this.</td>
</tr>
</tbody>
</table>

<p><strong>Example:</strong></p>
<p>&lt;Image Anchor=&quot;L,C&quot; TextureOffset=&quot;0,0&quot; AnchorSide=&quot;O,O&quot; Texture=&quot;buttonsides.dds&quot; Size=&quot;8,16&quot; /&gt;</p>


<p>StretchModes work in the following manner:</p>
<p>None</p>
<ul>
<li>
<p>Displays the image at its normal size, clipping if necessary</p>
</li>
</ul>
<p>Uniform</p>
<ul>
<li>
<p>Fills a portion of the control size with the entire image while maintaining aspect ratio. Image is not clipped.</p>
</li>
</ul>
<p>Fill</p>
<ul>
<li>
<p>Stretches the texture image to fit within the size.</p>
</li>
</ul>
<p>UniformToFill</p>
<ul>
<li>
<p>Fills the entire control size with the image while maintaining aspect ratio. Image may be clipped.</p>
</li>
</ul>
<p>Tile</p>
<ul>
<li>
<p>Repeat the texture to fill a region.</p>
</li>
</ul>
<p>TileX</p>
<ul>
<li>
<p>Just tile in the horizontal direction, clipping in the vertical direction if necessary.</p>
</li>
</ul>
<p>TileY</p>
<ul>
<li>
<p>Just tile in the vertical direction, clipping in the horizontal if necessary.</p>
</li>
</ul>
<p>Auto</p>
<ul>
<li>
<p>Resize the image control to whatever the native size of the texture is… the control will expand or shrink as necessary.</p>
</li>
</ul>

</div> <!-- panel body --> 
</div> <!-- panel -->

<div class="panel panel-primary" id="Forge%20UI%5CControls%5CInclude">
<div class="panel-heading">
<div class="panel-title">Include
</div>
</div>
<div class="panel-body">

<p>&lt;Include&gt;</p>
<p>Tuesday, July 25, 2017</p>
<p>5:22 PM</p>

<p>Includes the contents of an xml file into the existing context. It's mostly used to include instances shared by multiple contexts.</p>

<p><strong>Example:</strong></p>
<p>&lt;!-- Include Popup Dialog Instances --&gt;</p>
<p>&lt;Include File=&quot;PopupDialog&quot; /&gt;</p>

<p>&lt;!-- Create Popup Dialog Instance --&gt;</p>
<p>&lt;MakeInstance Name=&quot;PopupDialog&quot;/&gt;</p>
</div> <!-- panel body --> 
</div> <!-- panel -->

<div class="panel panel-primary" id="Forge%20UI%5CControls%5CInstance">
<div class="panel-heading">
<div class="panel-title">Instance
</div>
</div>
<div class="panel-body">

<p>&lt;Instance&gt;</p>
<p>Tuesday, July 25, 2017</p>
<p>5:22 PM</p>

<p>Defines a collection of controls that can be created either using the <strong>&lt;MakeInstance&gt;</strong> tag or by calling <strong>ContextPtr:BuildInstanceForControl()</strong></p>

<p><strong>Example:</strong></p>
<p>&lt;Instance Name=&quot;MyInstance&quot;&gt;</p>

<p>&lt;Bar ID=&quot;TopControl&quot; Size=&quot;10,10&quot; Hidden=&quot;1&quot;/&gt;</p>

<p>&lt;/Instance&gt;</p>

<p>&lt;Stack ID=&quot;MyStack&quot;&gt;</p>
<p>&lt;MakeInstance Name=&quot;MyInstance&quot;/&gt;</p>
<p>&lt;/Stack&gt;</p>

<p>-- Create instance in Lua:</p>
<p>local myInstance:table = {};</p>
<p>ContextPtr:BuildInstanceForControl(&quot;MyInstance&quot;, myInstance, Controls.MyStack);</p>

</div> <!-- panel body --> 
</div> <!-- panel -->

<div class="panel panel-primary" id="Forge%20UI%5CControls%5CLabel">
<div class="panel-heading">
<div class="panel-title">Label
</div>
</div>
<div class="panel-body">

<p><strong>&lt;Label&gt;</strong></p>
<p>Friday, February 21, 2014</p>
<p>2:42 PM</p>

<p>The internal “TextControl” which is used to display text. Its <strong>size</strong> will automatically be calculated to the bounds of the text string, and should not be set manually.</p>

<table>
<thead>
<tr class="header">
<th><strong>Attribute</strong></th>
<th><strong>Details</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>Align</strong></td>
<td>How to align the lines of text: &quot;<strong>left</strong>&quot; &quot;<strong>center</strong>&quot; &quot;<strong>right</strong>&quot; - *Note: text will align based on the width of the longest text string (in the case of a paragraph) or based on the width of its parent control.</td>
</tr>
<tr class="even">
<td><strong>Color0</strong></td>
<td>Has same meaning as the base control’s “<strong>Color</strong>”. (Currently if you specify both in the same tag, Color0 will override Color)</td>
</tr>
<tr class="odd">
<td><strong>Color1</strong></td>
<td>DEPRECATED: See <em>EffectColor</em></td>
</tr>
<tr class="even">
<td><strong>Color2</strong></td>
<td>DEPRECATED: See GradientColor</td>
</tr>
<tr class="odd">
<td><strong>ColorSet</strong></td>
<td>The name of the color set to use.</td>
</tr>
<tr class="even">
<td><strong>EffectColor</strong></td>
<td>(optional) The secondary color used for FontStyles such as “<strong>Stroke</strong>”, “<strong>Glow</strong>”, and “<strong>Shadow</strong>”.</td>
</tr>
<tr class="odd">
<td><strong>Font</strong></td>
<td>The name of the font to use for this control.</td>
</tr>
<tr class="even">
<td><strong>FontSize</strong></td>
<td>The point size of the font to use.</td>
</tr>
<tr class="odd">
<td><strong>FontStyle</strong></td>
<td>The name of the font style to use. Valid styles are: &quot;<strong>Shadow</strong>&quot;, &quot;<strong>Glow</strong>&quot;, &quot;<strong>Stroke</strong>&quot;</td>
</tr>
<tr class="even">
<td><strong>GradientColor</strong></td>
<td>(optional) Gradient color to use at the bottom of the font.</td>
</tr>
<tr class="odd">
<td><strong>LeadingOffset</strong></td>
<td>Leading offset from line to line.</td>
</tr>
<tr class="even">
<td><strong>ReduceWidth</strong></td>
<td>Shrink the FontSize until the string fits within this width. *NOT IMPLEMENTED*</td>
</tr>
<tr class="odd">
<td><strong>Rotation</strong></td>
<td>Number of degrees to rotate the text. Rotation pivot is from the left-bottom of the first glyph.</td>
</tr>
<tr class="even">
<td><strong>SmallCaps</strong></td>
<td>Size of font to use for the capitalization</td>
</tr>
<tr class="odd">
<td><strong>SmallCapsLeading</strong></td>
<td>Amount of leading to add to the non-small caps letters.</td>
</tr>
<tr class="even">
<td><strong>SmallCapsType</strong></td>
<td>How to apply small caps, either: &quot;<strong>EveryWord</strong>&quot; (default) or &quot;<strong>FirstOnly</strong>&quot;</td>
</tr>
<tr class="odd">
<td><strong>String</strong></td>
<td>Control text.</td>
</tr>
<tr class="even">
<td><strong>TruncateWidth</strong></td>
<td>The width (in pixels) to cut the string off.</td>
</tr>
<tr class="odd">
<td><strong>WrapWidth</strong></td>
<td>The width (in pixels) to start wrapping to the next line.</td>
</tr>
</tbody>
</table>


<p><strong>Example: Gradient Text</strong></p>
<p><em>Game_ColorAtlas.xml:</em></p>
<p>&lt;ColorSet Name=&quot;ResCultureLabelCS&quot; Color0=&quot;190,89,189,255&quot; Color1=&quot;0,0,0,100&quot; Color2=&quot;255,214,255,255&quot; /&gt;</p>
<p>Where..</p>
<table>
<thead>
<tr class="header">
<th>Color0</th>
<th>Top gradient</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Color1</td>
<td>Color of shadow, stroke, or glow</td>
</tr>
<tr class="even">
<td>Color2</td>
<td>Bottom gradient</td>
</tr>
</tbody>
</table>

<p><em>SomeTechCivicToggle.xml</em></p>
<p>&lt;Label Offset=&quot;32,6&quot; Style=&quot;FontNormal14&quot; FontStyle=&quot;Glow&quot; ColorSet=&quot;ResCultureLabelCS&quot; /&gt;</p>

<p>Produces:</p>
<p><img src="Forge UI\Controls\Label/media/image1.png" alt="C:\E3AD9F25\673868D8-982B-4885-B090-A5DC822099F8_files\image001.png" width="83" height="33" /></p>


<p><strong>Example: Small Caps</strong></p>
<p>&lt;Label FontSize=&quot;20&quot; String=&quot;NATIVE SMALL CAPS SUPPORT&quot; Offset=&quot;10,10&quot; Color=&quot;green&quot; SmallCaps=&quot;28&quot; SmallCapsLeading=&quot;6&quot; SmallCapsType=&quot;EveryWord&quot; /&gt;</p>
<p><img src="Forge UI\Controls\Label/media/image2.png" alt="cid:image002.png@01D06594.25B3CD10" width="463" height="97" /></p>

<p><strong>Example: WrapWidth</strong></p>
<table>
<tbody>
<tr class="odd">
<td><p><img src="Forge UI\Controls\Label/media/image3.png" alt="Machine generated alternative text: I’m excited for the new super troopers movie. I’m excited for the new super troopers movie. I’m excited for the new super troopers movie. I’m excited for the new super troopers movie. I’m excited for the new super troopers movie. I’m excited for the new super troopers movie." width="341" height="369" /></p>
</td>
<td><p>&lt;Box Size=&quot;200,50&quot; Color=&quot;99,88,77&quot;&gt;</p>
<p>&lt;Label String=&quot;I'm excited for the new super troopers movie.&quot; Size=&quot;parent,100&quot; debug=&quot;1&quot; /&gt;</p>
<p>&lt;/Box&gt;</p>
<p>&lt;Box Size=&quot;200,50&quot; Color=&quot;99,88,77&quot; Offset=&quot;0,60&quot;&gt;</p>
<p>&lt;Label String=&quot;I'm excited for the new super troopers movie.&quot; Size=&quot;200,100&quot; debug=&quot;1&quot; /&gt;</p>
<p>&lt;/Box&gt;</p>
<p>&lt;Box Size=&quot;200,50&quot; Color=&quot;99,88,77&quot; Offset=&quot;0,120&quot;&gt;</p>
<p>&lt;Label String=&quot;I'm excited for the new super troopers movie.&quot; debug=&quot;1&quot; /&gt;</p>
<p>&lt;/Box&gt;</p>
<p>&lt;Box Size=&quot;200,50&quot; Color=&quot;99,88,77&quot; Offset=&quot;0,180&quot;&gt;</p>
<p>&lt;Label String=&quot;I'm excited for the new super troopers movie.&quot; WrapWidth=&quot;200&quot; debug=&quot;1&quot; /&gt;</p>
<p>&lt;/Box&gt;</p>
<p>&lt;Box Size=&quot;200,50&quot; Color=&quot;99,88,77&quot; Offset=&quot;0,240&quot;&gt;</p>
<p>&lt;Label String=&quot;I'm excited for the new super troopers movie.&quot; WrapWidth=&quot;parent&quot; debug=&quot;1&quot; /&gt;</p>
<p>&lt;/Box&gt;</p>
<p>&lt;Box Size=&quot;200,50&quot; Color=&quot;99,88,77&quot; Offset=&quot;0,300&quot;&gt;</p>
<p>&lt;Label String=&quot;I'm excited for the new super troopers movie.&quot; Size=&quot;parent,100&quot; WrapWidth=&quot;parent&quot; debug=&quot;1&quot; /&gt;</p>
<p>&lt;/Box&gt;</p></td>
</tr>
</tbody>
</table>

<p><strong>LUA Functions</strong></p>
<table>
<thead>
<tr class="header">
<th><strong>Function</strong></th>
<th><strong>Returns</strong></th>
<th><strong>Arguments</strong></th>
<th><strong>Description</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>SetColor</strong></td>
<td><strong>n/a</strong></td>
<td><p><strong>uint ABGR, (uint layer)</strong></p>
<p><strong>ABGR</strong>, is a single ABGR to represent the alpha, blue, green, and red values as a single HEX value. (0xAABBGGRR)</p>
<p><strong>layer</strong>, (optional) a value 0 to 2 representing which &quot;layer&quot; of color to change. 0 is the main color of the glyphs, 1 is the effect color (shadow, glow, etc…) and 2 is a layer that isn't used… yet.</p></td>
<td> </td>
</tr>
<tr class="even">
<td><strong>SetColorByName</strong></td>
<td><strong>n/a</strong></td>
<td><strong>name</strong>, The name of a color set in the color atlas</td>
<td>Sets the label to use all of the controls in the existing colorset. (Overrides the base implementation which only grabs the first color in the color set).</td>
</tr>
</tbody>
</table>
</div> <!-- panel body --> 
</div> <!-- panel -->

<div class="panel panel-primary" id="Forge%20UI%5CControls%5CLine">
<div class="panel-heading">
<div class="panel-title">Line
</div>
</div>
<div class="panel-body">

<p><strong>&lt;Line&gt;</strong></p>
<p>Friday, February 21, 2014</p>
<p>2:45 PM</p>

<p>Draw a line with a solid stroke</p>

<table>
<thead>
<tr class="header">
<th><strong>Attribute</strong></th>
<th><strong>Details</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>Color</strong></td>
<td>RGBA for the color and alpha of line.</td>
</tr>
<tr class="even">
<td><strong>End</strong></td>
<td>Ending point for the line.</td>
</tr>
<tr class="odd">
<td><strong>Start</strong></td>
<td>Starting point for the line.</td>
</tr>
<tr class="even">
<td><strong>Width</strong></td>
<td>Thickness of the line.</td>
</tr>
</tbody>
</table>

<p><strong>Examples:</strong></p>

<p>&lt;Line Start=&quot;100,100&quot; End=&quot;400,400&quot; Width=&quot;10&quot; Color=&quot;255,128,63,200&quot; /&gt;</p>
</div> <!-- panel body --> 
</div> <!-- panel -->

<div class="panel panel-primary" id="Forge%20UI%5CControls%5CLuaContext">
<div class="panel-heading">
<div class="panel-title">LuaContext
</div>
</div>
<div class="panel-body">

<p>&lt;LuaContext&gt;</p>
<p>Tuesday, March 04, 2014</p>
<p>4:48 PM</p>

<p>Control to load a new .XML file of controls that is backed by a .LUA scripting file.</p>
<p>When not the top level tag of the file (a root context), the following attributes are allowed:</p>

<p><strong>XML</strong></p>
<table>
<thead>
<tr class="header">
<th><strong>Attribute</strong></th>
<th><strong>Details</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>FileName</strong></td>
<td>Name of the xml file to load (without the .xml extension)</td>
</tr>
<tr class="even">
<td><strong>ID</strong></td>
<td>(optional) An identifier for the LUA context</td>
</tr>
</tbody>
</table>


<p><strong>LUA</strong></p>
<p>Note: Since a Context is a ControlBase (e.g., &lt;Container&gt;), all LUA functions on a ControlBase can be used here as well. Below are the Context specific functions:</p>
<table>
<thead>
<tr class="header">
<th><strong>Function</strong></th>
<th><strong>Returns</strong></th>
<th><strong>Arguments</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>BuildInstance</strong></td>
<td>nil</td>
<td>Creates an instance and attached is to the context as the parent.</td>
</tr>
<tr class="even">
<td><strong>BuildInstanceForControl( name, outTable, parent)</strong></td>
<td>nil</td>
<td><p>Creates an instance and attaches is to a control.</p>
<p><strong>name</strong> is the string name of a control</p>
<p><strong>outTable</strong> is an (empty) table which will reference the control in LUA</p>
<p><strong>parent</strong> is an existing control that will be the parent of the newly created instance</p></td>
</tr>
<tr class="odd">
<td><strong>BuildInstanceForControlAtIndex( )</strong></td>
<td>nil</td>
<td>Creates an instance and attaches is to a control at a specified index.</td>
</tr>
<tr class="even">
<td><strong>CallParentShowHideHandler( func )</strong></td>
<td>nil</td>
<td>DEPRECATED</td>
</tr>
<tr class="odd">
<td><strong>ClearRefreshHandler( )</strong></td>
<td>nil</td>
<td>Removes the refresh callback function.</td>
</tr>
<tr class="even">
<td><strong>ClearRequestRefresh( )</strong></td>
<td>nil</td>
<td>Manually reset the flag that tells the context to refresh next C++ Update(). Note: this is internally (automatically) called after a refresh occurs.</td>
</tr>
<tr class="odd">
<td><strong>ClearUpdate( )</strong></td>
<td>nil</td>
<td>Clears the update callback function.</td>
</tr>
<tr class="even">
<td><strong>IsHotLoad</strong></td>
<td>bool</td>
<td>Is the context in a hotload situation.</td>
</tr>
<tr class="odd">
<td><strong>LoadNewContext( nameAndPath )</strong></td>
<td>nil</td>
<td>Dynamically load a new context and make it a child of this one.</td>
</tr>
<tr class="even">
<td><strong>Reload( )</strong></td>
<td>nil</td>
<td>Reload the context.</td>
</tr>
<tr class="odd">
<td><strong>RequestRefresh( )</strong></td>
<td>nil</td>
<td>Requests a refresh callback to occur on the next C++ Update().</td>
</tr>
<tr class="even">
<td><strong>SetAppLostFocusHandler( func )</strong></td>
<td>nil</td>
<td>Called when a player's OS focus of the application is lost. (Not supported on iOS).</td>
</tr>
<tr class="odd">
<td><strong>SetAppRegainedFocusHandler( func )</strong></td>
<td>nil</td>
<td>Called when a player's OS focus of the application is regained. (Not support on iOS).</td>
</tr>
<tr class="even">
<td><strong>SetHideHandler( func )</strong></td>
<td>nil</td>
<td>Called when the context is made hidden.</td>
</tr>
<tr class="odd">
<td><strong>SetInitHandler( func )</strong></td>
<td>nil</td>
<td>Set a callback function when the first context has just finished initializing. The callback function will also be called when a hotload occurs.</td>
</tr>
<tr class="even">
<td><strong>SetInputHandler( func, isUsingStruct )</strong></td>
<td>nil</td>
<td><p>func, A callback function it's method signature depends on whether the 2nd argument is true/false.</p>
<p>bool, If false the function is expected to use the old, DEPRECATED, style of receiving input as 3 values. If true, the function will receive an input structure object. See <em>LUA Input</em> for more information.</p></td>
</tr>
<tr class="odd">
<td><strong>SetPostInit( func )</strong></td>
<td>nil</td>
<td>Sets a function to call after the C++ Initialize() has completed.</td>
</tr>
<tr class="even">
<td><strong>SetRefreshHandler( func )</strong></td>
<td>nil</td>
<td>Sets a callback function which will occur explicitly, once on C++ Update(). Used when a lot of values are changing but rather than realize real-time, a delay is fine; usually to prevent recomputing sub-pieces of a complex screen.</td>
</tr>
<tr class="odd">
<td><strong>SetShowHandler( func )</strong></td>
<td>nil</td>
<td>Called when the context is made visible.</td>
</tr>
<tr class="even">
<td><strong>SetShowHideHandler( func )</strong></td>
<td>nil</td>
<td><p>DEPRECATED: single function called when context is shown/hidden.</p>
<p><strong>WARNING</strong>: This callback will not work if SetShowHandler or SetHidHandler are used.</p></td>
</tr>
<tr class="odd">
<td><strong>SetShutdown( func )</strong></td>
<td>nil</td>
<td>function, Will callback before the context shuts down. (e.g., will occur during a hotload)</td>
</tr>
<tr class="even">
<td><strong>SetUpdate( func )</strong></td>
<td>nil</td>
<td><p><strong>WARNING</strong>: Avoid using this function at all costs (check out refresh handler above), as this will call per C++ Update() which really does a number on fragmenting memory, since LUA loves to make many small allocations.</p>
<p>A function to be updated each frame; where the function signature is: <strong>function( fdTime )</strong> Each frame <strong>fdTime</strong> will contain a number representing how long since the last update.</p></td>
</tr>
<tr class="odd">
<td><strong>UnifyClickAndTap( isUnified )</strong></td>
<td>nil</td>
<td>Set mouse clicking and finger tapping to be considered one and the same.</td>
</tr>
</tbody>
</table>

<p>Example:</p>
<p><strong>ContextPtr:ClearRequestRefresh( );</strong></p>


</div> <!-- panel body --> 
</div> <!-- panel -->

<div class="panel panel-primary" id="Forge%20UI%5CControls%5CMakeInstance">
<div class="panel-heading">
<div class="panel-title">MakeInstance
</div>
</div>
<div class="panel-body">

<p><strong>&lt;MakeInstance&gt;</strong></p>
<p>Friday, February 21, 2014</p>
<p>2:35 PM</p>

<p>Immediately creates an instance of an object; similar to calling <strong>ContextPtr:BuildInstanceForControl</strong>.</p>
<p>You can define how to access the instance within the <strong>Controls</strong> table by setting the <strong>ID</strong> attribute. If you don't set the attribute, the <strong>Name</strong> of the instance will be used instead.</p>

<p><strong>Examples:</strong></p>
<p>&lt;Instance Name=&quot;MyBarInstance&quot;&gt;</p>

<p>&lt;Bar ID=&quot;BarControl&quot; Size=&quot;10,10&quot; Hidden=&quot;1&quot;/&gt;</p>

<p>&lt;/Instance&gt;</p>

<p>&lt;Instance Name=&quot;MyBoxInstance&quot;&gt;</p>

<p>&lt;Box ID=&quot;BoxControl&quot; Size=&quot;10,10&quot; Hidden=&quot;1&quot;/&gt;</p>

<p>&lt;/Instance&gt;</p>

<p>&lt;Stack&gt;</p>
<p>&lt;MakeInstance Name=&quot;MyBarInstance&quot;/&gt;</p>
<p>&lt;MakeInstance Name=&quot;MyBoxInstance&quot; ID=&quot;MyBoxWithID&quot;/&gt;</p>
<p>&lt;/Stack&gt;</p>

<p>-- In Lua:</p>
<p>Controls.MyBarInstance.BarControl:SetHide(false);</p>
<p>Controls.MyBoxWithID.BoxControl:SetHide(false);</p>
</div> <!-- panel body --> 
</div> <!-- panel -->

<div class="panel panel-primary" id="Forge%20UI%5CControls%5CMeter">
<div class="panel-heading">
<div class="panel-title">Meter
</div>
</div>
<div class="panel-body">

<p><strong>&lt;Meter&gt;</strong></p>
<p>Friday, February 21, 2014</p>
<p>4:17 PM</p>

<p>Rotational progress meter.</p>


<p><strong>XML</strong></p>
<table>
<thead>
<tr class="header">
<th><strong>Attribute</strong></th>
<th><strong>Type</strong></th>
<th><strong>Details</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Color</td>
<td>String</td>
<td>The red, green, blue and (optional) alpha values to apply to the meter texture. (Default is white with full alpha e.g., &quot;255,255,255,255);</td>
</tr>
<tr class="even">
<td>CounterClockwise</td>
<td>Bool</td>
<td>If true will have the meter run counter-clockwise .</td>
</tr>
<tr class="odd">
<td>Follow</td>
<td>Bool</td>
<td>If true the texture will rotate and &quot;follow&quot; whatever percentage the mask has currently revealed. Essentially revealing more of itself as the mask moves.</td>
</tr>
<tr class="even">
<td>HasShadow</td>
<td>Bool</td>
<td>If true a second version of the texture will be used that sits under the main texture.</td>
</tr>
<tr class="odd">
<td>Percent</td>
<td>Number</td>
<td>Start value of the meter, by default this is 0.</td>
</tr>
<tr class="even">
<td>ShadowAlpha</td>
<td>Number</td>
<td>Alpha value to apply to the &quot;shadow&quot; version</td>
</tr>
<tr class="odd">
<td>Speed</td>
<td>Number</td>
<td>How fast the meter should animate. If 0 (the default) no animation is used, it instantly</td>
</tr>
<tr class="even">
<td>Texture</td>
<td>String</td>
<td>The texture to use for the meter (and optional &quot;shadow&quot;) of the meter.</td>
</tr>
</tbody>
</table>

<p><strong>LUA Functions</strong></p>
<table>
<thead>
<tr class="header">
<th><strong>Function</strong></th>
<th><strong>Returns</strong></th>
<th><strong>Arguments</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>SetAnimationSpeed</strong></td>
<td><strong>n/a</strong></td>
<td><strong>float</strong>, 0 to animation speed where 0 is none</td>
</tr>
<tr class="even">
<td><strong>SetCounterClockwise</strong></td>
<td><strong>n/a</strong></td>
<td><strong>bool</strong> if true, meter runs counterclockwise; if false runs the meter clockwise</td>
</tr>
<tr class="odd">
<td><strong>SetFollow</strong></td>
<td><strong>n/a</strong></td>
<td><strong>Bool</strong> if true, the texture will follow the rotation of the revealed mask. If false, the texture is stationary as the mask rotates around, revealing more of it.</td>
</tr>
<tr class="even">
<td><strong>SetPercent</strong></td>
<td><strong>n/a</strong></td>
<td><strong>float</strong>, 0.0 - 1.0 percent of the texture that is displayed (filled)</td>
</tr>
<tr class="odd">
<td><strong>SetPercents</strong></td>
<td><strong>n/a</strong></td>
<td><strong>float</strong> 0.0-1.0<strong>, float</strong> 0.0-1.0 Sets both the main percent and &quot;shadow&quot; percent</td>
</tr>
<tr class="even">
<td><strong>SetShadowColor</strong></td>
<td><strong>n/a</strong></td>
<td><strong>uint</strong>, ABGR value that sets the color of the 'shadow'</td>
</tr>
<tr class="odd">
<td><strong>SetShadowPercent</strong></td>
<td><strong>n/a</strong></td>
<td><strong>float</strong>, 0.0-1.0 percent of texture used as a 'shadow'</td>
</tr>
</tbody>
</table>

<p><strong>Examples</strong></p>


<p><img src="Forge UI\Controls\Meter/media/image1.png" alt="Machine generated alternative text: " width="255" height="255" /></p>
<p>&lt;Meter Size=&quot;256,256&quot; Texture=&quot;TestImage.dds&quot; Percent=&quot;0.65&quot; /&gt;</p>


<p><img src="Forge UI\Controls\Meter/media/image2.png" alt="Machine generated alternative text: ." width="255" height="255" /></p>
<p>&lt;Meter Size=&quot;256,256&quot; Texture=&quot;TestImage.dds&quot; Percent=&quot;0.65&quot; <strong>CounterClockwise=&quot;1&quot;</strong> /&gt;</p>


<p><img src="Forge UI\Controls\Meter/media/image3.png" alt="Machine generated alternative text: " width="243" height="255" /></p>
<p>&lt;Meter Size=&quot;256,256&quot; Texture=&quot;TestImage.dds&quot; Percent=&quot;0.62&quot; <strong>Follow=&quot;1&quot;</strong> /&gt;</p>


<p><img src="Forge UI\Controls\Meter/media/image4.png" alt="Machine generated alternative text: " width="246" height="255" /></p>
<p>&lt;Meter Size=&quot;256,256&quot; Texture=&quot;TestImage.dds&quot; Percent=&quot;0.62&quot; <strong>CounterClockwise=&quot;1&quot;</strong> <strong>Follow=&quot;1&quot;</strong> /&gt;</p>


<p><img src="Forge UI\Controls\Meter/media/image5.png" alt="Machine generated alternative text: " width="255" height="255" /></p>
<p>&lt;Meter Size=&quot;256,256&quot; Texture=&quot;TestImage.dds&quot; Percent=&quot;0.1&quot; <strong>HasShadow=&quot;1&quot;</strong> /&gt;</p>
</div> <!-- panel body --> 
</div> <!-- panel -->

<div class="panel panel-primary" id="Forge%20UI%5CControls%5CMovie">
<div class="panel-heading">
<div class="panel-title">Movie
</div>
</div>
<div class="panel-body">

<p><strong>&lt;Movie&gt;</strong></p>
<p>Friday, February 21, 2014</p>
<p>2:35 PM</p>
<p>The &lt;Movie&gt; control (formally part of Image) is used to display a movie texture.</p>

<p><strong>XML</strong></p>
<table>
<thead>
<tr class="header">
<th><strong>Attribute</strong></th>
<th><strong>Details</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>FlipX</strong></td>
<td>Horizontally flip the image</td>
</tr>
<tr class="even">
<td><strong>FlipY</strong></td>
<td>Vertically flip the image</td>
</tr>
<tr class="odd">
<td><strong>LoopMovie</strong></td>
<td>If a Movie is specified, repeat the playing movie after it is done playing.</td>
</tr>
<tr class="even">
<td><strong>LoopMoviemask</strong></td>
<td>If a MovieMask is specified, repeat playing the movie after it is done playing.</td>
</tr>
<tr class="odd">
<td><strong>MaskTexture</strong></td>
<td>The filename of a texture to use as an alpha mask.</td>
</tr>
<tr class="even">
<td><strong>MaskTextureOffset</strong></td>
<td>The x,y offset (in pixels) into the mask texture.</td>
</tr>
<tr class="odd">
<td><strong>Movie</strong></td>
<td>A BINK (or other supported movie) to display in the image area.</td>
</tr>
<tr class="even">
<td><strong>MovieMask</strong></td>
<td>A BINK (or other supported movie) to mask the displayed image. (A moviemask can be used to mask a movie!)</td>
</tr>
<tr class="odd">
<td><strong>NormalizedQuad</strong></td>
<td>Programmer flag. Indicates that there is not a 1:1 ratio of pixels:texels</td>
</tr>
<tr class="even">
<td><strong>PointSample</strong></td>
<td>All images default to a point sampler, but if <strong>False</strong> then a linear sampling will be used instead.</td>
</tr>
<tr class="odd">
<td><strong>Rotate</strong></td>
<td>Rotate the texture on the quad (degrees) Note: In the current implementation, stretching will occur as the quad itself is not rotate.</td>
</tr>
<tr class="even">
<td><strong>Scale</strong></td>
<td>Uniformly scale up the texture by a multiplier. (e.g., “1.5” will scale it up 150%.)</td>
</tr>
<tr class="odd">
<td><strong>StretchMode</strong></td>
<td><p>How to stretch the texture; one of the following values:</p>
<p><strong>None</strong>, <strong>Uniform</strong>, <strong>Fill</strong>, <strong>Tile</strong>, or <strong>UniformToFill</strong></p></td>
</tr>
<tr class="even">
<td><strong>Texture</strong></td>
<td>The filename of the texture to use.</td>
</tr>
<tr class="odd">
<td><strong>TextureOffset</strong></td>
<td>The x,y offset (in pixels) into the texture for where to start drawing.</td>
</tr>
<tr class="even">
<td><strong>TextureOffsetUV</strong></td>
<td>The offset into the texture in UV coordinates.</td>
</tr>
<tr class="odd">
<td><strong>TextureSizeUV</strong></td>
<td>The size in floating-point UV texture coordinates to make this.</td>
</tr>
</tbody>
</table>

<p><strong>Example:</strong></p>
<p>&lt;Movie Movie=&quot;Test.bik&quot; Size=&quot;200,200&quot; /&gt;</p>


<p>MovieControl</p>
</div> <!-- panel body --> 
</div> <!-- panel -->

<div class="panel panel-primary" id="Forge%20UI%5CControls%5CPullDown">
<div class="panel-heading">
<div class="panel-title">PullDown
</div>
</div>
<div class="panel-body">

<p>&lt;PullDown&gt;</p>
<p>Friday, February 21, 2014</p>
<p>5:06 PM</p>

<p>Control for selecting one from a list of possible items (aka: combo box)</p>

<p><strong>XML</strong></p>
<table>
<thead>
<tr class="header">
<th><strong>Attribute</strong></th>
<th><strong>Details</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>AutoFlip</strong></td>
<td>Automatically flips the grid of the pulldown to be above the button, if it is rendered off the bottom of the window/screen area.</td>
</tr>
<tr class="even">
<td><strong>AutoSizePopUp</strong></td>
<td>Flag indicating that the grid should be automatically sized to however many buttons are inside the pulldown.</td>
</tr>
<tr class="odd">
<td><strong>SpaceForScroll</strong></td>
<td>Flag indicating that the grid should reserve some internal space for the scroll bar.</td>
</tr>
<tr class="even">
<td><strong>ScrollThreshold</strong></td>
<td>How large to allow the grid to grow before adding a scroll bar to the list.</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr class="header">
<th><strong>Child Tag</strong></th>
<th><strong>Details</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>&lt;ButtonData&gt;</strong></td>
<td>Sub-Control defining the button which opens the pull-down. Some type of <strong>&lt;Button&gt;</strong> should exist immediately within it.</td>
</tr>
<tr class="even">
<td><strong>&lt;GridData&gt;</strong></td>
<td>(Optional) Defines the formatting grid used behind the controls when the pull-down is open.</td>
</tr>
<tr class="odd">
<td><strong>&lt;ScrollPanelData&gt;</strong></td>
<td>(Optional) A scroll panel which contains the sub-buttons when the pull-down is open.</td>
</tr>
<tr class="even">
<td><strong>&lt;StackData&gt;</strong></td>
<td>The stack which contains the sub-buttons when the pull-down is open (mostly useful for changing the stack padding).</td>
</tr>
<tr class="odd">
<td><strong>&lt;InstanceData&gt;</strong></td>
<td>Template for what the sub-buttons will look like when the pull-down is in an open state.</td>
</tr>
</tbody>
</table>


<p><strong>LUA Methods</strong></p>
<table>
<thead>
<tr class="header">
<th><strong>Function</strong></th>
<th><strong>Returns</strong></th>
<th><strong>Arguments</strong></th>
<th><strong>Description</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>BuildEntry</strong></td>
<td> </td>
<td> </td>
<td>Add an entry.</td>
</tr>
<tr class="even">
<td><strong>CalcuateInternals</strong></td>
<td>void</td>
<td> </td>
<td>Calculates the size and contents of the grid, scroll panel, and stack.</td>
</tr>
<tr class="odd">
<td><strong>ClearEntries</strong></td>
<td> </td>
<td> </td>
<td>Remove all entries</td>
</tr>
<tr class="even">
<td><strong>ForceClose</strong></td>
<td>void</td>
<td> </td>
<td>Hides the grid and it's pieces</td>
</tr>
<tr class="odd">
<td><strong>GetButton</strong></td>
<td>Button</td>
<td> </td>
<td>Obtain component piece</td>
</tr>
<tr class="even">
<td><strong>GetGrid</strong></td>
<td>Grid</td>
<td> </td>
<td>Obtain component piece</td>
</tr>
<tr class="odd">
<td><strong>GetScrollPanel</strong></td>
<td>ScrollPanel</td>
<td> </td>
<td>Obtain component piece</td>
</tr>
<tr class="even">
<td><strong>GetStack</strong></td>
<td>Stack</td>
<td> </td>
<td>Obtain component piece</td>
</tr>
<tr class="odd">
<td><strong>IsOffBottom</strong></td>
<td>bool</td>
<td> </td>
<td>Is the pulldown showing above the open button because of limited room?</td>
</tr>
<tr class="even">
<td><strong>IsOpen</strong></td>
<td>bool</td>
<td> </td>
<td>Are the child elements showing.</td>
</tr>
<tr class="odd">
<td><strong>RegisterSelectionCallback</strong></td>
<td> </td>
<td>function</td>
<td>Callback to make after a selection is made.</td>
</tr>
<tr class="even">
<td><strong>SetDisabled</strong></td>
<td>void</td>
<td>bool</td>
<td>Enable or disables the control</td>
</tr>
</tbody>
</table>


<p><strong>Example</strong></p>
<p>&lt;PullDown ID=&quot;thePullDown&quot; ConsumeMouse=&quot;0&quot; Offset=&quot;0,0&quot; Anchor=&quot;L,T&quot; Size=&quot;200,50&quot; AutoSizePopUp=&quot;0&quot; SpaceForScroll=&quot;0&quot; ScrollThreshold=&quot;200&quot;&gt;</p>

<p>&lt;Label Anchor=&quot;C,C&quot; String=&quot;Click me to open!&quot; ID=&quot;theLabel&quot; /&gt;</p>
<p>&lt;ButtonData ID=&quot;theButtonData&quot;&gt;</p>
<p>&lt;GridButton ID=&quot;theOpenCloseButton&quot; Anchor=&quot;L,T&quot; /&gt;</p>
<p>&lt;/ButtonData&gt;</p>

<p>&lt;StackData ID=&quot;theStackData&quot; StackGrowth=&quot;Bottom&quot; Padding=&quot;0&quot; Size=&quot;200,500&quot; Anchor=&quot;L,T&quot; /&gt;</p>

<p>&lt;GridData Anchor=&quot;L,T&quot; Offset=&quot;0,100&quot; /&gt;</p>

<p>&lt;InstanceData Name=&quot;PullDownEntry&quot;&gt;</p>
<p>&lt;GridButton ID=&quot;Button&quot; Size=&quot;200,100&quot; Anchor=&quot;L,T&quot; Style=&quot;BaseButton&quot;/&gt;</p>
<p>&lt;/InstanceData&gt;</p>
<p>&lt;/PullDown&gt;</p>

</div> <!-- panel body --> 
</div> <!-- panel -->

<div class="panel panel-primary" id="Forge%20UI%5CControls%5CRadioButton">
<div class="panel-heading">
<div class="panel-title">RadioButton
</div>
</div>
<div class="panel-body">

<p>&lt;RadioButton&gt;</p>
<p>Friday, February 21, 2014</p>
<p>5:01 PM</p>
<p>A RadioButton control is very similar to the <strong>CheckBox</strong> and shares a lot of the same properties. A RadioButton is used when the selected state is mutually exclusive with other RadioButtons that share the same group. This group is specified using the <strong>RadioGroup</strong> parameter. The name set in the RadioGroup must be the same between all radio buttons in this group.</p>

<table>
<thead>
<tr class="header">
<th><strong>Attribute</strong></th>
<th><strong>5</strong></th>
<th><strong>F</strong></th>
<th><strong>Details</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>RadioGroup</strong></td>
<td> </td>
<td> </td>
<td>Name of the mutually exclusive group of radio buttons</td>
</tr>
<tr class="even">
<td><strong>BoxOnLeft</strong></td>
<td>N</td>
<td>Y</td>
<td>Replaces “<strong>TextAnchor</strong>”, if true places the box on the left of the text button, instead of to the right.</td>
</tr>
<tr class="odd">
<td><strong>ButtonSize</strong></td>
<td> </td>
<td>Y</td>
<td>Size of the check button itself.</td>
</tr>
<tr class="even">
<td><strong>ButtonTexture</strong></td>
<td> </td>
<td>Y</td>
<td>Texture to use for the button</td>
</tr>
<tr class="odd">
<td><strong>CheckOffset</strong></td>
<td> </td>
<td>Y</td>
<td>Coordinate for positioning the check over the button.</td>
</tr>
<tr class="even">
<td><strong>CheckSize</strong></td>
<td> </td>
<td>Y</td>
<td>Size of the check texture.</td>
</tr>
<tr class="odd">
<td><strong>CheckTexture</strong></td>
<td> </td>
<td>Y</td>
<td>Texture to use as the check mark.</td>
</tr>
<tr class="even">
<td><strong>CheckTextureOffset</strong></td>
<td> </td>
<td>Y</td>
<td>Offset into the check texture.</td>
</tr>
<tr class="odd">
<td><strong>IsChecked</strong></td>
<td> </td>
<td>Y</td>
<td>Flag indicating the box should start checked</td>
</tr>
<tr class="even">
<td><strong>String</strong></td>
<td>Y</td>
<td>Y</td>
<td>Set the label</td>
</tr>
<tr class="odd">
<td><strong>TextAnchor</strong></td>
<td>Y</td>
<td> </td>
<td>Anchor flag for the TextButton</td>
</tr>
<tr class="even">
<td><strong>TextAnchorSide</strong></td>
<td> </td>
<td>D</td>
<td>DEPRECATED Anchor side flag for the TextButton</td>
</tr>
<tr class="odd">
<td><strong>TextButtonData</strong></td>
<td>Y</td>
<td>Y</td>
<td>All of the tags used for the TextButton control are used here to describe the text button portion of the check box</td>
</tr>
<tr class="even">
<td><strong>TextOffset</strong></td>
<td> </td>
<td>Y</td>
<td>Offset of the TextButton portion from the check button</td>
</tr>
</tbody>
</table>

<p><strong>XML Example:</strong></p>

<p>&lt;Stack ID=&quot;ListFilters&quot; StackGrowth=&quot;Right&quot; AnchorSide=&quot;I,O&quot; Anchor =&quot;C,T&quot; Offset=&quot;0,0&quot; StackPadding=&quot;10&quot;&gt;</p>
<p>&lt;CheckBox ID=&quot;MilitaryFilterCheck&quot; RadioGroup=&quot;FilterGroup&quot; ButtonTexture=&quot;CivicsGrid_Military.dds&quot; CheckTexture=&quot;MainMenuCheckMark.dds&quot; IsChecked=&quot;true&quot; BoxOnLeft=&quot;true&quot;/&gt;</p>
<p>&lt;CheckBox ID=&quot;EconomicFilterCheck&quot; RadioGroup=&quot;FilterGroup&quot; ButtonTexture=&quot;CivicsGrid_Economic.dds&quot; CheckTexture=&quot;MainMenuCheckMark.dds&quot; IsChecked=&quot;true&quot; BoxOnLeft=&quot;true&quot; /&gt;</p>
<p>&lt;CheckBox ID=&quot;DiplomaticFilterCheck&quot; RadioGroup=&quot;FilterGroup&quot; ButtonTexture=&quot;CivicsGrid_Diplomatic.dds&quot; CheckTexture=&quot;MainMenuCheckMark.dds&quot; IsChecked=&quot;true&quot; BoxOnLeft=&quot;true&quot; /&gt;</p>
<p>&lt;/Stack&gt;</p>
</div> <!-- panel body --> 
</div> <!-- panel -->

<div class="panel panel-primary" id="Forge%20UI%5CControls%5CScrollAnim">
<div class="panel-heading">
<div class="panel-title">ScrollAnim
</div>
</div>
<div class="panel-body">

<p>&lt;ScrollAnim&gt;</p>
<p>Friday, February 21, 2014</p>
<p>3:02 PM</p>


<p>Animation which smoothly slides a texture offset</p>

<p><strong>Texture</strong> - Filename of the animated texture</p>
<p><strong> </strong></p>
<p><strong>MaskTexture</strong> - Filename of a texture to use as a mask</p>

<p>For additional controls see: <em>Animation</em></p>

<p><strong>LUA Methods</strong></p>

<table>
<thead>
<tr class="header">
<th><strong>Function</strong></th>
<th><strong>Returns</strong></th>
<th><strong>Arguments</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>SetTexture</strong></td>
<td>bool</td>
<td>string</td>
</tr>
<tr class="even">
<td><strong>SetMask</strong></td>
<td>bool</td>
<td>string</td>
</tr>
<tr class="odd">
<td><strong>SetTextureAndMask</strong></td>
<td>bool</td>
<td>string, string</td>
</tr>
</tbody>
</table>

<p>For Common LUA animation methods, see: <em>LUA Animation Methods</em></p>
</div> <!-- panel body --> 
</div> <!-- panel -->

<div class="panel panel-primary" id="Forge%20UI%5CControls%5CScrollPanel">
<div class="panel-heading">
<div class="panel-title">ScrollPanel
</div>
</div>
<div class="panel-body">

<p>&lt;ScrollPanel&gt;</p>
<p>Friday, February 21, 2014</p>
<p>5:04 PM</p>

<p>The scroll panel has a large panel with a smaller viewport into that space.</p>


<p><strong>AutoScrollBar</strong> - Flag to indicate that we should automatically hide the scroll bar when the internal size is equal to the viewport size and scrolling is not necessary.</p>
<p><strong> </strong></p>
<p><strong>HideScrollBar</strong> - Flag to never show the scroll bar.</p>
<p><strong> </strong></p>
<p><strong>Vertical</strong> - Flag to indicate that we scroll up/down rather than left/right</p>

<p><strong>*NOTE* for some reason the default is horizontal, this needs to be set to true in order for a vertical scroll panel to properly clip</strong></p>

<p><strong> </strong></p>
<p><strong>FullClip</strong> - By default we only clip the visuals in the direction which we scroll, this flag indicates that we should clip in both dimensions.</p>
<p><strong> </strong></p>

<p><strong>Sub-Controls:</strong></p>
<p><strong>&lt;UpButton&gt;</strong> - Sub-control which defines the button to scroll up</p>
<p><strong> </strong></p>
<p><strong>&lt;DownButton&gt;</strong> - Sub-control which defines the button to scroll down</p>
<p><strong> </strong></p>
<p><strong>&lt;ScrollBar&gt;</strong> - Sub-control which defines the slider used to move the panel</p>


<p><strong>LUA</strong></p>

<table>
<thead>
<tr class="header">
<th><strong>Function</strong></th>
<th><strong>Returns</strong></th>
<th><strong>Arguments</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>CalculateSize</strong></td>
<td><strong>void</strong></td>
<td> </td>
</tr>
<tr class="even">
<td><strong>CalculateInternalSize</strong></td>
<td><strong>void</strong></td>
<td><strong>DEPRECATED</strong></td>
</tr>
<tr class="odd">
<td><strong>GetScrollValue</strong></td>
<td>float</td>
<td>..</td>
</tr>
<tr class="even">
<td><strong>SetScrollValue</strong></td>
<td>void</td>
<td>Float (0.0-1.0)</td>
</tr>
<tr class="odd">
<td><strong>GetUpButton</strong></td>
<td> </td>
<td> </td>
</tr>
<tr class="even">
<td><strong>GetDownButton</strong></td>
<td> </td>
<td> </td>
</tr>
<tr class="odd">
<td><strong>GetRatio</strong></td>
<td> </td>
<td> </td>
</tr>
<tr class="even">
<td><strong>RegisterScrollCallback</strong></td>
<td> </td>
<td> </td>
</tr>
<tr class="odd">
<td><strong>RegisterUpEndCallback</strong></td>
<td> </td>
<td> </td>
</tr>
<tr class="even">
<td><strong>RegisterDownEndCallback</strong></td>
<td> </td>
<td> </td>
</tr>
</tbody>
</table>



</div> <!-- panel body --> 
</div> <!-- panel -->

<div class="panel panel-primary" id="Forge%20UI%5CControls%5CSimplePullDown">
<div class="panel-heading">
<div class="panel-title">SimplePullDown
</div>
</div>
<div class="panel-body">

<p>&lt;SimplePullDown&gt;</p>
<p>Wednesday, May 18, 2016</p>
<p>2:33 PM</p>

<p>Simplified version of &lt;PullDown&gt; or &quot;drop down box&quot; control. XML Configuration is identical to &lt;PullDown&gt; except for one additional attribute documented below. Made for tools in the interest of rapid UI development.</p>

<p><strong>XML</strong></p>
<table>
<thead>
<tr class="header">
<th><strong>Attribute</strong></th>
<th><strong>Details</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>EntryInstance</strong></td>
<td>The ID of the instance to use for building entries</td>
</tr>
</tbody>
</table>

<p><strong>LUA Methods</strong></p>
<table>
<thead>
<tr class="header">
<th><strong>Function</strong></th>
<th><strong>Returns</strong></th>
<th><strong>Arguments</strong></th>
<th><strong>Description</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>SetEntries</strong></td>
<td>void</td>
<td><p>Table entries,</p>
<p>uint selected</p></td>
<td>The entries table should be an array of tables. Each table represents an entry for the pulldown and must contain a &quot;Text&quot; value.</td>
</tr>
<tr class="even">
<td><strong>ClearEntries</strong></td>
<td>void</td>
<td> </td>
<td>Remove all entries</td>
</tr>
<tr class="odd">
<td><strong>SetSelectedIndex</strong></td>
<td>void</td>
<td><p>uint selected,</p>
<p>bool callback</p></td>
<td>Sets the selected entry by index. If callback is set to true then the entry selected callback will be called if the selected index has changed.</td>
</tr>
<tr class="even">
<td><strong>GetSelectedIndex</strong></td>
<td>uint</td>
<td> </td>
<td> </td>
</tr>
<tr class="odd">
<td><strong>GetSelectedEntry</strong></td>
<td>Table</td>
<td> </td>
<td>Will return the table provided in SetEntries for the selected entry</td>
</tr>
<tr class="even">
<td><strong>SetEntrySelectedCallback</strong></td>
<td>void</td>
<td>function</td>
<td>The entry selected callback will be called when the selected entry changes. The callback will be passed the table provided in SetEntries for the selected entry.</td>
</tr>
<tr class="odd">
<td><strong>CalcuateInternals</strong></td>
<td>void</td>
<td> </td>
<td>Calculates the size and contents of the grid, scroll panel, and stack.</td>
</tr>
<tr class="even">
<td><strong>ClearEntries</strong></td>
<td> </td>
<td> </td>
<td>Remove all entries</td>
</tr>
<tr class="odd">
<td><strong>ForceClose</strong></td>
<td>void</td>
<td> </td>
<td>Hides the grid and it's pieces</td>
</tr>
<tr class="even">
<td><strong>GetButton</strong></td>
<td>Button</td>
<td> </td>
<td>Obtain component piece</td>
</tr>
<tr class="odd">
<td><strong>GetGrid</strong></td>
<td>Grid</td>
<td> </td>
<td>Obtain component piece</td>
</tr>
<tr class="even">
<td><strong>GetScrollPanel</strong></td>
<td>ScrollPanel</td>
<td> </td>
<td>Obtain component piece</td>
</tr>
<tr class="odd">
<td><strong>GetStack</strong></td>
<td>Stack</td>
<td> </td>
<td>Obtain component piece</td>
</tr>
<tr class="even">
<td><strong>IsOffBottom</strong></td>
<td>bool</td>
<td> </td>
<td>Is the pulldown showing above the open button because of limited room?</td>
</tr>
<tr class="odd">
<td><strong>IsOpen</strong></td>
<td>bool</td>
<td> </td>
<td>Are the child elements showing.</td>
</tr>
<tr class="even">
<td><strong>SetDisabled</strong></td>
<td>void</td>
<td>bool</td>
<td>Enable or disables the control</td>
</tr>
</tbody>
</table>
</div> <!-- panel body --> 
</div> <!-- panel -->

<div class="panel panel-primary" id="Forge%20UI%5CControls%5CSlideAnim">
<div class="panel-heading">
<div class="panel-title">SlideAnim
</div>
</div>
<div class="panel-body">

<p><strong>&lt;SlideAnim&gt;</strong></p>
<p>Friday, February 21, 2014</p>
<p>3:03 PM</p>
<p>Moves a control in screen space between two offset values.</p>

<p><strong>Begin</strong> - Offset to start from</p>
<p><strong> </strong></p>
<p><strong>End</strong> - Offset to end at</p>

<p>For additional controls see: <em>Animation</em></p>

<p><strong>LUA Methods</strong></p>

<table>
<thead>
<tr class="header">
<th><strong>Function</strong></th>
<th><strong>Returns</strong></th>
<th><strong>Arguments</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>SetBeginVal</strong></td>
<td>n/a</td>
<td><strong>float</strong> x, <strong>float</strong> y</td>
</tr>
<tr class="even">
<td><strong>SetEndVal</strong></td>
<td>n/a</td>
<td><strong>float</strong> x, <strong>float</strong> y</td>
</tr>
<tr class="odd">
<td><strong>SetRealiveEndVal</strong></td>
<td>n/a</td>
<td><strong>float</strong> x, <strong>float</strong> y</td>
</tr>
</tbody>
</table>

<p>For Common LUA animation methods, see: <em>LUA Animation Methods</em></p>
</div> <!-- panel body --> 
</div> <!-- panel -->

<div class="panel panel-primary" id="Forge%20UI%5CControls%5CSlider">
<div class="panel-heading">
<div class="panel-title">Slider
</div>
</div>
<div class="panel-body">

<p>&lt;Slider&gt;</p>
<p>Friday, February 21, 2014</p>
<p>5:03 PM</p>

<p>The slider control is used for both picking a value along a spectrum (volume slider) and as the scroll bar for scroll panels. The background is built from one Grid, and the Thumb is another.</p>
<p>For picking values, the thumb does not need to grow, but for a scroll bar we size the thumb based on the content of the scroll panel.</p>

<p><strong>Style</strong> - The style attribute should be used to name a grid style to use for the background of the slider</p>
<p><strong> </strong></p>
<p><strong>Gutter</strong> - Gutter region to stop the slider before it reaches the ends of the background</p>
<p><strong> </strong></p>
<p><strong>Vertical</strong> - Flag to indicate that the slider moves up/down rather than left/right</p>
<p><strong> </strong></p>
<p><strong>Length</strong> - Size of the slider, in which ever direction the slider moves</p>
<p><strong> </strong></p>
<p><strong>&lt;Thumb&gt;</strong> - The thumb sub-control is itself a grid control and should also use a grid style</p>
</div> <!-- panel body --> 
</div> <!-- panel -->

<div class="panel panel-primary" id="Forge%20UI%5CControls%5CStack">
<div class="panel-heading">
<div class="panel-title">Stack
</div>
</div>
<div class="panel-body">

<p><strong>&lt;Stack&gt;</strong></p>
<p>Friday, February 21, 2014</p>
<p>2:47 PM</p>
<p>The <strong>Stack</strong> is used to arrange children into a line, or a grid. If the children change sizes, their positions will be adjusted correctly, but the Stack itself will not have its size update until <strong>CalculateSize()</strong> is called.</p>

<table>
<thead>
<tr class="header">
<th><strong>Attribute</strong></th>
<th><strong>Details</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>Padding</strong></td>
<td>Deprecated: See “StackPadding”</td>
</tr>
<tr class="even">
<td><strong>StackGrowth</strong></td>
<td>Direction the stack grows in: &quot;Bottom&quot; &quot;Down&quot; &quot;Top&quot; &quot;Up&quot; &quot;Left&quot; &quot;Right&quot;</td>
</tr>
<tr class="odd">
<td><strong>StackPadding</strong></td>
<td>Number of pixels to insert in between child elements. (Formally: “Padding”)</td>
</tr>
<tr class="even">
<td><strong>WrapGrowth</strong></td>
<td>How items that exceed the wrap width will continue to stack.</td>
</tr>
<tr class="odd">
<td><strong>WrapWidth</strong></td>
<td>How far (wide or tall, depending on stack growth) items can be put into the stack before subsequent items are “wrapped”.</td>
</tr>
</tbody>
</table>

<p>When <strong>WrapGrowth</strong> &amp; <strong>WrapWidth</strong> are utilized, they are what allow for 2D layout to occur once a line of stacking exceeds a certain limit.</p>
<p><img src="Forge UI\Controls\Stack/media/image1.png" alt="Machine generated alternative text: L&gt; Wrap Width is set. Until it is Without Wrap Width this ...since WrapGrowth is hit items are place in a line, would occur but instead... bottom, a new line, below the original is started." width="971" height="300" /></p>
</div> <!-- panel body --> 
</div> <!-- panel -->

<div class="panel panel-primary" id="Forge%20UI%5CControls%5CTabControl">
<div class="panel-heading">
<div class="panel-title">TabControl
</div>
</div>
<div class="panel-body">

<p>&lt;TabControl&gt;</p>
<p>Wednesday, May 18, 2016</p>
<p>3:08 PM</p>
<p>Supports tab pages with buttons to switch between them. The visual style of the buttons and tab pages is extremely open ended. No lua code is necessary for basic functionality. All configuration takes place in XML. Tab buttons are not necessary if you just want to change the selected tab from lua.</p>

<p><strong>XML</strong></p>
<table>
<thead>
<tr class="header">
<th><strong>Attribute</strong></th>
<th><strong>Details</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>TabContainer</strong></td>
<td>The ID of the control that contains the tab pages. The default value is &quot;TabContainer&quot;. All children of this control will be considered tab pages. Tab pages can be any kind of control. The pages will be shown and hidden as they are selected. The tab pages will be referred to by their IDs.</td>
</tr>
<tr class="even">
<td><strong>TabButtons</strong></td>
<td>The ID of the control that contains the tab buttons. The default value is &quot;TabButtons&quot;. Any button within the control tree underneath this control that has an ID that starts with &quot;SelectTab_&quot; will be considered a tab button. It can be any kind of button control. The tab button IDs should be in the format &quot;SelectTab_&lt;tab page ID&gt;&quot;. The functionality of the buttons will be handled automatically by the TabControl. Buttons will be in the &quot;selected&quot; state when their corresponding tab page is selected. Tab buttons are not necessary if you just want to change the selected tab from lua.</td>
</tr>
<tr class="odd">
<td><strong>SelectedTab</strong></td>
<td>The ID of the initial selected tab page. If this attribute is not used the first tab page will be selected by default.</td>
</tr>
</tbody>
</table>


<p><strong>LUA Methods</strong></p>
<table>
<thead>
<tr class="header">
<th><strong>Function</strong></th>
<th><strong>Returns</strong></th>
<th><strong>Arguments</strong></th>
<th><strong>Description</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>SelectTab</strong></td>
<td>void</td>
<td>ControlBase*</td>
<td>Select a tab by passing in a reference to the tab page control</td>
</tr>
<tr class="even">
<td><strong>SelectTabByID</strong></td>
<td>void</td>
<td>string</td>
<td>Select a tab using its ID</td>
</tr>
<tr class="odd">
<td><strong>GetSelectedTab</strong></td>
<td>ControlBase*</td>
<td> </td>
<td>Get a reference to the selected tab page</td>
</tr>
<tr class="even">
<td><strong>GetSelectedTabID</strong></td>
<td>string</td>
<td> </td>
<td>Get the ID of the selected tab page</td>
</tr>
<tr class="odd">
<td><strong>SetTabSelectedCallback</strong></td>
<td>void</td>
<td>function</td>
<td>The tab selected callback will be called whenever the selected tab is changed. The tab page and tab button will be provided to the callback as arguments.</td>
</tr>
</tbody>
</table>
</div> <!-- panel body --> 
</div> <!-- panel -->

<div class="panel panel-primary" id="Forge%20UI%5CControls%5CTextButton">
<div class="panel-heading">
<div class="panel-title">TextButton
</div>
</div>
<div class="panel-body">

<p><strong>&lt;TextButton&gt;</strong></p>
<p>Friday, February 21, 2014</p>
<p>4:49 PM</p>

<p>Button control which is text only. The color and style can be specified for each button state.</p>

<p><strong>XML</strong></p>
<table>
<thead>
<tr class="header">
<th><strong>Attribute</strong></th>
<th><strong>Details</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>Style</strong></td>
<td>The style of the button to use in the normal state. This style is not applied to the text button in its other states!</td>
</tr>
<tr class="even">
<td><strong>MouseOverStyle</strong></td>
<td>Style to use for MouseOver</td>
</tr>
<tr class="odd">
<td><strong>ButtonDownStyle</strong></td>
<td>The style to use for when the button is “pressed” Down</td>
</tr>
<tr class="even">
<td><strong>DisabledStyle</strong></td>
<td>The style to use for Disabled.</td>
</tr>
<tr class="odd">
<td><strong>Font</strong></td>
<td>Name of the font to use for this control.</td>
</tr>
<tr class="even">
<td><strong>FontSize</strong></td>
<td>Point size of the font to use.</td>
</tr>
<tr class="odd">
<td><strong>FontStyle</strong></td>
<td>Style (“<strong>stroke</strong>”, “<strong>shadow</strong>”, “<strong>glow</strong>”) of the font to use in its normal state.</td>
</tr>
<tr class="even">
<td><strong>String</strong></td>
<td>Text to use as the button</td>
</tr>
<tr class="odd">
<td><strong>ButtonDownColor</strong></td>
<td><strong>DEPRECATED:</strong> The ColorSet to use when in the “pressed” Down state.</td>
</tr>
<tr class="even">
<td><strong>DisabledColor</strong></td>
<td><strong>DEPRECATED:</strong> The ColorSet to use when Disabled</td>
</tr>
<tr class="odd">
<td><strong>MouseOverColor</strong></td>
<td><strong>DEPRECATED</strong>: ColorSet to use for MouseOver</td>
</tr>
<tr class="even">
<td><strong>NormalColor</strong></td>
<td><strong>DEPRECATED:</strong> ColorSet to use normally</td>
</tr>
</tbody>
</table>



<p><strong>Example</strong></p>

<p>&lt;!-- defined in styles.xml --&gt;</p>
<p>&lt;TestNormal Font=&quot;HelveticaNeue.ttf&quot; FontSize=&quot;22&quot; Color0=&quot;255,0,0,255&quot; Color1=&quot;0,99,99,200&quot; FontStyle=&quot;Stroke&quot; /&gt;</p>
<p>&lt;TestOver Font=&quot;HelveticaNeue.ttf&quot; FontSize=&quot;26&quot; Color0=&quot;255,255,0,255&quot; Color1=&quot;9,9,200,255&quot; FontStyle=&quot;Shadow&quot; /&gt;</p>
<p>&lt;TestDown Font=&quot;HelveticaNeue.ttf&quot; FontSize=&quot;18&quot; Color0=&quot;255,255,0,255&quot; Color1=&quot;255,0,0,255&quot; FontStyle=&quot;Stroke&quot; /&gt;</p>
<p>&lt;TestDisabled Font=&quot;HelveticaNeue.ttf&quot; FontSize=&quot;26&quot; Color0=&quot;90,90,90,190&quot; Color1=&quot;0,0,0,255&quot; FontStyle=&quot;Normal&quot; /&gt;</p>

<p>&lt;!-- used in specific screen's .xml --&gt;</p>
<p>&lt;TextButton ID=&quot;test&quot; Anchor=&quot;C,B&quot; Offset=&quot;0,0&quot; String=&quot;This is a test!&quot;</p>
<p>Style=&quot;TestNormal&quot;</p>
<p>MouseOverStyle=&quot;TestOver&quot;</p>
<p>ButtonDownStyle=&quot;TestDown&quot;</p>
<p>DisabledStyle=&quot;TestDisabled&quot; /&gt;</p>


</div> <!-- panel body --> 
</div> <!-- panel -->

<div class="panel panel-primary" id="Forge%20UI%5CControls%5CTextureBar">
<div class="panel-heading">
<div class="panel-title">TextureBar
</div>
</div>
<div class="panel-body">

<p><strong>&lt;TextureBar&gt;</strong></p>
<p>Friday, February 21, 2014</p>
<p>3:12 PM</p>

<p>Progress bar control made of a texture.</p>

<p><strong>XML</strong></p>
<table>
<thead>
<tr class="header">
<th><strong>Attribute</strong></th>
<th><strong>Type</strong></th>
<th><strong>Details</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Color</td>
<td>String</td>
<td>The red, green, blue and (optional) alpha values to apply to the meter texture. (Default is white with full alpha e.g., &quot;255,255,255,255);</td>
</tr>
<tr class="even">
<td>Direction</td>
<td>String</td>
<td>In which way does the bar fill: <strong>&quot;Up&quot; &quot;Down&quot; &quot;Left&quot; &quot;Right&quot;</strong></td>
</tr>
<tr class="odd">
<td>Percent</td>
<td>Number</td>
<td>Start value of the bar, by default this is 0.</td>
</tr>
<tr class="even">
<td>Sampler</td>
<td>String</td>
<td>Linear</td>
</tr>
<tr class="odd">
<td>ShadowColor</td>
<td>Number</td>
<td>&quot;R,G,B&quot; Color 'tint' for the drop shadow version of the texture. Greyscale values work best (ie: 112, 112, 112)</td>
</tr>
<tr class="even">
<td>Speed</td>
<td>Number</td>
<td>(default: &quot;<strong>0</strong>&quot;) What speed to animate the fill. If 0, no animation; immediately set percentage.</td>
</tr>
<tr class="odd">
<td>Texture</td>
<td>String</td>
<td>Filename of the texture to use for the bar.</td>
</tr>
<tr class="even">
<td>TextureOffset</td>
<td>String</td>
<td>-&quot;X,Y&quot; value in pixels to offset the Texture</td>
</tr>
</tbody>
</table>



<p><strong>LUA Functions</strong></p>
<table>
<thead>
<tr class="header">
<th><strong>Function</strong></th>
<th><strong>Returns</strong></th>
<th><strong>Arguments</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>SetPercent</strong></td>
<td><strong>n/a</strong></td>
<td><strong>float</strong>, 0.0 - 1.0 percent of the texture bar that is displayed (filled)</td>
</tr>
<tr class="even">
<td><strong>SetShadowPercent</strong></td>
<td><strong>n/a</strong></td>
<td><strong>float</strong>, 0.0-1.0 percent of texture used as a 'drop shadow'</td>
</tr>
<tr class="odd">
<td><strong>SetAnimationSpeed</strong></td>
<td><strong>n/a</strong></td>
<td><strong>float</strong>, 0 to animation speed where 0 is none</td>
</tr>
</tbody>
</table>
</div> <!-- panel body --> 
</div> <!-- panel -->

<div class="panel panel-primary" id="Forge%20UI%5CControls%5CToolTipType">
<div class="panel-heading">
<div class="panel-title">ToolTipType
</div>
</div>
<div class="panel-body">

<p><strong>&lt;ToolTipType&gt;</strong></p>
<p>Friday, February 21, 2014</p>
<p>2:21 PM</p>

<p>Defines a custom tool tip that overrides the default tool tip.</p>

<p><strong>XML</strong></p>
<table>
<thead>
<tr class="header">
<th><strong>Attribute</strong></th>
<th><strong>Type</strong></th>
<th><strong>Details</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Name</td>
<td>String</td>
<td>The tool tip instance name used by other components to reference this tooltip.</td>
</tr>
</tbody>
</table>

<p><em><em>Example:</em></em></p>
<p>&lt;ToolTipType Name=&quot;TypeRoundImage&quot;&gt;</p>
<p>&lt;Image ID=&quot;ToolTipFrame&quot; Anchor=&quot;L,T&quot; Size=&quot;64,64&quot; Offset=&quot;20,-32&quot; Texture=&quot;64x64FrameButtons.dds&quot; &gt;</p>
<p>&lt;Image ID=&quot;ToolTipImage&quot; Anchor=&quot;C,C&quot; Size=&quot;64,64&quot; Texture=&quot;UnitPortraitsEarly512.dds&quot; /&gt;</p>
<p>&lt;/Image&gt;</p>
<p>&lt;/ToolTipType&gt;</p>

<p>&lt;!-- Defining use of the tooltip --&gt;</p>
<p>&lt;GridButton        ID=&quot;CustomButton&quot; ToolTipType=&quot;TypeRoundImage&quot; /&gt;</p>


<p><strong>LUA Functions</strong></p>
<table>
<thead>
<tr class="header">
<th><strong>Function</strong></th>
<th><strong>Returns</strong></th>
<th><strong>Arguments</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>SetToolTipCallback()</td>
<td>nil</td>
<td>Tooltip callback function.</td>
</tr>
</tbody>
</table>

<p><em><em>Example:</em></em></p>
<p>-- Set the function to call when a tooltip is activated</p>
<p>Controls.MyButton:SetToolTipCallback( OnToolTip );</p>

<p>-- Fill a table with the controls used by the tooltip</p>
<p>local tipControlTable = {};</p>
<p>TTManager:GetTypeControlTable( &quot;TypeRoundImage&quot;, tipControlTable );</p>

<p>-- Callback function populating elements</p>
<p>function OnToolTip( control )</p>

<p>local id = control:GetVoid1();        </p>
<p>local article = m_categorizedListOfArticles[(m_selectedCategory * MAX_ENTRIES_PER_CATEGORY) + id];</p>
<p>if article and article.tooltipTexture then</p>
<p>tipControlTable.ToolTipImage:SetTexture( article.tooltipTexture );</p>
<p>tipControlTable.ToolTipImage:SetTextureOffset( article.tooltipTextureOffset );</p>
<p>tipControlTable.ToolTipFrame:SetHide( false );</p>
<p>else</p>
<p>tipControlTable.ToolTipFrame:SetHide( true );</p>
<p>end                </p>

<p>end</p>
</div> <!-- panel body --> 
</div> <!-- panel -->

<div class="panel panel-primary" id="Forge%20UI%5CControls%5CTutorial">
<div class="panel-heading">
<div class="panel-title">Tutorial
</div>
</div>
<div class="panel-body">

<p><strong>&lt;Tutorial&gt;</strong></p>
<p>Friday, February 21, 2014</p>
<p>2:21 PM</p>

<p>Starts a section of controls that are triggered to be shown/hidden based on the tutorial system.</p>


<p><strong>XML</strong></p>
<table>
<thead>
<tr class="header">
<th><strong>Attribute</strong></th>
<th><strong>Type</strong></th>
<th><strong>Details</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>AlwaysShow</td>
<td>Bool</td>
<td>Debug attribute when live editing. When true, the control ignores the show/hide calls from the manager and will just always show itself.</td>
</tr>
<tr class="even">
<td>ID</td>
<td>String</td>
<td>(optional) An ID for the tutorial control. If none is provided the first parent control that contains an ID will be set to the trigger list.</td>
</tr>
<tr class="odd">
<td>TriggerBy</td>
<td>String</td>
<td>Comma separated list of IDs that this tutorial control will react to. (The tutorial's ID is automatically added to the trigger list.)</td>
</tr>
</tbody>
</table>

<p><em>Example:</em></p>
<p>&lt;Box        ID=&quot;DoSomethingArea&quot; Color=&quot;0,255,128,100&quot; Size=&quot;100,100&quot;&gt;</p>
<p>&lt;Tutorial&gt;</p>
<p>&lt;BoxButton ID=&quot;CloseTutorial&quot; Color=&quot;255,0,0,200&quot; Size=&quot;50,50&quot; /&gt;                        </p>
<p>&lt;/Tutorial&gt;                </p>
<p>&lt;BoxButton ID=&quot;DoSomething&quot; Anchor=&quot;C,C&quot; Size=&quot;25,25&quot; Color=&quot;200,200,200,200&quot; /&gt;</p>
<p>&lt;Tutorial&gt;</p>
<p>&lt;Box Color=&quot;0,0,255,200&quot; Size=&quot;50,50&quot; Anchor=&quot;R,B&quot; /&gt;</p>
<p>&lt;/Tutorial&gt;                </p>
<p>&lt;/Box&gt;</p>

<p>-- LUA for the above XML:</p>
<p>Controls.DoSomething:RegisterCallback(Mouse.eLClick,function() UITutorialManager:ShowControlsByID(&quot;DoSomethingArea&quot;); end);</p>
<p>Controls.CloseTutorial:RegisterCallback(Mouse.eLClick,function() UITutorialManager:HideControlsByID(&quot;DoSomethingArea&quot;); end);</p>

<p><strong>LUA Functions</strong></p>
<table>
<tbody>
<tr class="odd">
<td><strong>Function</strong></td>
<td><strong>Returns</strong></td>
<td><strong>Arguments</strong></td>
</tr>
</tbody>
</table>
<p>Currently tutorial controls do not have function on themselves, other than what they inherent from ControlBase.</p>
<p>Be careful using Show/Hide as Tutorial controls should only be shown/hidden via the manager's calls or there is a possibility their visibility state will be out-of-sync with the manager.</p>

<p>The tutorial manager has functions that act on tutorial controls (as well as other controls with matching IDs)</p>

<p>UITutorialManager:ShowControlsByID(&quot;MyControlIDorTrigger&quot;);</p>
<p>UITutorialManager:HideControlsByID(&quot;MyControlIDorTrigger&quot;);</p>
<p>UITutorialManager:HideAll();</p>

</div> <!-- panel body --> 
</div> <!-- panel -->

<div class="panel panel-primary" id="Modding%5C2D%20Leader%20Background%20Mods">
<div class="panel-heading">
<div class="panel-title">2D Leader Background Mods
</div>
</div>
<div class="panel-body">

<h3>Creating the Texture and adding it to the XLP</h3>
<p>See: <a href="#Modding%5CTexture%20System%20Mods">Texture System Mods</a>.  Replace %XLP_CLASS% with <code>LeaderFallback</code>.
See: <a href="#Modding%5CAdd%20and%20Update%20Libraries%20in%20Mod%20Art%20File">Add and Update Libraries in Mod Art File</a>.  Replace %LIBRARY_NAME% with <code>LeaderFallback</code></p>
<h3>Creating the ArtDef and Referencing the Texture</h3>
<ol>
<li>Go to File -&gt; New -&gt; ArtDef</li>
<li>Change the <strong>Art Definition Template</strong> to LeaderFallback.</li>
<li>Select the <strong>Leaders</strong> item in the Tree, right-click, and press <em>Add Element</em>.</li>
<li>Change the name of the newly created element to the name of the leader.</li>
<li>Select the <strong>Animations</strong> item in the Tree, right-click, and press <em>Add Element</em>.</li>
<li>Change the <strong>Name</strong> to <code>DEFAULT</code>.</li>
<li>Under the <strong>BLP Entry</strong> column, select the field, click the dropdown, and then click the <em>Browse</em> button.</li>
<li>Find the newly created entry in the XLP browser.</li>
<li>Select the entry and press the <em>OK</em> button.</li>
<li>Save the ArtDef.</li>
</ol>
<p>See: <a href="#Modding%5CAdd%20and%20Update%20Consumers%20in%20Mod%20Art%20File">Add and Update Consumers in Mod Art File</a>.  Replace %CONSUMER_NAME% with <code>LeaderFallback</code></p>
<h3>Seeing art in the game</h3>
<p>See: <a href="#Modding%5CCooking%20Art%20Files">Cooking Art Files</a></p>
</div> <!-- panel body --> 
</div> <!-- panel -->

<div class="panel panel-primary" id="Modding%5CAdd%20and%20Update%20Consumers%20in%20Mod%20Art%20File">
<div class="panel-heading">
<div class="panel-title">Add and Update Consumers in Mod Art File
</div>
</div>
<div class="panel-body">

<h3>Creating Art Consumers in Mod Art File.</h3>
<ol>
<li>Open the Mod Art File that has been created for the mod.</li>
</ol>
<p><img src="Images/selectModArt.png" alt="" /></p>
<ol start="2">
<li>Select the consumer you wish to add from the list of Consumers to the right of the <strong>Art Consumers</strong> section.</li>
<li>Save the Mod Art File.</li>
</ol>
<p><strong>Do not press the <em>Add...</em> button for consumers.  You can create a new consumer, but would need to modify game-code in order to make use of it.</strong></p>
<h3>Adding the ArtDef to the Mod Art File.</h3>
<ol>
<li>Open up the Mod Art File that has been created for this mod (ending in *.Art.xml).</li>
</ol>
<p><img src="Images/AddConsumers_1.png" alt="" /></p>
<ol start="2">
<li>If your Consumer does not exist in the <strong>Art Consumers</strong> section, create it.</li>
</ol>
<p><img src="Images/AddConsumers_2.png" alt="" /></p>
<ol start="3">
<li>Select the your Consumer.</li>
</ol>
<p><img src="Images/AddConsumers_3.png" alt="" /></p>
<ol start="4">
<li>Press the <em>Add...</em> button next to the <strong>ArtDefs</strong> section.</li>
</ol>
<p><img src="Images/AddConsumers_4.png" alt="" /></p>
<ol start="5">
<li>Select the ArtDef that you have created and press the <em>Open</em> button.</li>
<li>Save the Mod Art File.</li>
</ol>
</div> <!-- panel body --> 
</div> <!-- panel -->

<div class="panel panel-primary" id="Modding%5CAdd%20and%20Update%20Libraries%20in%20Mod%20Art%20File">
<div class="panel-heading">
<div class="panel-title">Add and Update Libraries in Mod Art File
</div>
</div>
<div class="panel-body">

<h3>Creating Libraries in Mod Art File.</h3>
<ol>
<li>Open the Mod Art File that has been created for the mod.</li>
</ol>
<p><img src="Images/selectModArt.png" alt="" /></p>
<ol start="2">
<li>If the library that is being modified exists in the base game...
<ul>
<li>Select it from the ListBox next to the <strong>Libraries</strong> section.</li>
</ul>
</li>
</ol>
<p><img src="Images/AddLibraries_1.png" alt="" /></p>
<ol start="3">
<li>If the library does not exist...
<ul>
<li>Press the <em>Add...</em> button.</li>
<li>Change the name of the Library to the desired name.</li>
</ul>
</li>
<li>Save the Mod Art File.</li>
</ol>
<h3>Adding the XLP to the Mod Art File.</h3>
<ol>
<li>Open up the Mod Art File that has been created for this mod (ending in *.Art.xml).</li>
</ol>
<p><img src="Images/AddConsumers_1.png" alt="" /></p>
<ol start="2">
<li>If your library does not exist under the <strong>Libraries</strong> section, create it.</li>
<li>Select your library.</li>
</ol>
<p><img src="Images/AddLibraries_2.png" alt="" /></p>
<ol start="4">
<li>Press the <em>Add</em> button next to the <strong>Packages</strong> heading.</li>
</ol>
<p><img src="Images/AddLibraries_4.png" alt="" /></p>
<ol start="5">
<li>Select the XLP that you have created and press the <em>Open</em> button.</li>
<li>Save the Mod Art File.</li>
</ol>
</div> <!-- panel body --> 
</div> <!-- panel -->

<div class="panel panel-primary" id="Modding%5CAdding%20New%20Screens">
<div class="panel-heading">
<div class="panel-title">Adding New Screens
</div>
</div>
<div class="panel-body">

<p>In Civ 6, screens are referred to as LuaContexts. LuaContexts are made up of two separate files:</p>
<ol>
<li>An XML file that defines the layout and composition of the screen</li>
<li>A LUA script file that populates controls with game data and handles user interaction</li>
</ol>
<p>Both of these files must have the same filename, ex:</p>
<pre><code>MyNewScreen.xml
MyNewScreen.lua
</code></pre>
<hr />
<p><em>Note:</em>
The <code>&lt;ReplaceUIScript&gt;</code> modinfo element allows you to specify a different lua file for a LuaContext. This is mainly used for extending base game UI files, and not something you need to worry about if creating entirely new UI screens.</p>
<hr />
<p>Adding new UI screens to Civ 6 consists of a few steps:</p>
<ol>
<li>Create the XML and LUA files, for example:</li>
</ol>
<p><code>MyNewScreen.xml</code></p>
<pre><code class="language-xml">&lt;?xml version=&quot;1.0&quot; encoding=&quot;utf-8&quot;?&gt;

&lt;Context Name=&quot;MyNewScreen&quot;&gt;
    &lt;Label ID=&quot;MyText&quot; Anchor=&quot;C,C&quot; Align=&quot;Center&quot; Style=&quot;HeaderFont&quot; String=&quot;My New Screen&quot;/&gt;
&lt;/Context&gt;
</code></pre>
<p><code>MyNewScreen.lua</code>:</p>
<pre><code class="language-lua">-- We usually define an Initialize function at the bottom of the file and immediately call it. This is a convention we use to organizate our code and is completely optional.
function Initialize()
    Controls.MyText:SetText(Controls.MyText:GetText() .. &quot; is Awesome!&quot;);
end
Initialize();
</code></pre>
<ol start="3">
<li>Add a reference to both files in the <code>&lt;Files&gt;</code> section of the modinfo using the <code>&lt;File&gt;</code> tag, ex:</li>
</ol>
<pre><code class="language-xml">&lt;Files&gt;
    &lt;File&gt;UI/MyNewScreen.xml&lt;/File&gt;
    &lt;File&gt;UI/MyNewScreen.lua&lt;/File&gt;
&lt;/Files&gt;
</code></pre>
<ol start="4">
<li>Ensure your modinfo defines a <code>&lt;InGameActions&gt;</code> and <code>&lt;Files&gt;</code> sections, then:
<ol>
<li>Create <code>&lt;AddUserInteraces&gt;</code> section within <code>&lt;InGameActions&gt;</code>.</li>
<li>Create <code>&lt;Properties&gt;</code> section within <code>&lt;AddUserInteraces&gt;</code>.</li>
<li>Add <code>&lt;Context&gt;InGame&lt;/Context&gt;</code> within <code>&lt;Properties&gt;</code> section, this specifies that the following LuaContexts will only be loaded within the game.</li>
<li>Create <code>&lt;ImportFiles&gt;</code> section within <code>&lt;InGameActions&gt;</code>.</li>
<li>Add a reference to your new files in the <code>&lt;ImportFiles&gt;</code> section using the <code>&lt;File&gt;</code> tag.</li>
</ol>
</li>
</ol>
<hr />
<p>Here's an example asimple  modinfo file that incorporates all of the steps above:</p>
<p><code>MyMod.modinfo</code>:</p>
<pre><code class="language-xml">&lt;?xml version=&quot;1.0&quot; encoding=&quot;utf-8&quot;?&gt;
&lt;Mod id=&quot;xxxxxxxxxxxxxxxxxxxxxxxxxxxxxx&quot; version=&quot;1&quot;&gt;
    &lt;Properties&gt;
        &lt;Name&gt;MyMod&lt;/Name&gt;
        &lt;Teaser&gt;My Mod is Awesome&lt;/Teaser&gt;
        &lt;Description&gt;My Mod adds new UI screens&lt;/Description&gt;
        &lt;Authors&gt;Me&lt;/Authors&gt;
        &lt;EnabledByDefault&gt;1&lt;/EnabledByDefault&gt;
    &lt;/Properties&gt;
    &lt;ActionCriteria&gt;
        &lt;Criteria id=&quot;MyNewMod&quot;&gt;
            &lt;RuleSetInUse&gt;My New Rules!&lt;/RuleSetInUse&gt;
        &lt;/Criteria&gt;
    &lt;/ActionCriteria&gt;
    &lt;InGameActions&gt;
        &lt;AddUserInterfaces id=&quot;MyNewModInGameUI&quot; criteria=&quot;MyNewMod&quot;&gt;
            &lt;Properties&gt;
                &lt;Context&gt;InGame&lt;/Context&gt;
            &lt;/Properties&gt;
            &lt;File&gt;UI/MyNewScreen.xml&lt;/File&gt;
            &lt;File&gt;UI/MyNewScreen.lua&lt;/File&gt;
        &lt;/AddUserInterfaces&gt;
        &lt;ImportFiles id=&quot;MyNewModFiles&quot; criteria=&quot;MyNewMod&quot;&gt;
            &lt;File&gt;UI/MyNewScreen.xml&lt;/File&gt;
            &lt;File&gt;UI/MyNewScreen.lua&lt;/File&gt;
        &lt;/ImportFiles&gt;
    &lt;/InGameActions&gt;
    &lt;Files&gt;
        &lt;File&gt;UI/MyNewScreen.xml&lt;/File&gt;
        &lt;File&gt;UI/MyNewScreen.lua&lt;/File&gt;
    &lt;/Files&gt;
&lt;/Mod&gt;
</code></pre>
<p>// TODO: Explain id and criteria attributes</p>
</div> <!-- panel body --> 
</div> <!-- panel -->

<div class="panel panel-primary" id="Modding%5CAdding%20or%20Modifying%20Icons">
<div class="panel-heading">
<div class="panel-title">Adding or Modifying Icons
</div>
</div>
<div class="panel-body">

<p>// TODO</p>
</div> <!-- panel body --> 
</div> <!-- panel -->

<div class="panel panel-primary" id="Modding%5CColorKey%20Mods">
<div class="panel-heading">
<div class="panel-title">ColorKey Mods
</div>
</div>
<div class="panel-body">

<h3>Creating the Texture and adding it to the XLP</h3>
<p>Note about ColorKey Source Files:  Our ColorKey textures are 3D textures, with a resolution of 64 x 64 x 64.  This is typically represented by a 2048 x 128 texture band.
We support other resolutions, but this requires modifying the Texture Export Settings for the ColorKey.</p>
<p>See: <a href="#Modding%5CTexture%20System%20Mods">Texture System Mods</a>.  Replace %XLP_CLASS% with <code>ColorKey</code>.
See: <a href="#Modding%5CAdd%20and%20Update%20Libraries%20in%20Mod%20Art%20File">Add and Update Libraries in Mod Art File</a>.  Replace %LIBRARY_NAME% with <code>ColorKey</code></p>
</div> <!-- panel body --> 
</div> <!-- panel -->

<div class="panel panel-primary" id="Modding%5CCooking%20Art%20Files">
<div class="panel-heading">
<div class="panel-title">Cooking Art Files
</div>
</div>
<div class="panel-body">

<h3>Getting Art in the Game</h3>
<ol>
<li>Open up the AssetCloud.</li>
<li>Ensure that your Mod Project is selected.</li>
<li>Right-Click on AssetCloud.
<ul>
<li>Select <code>Cook Local Assets</code></li>
<li>Click on <code>All Files...</code></li>
</ul>
</li>
<li>Launch <code>Sid Meier's Civilization VI</code>.</li>
<li>Press the <em>Additional Content</em> button.</li>
<li>Ensure that your mod is enabled.  If it is enabled, it will have a check-mark next to it.</li>
<li>Play the game, and enjoy!</li>
</ol>
</div> <!-- panel body --> 
</div> <!-- panel -->

<div class="panel panel-primary" id="Modding%5CFireFX%20Built-In%20Functions">
<div class="panel-heading">
<div class="panel-title">FireFX Built-In Functions
</div>
</div>
<div class="panel-body">

<h2>mix</h2>
<p>Performs linear interpolation of <em>a</em> and <em>b</em> by <em>f</em>.  Return value is same type as <em>a</em>.</p>
<p><code>ret mix( a, b, f );</code></p>
<h3>Parameters</h3>
<ul>
<li><em>a</em> (<em>required</em>) can be any scalar or vector type.</li>
<li><em>b</em> (<em>required</em>) must be of the same type as <em>a</em>.</li>
<li><em>f</em> (<em>required</em>) must be a number.</li>
</ul>
<h2>delta_time</h2>
<p>Get time in seconds since the last update as a <code>number</code>.  Only valid in SIM module.</p>
<p><code>ret delta_time();</code></p>
<h2>root_position</h2>
<p>Get the root position for the instance as a <code>float3</code>.  Root transform is inherited down the entire emitter tree.</p>
<p><code>ret root_position();</code></p>
<h2>root_scale</h2>
<p>Get the root (uniform) scale for the instance as a <code>number</code>.  Root transform is inherited down the entire emitter tree.</p>
<p><code>ret root_scale();</code></p>
<h2>root_rotation</h2>
<p>Get the root rotation (quaternion) for the instance as a <code>float4</code>.  Root transform is inherited down the entire emitter tree.</p>
<p><code>ret root_rotation();</code></p>
<h2>is_orphan</h2>
<p>Returns 1 if the parent is orphaned, 0 otherwise.  Note that orphaned particles are force-killed after several seconds, so this function is essentially only used to begin a death behavior (such as fading).  Only valid in SIM module.</p>
<p><code>ret is_orphan();</code></p>
<h2>unique_id</h2>
<p>Returns the unique ID for the particle, which is non-deterministic and sparse.  Use unique ID to drive behavior that you intend to be completely uncorrelated with the number of particles in the instance.  Only valid in SPAWN module.</p>
<p><code>ret unique_id();</code></p>
<h2>index</h2>
<p>Returns the index for the particle.  Indices are 'packed', so if there are 16 particles in the instance each particle will get a number in the range [0,15].  Particle index does not change after the particle is spawned.  Only valid in SPAWN module.</p>
<p><code>ret index();</code></p>
<h2>instance_id</h2>
<p>Returns the instance ID that the particle belongs to.  Instance IDs are unique, so this value is useful if you want to have all particles in the same instance perform the same action.  This is a constant after the particle is spawned.</p>
<p><code>ret instance_id();</code></p>
<h2>terrain_height</h2>
<p>Get predicated terrain height at a specific location as a <code>number</code>.  If the terrain height at the world-space location (x,y components of <em>a</em>) is greater than the height predicate (z component of <em>a</em>), the return value will be terrain height at that location.  Otherwise the return value will be 'a.z'.  Use <code>ret &gt; a.z</code> to test if the predicate was below terrain height.</p>
<p><code>ret terrain_height( a );</code></p>
<h3>Parameters</h3>
<ul>
<li><em>a</em> (<em>required</em>) is <code>float3</code> with a world-space (x,y,z) position.</li>
</ul>
<h2>terrain_height_grad</h2>
<p>Returns predicated terrain height and gradient at a specific location as a <code>float3</code>.  If the terrain height at the world-space location (x,y components of <em>a</em>) is greater than the height predicate (z component of <em>a</em>), the return value will have terrain gradient (x, y components) and terrain height (z component).  Otherwise the return value will be <code>(0,0,_a.z_)</code>.  Use <code>ret.z &gt; a.z</code> to test if the gradient was returned.</p>
<p><code>ret terrain_height_grad( a );</code></p>
<h3>Parameters</h3>
<ul>
<li><em>a</em> (<em>required</em>) is <code>float3</code> with a world-space (x,y,z) position.</li>
</ul>
<h2>sample_fow</h2>
<p>Returns weights for FOW states at a specific location as a <code>float2</code>.  The x channel will contain the max of weights for FOW_GREY and FOW_WHITE, while the y channel will contain the weight for FOW_WHITE.  To get the weight for FOW_GREY, use <code>x - y</code>.  To get the weight for FOW_BLACK, use <code>1 - x</code>.  To convert to discrete state use largest weight returned.</p>
<p><code>ret sample_fow( a );</code></p>
<h3>Parameters</h3>
<ul>
<li><em>a</em> (<em>required</em>) is <code>float2</code> with a world-space (x,y) position.</li>
</ul>
<h2>hash</h2>
<p>Returns a random <code>number</code> in the range in the range (0,1) generated by hashing <em>f</em>.  The same value for <em>f</em> will always return the same random number, but a small change in <em>f</em> will cause an arbitrary change in the output value.</p>
<p><code>ret hash( f );</code></p>
<h3>Parameters</h3>
<ul>
<li><em>f</em> (<em>required</em>) input to hash.</li>
</ul>
<h2>sin</h2>
<p>Returns the sine of <em>f</em> as a <code>number</code>.</p>
<p><code>ret sin( f );</code></p>
<h3>Parameters</h3>
<ul>
<li><em>f</em> (<em>required</em>) must be a <code>number</code>.</li>
</ul>
<h2>cos</h2>
<p>Returns the cosine of <em>f</em> as a <code>number</code>.</p>
<p><code>ret cos( f );</code></p>
<h3>Parameters</h3>
<ul>
<li><em>f</em> (<em>required</em>) must be a <code>number</code>.</li>
</ul>
<h2>frac</h2>
<p>Returns the fractional component of <em>f</em> as a <code>number</code>.</p>
<p><code>ret frac( f );</code></p>
<h3>Parameters</h3>
<ul>
<li><em>f</em> (<em>required</em>) must be a <code>number</code>.</li>
</ul>
<h2>sqrt</h2>
<p>Returns the square root of <em>f</em> as a <code>number</code>.</p>
<p><code>ret sqrt(_f_);</code></p>
<h3>Parameters</h3>
<ul>
<li><em>f</em> (<em>required</em>) must be a <code>number</code>.</li>
</ul>
<h2>floor</h2>
<p>Returns the largest integer not greater than <em>f</em> as a <code>number</code>.</p>
<p><code>ret floor( f );</code></p>
<h3>Parameters</h3>
<ul>
<li><em>f</em> (<em>required</em>) must be a <code>number</code>.</li>
</ul>
<h2>ceil</h2>
<p>Returns the smallest integer not smaller than <em>f</em> as a <code>number</code>.</p>
<p><code>ret ceil( f );</code></p>
<h3>Parameters</h3>
<ul>
<li><em>f</em> (<em>required</em>) must be a <code>number</code>.</li>
</ul>
<h2>abs</h2>
<p>Returns the absolute value of <em>f</em> as a <code>number</code>.</p>
<p><code>ret abs( f );</code></p>
<h3>Parameters</h3>
<ul>
<li><em>f</em> (<em>required</em>) must be a <code>number</code>.</li>
</ul>
<h2>min</h2>
<p>Returns the minimum of <em>f</em> and <em>g</em> as a <code>number</code>.</p>
<p><code>ret min( f, g );</code></p>
<h3>Parameters</h3>
<ul>
<li><em>f</em> (<em>required</em>) must be a <code>number</code>.</li>
<li><em>g</em> (<em>required</em>) must be a <code>number</code>.</li>
</ul>
<h2>max</h2>
<p>Returns the maximum of <em>f</em> and <em>g</em> as a <code>number</code>.</p>
<p><code>ret max( f, g );</code></p>
<h3>Parameters</h3>
<ul>
<li><em>f</em> (<em>required</em>) must be a <code>number</code>.</li>
<li><em>g</em> (<em>required</em>) must be a <code>number</code>.</li>
</ul>
<h2>log</h2>
<p>Returns the natural logarithm of <em>f</em> as a <code>number</code>.</p>
<p><code>ret log( f );</code></p>
<h3>Parameters</h3>
<ul>
<li><em>f</em> (<em>required</em>) must be a <code>number</code>.</li>
</ul>
<h2>exp</h2>
<p>Returns the natural exponential of <em>f</em> as a <code>number</code>.</p>
<p><code>ret exp( f );</code></p>
<h3>Parameters</h3>
<ul>
<li><em>f</em> (<em>required</em>) must be a <code>number</code>.</li>
</ul>
<h2>round</h2>
<p>Returns the closest integral value to <em>f</em> as a <code>number</code>.</p>
<p><code>ret round( f );</code></p>
<h3>Parameters</h3>
<ul>
<li><em>f</em> (<em>required</em>) must be a <code>number</code>.</li>
</ul>
<h2>pow</h2>
<p>Returns <em>f</em> raised to the power <em>e</em> as a <code>number</code>.</p>
<p><code>ret pow( f, e );</code></p>
<h3>Parameters</h3>
<ul>
<li><em>f</em> (<em>required</em>) must be a <code>number</code>.</li>
<li><em>e</em> (<em>required</em>) must be a <code>number</code>.</li>
</ul>
<h2>dot</h2>
<p>Performs dot product of <em>a</em> and <em>b</em>.  Return value is <code>number</code>.</p>
<p><code>ret dot( a, b );</code></p>
<h3>Parameters</h3>
<ul>
<li><em>a</em> (<em>required</em>) can be any vector type.</li>
<li><em>b</em> (<em>required</em>) must be of the same type as <em>a</em>.</li>
</ul>
<h2>length</h2>
<p>Returns length of <em>a</em> as a <code>number</code>.</p>
<p><code>ret length( a );</code></p>
<h3>Parameters</h3>
<ul>
<li><em>a</em> (<em>required</em>) can be any vector type.</li>
</ul>
<h2>distance</h2>
<p>Returns distance between two vector types as a <code>number</code>.</p>
<p><code>ret distance( a, b );</code></p>
<h3>Parameters</h3>
<ul>
<li><em>a</em> (<em>required</em>) can be any vector type.</li>
<li><em>b</em> (<em>required</em>) must be the same type as <em>a</em>.</li>
</ul>
<h2>normalize</h2>
<p>Returns normalized vector of the same type as <em>a</em>.</p>
<p><code>ret normalize( a, b );</code></p>
<h3>Parameters</h3>
<ul>
<li><em>a</em> (<em>required</em>) can be any vector type.</li>
</ul>
<h2>random</h2>
<p>Return a random <code>number</code> between 0 and 1, inclusive.  Subsequent calls to <code>random()</code> will produce the next random number in the stream.  Calling <code>srand()</code> before calling <code>random()</code> will set the random seed if you want deterministic random numbers.  Any script that uses <code>random()</code> without first calling <code>srand()</code> will behave as if <code>srand( unique_id() )</code> was called first.</p>
<p><code>ret random();</code></p>
<h2>srand</h2>
<p>Sets the random seed so that all subsequent calls to <code>random()</code> in this script will be deterministic for the same value of <em>f</em>.  Any script that uses <code>random()</code> without first calling <code>srand()</code> will behave as if <code>srand( unique_id() )</code> was called first.</p>
<p><code>ret srand( f );</code></p>
<h3>Parameters</h3>
<ul>
<li><em>f</em> (<em>required</em>) must be a number.</li>
</ul>
</div> <!-- panel body --> 
</div> <!-- panel -->

<div class="panel panel-primary" id="Modding%5CFog%20of%20War%20Overview">
<div class="panel-heading">
<div class="panel-title">Fog of War Overview
</div>
</div>
<div class="panel-body">

<p>The Civ6 Fog of War system determines how parts of the map that have never been visible and/or are not currently visible get rendered.  By default, Civ6 uses a map-like style to render things that are in the &quot;mid-fog&quot;,
which is terrain that you have explored but do not currently have vision on.</p>
<p>This document provides an overview of how to modify the appearance of the Fog of War in Civ6.</p>
<p>Note:  The sepia-tone mid-fog is a shader, and cannot be modified by end users.</p>
<p>The below applies to creating a new Fog of War ArtDef.  Select the &quot;FOWConfig&quot; Art Definition Template for Fog of War ArtDefs.</p>
<h3>FOWConfig Collection</h3>
<p>The FOWConfig Collection always and only contains one value - &quot;Default&quot;.  Elements with any other name will not be read.  A collection without a &quot;Default&quot; element will not influence Fog of War in the game.</p>
<h3>The &quot;Default&quot; FOWConfig Element</h3>
<p>This element has numerous parameters.  In addition, it has children collections that allow further specification.</p>
<p>Name:</p>
<ul>
<li>Must be set to &quot;Default&quot;.</li>
</ul>
<p>MidFog:</p>
<ul>
<li>MidFog_RiverParchment -&gt; Texture to combine with the river in fog of war.</li>
<li>TerrainHatchColor -&gt; Controls the color at the MidFog/FullFog boundary.</li>
<li>TerrainHatchRotation -&gt; Changes the direction of the terrain hatch.</li>
<li>MidFog_CoastStripeThickness -&gt; Thickness of the coast outline in mid-fog.  The outline expands in-land as it grows larger.  The default value is 0.04.</li>
<li>MidFog_CoastStripeColor -&gt; Color of the coast outline in mid-fog.</li>
<li>TerrainHatchTileRate -&gt; Controls the smoothness of the hatch pattern.  Lower values are smoother, higher values are rougher.  The default value is 50.</li>
<li>MidFog_WaterParchmentTiling -&gt; Scales the Water Parchment texture.  The default value is 200.  The higher the value, the more space the texture takes up in the world.</li>
<li>MidFog_ShallowWaveJitter -&gt; Doesn't appear to do anything. ###</li>
<li>MidFog_OceanWaveJitter -&gt; Appears to effect the randomness of where ocean waves are placed in mid-fog.</li>
<li>MidFog_DeepWaterParchment -&gt; Changes the texture that is used to render deep-water (ocean) in mid-fog.</li>
<li>MidFog_ShallowWaterParchmet -&gt; Changes the texture that is used to render shallow-water (lakes and coast) in mid-fog.</li>
<li>MidFog_WaterParchmentRotation -&gt; Rotates the water parchment.</li>
<li>MidFog_CoastalWavesExtrudeDistance -&gt; Determines how far out the coastal wave texture gets drawn into the hex in mid-fog.</li>
<li>MidFog_CoastalWavesTiling -&gt; Changes the scale of the waves that are rendered.  The default value is 270.  A higher value makes the waves larger, a smaller value makes them smaller.</li>
<li>MidFog_CoastalWaves -&gt; Changes the texture that is used to render waves on top of coast.</li>
<li>MidFog_FlowLineColor -&gt; Doesn't appear to do anything. ###</li>
<li>MidFog_FlowLineThickness -&gt; Doesn't appear to do anything. ###</li>
<li>MidFog_FlowLineOpacity -&gt; Doesn't appear to do anything. ###</li>
<li>MidFog_FlowLineHeightBias -&gt; Doesn't appear to do anything. ###</li>
<li>MidFog_FlowLineOffset -&gt; Doesn't appear to do anything. ###</li>
</ul>
<p>FullFog:</p>
<ul>
<li>FullFog_LineOpacityTiling -&gt; Doesn't appear to do anything. ###</li>
<li>FullFog_ParchmentTiling -&gt; Changes the frequency that the parchment tiles.  Smaller numbers increase frequency.  The default value is 600.</li>
<li>FullFog_Parchment -&gt; Changes the texture that is used for the parchment.</li>
<li>FullFog_LineOpacityNoise -&gt; Changes the texture that is used for the LineOpacityNoise.</li>
<li>FullFog_LineOpacity -&gt; Doesn't appear to do anything. ###</li>
<li>FullFog_LineColor -&gt; Doesn't appear to do anything. ###</li>
<li>FullFog_ParchmentRotation -&gt; Rotates the parchment tiles (the squares in full-fog).</li>
<li>FullFog_DecoJitter -&gt; Appears to effect the randomness of where Deco sprites are placed.</li>
<li>FullFog_LineThicknessY -&gt; Doesn't appear to do anything. ###</li>
<li>FullFog_LineIntervalY -&gt; Doesn't appear to do anything. ###</li>
<li>FullFog_LineIntervalX -&gt; Doesn't appear to do anything. ###</li>
<li>FullFog_LineThicknessX -&gt; Doesn't appear to do anything. ###</li>
</ul>
<p>Value:</p>
<ul>
<li>BackgroundColor -&gt; Doesn't appear to do anything. ###</li>
</ul>
<p>FogBorder:</p>
<ul>
<li>FogBorderUVScale -&gt; Determines the UV Scale sampling from the Noise Texture at fog borders.  Values range from 0.0 to 1.0.  The default value is 0.0045.  Values higher than 0.01 make the edge incredibly noisy.</li>
<li>FogBorderNoiseIntensity -&gt; The noise intensity at fog borders.  Values range from 0.0 to 1.0.  Lower values cause fog to encroach on visible tiles more heavily.</li>
<li>FogBorderColor -&gt; Determines the color of the border between no-fog and mid-fig/full-fog.</li>
</ul>
<p>Models:</p>
<ul>
<li>Models_HatchTileRate -&gt; Effects the density of the hatch rate.  The default value is 50.  Lower values create a smoother appearance, while higher values make the hatch sharper.  Values between 40 and 70 tend to produce the best results.</li>
<li>Models_HatchRotation -&gt; Rotates the &quot;hatch&quot; on models in Fog of War.</li>
<li>Models_HatchColor -&gt; Determines the color of the vertical hatch that appears vertically on Fog of War models and resources.</li>
<li>Models_StrokeColor -&gt; Determines the color of the model outline in Fog of War.</li>
<li>Models_StrokeOpacity -&gt; Determines the visibility of the stroke that outlines models in Fog of War.</li>
<li>Models_StrokeThickness -&gt; Determines the thickness of the model outline.</li>
<li>Models_Parchment -&gt; The parchment texture that is used to be mixed with the parchment weight.</li>
<li>Models_ParchmentWeight -&gt; Controls how heavily the parchment texture influences the base color texture.</li>
</ul>
<p>CompassLines: -- Appear as diagnal lines that bisect the FullFog parchment.</p>
<ul>
<li>
<p>CompassLine_Texture -&gt; Controls the texture that is used to render compass lines.</p>
</li>
<li>
<p>CompassLine_Width -&gt; Controls how wide the compass lines are.</p>
</li>
<li>
<p>CompassLine_SeparationAngle -&gt; Controls how close together or separated the compass lines are.</p>
</li>
<li>
<p>Children:</p>
<ul>
<li>OceanWaveSets
<ul>
<li>LargeWaves
<ul>
<li>Rarity -&gt; Determines the frequency of LargeWaves in the total set of OceanWaves.</li>
<li>Sprites [Collection] -&gt; Each entry has a name, a texture assigned to it, and a scale factor.</li>
</ul>
</li>
<li>MediumWaves
<ul>
<li>Rarity -&gt; Determines the frequency of MediumWaves in the total set of OceanWaves.</li>
<li>Sprites [Collection] -&gt; Each entry has a name, a texture assigned to it, and a scale factor.</li>
</ul>
</li>
<li>SmallWaves
<ul>
<li>Rarity -&gt; Determines the frequency of SmallWaves in the total set of OceanWaves.</li>
<li>Sprites [Collection] -&gt; Each entry has a name, a texture assigned to it, and a scale factor.</li>
</ul>
</li>
</ul>
</li>
<li>FullFogDecotSets
<ul>
<li>Rarity -&gt; Determines how frequently a Deco sprite will be placed on the full-fog map parchment.</li>
<li>Sprites [Collection] -&gt; Each entry has a name, a texture assigned to it, and a scale factor.</li>
</ul>
</li>
<li>ShallowWaveSets
<ul>
<li>Rarity -&gt; Determines the frequency of Waves in the total set of ShallowWaveSets.</li>
<li>Sprites [Collection] -&gt; Each entry has a name, a texture assigned to it, and a scale factor.</li>
</ul>
</li>
<li>MapBorders
<ul>
<li>Rarity -&gt; Determines the frequency of MapBorders in the total set of MapBorders.</li>
<li>Sprites [Collection] -&gt; Each entry has a name, a texture assigned to it, and a scale factor.</li>
</ul>
</li>
<li>HatchTextures [Collection] -&gt; Maps a name to a Hatch texture.</li>
<li>ModelHatchTextures [Collection] -&gt; Maps a name to a Model Hatch texture.</li>
</ul>
</li>
</ul>
</div> <!-- panel body --> 
</div> <!-- panel -->

<div class="panel panel-primary" id="Modding%5CFoW%20Hatch%20Texture%20Mods">
<div class="panel-heading">
<div class="panel-title">FoW Hatch Texture Mods
</div>
</div>
<div class="panel-body">

<h3>Creating the Texture and adding it to the XLP</h3>
<p>See: <a href="#Modding%5CTexture%20System%20Mods">Texture System Mods</a>.  Replace %XLP_CLASS% with <code>FOWTexture</code>.
See: <a href="#Modding%5CAdd%20and%20Update%20Libraries%20in%20Mod%20Art%20File">Add and Update Libraries in Mod Art File</a>.  Replace %LIBRARY_NAME% with <code>FOWTexture</code></p>
<p>Hatch textures are typically FOWGreyscale textures, not FOW textures.</p>
<h3>Creating the ArtDef and Referencing the Sprites</h3>
<ol>
<li>Go to File -&gt; New -&gt; ArtDef</li>
<li>Change the <strong>Art Definition Template</strong> to <code>FOWConfig</code>.</li>
</ol>
<h3>Selecting the new Hatch Textures</h3>
<p>Hatch textures are used to hatch models and terrain in Fog of War.  They are added in a list under Default -&gt; HatchTextures and Default -&gt; ModelHatchTextures.</p>
<p>After creating adding a hatch texture to the FOWTexture XLP, you can add it to the HatchTextures collection.</p>
<h3>Adding the ArtDef to the Game</h3>
<p>See: <a href="#Modding%5CAdd%20and%20Update%20Consumers%20in%20Mod%20Art%20File">Add and Update Consumers in Mod Art File</a>.  Replace %CONSUMER_NAME% with <code>FOW</code></p>
<h3>Seeing art in the game</h3>
<p>See: <a href="#Modding%5CCooking%20Art%20Files">Cooking Art Files</a></p>
</div> <!-- panel body --> 
</div> <!-- panel -->

<div class="panel panel-primary" id="Modding%5CFoW%20Parchment%20Texture%20Mods">
<div class="panel-heading">
<div class="panel-title">FoW Parchment Texture Mods
</div>
</div>
<div class="panel-body">

<h3>Creating the Texture and adding it to the XLP</h3>
<p>See: <a href="#Modding%5CTexture%20System%20Mods">Texture System Mods</a>.  Replace %XLP_CLASS% with <code>FOWTexture</code>.
See: <a href="#Modding%5CAdd%20and%20Update%20Libraries%20in%20Mod%20Art%20File">Add and Update Libraries in Mod Art File</a>.  Replace %LIBRARY_NAME% with <code>FOWTexture</code></p>
<p>Parchments textures are typically FOW textures.</p>
<h3>Creating the ArtDef and Referencing the Sprites</h3>
<ol>
<li>Go to File -&gt; New -&gt; ArtDef</li>
<li>Change the <strong>Art Definition Template</strong> to <code>FOWConfig</code>.</li>
</ol>
<h3>Selecting the new Parchment Textures</h3>
<p>Parchment textures are used by the <code>Default</code> element in the <code>FOWConfig</code> ArtDef Element.  In Fog of War, separate textures are used for the mid-fog river, ocean, shallow waters,
as well as the shallow waves.  Additional textures are used for the compass lines, the full-fog parchment, and the model parchment.</p>
<h3>Adding the ArtDef to the Game</h3>
<p>See: <a href="#Modding%5CAdd%20and%20Update%20Consumers%20in%20Mod%20Art%20File">Add and Update Consumers in Mod Art File</a>.  Replace %CONSUMER_NAME% with <code>FOW</code></p>
<h3>Seeing art in the game</h3>
<p>See: <a href="#Modding%5CCooking%20Art%20Files">Cooking Art Files</a></p>
</div> <!-- panel body --> 
</div> <!-- panel -->

<div class="panel panel-primary" id="Modding%5CFoW%20Sprite%20Texture%20Mods">
<div class="panel-heading">
<div class="panel-title">FoW Sprite Texture Mods
</div>
</div>
<div class="panel-body">

<h3>Creating the Texture and adding it to the XLP</h3>
<p>See: <a href="#Modding%5CTexture%20System%20Mods">Texture System Mods</a>.  Replace %XLP_CLASS% with <code>FOWSprite</code>.
See: <a href="#Modding%5CAdd%20and%20Update%20Libraries%20in%20Mod%20Art%20File">Add and Update Libraries in Mod Art File</a>.  Replace %LIBRARY_NAME% with <code>FOWSprite</code></p>
<p>Sprite textures belong to the FOWSprite texture class.</p>
<h3>Creating the ArtDef and Referencing the Sprites</h3>
<ol>
<li>Go to File -&gt; New -&gt; ArtDef</li>
<li>Change the <strong>Art Definition Template</strong> to <code>FOWConfig</code>.</li>
</ol>
<h3>Selecting the new Sprite Textures</h3>
<p>Sprite textures are used to draw on top of the mid-fog and full-fog sections of the map.  The sea-dragons and other fantasy creatures, the wave sprites in shallow
and deep water, and the map borders are all FOWSprites.</p>
<p>There are four collections that accept sprite textures -&gt; OceanWaveSets, FullFogDecoSets, ShallowWaveSets, and MapBorders.  Each of these collections have a child
element that contains a rarity and a collection of sprites.  Once your textures exist in the FOWSprite XLPs, they can be added to the appropriate Sprites collection.</p>
<h3>Adding the ArtDef to the Game</h3>
<p>See: <a href="#Modding%5CAdd%20and%20Update%20Consumers%20in%20Mod%20Art%20File">Add and Update Consumers in Mod Art File</a>.  Replace %CONSUMER_NAME% with <code>FOW</code></p>
<h3>Seeing art in the game</h3>
<p>See: <a href="#Modding%5CCooking%20Art%20Files">Cooking Art Files</a></p>
</div> <!-- panel body --> 
</div> <!-- panel -->

<div class="panel panel-primary" id="Modding%5CHallofFame_Backend">
<div class="panel-heading">
<div class="panel-title">HallofFame_Backend
</div>
</div>
<div class="panel-body">

<p>It's time to dive into the internals of the hall of fame system and how it can be modded.</p>
<h1>Quick explanation of this post</h1>
<p>Because of the length, I'm going to break this up into two posts; one for the back-end and one for the front-end.  The back-end section, which we'll start with, consists of collecting data while a game is running and persisting this data in the saved game.  The front-end section is all about visualizing and presenting that data in the hall of fame section.  These aspects are loosely tied to each other to ensure plenty of flexibility.</p>
<p>Before diving into the front end and back end, I'd like to explain object references and type references.  There are plenty of times when data needs to be associated with more than just a game or even a player.  Sometimes it needs to be associated with a city, or religion, or some arbitrary game concept.  These are 'objects'.  Objects are a chunk of meta-data that additional data points and data sets can reference.  Objects contain information such as name, description, owning player, plot index, type, iconage, etc.  We can then reference this object using a simple integer and associate data with it.  For example, if we wanted to track the number of units trained by a player, we would pass in something like &quot;PlayerUnitsTrained&quot;, an object id (let's say '5'), and the number of units trained (let's say '100').</p>
<p>However, there are some cases where objects just aren't as abstract as we'd like.  For example, if we're tracking the number of units trained by a player for each unit type.  In that case we need both the player's object id as well as a specific unit type such as UNIT_WARRIOR.  We <em>could</em> make an additional object that represents this, or we could just specify both the player object and an additional 'Type' field, which simplifies things quite a bit.  So, for example, our &quot;PlayerUnitsTrainedByType&quot; would then have the object id of the player (5) along with the type (UNIT_WARRIOR).</p>
<h1>Back-End</h1>
<p>At present, there are two main types of data that is stored for the Hall of Fame; data points and data sets.</p>
<h2>Data points</h2>
<p>Data points are name-value pairs that can be associated with a ruleset, a game, or a specific object.  Data points are identified with a string and associate with a value that can be a number, a string, an object reference or a type.  Data points are typically visualized via statistics or reports.</p>
<p>Here are some examples:
|Data Point | Object Id | Value Numeric|Value Type|
|---|---|---|---|
|PlayerUnitsTrained|5|100||
|PlayerUnitsTrainedByType|5|30|UNIT_WARRIOR|
|FavoriteUnit|5| |UNIT_WARRIOR|
|CityProduction| 12 | 500|</p>
<h2>Data Sets</h2>
<p>Data sets are similar to points but rather than have a single value, they have X,Y integer pairs as values.  These are typically used to track per-turn values or per-era etc.  Just like data points, the data sets can be arbitrarily named and associated with games, objects, or types.  However, unlike data points, only numeric values can be used.  Data sets are typically visualized via graphs.</p>
<p>|Data  Set | Object Id | X | Y|
|---|---|---|---|
|CityProductionPerTurn| 12 | 1 | 20 |
|CityProductionPerTurn| 12| 2 | 25  |
|CityProductionPerTurn| 12 | 3 | 30 |</p>
<h1>Modding / Providing Data to the back-end</h1>
<h2>Game Database</h2>
<p>At present, no additional data is needed in the gameplay database when it comes to providing/recording additional data for the hall-of-fame.  However, when recording data that references a type, that type needs to be provided as well in order for the front-end to understand the name, icon, and other meta-data about that type.</p>
<h2>Lua</h2>
<p>Recording data can be done via Lua in the form of gameplay scripts.  Most of the functionality is exposed via a new API that resides in the global 'HallofFame'.   While this API is subject to change, here's it in its current form.</p>
<h3>Ruleset Types</h3>
<p><strong>HallofFame.GetRulesetTypes() -&gt; ruleset_types:array</strong>
Returns an array of all recorded ruleset types.  The structure is as follows:
|Field|Type|Description|
|---|---|---|
|Type|string|The type of the item (e.g UNIT_WARRIOR)|
Kind|string|The kind of the item (e.g KIND_UNIT)|
Name|string|The name of the item.|
Icon|[string]|The icon tag to use for the item.|</p>
<p><strong>HallofFame.SetRulesetType(type:string, kind:string, name:string, [icon:string])</strong>
Records the meta-data for a ruleset type.
If the type already exists, it will be replaced with the new data.</p>
<h3>Objects</h3>
<p><strong>HallofFame.CreateObject(type:string, [player_id:int], [name:string], [plot_index:int], [extra_data:string], [icon:string]) -&gt; object_id:int</strong>
Creates a new object w/ the specified data and returns the object id.</p>
<p><strong>HallofFame.GetObjects([type:string]) -&gt; objects:array</strong>
Returns an array of integers representing object id's.
The table structure is that of HallofFame.GetObject(objectId).</p>
<p><strong>HallofFame.GetCityObject([type:string]) -&gt; objects:array</strong>
Returns an array of integers representing object id's.
The table structure is that of HallofFame.GetObject(objectId).</p>
<p><strong>HallofFame.GetPlayerObject(playerId:int) -&gt; objects:array</strong>
Returns an array of integers representing object id's.
The table structure is that of HallofFame.GetObject(objectId).</p>
<h3>Data Points</h3>
<p><strong>HallofFame.FindDataPoint(data_point:string, [object_id:int], [type:string]) -&gt; result:int</strong>
Attempts to find a datapoint.
The result is the lookup id of the data point or nil if one does not exist.</p>
<p><strong>HallofFame.GetOrCreateDataPoint(data_point:string, [object_id:int], [type:string]) -&gt; result:int</strong>
Attempts to find a datapoint or creates one if it does not exist.
The result is the lookup id of the data point.</p>
<p><strong>HallofFame.GetDataPoints([object_id:int],[type:string]) -&gt; data_points:int_array</strong>
Returns an array of all data point lookup ids that matches the specified criteria.</p>
<p><strong>HallofFame.SetDataPoint(data_point:string, [object_id:int], [type:string], value:table) -&gt; result:bool</strong>
Creates or updates a datapoint with the specified value.
The structure of 'value' is as follows:
|Field|Type|Description|
|---|---|---|
|ValueNumeric|[int]|The numeric value associated with the data point.|
|ValueString|[string]|A string value associated with the data point.|
|ValueObjectId|[int]|An object id associated with the data point.|</p>
<p><strong>HallofFame.UpdateDataPoint(lookup_id:int, value:table) -&gt; result:bool</strong>
Updates a datapoint with the specified value.
The structure of 'value' is as follows:
|Field|Type|Description|
|---|---|---|
|ValueNumeric|[int]|The numeric value associated with the data point.|
|ValueString|[string]|A string value associated with the data point.|
|ValueObjectId|[int]|An object id associated with the data point.|</p>
<p><strong>HallofFame.LookupDataPoint(lookup_id:int) -&gt; result:int</strong>
Attempts to find a datapoint, returns nil if none can be found.
The structure of 'result' is as follows:
|Field|Type|Description|
|---|---|---|
|DataPoint|string|The identifier of the data point.|
|ObjectId|[int]|The object associated with the data point.|
|Type|[string]|The type associated with the data point.|
|ValueNumeric|[int]|The numeric value associated with the data point.|
|ValueString|[string]|A string value associated with the data point.|
|ValueObjectId|[int]|An object id associated with the data point.|</p>
<h3>Data Sets</h3>
<p><strong>HallofFame.FindDataSet(data_set:string, [object_id:int], [type:string]) -&gt; result:int</strong>
Attempts to lookup a specific data set.
The result is either the integer lookup id or nil.</p>
<p><strong>HallofFame.GetOrCreateDataSet(data_set:string, [object_id:int], [type:string]) -&gt; result:int</strong>
Attempts to lookup a specific data set or create one if it does not exist.
The result is an integer lookup Id.</p>
<p><strong>HallofFame.GetDataSets([object_id:int], [type:string]) -&gt; result:int_array</strong>
Returns all data set lookup id's for a game or given object id.</p>
<p><strong>HallofFame.GetDataSetValue(lookup_id:int, x:int) -&gt; Y:int</strong>
Returns a single integer representing the Y value or nil if not exist.</p>
<p><strong>HallofFame.GetLastDataSetValue(lookup_id:int) -&gt; X:int,Y:int</strong>
Returns two integers representing the x and y value or nil if dataset is invalid or empty.</p>
<p><strong>HallofFame.SetDataSetValue(lookup_id:int, x:int, y:int)</strong>
Assigns the x,y value of a dataset.</p>
<p><strong>HallofFame.AdjustDataSetValue(lookup_id:int, x:int, y:int) -&gt; value:int</strong>
Assigns or offsets the y value for a given x value in a dataset.
Returns the adjusted value.</p>
<p><strong>HallofFame.LookupDataSet(lookup_id:int) -&gt; result:table_array</strong>
Attempts to lookup a specific data set or create one if it does not exist.
The result is a combination table/array.
The array of the result contains the X,Y values, ordered by X.
The table structure is as follows.
|Field|Type|Description|
|---|---|---|
|DataSet|string|The data set id.|
|ObjectId|[int]|The object id associated.|
|Type|[string]|The type associated.|</p>
</div> <!-- panel body --> 
</div> <!-- panel -->

<div class="panel panel-primary" id="Modding%5CHallofFame_Frontend">
<div class="panel-heading">
<div class="panel-title">HallofFame_Frontend
</div>
</div>
<div class="panel-body">

<p>It’s time to dive into the internals of the hall of fame system and how it can be modded.</p>
<h1>Quick explanation of this post</h1>
<p>Because of the length, I’m going to break this up into two posts; one for the back-end and one for the front-end. The back-end section, which we’ll start with, consists of collecting data while a game is running and persisting this data in the saved game. The front-end section is all about visualizing and presenting that data in the hall of fame section. These aspects are loosely tied to each other to ensure plenty of flexibility.</p>
<p>Before diving into the front end and back end, I’d like to explain object references and type references. There are plenty of times when data needs to be associated with more than just a game or even a player. Sometimes it needs to be associated with a city, or religion, or some arbitrary game concept. These are ‘objects’. Objects are a chunk of meta-data that additional data points and data sets can reference. Objects contain information such as name, description, owning player, plot index, type, iconage, etc. We can then reference this object using a simple integer and associate data with it. For example, if we wanted to track the number of units trained by a player, we would pass in something like “PlayerUnitsTrained”, an object id (let’s say ‘5’), and the number of units trained (let’s say ‘100’).</p>
<p>However, there are some cases where objects just aren’t as abstract as we’d like. For example, if we’re tracking the number of units trained by a player for each unit type. In that case we need both the player’s object id as well as a specific unit type such as UNIT_WARRIOR. We could make an additional object that represents this, or we could just specify both the player object and an additional ‘Type’ field, which simplifies things quite a bit. So, for example, our “PlayerUnitsTrainedByType” would then have the object id of the player (5) along with the type (UNIT_WARRIOR).</p>
<h1>Hall of Fame (Front-End)</h1>
<p>The front-end is where all of the presentation of the data happens.  Because the data is loosely coupled, it can be visualized in many different ways and those ways can be extended/tweaked by modders.</p>
<h2>Configuration Database</h2>
<p>The front-end details of the hall of fame are stored in the configuration database rather than the hall of fame database.  This is to further enforce loose coupling between the data and visualization as well as allow modders easy access to changing around visualization details without having it burned into the more persistent hall of fame database.</p>
<p>Relevant files:
|Name|Location|
|---|---|
|Schema|<GameDir>\Base\Assets\Configuration\Data\Schema\HallofFame.sql|
|Data|<GameDir>\Base\Assets\Configuration\Data\HallofFame.xml|</p>
<h3>Overriding ruleset type references</h3>
<p>Sometimes data points may reference ruleset types that do not exist in the persistent data.  Other times, the data may need to be adjusted.  In the configuration database, there is a table called RulesetTypes.  Any information in this table, will override the information in the hall of fame database.  This is useful for providing extra localization or icon references that may not have been written out.</p>
<h2>Statistics</h2>
<p>Statistics are categorized values that present data points.  Statistics typically have a caption along with an optional icon.  How they display the value varies based on the data shown and can also be tweaked using &quot;hints&quot; which will be described later.</p>
<h3>Database details</h3>
<p>Statistics are specified in the database under the table 'Statistics' with the following columns:
|Name|Description|
|---|---|
|DataPoint|The data point to use for the statistic.
|Name|The localized name of the statistic (do not include a trailing ':').
|Icon|The icon to show along side the name of the statistic.|
|ValueIconDefault|The default icon to show along side the value of the statistic.|
|ValueIconOverride|The icon to always show, even if the value is an object or type.|
|Annotation|A localized annotation to display additional details of the statistic.|
|Direction|An integer between -1 and 1 that represents whether greater or lesser values are 'better'.  1 for greater, 0 for indifferent, -1 for lesser.|
|Category|The category id that the statistic belongs in.|
|Importance|An integer value representing how important the statistic is.  This is used for both sorting as well as picking out &quot;highlights&quot;.|</p>
<p>Categories are specified by the table 'StatisticCategories' with the following columns:
|Name|Description|
|---|---|
|Category|The id of the category.|
|Name|The localized name of the category.|
|IsHidden|Whether or not the category is shown.|
|SortOrder|How the categories are sorted (lower values are shown first, equal values are sorted by Name).|</p>
<h3>Presentation Logic</h3>
<p>The following logic is used by default to display the value of the data point:
Does the data point reference a type? Show the type name
Does the data point reference an object?  Show the object name.
Does the data point reference a string? Show the string.
Otherwise, show the numeric value.</p>
<p>The following hierarchy is used to determine which icon to use for the data point:</p>
<ul>
<li>ValueIconOverride</li>
<li>Object Icon</li>
<li>Type Icon</li>
<li>ValueIconDefault</li>
</ul>
<p>When displaying an icon, the hall of fame will attempt to use any overriding icon specified by the value and then fall-back to using the &quot;ValueIcon&quot; property of the statistic.</p>
<p>An annotation localized string key can also be provided.  This string will receive named arguments (&quot;Name&quot; and &quot;Value&quot;) and will be shown in addition to showing the value.</p>
<p>For example:</p>
<pre><code>Favorite Unit: [ICON_WARRIOR] Warrior (Trained 50 units.);
</code></pre>
<p>The annotation here is &quot;Trained {Value} units.&quot;.</p>
<p>As mentioned earlier, statistics are partitioned by categories and within each category sorted first by their importance and second by their name.</p>
<h2>Reports</h2>
<p>Reports also make use of data points but rather than show single values, they show a spreadsheet view of values.  An example report would be showing all religions in the game with columns specifying their holy city, number of followers, etc.</p>
<h3>Database details</h3>
<p>Reports are specified using up to 3 tables; Reports, ReportColumns, and ReportQueries.  In many cases, ReportQueries is not needed as a pre-defined query is good enough.</p>
<p>Here are the details of each table:</p>
<h4>Reports</h4>
<p>|Name|Description|
|---|---|
|Report|A string identifier for the report.|
|Scope|The 'scope' of the report.  For a description of how scopes work, see below.|
|Name|The localized name of the report.|
|Description|An optional localized description of the report.|
|InitialColumnName|The localized name of the initial column.|
|InitialColumnDescription|An optional localized description shown when mousing over the initial column.|
|InitialColumnUxHint|A hint to the UI to tune/tweak how the initial column is presented.|
|InitialColumnValueIconDefault|The default icon to show for the initial column.|
|InitialColumnValueIconOverride|The icon to always show for the initial column.|
|ShowEmptyRows|A boolean field describing whether or not to show rows where none of the major columns have values.|
|Query|The query to use to determine the set of objects that will represent rows in the column.|
|ExtraData|Extra data provided to the query.|
|Importance|An integer value representing the importance of the report.  This is typically used to adjust sort order.|</p>
<h4>ReportColumns</h4>
<p>|Name|Description|
|---|---|
|Report|The report this is a column of.|
|Name|The localized name of the column.|
|Description|An optional localized description shown when mousing over.|
|SortOrder|The sort order of the column in the report left-to-right is lower-to-higher.|
|DataPoint|The data point identifier to visualize.|
|UxHint|A hint to the UI to tune/tweak how the data is presented.|
|Minor|A boolean field describing whether the column is 'minor'. Rows in reports are only shown if there are non-minor columns that actually have values.|
|AlwaysShow|A boolean field describing whether or not to show the column even if none of the rows actually have values.|
|ValueIconDefault|The default icon to show if the value of the cell does not contain any icons.|
|ValueIconOverride|The icon to always show.|</p>
<h4>ReportQueries</h4>
<p>|Name|Description|
|---|---|
|Query|The identifier of the query used by ReportColumns.Query|
|SQL|The actual SQL of the query.|</p>
<p>There are quite a few pre-defined queries that cover most bases.</p>
<p>Queries are SQL statements that execute against the hall of fame database and require knowledge of hall of fame schema.</p>
<p>The following return columns are expected from the query:
|Name|Description|
|---|---|
|ObjectId|The object id to use for a row. Can be optional so long as Type is specified.|
|Type|The ruleset type to use for a row.  Can be optional so long as ObjectId is specified.|</p>
<p>The following arguments are fed into the query:
|Name|Description|
|---|---|
|@ObjectId|The object id (often a player object)|
|@GameId|The game id.|
|@Ruleset|The ruleset.|
|@ExtraData| An extra field specified by 'Reports.ExtraData'.|</p>
<h3>Scope</h3>
<p>Scope details what sort of coverage the report has and how its data will be queried.  Scopes are usually one of 3 values; &quot;Ruleset&quot;, &quot;Game&quot; or &quot;Player&quot;.  &quot;Player&quot; scoped reports will go through each player in a game and generate a report.  Queries will have the player's object id as the @ObjectId specified.  Meanwhile, &quot;Game&quot; scoped reports will be generated once for each game with &quot;@GameId&quot; being the game's id but &quot;@ObjectId&quot; will be null.</p>
<p>An example &quot;Player&quot; report would be &quot;Player Cities&quot; that list all cities for a given player.  Meanwhile a &quot;Game&quot; report would be &quot;Religions&quot; that show all religions in the game.</p>
<h2>Graphs</h2>
<p>Graphs are the primary way of visualizing data sets in the hall of fame.  As of this writing, there is only 1 type of graph; a basic line graph.  However, in the future, additional styles of graphs may become available.</p>
<p>Graphs are similar to reports in that they use queries to enumerate sets of objects and scope to further dictate how those queries are called.</p>
<h2>Database Details</h2>
<p>Graphs are specified using up to 2 tables; Graphs and GraphQueries.  In many cases, GraphQueries is not needed as a pre-defined query is good enough.</p>
<p>Here are the details of each table:</p>
<h4>Graphs</h4>
<p>|Name|Description|
|---|---|
|Graph|The identifier of the graph.|
|Scope|The 'scope' of the graph.  For a description of how scopes work, see below.|
|Name|A localized name for the graph.|
|Description|An optional localized description of the graph.|
|Direction|An integer value representing whether lower or higher is better.  -1 for lower, 0 for indifferent, and 1 for higher.|
|XLabel|An optional localized string for the X-Axis label.|
|YLabel|An optional localized string for the Y-Axis label.|
|Query|The query to use to determine what data sets to show.|
|DataSet|A variable passed into the query representing the desired data set identifier.|
|ExtraData|An extra data variable that can be passed into the query.
|Importance|A integer value representing how important the graph is.  Typically used for sorting.|
|UxHint|A presently unused value that hints to the UI as to how the graph should be visualized.|</p>
<h4>GraphQueries</h4>
<p>|Name|Description|
|---|---|
|Query|The identifier of the query used by Graphs.Query|
|SQL|The actual SQL of the query.|</p>
<p>There are quite a few pre-defined queries that cover most bases.</p>
<p>Queries are SQL statements that execute against the hall of fame database and require knowledge of hall of fame schema.</p>
<p>The following return columns are expected from the query:
|Name|Description|
|---|---|
|ObjectId|An object id reference. Can be optional if type is specified.|
|Type|The ruleset type. Can be optional if ObjectId is specified.|
|DataSetId|A reference to DataSets.DataSetId.|</p>
<p>The following arguments are fed into the query:
|Name|Description|
|---|---|
|@ObjectId|The object id (often a player object)|
|@GameId|The game id.|
|@Ruleset|The ruleset.|
|@DataSet|A field specified by 'Graphs.DataSet'.|
|@ExtraData| An extra field specified by 'Graphs.ExtraData'.|</p>
<h2>Aggregate Updates</h2>
<p>There are times when the data recorded on the back-end simply isn't enough or cannot be properly calculated at the time of recording.  A good example of this is when trying to compute averages for various statistics, such as average city population.  This is where aggregate updates come into play.  Aggregate updates are used to perform processing on the back-end database so that additional data can be derived.  This data is recorded into the database but is typically refreshed whenever the hall of fame Ux is visible.</p>
<p>Aggregate updates work by using a query to enumerate a set of data points for a given scope and then execute the specified operation (such as Sum, Min, Max, Count, etc).</p>
<h3>Database Details</h3>
<p>There are 4 tables used for aggregate updates, two for data points, and two for data sets.</p>
<h4>DataPointAggregateUpdates</h4>
<p>|Name|Description|
|---|---|
|AggregateDataPoint|The identifier of the data point to be written.|
|Scope|The scope of the process.|
|Operation|The operation to use. See below for details on what operations are available.|
|Query|The query to use.|
|DataPoint|The source data point, also a variable fed into the query.|
|ExtraData|An extra data value fed into the query.|
|SortIndex|The sort index that specifies the order the processes get executed.|</p>
<h4>DataPointAggregateQueries</h4>
<p>|Name|Description|
|---|---|
|Query|The identifier of the query used by DataPointAggregateUpdates.Query.|
|SQL|The actual SQL of the query.|</p>
<p>The following return columns are expected from the query:
|Name|Description|
|---|---|</p>
<p>The following arguments are fed into the query:
|Name|Description|
|---|---|
|@ObjectId|The object id (often a player object)|
|@GameId|The game id.|
|@Ruleset|The ruleset.|
|@DataPoint|A field specified by 'DataPointAggregateQueries.DataPoint'.|
|@ExtraData| An extra field specified by 'DataPointAggregateQueries.ExtraData'.|</p>
<h4>DatasetAggregateUpdates</h4>
<p>|Name|Description|
|---|---|
|AggregateDataPoint|The identifier of the data point to be written.|
|Scope|The scope of the process.|
|Operation|The operation to use. See below for details on what operations are available.|
|Query|The query to use.|
|Dataset|The source dataset, also a variable fed into the query.|
|ExtraData|An extra data value fed into the query.|
|SortIndex|The sort index that specifies the order the processes get executed.|</p>
<h4>DatasetAggregateQueries</h4>
<p>|Name|Description|
|---|---|
|Query|The identifier of the query used by DatasetAggregateUpdates.Query.|
|SQL|The actual SQL of the query.|</p>
<p>The following return columns are expected from the query:
|Name|Description|
|---|---|</p>
<p>The following arguments are fed into the query:
|Name|Description|
|---|---|
|@ObjectId|The object id (often a player object)|
|@GameId|The game id.|
|@Ruleset|The ruleset.|
|@Dataset|A field specified by 'DatasetAggregateUpdates.Dataset'.|
|@ExtraData| An extra field specified by 'DatasetAggregateUpdates.ExtraData'.|</p>
<h3>Work flow</h3>
<p>Aggregate updates are executed in a well defined order so that values calculated from aggregates can be used in later ones.</p>
<p>Data set aggregate updates happen first.  This is because they don't rely on any existing data points and only on the data-sets which at present cannot be updated via aggregates.</p>
<p>Data set aggregate updates follow the same scope order as everything else, that is player then game then ruleset.</p>
<p>Afterwards, Data point aggregate updates are processed using the same scope order.</p>
<h3>Operations</h3>
<p>The following operations can be used:</p>
<p>|Name|Description|
|---|---|
|Sum|Accumulates all numeric values and returns the total.|
|Min|Finds the row with the minimal value and returns the object id and/or type along with that value.|
|MinSum|Finds the object id and/or type with an accumulated minimal value.|
|Max|Finds the row with the maximum value and returns the object id/and or type along with that value.|
|MaxSum|Finds the object id and/or type with an accumulated maximum value.|
|First|Writes the values of the first row.|
|Last|Writes the values of the last row.|
|Count|Count the number of rows.|
|Average|Average the numeric value of each row.|
|Median|Find the median of each row.|</p>
</div> <!-- panel body --> 
</div> <!-- panel -->

<div class="panel panel-primary" id="Modding%5CHotLoading">
<div class="panel-heading">
<div class="panel-title">HotLoading
</div>
</div>
<div class="panel-body">

<h3>Hot Loading</h3>
<hr />
<p>Hot loading is a way to apply changes from the mod tools in real time to what you see in-game and can be a great way to make adjustments to what you're currently working on.</p>
<p>First, you will need to open the Asset Editor as well as the main game. Start a game and make sure it is running the mod you are currently working on.</p>
<p>Once these things are open, select an entity you want to modify, make a change to it and then save it.</p>
<p><img src="Images/HotLoad_2.PNG" alt="" /></p>
<p>You will then need to hit &quot;Build&quot; in the solution of your mod.</p>
<p><img src="Images/HotLoad_3.PNG" alt="" /></p>
<p>If your build completes without errors you should be able to hit the &quot;Hot Load&quot; button and the changes will be applied and visible in the current game.</p>
<p><img src="Images/HotLoad_4.PNG" alt="" /></p>
</div> <!-- panel body --> 
</div> <!-- panel -->

<div class="panel panel-primary" id="Modding%5CLoadOrder">
<div class="panel-heading">
<div class="panel-title">LoadOrder
</div>
</div>
<div class="panel-body">

<h1>Load order</h1>
<p>Load order in mods is a way of explicitly controlling when an action should take place.  By default, all actions have a load order of &quot;0&quot;.</p>
<h2>&quot;What should I typically do?&quot;</h2>
<p>Unless actions specifically need to run BEFORE most content or AFTER most content, load order should remain the same.  Instead, as a general practice, make use of references and dependencies to ensure that most actions from the expansions typically occur before your own actions.</p>
<p>This will typically resolve inconsistencies regarding actions that 'override' things such as 'ImportFiles' or 'ReplaceUIScript'.</p>
<h2>Actions with equal load orders.</h2>
<p>Actions with equal load orders are sorted by their dependencies and references to packages. Otherwise, the order is not strictly defined.</p>
<p>If Mod A depends on Mod B, actions in Mod A that have the same load order as actions in Mod B will always be applied AFTER actions in Mod B have been applied.  The same goes for if Mod A references Mod B.</p>
<h2>Reverse reference/dependency</h2>
<p>If you need to ensure your actions occur before the actions of another mod, you can add that mod as a reverse reference.  This will tell the modding framework that the other mod now has a reference or dependency to your mod and cause your actions to be applied prior.</p>
<h2>Recommended Load Order Values</h2>
<p>|Value|Description|
|---|---|
|-100|Schema changes<br/>Remove Data<br/>Populate core data|
|-75|Unofficial Schema changes|
|-50|Premature Updates<br/>Updates that need to be made before content is typically added.|
|-25|Unofficial changes to premature updates|
|0|Standard Content Updates<br/>Most actions applied during this phase.|
|25|Unofficial changes to standard updates|
|50|Post Updates<br/>Updates that require most content to be provided.|
|75|Unofficial changes to post-update content|
|100|Scenario Updates<br/>Often applied at the very end of everything else.  Called out as its own phase.|
|125|Unofficial changes to Scenario updates.|</p>
</div> <!-- panel body --> 
</div> <!-- panel -->

<div class="panel panel-primary" id="Modding%5CModifying%20Existing%20Screens">
<div class="panel-heading">
<div class="panel-title">Modifying Existing Screens
</div>
</div>
<div class="panel-body">

<p>// TODO</p>
</div> <!-- panel body --> 
</div> <!-- panel -->

<div class="panel panel-primary" id="Modding%5CNotes%20shorthand">
<div class="panel-heading">
<div class="panel-title">Notes shorthand
</div>
</div>
<div class="panel-body">

<h2>Creating Units from Existing Pieces:</h2>
<p>The Civ VI engine and pantry makes it quite easy to create new units from existing pieces.
In this example, we are going to go through the process of creating a warrior clad in full
armor that fights using a sword and shield.  We will create a new asset for the body (based
on existing geometry and materials), but everything else will be based on existing assets.</p>
<ul>
<li>Open up the asset that has the geometry you want to re-use.</li>
<li>Determine what the geometry name is.</li>
<li>Create a new asset of the same class as the existing asset.</li>
<li>Go to the &quot;Geometries&quot; tab, and select &quot;Add Existing&quot;.</li>
<li>Browse for the geometry that you want (In this case, Knight_European_Armor_A).</li>
<li>Add the geometry to the asset.</li>
<li>Add the behaviors that you want to your asset.  (This example, Swordsman and SingleBiped_Deaths; ensure &quot;Swordsman&quot; behavior is topmost).</li>
</ul>
</div> <!-- panel body --> 
</div> <!-- panel -->

<div class="panel panel-primary" id="Modding%5CSkyBox%20Overview">
<div class="panel-heading">
<div class="panel-title">SkyBox Overview
</div>
</div>
<div class="panel-body">

<p>The Civ6 SkyBox system determine what is drawn off the edges of the map.  It displays a single texture that has this detail in it.</p>
<p>In order to modify this texture, you must create a new ArtDef with the ArtDef Template of &quot;SkyBox&quot;.</p>
<p>The SkyBox template has one collection inside of it - named SkyBox.  This collection has one element inside of it.  This element must be named &quot;SkyPlane&quot;.
The &quot;SkyPlane&quot; element has one reference in it - a BLP entry reference.  It draws its BLP from the SkyBox library.</p>
<p>See the &quot;SkyBox Texture Mod&quot; document for more information.</p>
</div> <!-- panel body --> 
</div> <!-- panel -->

<div class="panel panel-primary" id="Modding%5CSkyBox%20Texture%20Mods">
<div class="panel-heading">
<div class="panel-title">SkyBox Texture Mods
</div>
</div>
<div class="panel-body">

<h3>Creating the Texture and adding it to the XLP</h3>
<p>See: <a href="#Modding%5CTexture%20System%20Mods">Texture System Mods</a>.  Replace %XLP_CLASS% with <code>SkyBoxTexture</code>.
See: <a href="#Modding%5CAdd%20and%20Update%20Libraries%20in%20Mod%20Art%20File">Add and Update Libraries in Mod Art File</a>.  Replace %LIBRARY_NAME% with <code>SkyBoxTexture</code></p>
<h3>Creating the ArtDef and Referencing the Sprites</h3>
<ol>
<li>Go to File -&gt; New -&gt; ArtDef</li>
<li>Change the <strong>Art Definition Template</strong> to <code>SkyBox</code>.</li>
</ol>
<h3>Selecting the new SkyBox Textures</h3>
<p>In the SkyBox collection, create a new element named &quot;SkyPlane&quot;.  If there is already a &quot;SkyPlane&quot; element, modify its SkyBoxTexture value, setting it to the newly created SkyBox Texture.</p>
<h3>Adding the ArtDef to the Game</h3>
<p>See: <a href="#Modding%5CAdd%20and%20Update%20Consumers%20in%20Mod%20Art%20File">Add and Update Consumers in Mod Art File</a>.  Replace %CONSUMER_NAME% with <code>SkyBox</code></p>
<h3>Seeing art in the game</h3>
<p>See: <a href="#Modding%5CCooking%20Art%20Files">Cooking Art Files</a></p>
</div> <!-- panel body --> 
</div> <!-- panel -->

<div class="panel panel-primary" id="Modding%5CStrategicView%20Building%20Sprite%20Mods">
<div class="panel-heading">
<div class="panel-title">StrategicView Building Sprite Mods
</div>
</div>
<div class="panel-body">

<h3>Creating the Texture and adding it to the XLP</h3>
<p>See: <a href="#Modding%5CTexture%20System%20Mods">Texture System Mods</a>.  Replace %XLP_CLASS% with <code>StrategicView_Sprite</code>.
See: <a href="#Modding%5CAdd%20and%20Update%20Libraries%20in%20Mod%20Art%20File">Add and Update Libraries in Mod Art File</a>.  Replace %LIBRARY_NAME% with <code>StrategicView_Sprite</code></p>
<p>We have multiple different building states for each building sprite.</p>
<p>Visibility States:</p>
<ul>
<li>Revealed</li>
<li>Visible</li>
</ul>
<p>Building State:</p>
<ul>
<li>Normal (constructed)</li>
<li>Pillaged</li>
<li>Under Construction</li>
</ul>
<h3>Creating the ArtDef and Referencing the Sprites</h3>
<ol>
<li>Go to File -&gt; New -&gt; ArtDef</li>
<li>Change the <strong>Art Definition Template</strong> to <code>StrategicView</code>.</li>
</ol>
<h3>Adding the Building Entries</h3>
<ol>
<li>Select the <strong>BuildingEntries</strong> item in the Tree, right-click, and press <em>Add Element</em>.  Do this once for each construction state.</li>
<li>Change the name of the newly created elements to the name of the building and its construction state.</li>
<li>Under the <strong>Visible_XLPEntry</strong> field, click the dropdown, and then click the <em>Browse</em> button.</li>
<li>Find the newly created entry in the XLP browser.</li>
<li>Select the entry and press the <em>OK</em> button.</li>
<li>Under the <strong>Revealed_XLPEntry</strong> field, click the dropdown, and then click the <em>Browse</em> button.</li>
<li>Find the newly created entry in the XLP browser.</li>
<li>Select the entry and press the <em>OK</em> button.</li>
</ol>
<h3>Adding the Buildings</h3>
<ol>
<li>Select the <strong>Buildings</strong> item in the Tree, right-click, and press <em>Add Element</em>.  Do this once for each construction state.</li>
<li>Name the new entries based on the building and construction state that it will be in.</li>
<li>For each new entry, select the BuildingChain (which determines which district this building belongs in), the PositionSet (which determines how the game places the entries), and the placement rules (where in the Position Set does this particular entry live).</li>
<li>Expand the tree node for each of the newly created buildings.</li>
<li>Select <strong>Entries</strong>, right-click, and press <em>Add Element</em>.</li>
<li>Select the new entry.  Choose a new name for it, and then select the appropriate ArtDefEntry that you added in the above section.</li>
</ol>
<p>Please remember to save your work.</p>
<h3>Adding the ArtDef to the Game</h3>
<p>See: [Add and Update Consumers in Mod Art File][cons].  Replace %CONSUMER_NAME% with <code>StrategicView_Sprite</code></p>
<h3>Seeing art in the game</h3>
<p>See: <a href="#Modding%5CCooking%20Art%20Files">Cooking Art Files</a></p>
</div> <!-- panel body --> 
</div> <!-- panel -->

<div class="panel panel-primary" id="Modding%5CStrategicView%20Natural%20Wonder%20Sprite%20Mods">
<div class="panel-heading">
<div class="panel-title">StrategicView Natural Wonder Sprite Mods
</div>
</div>
<div class="panel-body">

<p>StrategicView Terrain Feature Sprites include elements that occur naturally in the world.</p>
<p>This includes, forest, rainforest/jungles, ice, marshes, oasis tiles, floodplains, and all Natural Wonders.
This does not include base terrain types (desert, mountain, etc.)</p>
<p>We allow variation in the items that get displayed in these instances.</p>
<h3>Creating the Texture and adding it to the XLP</h3>
<p>See: <a href="#Modding%5CTexture%20System%20Mods">Texture System Mods</a>.  Replace %XLP_CLASS% with <code>StrategicView_Sprite</code>.
See: <a href="#Modding%5CAdd%20and%20Update%20Libraries%20in%20Mod%20Art%20File">Add and Update Libraries in Mod Art File</a>.  Replace %LIBRARY_NAME% with <code>StrategicView_Sprite</code></p>
<p>We have two visibility states for Natural Wonder sprites.</p>
<p>Visibility States:</p>
<ul>
<li>Revealed</li>
<li>Visible</li>
</ul>
<h3>Creating the ArtDef and Referencing the Sprites</h3>
<ol>
<li>Go to File -&gt; New -&gt; ArtDef</li>
<li>Change the <strong>Art Definition Template</strong> to <code>StrategicView</code>.</li>
</ol>
<h3>Adding the Feature Entries</h3>
<ol>
<li>Select the <strong>FeatureEntries</strong> item in the Tree, right-click, and press <em>Add Element</em>.</li>
<li>Change the name of the newly created elements to the name of the Feature.</li>
<li>Under the <strong>Visible_XLPEntry</strong> field, click the dropdown, and then click the <em>Browse</em> button.</li>
<li>Find the newly created entry in the XLP browser.</li>
<li>Select the entry and press the <em>OK</em> button.</li>
<li>Under the <strong>Revealed_XLPEntry</strong> field, click the dropdown, and then click the <em>Browse</em> button.</li>
<li>Find the newly created entry in the XLP browser.</li>
<li>Select the entry and press the <em>OK</em> button.</li>
</ol>
<h3>Adding the Features</h3>
<ol>
<li>Select the <strong>Features</strong> item in the Tree, right-click, and press <em>Add Element</em>.</li>
<li>Name the new entries based on the feature or natural wonder being replaced.</li>
<li>For each new entry, select the BuildingChain (which determines which district this building belongs in), the PositionSet (which determines how the game places the entries), and the placement rules (where in the Position Set does this particular entry live).</li>
<li>Expand the tree node for each of the newly created buildings.</li>
<li>Select <strong>Entries</strong>, right-click, and press <em>Add Element</em>.</li>
<li>Select the new entry.  Choose a new name for it, and then select the appropriate ArtDefEntry that you added in the above section.</li>
</ol>
<p>Please remember to save your work.</p>
<h3>Adding the ArtDef to the Game</h3>
<p>See: [Add and Update Consumers in Mod Art File][cons].  Replace %CONSUMER_NAME% with <code>StrategicView_Sprite</code></p>
<h3>Seeing art in the game</h3>
<p>See: <a href="#Modding%5CCooking%20Art%20Files">Cooking Art Files</a></p>
</div> <!-- panel body --> 
</div> <!-- panel -->

<div class="panel panel-primary" id="Modding%5CStrategicView%20Overview">
<div class="panel-heading">
<div class="panel-title">StrategicView Overview
</div>
</div>
<div class="panel-body">

<p>The StrategicView provides a 2D visualization of the map in a Civ game.  Numerous aspects of its visuals can be modified by changing the StrategicView.artdef file.</p>
<p>This document provides an overview of the different Root Collections in the StrategicView ArtDef.</p>
<h3>Properties Collection</h3>
<p>The properties collection contains general propreties that affect how the entire StrategicView is displayed, particularly colors between or
around hexes and the size of a terrain texture in world units.  TerrainTiling is used as a scale factor for how frequently terrain textures
are repeated.  Lower numbers cause terrain textures to get drawn at a higher frequency, as each texture takes up less world space.</p>
<h3>PositionSets Collection</h3>
<p>Position sets are used to determine the location of sprites within a StrategicView Tile.  Each PositionSet has a collection of positions.
Each Position has a name and a coordinate value ([x,y] pair).  The valid range of positions is from -0.5 to 0.5 for the x value,
and -0.57 to 0.57 for the y value, though values beyond +/- 0.3 are very near to the hex edge.</p>
<p>Each entry in the position set corresponds to an entry in the element that is making use of it.  When a StrategicView Sprite entry makes use
of a PositionSet, the PositionSet needs to have at least one position defined for each entry in the Sprite.</p>
<h3>PlacementRules Collection</h3>
<p>This is a fixed collection and should not be modified.  Sprite entries make use of this to determine how they get arranged around the hex.</p>
<p>AtEdges_NotScaled -&gt;
Centered -&gt; The first entry is selected and it is displayed in the center of the hex.
Centered_NotScaled -&gt; The first entry is selected and it is displayed in the center of the hex.  It is not scaled.
Centered_NotScaled_Animate
Centered_Random -&gt; A random entry from the collection is selected and it is displayed in the center.
GreatWall
OneEntryPerTile -&gt; For multiple tile features, this informs the feature that a single entry will be displayed per tile.</p>
<h3>TerrainBlends</h3>
<p>TO-DO:</p>
<h3>TerrainBlendCorners:</h3>
<p>TO-DO:</p>
<h3>TerrainSpriteEntries</h3>
<p>Defines the set of possible terrain sprite.  Each entry has a name, a Visble XLP Entry reference with positional offsets, and a Revealed XLP Entry reference with positional offsets.</p>
<h3>TerrainSprites</h3>
<p>Defines the terrain sprite collections that will be used by the game.  Each element has a name, position set, a placement rule, a render flag, and the number of tiles it occupies.  Additionally, these elements have child
collections that reference TerrainSpriteEntries that have been defined by the TerrainSpriteEntries collection.</p>
<p>When a terrain sprite has multiple entries within it AND the &quot;Centered_Random&quot; PlacementRule is chosen, the entry that is rendered by the StrategicView is chosen at random.  Each entry has an equally likely chance of getting chosen.</p>
<h3>TerrainTypes</h3>
<p>Assigns art to the different types of terrain in the game.  The terrain name is based on the GameCore name.  For any given terrain, an entry is chosen at random from the terrain entries collection.  An entry maps a visible texture
and offset, a revealed texture and offset, and an optional sprite (used for rendering hills and mountains - but it can be used for anything) to a particular type of terrain.  Each terrain type (coast, desert, ocean, grassland, plains,
snow, tundra) is its own entry.  Additionally, any terrain that can support mountains or hills also has an additional entry for that type (e.g. Snow, SnowHills, and SnowMountains are all different TerrainTypes).</p>
<p>The sprites that are chosen for the TerrainTypes collection are defined in the TerrainSprites root collection above.</p>
<p>These terrain types need to match the terrain types that are defined by GameCore.</p>
<h3>FeatureEntries</h3>
<p>Defines the set of possible feature asset entries.  Each feature asset entry has a name, a Visble XLP entry with offsets, and a revealed XLP entry with offsets.</p>
<h3>Features</h3>
<p>Features are anything that naturally appears on top of terrain without player intervention.  Examples of this include forest and rainforest, as well as all natural wonders.</p>
<p>The Features collection assigns feature entry art to features in the game.  Each element in the Features collection has a name (must match a GameCore name), a PositionSet (varies heavily), a PlacementRule (also varies), a render flag
(true if this feature should be rendered, false otherwise), a flag to render a terrain sprite on top of the terrain, a TileCount field (which must match the number of tiles the Natural Wonder occupies as defined by GameCore), and a
TerrainTypeOverride list.  The TerrainTypeOverride list allows you to specify that a given feature (typically a Natural Wonder) completely overrides terrains with the types displayed in the list.</p>
<p>Each Feature element also has an Entries collection, which is used to map FeatureEntries to the Feature.</p>
<h3>EffectEntries</h3>
<p>Defines the set of possible effect entries.  Each entry has a name, a Visible XLP entry and offsets, and a Revealed XLP Entry and offsets.</p>
<h3>Effects</h3>
<p>Assigns are to the different effects in the game.  Currently, the only effect is &quot;NuclearFallout&quot;.  This can be assigned a position set, a placement rule, a render variable, and a tile-count.  Additionally, it has an effects collection
that allow it to reference effect entries.</p>
<h3>Routes</h3>
<p>Assigns art to different routes used in the game.  Each entry has a name (which must match its GameCore name), a route XLP entry, and a bridge XLP entry.</p>
<h3>ImprovementEntries</h3>
<p>Defines the set of possible improvement asset entries.  Each improvement asset entry has a name, a Visble XLP entry with offsets, and a revealed XLP entry with offsets.</p>
<h3>Improvements</h3>
<p>An improvement is anything that is placed on a tile by a builder (e.g. farms, pastures, etc.).  Barbarian Camps and Airstrips also count as improvements.</p>
<p>The Improvements collection assigns art to in-game improvements.  The name of the element should be the GameCore name of the improvement.  If the improvement can be pillaged, there should be one element for its regular state, and one
element for its pillaged state.  Each element has a position set (typically &quot;1_Center&quot; is chosen), a PlacementRule (typically &quot;Centered&quot;) is chosen, a Render flag (if the improvement should be visible, set this flag to true), and a tile-count
value (this needs to match the GameCore value that says how large the improvement is - currently all improvements are only one tile).</p>
<p>Each Improvement element has an &quot;Entries&quot; collection, where entries defined in the ImprovementEntries collection are assigned to the improvement element.</p>
<h3>DistrictEntries</h3>
<p>Defines the set of possible district asset entries.  Each district asset entry has a name, a Visble XLP entry with offsets, and a revealed XLP entry with offsets.</p>
<h3>Districts</h3>
<p>Districts are extensions of the city, built by the city itself in a tile outside of its city center, but within the city borders.  Districts contain buildings based on their specialty.</p>
<p>The Districts collection assigns art to districts, based on the name of the district in GameCore.  All districts can be pillaged, and all districts must be constructed, so there are three states that any district art should include -
the base, constructed district, the pillaged district, and the district under construction.  Each state has its own element within the Districts collection.  The naming convention is District, District_Pillaged, and District_UnderConstruction.
Each element has a PositionSet (typically 1_Center), a PlacementRule (typically Centered), a Render flag (true for all visible districts, false for Wonder and CityCenter), and a TileCount (currently always 1) that must match its GameCore definition.</p>
<p>Additionally, each District has an Entries collection that maps one of the entries defined in the DistrictEntries collection above to the District.</p>
<h3>BuildingEntries</h3>
<p>Defines the set of possible building asset entries.  Each building asset entry has a name, a Visble XLP entry with offsets, and a revealed XLP entry with offsets.
There should be a building entry for each of the construction states - constructed, pillaged, and under construction.</p>
<p>Our naming convention is typically Building, Building_Pillaged, Building_UnderConstruction, but this is simply a convention.</p>
<h3>Buildings</h3>
<p>Buildings comprise of every structure that a city can build that is not a district.  This includes buildings that go within each district, buildings that go within the City Center, and any World Wonders that a City produces.</p>
<p>The Buildings collection assigns art to in-game buildings.  The name of the element should be the GameCore name of the building.  There should be one element for each building's regular state, one element for its pillaged state,
and one element for its under construction state.  All buildings, including World Wonders, can be placed into the pillaged state, so having art for this state is advised.</p>
<p>Each element has a position set (typically &quot;1_Center&quot; is chosen), a PlacementRule (typically &quot;Centered&quot;) is chosen, a Render flag (if the building should be visible, set this flag to true), a tile-count value (this needs to match
the GameCore value that says how large the building is - currently all buildings are only one tile), and a BuildingChain.  The BuildingChain determines which district the building appears in.  City Center Buildings and World Wonders
leave the BuildingChain value blank.  All other buildings must be assigned to the correct chain to display in the appropriate district.</p>
<p>Each building element has an &quot;Entries&quot; collection, where entries defined in the BuildingEntries collection are assigned to the building element.</p>
<h3>CityEntries</h3>
<p>Defines the set of possible city asset entries.  Each city asset entry has a name, a Visble XLP entry with offsets, and a revealed XLP entry with offsets.</p>
<h3>Cities</h3>
<p>A city is constructed when a settler settles in a location.  Cities change their appearance throughout the game.  As the game time progresses, the visuals for a city reflect the current age of the game.</p>
<p>The city definition need to match the GameCore names.  The current set of names are Ancient_City, Industrial_City, Medieval_City, and Modern_City.  Each element in the Cities collection has a name, a PositionSet (typically 1_Center),
a PlacementRule (typically Centered), a Render flag (render the city or not), and a TileCount (typically 1).  Each city element also has an Entries collection that contains a value from the CityEntries collection defined above.</p>
<h3>UILenses</h3>
<p>UI Lenses are views that are displayed on top of the map to help provide additional information about an activity or state of the game.</p>
<p>The names of the elements of the UI Lens collection follow no hard rule, however, they need to match the same name that is being called from LUA.</p>
<p>Each UI Lens element has a PositionSet (as described above), a PlacementRule (as described above), and a render flag (true to render the element, false otherwise).  There are no consistent defaults for UI lens entries.
Additionally, each UI Lens element has an AnimDuration parameter, an AnimType parameter, and a RotateToAlign parameter.</p>
<p>UI lenses can animate between textures (if any INTERPOLATE animation type is chosen) or between alpha values (if any FADE animation type is chosen).  If an INTERPOLATE animation type is chosen, the lens element animates
between its first two texture entries (first -&gt; second if forward is chosen, second -&gt; first is backwards is chosen, and first -&gt; second -&gt; first -&gt; second etc. if loop is chosen).  If a FADE animation type is chosen, the
lens element animates from invisible to visible if FADE_IN_ONCE is chosen, visible to invisible if FADE_OUT_ONCE is chosen, and between visible and invisible repeatedly if FADE_LOOP is chosen.</p>
<p>Each UI lens entry has a certain number of parameters associated with it.  They can be set at the asset level itself.  The UI Lenses which derived from those entries have a position set with it, a placement rule, a render flag.</p>
<p>In the base game, placement lenses are examples of UI Lens elements that make use of animations.</p>
<p>The rotate to align flag allows textures to be aligned along the egde of the hex (as opposed to forcing their alignment to the center of the hex).  It makes placing lenses that lay along hex boundaries easier.</p>
<h3>UILensEntries</h3>
<p>Defines the set of possible UI Lens asset entries.  Each UI Lens asset entry has a name, a Visble XLP entry with offsets, a revealed XLP entry with offsetsm a tint color, and a scale factor.</p>
</div> <!-- panel body --> 
</div> <!-- panel -->

<div class="panel panel-primary" id="Modding%5CTexture%20System%20Mods">
<div class="panel-heading">
<div class="panel-title">Texture System Mods
</div>
</div>
<div class="panel-body">

<h3>Creating the Texture and adding it to the XLP</h3>
<ol>
<li>Open <code>Asset Editor</code>.</li>
<li>File -&gt; New -&gt; XLP.</li>
</ol>
<p><img src="Images/TextureSystem_1.png" alt="" /></p>
<ol start="3">
<li>Change the <strong>XLP Class</strong> field to the desired class.</li>
</ol>
<p><img src="Images/TextureSystem_2.png" alt="" /></p>
<ol start="4">
<li>Choose a package name for the XLP.</li>
<li>Save the XLP.</li>
<li>Under the <strong>Entries</strong> section, click on the <em>Add New</em> button.</li>
<li>Click <em>Add Source File...</em> and select the image that should be used.</li>
<li>Set the name of the Texture that will be created, or leave it as the default value.</li>
<li>Press the <em>Import</em> button.</li>
<li>Save the XLP now that it has changed.</li>
</ol>
</div> <!-- panel body --> 
</div> <!-- panel -->

<div class="panel panel-primary" id="Modding%5CUnderstanding%20modinfo%20files">
<div class="panel-heading">
<div class="panel-title">Understanding modinfo files
</div>
</div>
<div class="panel-body">

<p>// TODO</p>
</div> <!-- panel body --> 
</div> <!-- panel -->

<div class="panel panel-primary" id="Modding%5CUnit%20Mods">
<div class="panel-heading">
<div class="panel-title">Unit Mods
</div>
</div>
<div class="panel-body">

<p>Unit system... unit system... How does one make a unit?</p>
<p>There's so much that goes into it!  Where to start?</p>
<p>Maybe at the core principles.</p>
<p>The Unit System in Civilization 6 has been designed to support a tremendous amount of unit variation.
This variation is achieved by utilizing an attachment style system.  Units don't exist as a single model
with a head, body, sword, shield, etc.  Each of the things that I listed are components of a unit, and they
can be put together piece by piece to compose a complete unit.</p>
<p>Units also have additional attributes that define how they behave in game that are also configured, such as what their
formations look like, how they fight, or how they move when escorting someone.  Each of these different categorizations
is a separate Root Collection in the Units ArtDef.</p>
<p>The unit with the most variation is the warrior, so let's start there.  The Warrior Unit has its formation set to the &quot;Warrior&quot;
Formation, it's UnitCombat set to the &quot;Warrior&quot; UnitCombat member, and its EscortFormation set to the &quot;WarriorEscort&quot; formation.
The unit members of the warrior Unit are of type &quot;Warrior&quot;, with a scale of 1 and a count of 4.</p>
<p>All of these values are defined in other Root Collections of the Unit ArtDef.</p>
<p>The UnitMemberTypes defines what set of bins will compose a given unit.  The UnitMemberType has a Movement type, a Combat field,
a VFX MaterialType, and a VFXWeaponImpact type.  Additionally, it has a cultures children collection that defines what cultural variations
will exist for a unit.  All units should at least have the &quot;Any&quot; culture.  Additional cultural options include &quot;Barbarian&quot;, &quot;EastAsian&quot;,
&quot;Mediterranean&quot;, &quot;Mughal&quot;, &quot;NorthAfrican&quot;, &quot;NorthernEuropean&quot;, &quot;SouthAfrican&quot;, and &quot;SouthAmerican&quot;.  Each of these cultures has a
&quot;Variations&quot; collection.  Variations allow you to specify the scale of the unit variation, whether or not the variation is an attachment,
and attachments that the variation will make use of.  The Attachments child collection contains attachment definition elements.  These
elements have a Name (the name of the attachment), a &quot;Point&quot; (the attachment point in the root skeleton that the attachment will be attached
to), and a Tint (custom color scheme that will be used to tint the asset).  The attachment definition element also specifies one or more bins
from which to draw assets from.  These bins are defined as follows:  &quot;Bin_Name/Group_Name&quot;.</p>
<h2>Unit Attachment Mods:</h2>
<p>Units in Civ VI use attachments to be built compositionally.  Some of the easiest
things to change in the base game include swords, shields, and other attachments
that are used to compose units.</p>
<p>Swords and other unit attachments are Assets of the Unit class.  Unit asset classes
accept Geometries of the &quot;Unit&quot; Geometry Class, and Materials of the &quot;Unit&quot; Material
Class to bind to those geometries.  Typically, an attachment asset is composed of one
Unit Geometry (that contains the model information), with one Unit Material assigned
to that Geometry.</p>
<p>The majority of materials in Civ VI are based on PBR, so these materials slots for
an ambient Occlusion texture, an Albedo/BaseColor texture, a Gloss texture, a
Metalness texture, and a Normal texture.  These textures typically fall under a
&quot;generic&quot; texture class that is based on the given texture type.  (Look up PBR/Metalness
pipelines to understand how each of these texture slots are used).</p>
<p>Our material projects tend to be set up using DDO (by Quixel).  Each texture has its
own separate source file, which is a .tga file that is generated from DDO.  This is
not a requirement to authoring textures for our pipeline - just something that our
Art Team found useful.  If you have Photoshop installed, our texture pipeline supports
any texture that Photoshop supports.  Otherwise it supports 32-bit targa files.  There
are plans to add support for other source-file types in the future.</p>
<p>The easiest way to make a Unit Material is using the Asset Editor.  Open up the Asset
Editor (ensuring that the project you have selected in the upper right-hand corner is
your mod project).  Go to File -&gt; New, and select &quot;Material&quot; from the list of options.
When the new material opens, first select a name for the material, and then change its
class to &quot;Unit&quot;.</p>
<p>If the name of the material matches the name of the material/triangle group in the
geometry source file, when the geometry is assigned to the asset, its material will
automatically be bound.  Otherwise, you need to assign the material yourself
(explained below).</p>
<p>After changing the class of the material, you should see the Cook Parameters window
populate with various options.  In the Cook Parameters window, press &quot;Add New&quot;.
Select the source files that you will be using for the individual textures in the File
Browser.  Once these are selected, press &quot;Open&quot;.</p>
<p>This will bring up an assignment window.  In this window, you can assign each texture
to its corresponding slot.  Slots that are marked yellow indicate that an automatic
assignment could not be made.  Once all of the source files you want to import have
been assigned to a slot, press the &quot;OK&quot; button.  This will import the textures into
your pantry and then assign them to the appropriate slots in the material.  Once
this is done, press the &quot;Save&quot; button.  All of the textures that have been imported
have already been saved.</p>
<p>Now that the material has been created, it's time to create the Asset.  Go to
File -&gt; New and select &quot;Asset&quot; from the choices.  Select a name for the Asset, and
then change its class to &quot;Unit&quot;.  After changing the class to &quot;Unit&quot;, choose the
appropriate DSG for the asset.  For attachments, this is typically the
&quot;potential_any_graph&quot; DSG.  The DSG should match the DSG of the asset that the
attachment is being attached to.  Save the Asset.</p>
<p>Now that the Asset has been saved, go to the &quot;Geometries&quot; tab and press &quot;Add New&quot;.
This will populate a window allowing you to select a geometry source file.  Click
the &quot;+ Add Source File...&quot; button.  A list of models from the source file will he
displayed.  Select the model(s) that you want add to your Asset, and then press the
&quot;OK&quot; button.  The models will be imported.  Save the Asset.  Select the newly imported
Geometry in the Geometry tab.  In the &quot;Mesh&quot; window, under materials, press &quot;Add
Existing&quot;, and select the material that you have already created.  Save the Asset.  Your
attachment asset now has been created.</p>
<p>The next step is to create (or modify) an XLP with the &quot;Unit&quot; XLP class.  Go to
File -&gt; New, and select XLP.  Change the XLP class to &quot;Unit&quot;.  Choose a package name
(it can be anything, though we try to make use of the xlp name is package name
paradigm).  Save the XLP.  Add the asset that you created above to the XLP.</p>
<p>The next step is to modify the *.Art.xml file that you have created for this mod project
to ensure that it contains the &quot;Units&quot; consumer and the &quot;Unit&quot; library.  Open up the
Project Builder tool.  Go to File -&gt; Open, and select the *.Art.xml file that you have
created for this project.  If &quot;Units&quot; doesn't appear in the &quot;Art Consumers&quot; window,
select it from the drop down below the Add and Remove buttons.  If this drop down doesn't
appear, ensure that your mod depends on the Civ6 art project.</p>
<p>Now, go to Libraries.  If there is not a &quot;Unit&quot; library under the Libraries section, add
it now (again, using the drop down next to the Add/Remove buttons).  Then, select the Unit
library, and in the &quot;Packages&quot; section, press the Add button.  Browse to the XLP that you
created, and press &quot;Open&quot;.  The package name that you chose will appear in the Packages list.</p>
<p>After saving the *.Art.xml file for your project, restart the Asset Editor.</p>
<p>The next step is to create (or modify) an ArtDef with the &quot;Units&quot; template.  Go to
File -&gt; New, and select ArtDef.  Change the template to &quot;Units&quot;, and then save the file.
Additionally, open the original ArtDef that defines the units you plan on modifying
(File -&gt; Open ArtDef).  The definition for all base Civ6 units is found in the Civ6 Pantry,
with the name &quot;Units.artdef&quot;.  The definition for base Civ6 Unit Bins is found in
Unit_Bins.artdef.</p>
<p>From here, there are a few options available, depending on the scope of changes that you are
trying to make.  I will start with the simplest example of adding a weapon to an already
existing bin.  In the mod ArtDef, go to the &quot;UnitAttachmentBins&quot; root collection, and add an
element.  Once the new element has been created, change its name to match the name in the
Unit_Bins.artdef collection (for example, if you are adding a generic melee weapon, change
the attachment bin name to &quot;Weapons&quot;).  Then, click on the &quot;Groups&quot; tree node, and add a
group to the collection.  Change the name of the group to match the name of the group that
you are trying to extend (e.g. &quot;Warrior&quot;).  Click the &quot;Cultures&quot; tree node, and add an
element to it.  Change the name of the new element to the appropriate culture, or &quot;Any&quot; if
you want this new weapon to show up on units of any culture.</p>
<p>With the &quot;Assets&quot; element selected, press the &quot;Add&quot; button to create a row in the GridView.
Ensure that the new row has a unique name, and then under the &quot;Asset&quot; section, browse for
the asset entry that you created above.</p>
<p>If you want to completely replace the set of weapons that a unit uses instead of adding a
new weapon that can be randomly selected, for each entry in the original bin, create a
corresponding entry with the same name as the original entry.  For each of these entries,
select the asset that you want it to point to.  These new entries will overwrite the
original entries listed in the Unit_Bins.artdef file.</p>
<p>Another way to completely replace the set of weapons that a very specific unit uses is to
create a new, uniquely named attachment bin element, with a new, uniquely named attachment
bin group.  Then, find the UnitMemberType that you are attempting to overwrite in the
original ArtDef (e.g. &quot;Warrior&quot;).  Create a new UnitMemberType with the given name, and copy
all of the values from the original that you do not want to change (movement, combat, etc).</p>
<p>Select Cultures, and add a new culture (with the same name as the cultural variant that you
are trying to overwrite).  Select Variations, and create a new variation (with the same name
as the variation that you are trying to overwrite).  Expand the Variations to get the
&quot;Attachments&quot; node, and then create a new Attachment element.  Rename the attachment to the
type of attachment that you plan on overwriting (e.g., Armor, Body, Weapon).  Look at the
primary element, and copy the attachment point name where the asset gets assigned.  (e.g.
WeaponPrimary for Warrior -&gt; Any -&gt; BuffA -&gt; Attachments -&gt; Weapon).  Select a tint if
you desire.</p>
<p>Click on the &quot;Bins&quot; node, and press the Add button.  Set the name in the bin to the
&lt;attachment_bin_name&gt;/&lt;attachment_bin_group&gt;.  This will replace the attachment bin that
units from the given Cultural Variation will draw their attachments from.</p>
<h2>Creating New Units:</h2>
<p>I recommend reading the guide about &quot;Unit Attachment Mods&quot; prior to reading the guide
on creating new units.  The Unit Attachments Mods guide contains information on how to
create Unit assets.  This guide will provide an extension to that.</p>
<p>As mentioned in &quot;Unit Attachment Mods&quot;, Units in Civilization VI are composed together
from multiple parts.  This allows tremendous unit variation without requiring a tremendous
number of assets.  For an example of the number and variety of pieces that a unit can be
created from, open up the &quot;Units.artdef&quot; file in the Civilization VI pantry, and then expand
the &quot;UnitMemberTypes&quot; root collection.  Here you will see all of the units in the game
defined.  Look for a unit that is similar to the type of unit you want to create, select it,
and expand its tree nodes until you get to the leaves.  For this example, we are going to
look at the &quot;Warrior&quot; entry in the UnitMemberTypes.</p>
<p>When you expand the Warrior, and then Cultures node, all of the different cultural variations
of a Warrior are listed.  Each of these cultures has a distinct look for their warrior.
Within each culture is an additional variation of that culture.  For the warrior, most
cultures simply have a &quot;BuffA&quot; variation (named based on the body asset), but the Barbarian
culture also has a &quot;HeavyA&quot; variation, allowing barbarian warriors to look heavier than
warriors from other cultures.  What is common between each variation is the attachments that
they include.</p>
<p>Expand any of the variations, and its attachments collection, and a list of attachments will
be displayed.  Warriors are built using an Armor attachment, a Body attachment, a Hats
attachment, a Head attachment, a Necklaces attachment, a Skirt attachment, and a Weapon
attachment.  Each one of these attachments defines a point to which it is attached, a possible
tint (to help denote different cultures), and then a set of bins from which to draw assets from.</p>
<p>The &quot;points&quot; that are specified in the ArtDef correspond to joints on the root skeleton that
all body attachments come from.  All body attachments should come from one skeleton.  If you
have no desire to alternate heads, hands, etc, the entire body can be a single asset.  A unit
will be composed of one item from each attachment listed.  If you list only a single attachment,
the unit will be defined by that one attachment (for example, if you want to make a swordsman
that has his sword and shield on his primary body instead of attached using the attachment system).</p>
<p>So, in order to compose a new unit from component parts, select the granularity of the components
that you want, and then begin creating an asset for each component.  Assets should be added to a
units XLP, and the packages and ArtDefs should be added to the appropriate Library/Consumer,
as detailed above.</p>
<h2>Making your Units Move:</h2>
<p>The Civ VI Pantry contains numerous animations that can be used out of the box so long as
the unit you are animating has a matching skeleton.  If the unit you are animating does
not have a skeleton that matches our canonical skeleton, or if you want to author your own
animations anyway, the engine provides ways to import animations from Max, Maya, and FBX
file formats.</p>
<p>In order to add animations to your unit, you must ensure that your unit has a DSG assigned
to it.  The DSG that is typically used for bipeds is potential_any_graph.  Other unit types
tend to use other DSGs.  Assigning a DSG populates the &quot;Animations&quot; tab with the animation
slots that the DSG exposes.  In order to bind an animation to a slot, click on the
&quot;Animations&quot; tab, select the slot that you want to bind an animation to, and click on the
&quot;...&quot; button that becomes available.</p>
<p>If you do not have any animations in your pantry yet, you can import new animations from
the Animation tab by selecting the &quot;Add New&quot; button, selecting an appropriate source file
that has an animation (Max, Maya, or FBX file), and then selecting the animation that you
want to import.  Once the animation has been imported, it will appear in the list of
animations when you click on the &quot;...&quot; button.</p>
<p>By convention, &quot;Body&quot; or &quot;Armor&quot; assets define the animation for the whole unit (unless
the unit is mounted - in which case the armor asset defines the animation for the rider,
while the mount unit defines its own animations).  Assets that have the parts of the
skeleton that will be animation should define the animations for a combined unit.</p>
<p>Once your animations have been added to your asset, switch the tab on the bottom of the
Asset Editor to the &quot;Asset Trigger Editor&quot; tab.  Then, press the &quot;Add timelines for...&quot;
button, which will add a timeline for every bound animation.  Then, save the asset.
Timelines allow you to define particle effects, sound effects, and lights on assets that
get played at particular times of a given animation.  These triggers can be transferred
to other assets using &quot;Transfer&quot; triggers (which is how the archer sends an arrow trail
out when it fires).</p>
<p>Units can also share animations between each other through behaviors.  A behavior is an
object that defines the DSG, a set of common animations, a set of common timelines, and
a set of common attachment points that gets shared between assets.  Behaviors can also
contain other behaviors.</p>
<p>An example of a re-usable behavior is the &quot;SingleBiped_Deaths&quot; behavior.  You can load
this behavior by going to File -&gt; Open Entity, selecting the &quot;Behaviors&quot; item, and then
searching for it.  This behavior defines all of the common death animations that are
shared between bipeds.  It also defines attachment points on an arbitrary skeleton,
remapping bone names to attachment point names.  Any skeleton (geometry) that contains
bones with the names listed will automatically inherit the attachment points defined in
the behavior if the behavior is assigned to it.</p>
<p>The order of behaviors in an asset are important.  Behaviors are resolved bottom to top,
with the asset (and then the highest listed behavior) taking precedence.  If you assign
the &quot;SingleBiped_Deaths&quot; behavior to an asset, but want the &quot;DeathBone&quot; attachment point
to refer to a bone named &quot;Head&quot; instead of a bone names &quot;Pelvis&quot;, you can create an
attachment point on the asset that has SingleBiped_Deaths equipped to it with the name
&quot;DeathBone&quot;, and then assign it the characteristics that you desire.  When the asset is
cooked, the game will see the &quot;DeathBone&quot; defined by the asset, not by the behavior.</p>
</div> <!-- panel body --> 
</div> <!-- panel -->

						</div><!-- col-md-9 -->

<div class="col-md-3">
<ul class="nav firaxis-sidenav">
<li><h5>Content Creation</h5></li>
<li>
<a href="#Animation">Animation</a>
</li>
<li>
<a href="#ArtDefFiles">ArtDefFiles</a>
</li>
<li>
<a href="#BuildingsProcess">BuildingsProcess</a>
</li>
<li>
<a href="#ColorKey">ColorKey</a>
</li>
<li>
<a href="#DataDocumentation">DataDocumentation</a>
</li>
<li>
<a href="#Geometry">Geometry</a>
</li>
<li>
<a href="#IconXML">IconXML</a>
</li>
<li>
<a href="#Iteration">Iteration</a>
</li>
<li>
<a href="#MappingToGameCore">MappingToGameCore</a>
</li>
<li>
<a href="#PackagingAssets">PackagingAssets</a>
</li>
<li>
<a href="#ParticleEffects">ParticleEffects</a>
</li>
<li>
<a href="#ParticleEffectsWorkflow">ParticleEffectsWorkflow</a>
</li>
<li>
<a href="#TerrainBounceLighting">TerrainBounceLighting</a>
</li>
<li>
<a href="#TerrainOverview">TerrainOverview</a>
</li>
<li>
<a href="#Texture">Texture</a>
</li>
<li>
<a href="#TextureExportSettings">TextureExportSettings</a>
</li>
<li>
<a href="#The%20Life%20of%20a%20Leader">The Life of a Leader</a>
</li>
<li>
<a href="#TileBase">TileBase</a>
</li>
<li>
<a href="#UnitPreviewingScript">UnitPreviewingScript</a>
</li>
<li>
<a href="#World%20Builder">World Builder</a>
</li>
<li><h5>FireFX</h5></li>
<li>
<a href="#FireFX%5CEmitter%20Properties">Emitter Properties</a>
</li>
<li>
<a href="#FireFX%5CFireFX%20UI%20Backend">FireFX UI Backend</a>
</li>
<li>
<a href="#FireFX%5CUnderstanding%20FireFX%20Scripts">Understanding FireFX Scripts</a>
</li>
<li><h5>Forge UI</h5></li>
<li>
<a href="#Forge%20UI%5CDebug%20Features">Debug Features</a>
</li>
<li>
<a href="#Forge%20UI%5CLUA%20Conventions">LUA Conventions</a>
</li>
<li>
<a href="#Forge%20UI%5CLUA%20Input">LUA Input</a>
</li>
<li>
<a href="#Forge%20UI%5CLUA%20Reference">LUA Reference</a>
</li>
<li>
<a href="#Forge%20UI%5CReference%20Guide">Reference Guide</a>
</li>
<li><h5>Forge UI\Controls</h5></li>
<li>
<a href="#Forge%20UI%5CControls%5CAlphaAnim">AlphaAnim</a>
</li>
<li>
<a href="#Forge%20UI%5CControls%5CBar">Bar</a>
</li>
<li>
<a href="#Forge%20UI%5CControls%5CBox">Box</a>
</li>
<li>
<a href="#Forge%20UI%5CControls%5CBoxButton">BoxButton</a>
</li>
<li>
<a href="#Forge%20UI%5CControls%5CButton">Button</a>
</li>
<li>
<a href="#Forge%20UI%5CControls%5CCheckBox">CheckBox</a>
</li>
<li>
<a href="#Forge%20UI%5CControls%5CContainer">Container</a>
</li>
<li>
<a href="#Forge%20UI%5CControls%5CContext">Context</a>
</li>
<li>
<a href="#Forge%20UI%5CControls%5CDragPanel">DragPanel</a>
</li>
<li>
<a href="#Forge%20UI%5CControls%5CEditBox">EditBox</a>
</li>
<li>
<a href="#Forge%20UI%5CControls%5CFlipAnim">FlipAnim</a>
</li>
<li>
<a href="#Forge%20UI%5CControls%5CGrid">Grid</a>
</li>
<li>
<a href="#Forge%20UI%5CControls%5CGridButton">GridButton</a>
</li>
<li>
<a href="#Forge%20UI%5CControls%5CImage">Image</a>
</li>
<li>
<a href="#Forge%20UI%5CControls%5CInclude">Include</a>
</li>
<li>
<a href="#Forge%20UI%5CControls%5CInstance">Instance</a>
</li>
<li>
<a href="#Forge%20UI%5CControls%5CLabel">Label</a>
</li>
<li>
<a href="#Forge%20UI%5CControls%5CLine">Line</a>
</li>
<li>
<a href="#Forge%20UI%5CControls%5CLuaContext">LuaContext</a>
</li>
<li>
<a href="#Forge%20UI%5CControls%5CMakeInstance">MakeInstance</a>
</li>
<li>
<a href="#Forge%20UI%5CControls%5CMeter">Meter</a>
</li>
<li>
<a href="#Forge%20UI%5CControls%5CMovie">Movie</a>
</li>
<li>
<a href="#Forge%20UI%5CControls%5CPullDown">PullDown</a>
</li>
<li>
<a href="#Forge%20UI%5CControls%5CRadioButton">RadioButton</a>
</li>
<li>
<a href="#Forge%20UI%5CControls%5CScrollAnim">ScrollAnim</a>
</li>
<li>
<a href="#Forge%20UI%5CControls%5CScrollPanel">ScrollPanel</a>
</li>
<li>
<a href="#Forge%20UI%5CControls%5CSimplePullDown">SimplePullDown</a>
</li>
<li>
<a href="#Forge%20UI%5CControls%5CSlideAnim">SlideAnim</a>
</li>
<li>
<a href="#Forge%20UI%5CControls%5CSlider">Slider</a>
</li>
<li>
<a href="#Forge%20UI%5CControls%5CStack">Stack</a>
</li>
<li>
<a href="#Forge%20UI%5CControls%5CTabControl">TabControl</a>
</li>
<li>
<a href="#Forge%20UI%5CControls%5CTextButton">TextButton</a>
</li>
<li>
<a href="#Forge%20UI%5CControls%5CTextureBar">TextureBar</a>
</li>
<li>
<a href="#Forge%20UI%5CControls%5CToolTipType">ToolTipType</a>
</li>
<li>
<a href="#Forge%20UI%5CControls%5CTutorial">Tutorial</a>
</li>
<li><h5>Modding</h5></li>
<li>
<a href="#Modding%5C2D%20Leader%20Background%20Mods">2D Leader Background Mods</a>
</li>
<li>
<a href="#Modding%5CAdd%20and%20Update%20Consumers%20in%20Mod%20Art%20File">Add and Update Consumers in Mod Art File</a>
</li>
<li>
<a href="#Modding%5CAdd%20and%20Update%20Libraries%20in%20Mod%20Art%20File">Add and Update Libraries in Mod Art File</a>
</li>
<li>
<a href="#Modding%5CAdding%20New%20Screens">Adding New Screens</a>
</li>
<li>
<a href="#Modding%5CAdding%20or%20Modifying%20Icons">Adding or Modifying Icons</a>
</li>
<li>
<a href="#Modding%5CColorKey%20Mods">ColorKey Mods</a>
</li>
<li>
<a href="#Modding%5CCooking%20Art%20Files">Cooking Art Files</a>
</li>
<li>
<a href="#Modding%5CFireFX%20Built-In%20Functions">FireFX Built-In Functions</a>
</li>
<li>
<a href="#Modding%5CFog%20of%20War%20Overview">Fog of War Overview</a>
</li>
<li>
<a href="#Modding%5CFoW%20Hatch%20Texture%20Mods">FoW Hatch Texture Mods</a>
</li>
<li>
<a href="#Modding%5CFoW%20Parchment%20Texture%20Mods">FoW Parchment Texture Mods</a>
</li>
<li>
<a href="#Modding%5CFoW%20Sprite%20Texture%20Mods">FoW Sprite Texture Mods</a>
</li>
<li>
<a href="#Modding%5CHallofFame_Backend">HallofFame_Backend</a>
</li>
<li>
<a href="#Modding%5CHallofFame_Frontend">HallofFame_Frontend</a>
</li>
<li>
<a href="#Modding%5CHotLoading">HotLoading</a>
</li>
<li>
<a href="#Modding%5CLoadOrder">LoadOrder</a>
</li>
<li>
<a href="#Modding%5CModifying%20Existing%20Screens">Modifying Existing Screens</a>
</li>
<li>
<a href="#Modding%5CNotes%20shorthand">Notes shorthand</a>
</li>
<li>
<a href="#Modding%5CSkyBox%20Overview">SkyBox Overview</a>
</li>
<li>
<a href="#Modding%5CSkyBox%20Texture%20Mods">SkyBox Texture Mods</a>
</li>
<li>
<a href="#Modding%5CStrategicView%20Building%20Sprite%20Mods">StrategicView Building Sprite Mods</a>
</li>
<li>
<a href="#Modding%5CStrategicView%20Natural%20Wonder%20Sprite%20Mods">StrategicView Natural Wonder Sprite Mods</a>
</li>
<li>
<a href="#Modding%5CStrategicView%20Overview">StrategicView Overview</a>
</li>
<li>
<a href="#Modding%5CTexture%20System%20Mods">Texture System Mods</a>
</li>
<li>
<a href="#Modding%5CUnderstanding%20modinfo%20files">Understanding modinfo files</a>
</li>
<li>
<a href="#Modding%5CUnit%20Mods">Unit Mods</a>
</li>
</ul>
</div> <!-- col -->
<!-- BACK MATTER -->
			</div><!-- row -->
		</div>  <!-- container -->
	</body>
</html>
