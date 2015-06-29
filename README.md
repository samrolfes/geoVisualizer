# geoVisualizer
vertex animation from sound frequencies

Here's what we're using for the main inspiration:
http://srchea.com/experimenting-with-web-audio-api-three-js-webgl
and http://learningthreejs.com/blog/2014/05/07/funky-deformation-for-the-geometry-of-your-three-dot-js-game-with-threex-dot-vertexanimation/


We first need to be able to get values from different frequencies of an .mp3 (bass, mid, hi) 
and then be able to pass those values to the vertex animation or vertex displacement of the meshes. 

There's a difference between vertex displacement with the shader and vertex animation I think; we've tried vertex displacement
and it was a pain in the ass that didn't work so I suggest we use vertex animation first. 

P.S-
Here's a little post-effect by my friend Nick Briz where it doesn't refresh the background when an object moves:

/* ------------------- INSTRUCTIONS -----

	to leave trails
	replace the 'renderer = new ...' on line 27
	in the setup() function, with the code below

	-------------------------------------- */
 
	renderer = new THREE.WebGLRenderer( { preserveDrawingBuffer: true } );
	renderer.autoClearColor = false;
        
        /* -------------------------------------- 
        to see this in action, move and/or spin
        your mesh, add the code below to your
        draw() function
        -------------------------------------- */
        mesh.position.x = Math.sin( Date.now() * 0.001 ) * 50;  
	mesh.rotation.z = Date.now() * 0.0005;



Which I used in this site: badbehavior.co
