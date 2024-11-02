

    <h1>Getting Started with PDS Engine</h1>
    <p>Follow the steps below to set up and start using <b>PDS Engine</b>.</p>

    <h2>1. Installation</h2>
    <ol>
        <li>Download the <u>PDSengine.zip</u> file.</li>
        <li>Extract the contents of <u>PDSengine.zip</u> to a preferred directory on your system.</li>
    </ol>

    <h2>2. Setting Up the Local Server</h2>
    <ol start="3">
        <li>Install a simple HTTP server app on your mobile device (such as Simple HTTP Server).</li>
        <li>Upload the extracted <u>PDSengine</u> folder into the HTTP server app.</li>
        <li>Start the server within the app.</li>
        <li>Open Chrome on your device and enter <code>http://127.0.0.1:8080/</code> in the address bar to access the engine.</li>
        <li>Click on <u>Editor.html</u> to start the engine editor interface.</li>
    </ol>

    <h2>3. Designing Your Game Map</h2>
    <ol start="8">
        <li>Begin designing your game map within the editor. Refer to the tutorial for guidance on map creation and design techniques.</li>
    </ol>

    <h2>4. Creating a Simple Website</h2>
    <ol start="9">
        <li>After completing your game map, create a simple website to display it.</li>
        <li>Use the following HTML, CSS, and JavaScript template for your website:</li>
    </ol>

    <pre>
    &lt;!DOCTYPE html&gt;
    &lt;html&gt;
    &lt;head&gt;
        &lt;title&gt;Your Game Title&lt;/title&gt;
    &lt;/head&gt;
    &lt;style type="text/css"&gt;
        * {
            margin: 0;
        }
        canvas {
            border: 1px solid black;
            position: fixed;
        }
    &lt;/style&gt;
    &lt;body&gt;
        &lt;canvas id="canvas"&gt;&lt;/canvas&gt;

        &lt;script type="text/javascript"&gt;
            let canvas = document.getElementById("canvas");
            let ctx = canvas.getContext('2d');

            canvas.height = window.innerHeight;
            canvas.width = window.innerWidth;

            let camera = { x: 0, y: 0, range: { xFrom: -200, xTo: 700, yFrom: -200, yTo: 700 } };

            function animation() {
                ctx.clearRect(0, 0, canvas.width, canvas.height);
                requestAnimationFrame(animation);
            }

            animation();
        &lt;/script&gt;
    &lt;/body&gt;
    &lt;/html&gt;
    </pre>

    <p>Design the website further as per your requirements by adding more HTML, CSS, and JavaScript.</p>

    <h2>5. Downloading and Importing Your Map</h2>
    <ol start="11">
        <li>Download the map you created in the editor. This map will be saved as <code>map.js</code>.</li>
        <li>Ensure <code>map.js</code> is located in the same directory as your HTML file or update the path if it’s in a different location.</li>
        <li>In your HTML file, add the following line inside the <code>&lt;head&gt;</code> section or before your main script:</li>
    </ol>

    <pre>
    &lt;script type="text/javascript" src="./map.js"&gt;&lt;/script&gt;
    </pre>

    <p>Make sure the path to <code>map.js</code> is correct to avoid loading issues.</p>

    <h2>6. Viewing Your Game Map</h2>
    <ol start="14">
        <li>Stop the server for <u>PDSengine</u> and select the folder where your game website files are saved (including <code>map.js</code> and your main HTML file).</li>
        <li>Start the server again with this new game folder.</li>
        <li>Open Chrome and navigate to <code>http://127.0.0.1:8080/</code> to see your game with the loaded map.</li>
        <li>Your game map should now be visible, and you can start interacting with it.</li>
    </ol>
