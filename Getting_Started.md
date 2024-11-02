# Getting Started with PDS Engine
Follow the steps below to set up and start using **PDS Engine**.

## 1. Installation
1. Download the _PDSengine.zip_ file.
2. Extract the contents of _PDSengine.zip_ to a preferred directory on your system.

## 2. Setting Up the Local Server
3. Install a simple HTTP server app on your mobile device (such as Simple HTTP Server).
4. Upload the extracted _PDSengine_ folder into the HTTP server app.
5. Start the server within the app.
6. Open Chrome on your device and enter `http://127.0.0.1:8080/` in the address bar to access the engine.
7. Click on _Editor.html_ to start the engine editor interface.

## 3. Designing Your Game Map
8. Begin designing your game map within the editor. Refer to the tutorial for guidance on map creation and design techniques.

## 4. Creating a Simple Website
9. After completing your game map, create a simple website to display it.
10. Use the following HTML, CSS, and JavaScript template for your website:

    ```html
    <!DOCTYPE html>
    <html>
    <head>
        <title>Your Game Title</title>
    </head>
    <style type="text/css">
        * {
            margin: 0;
        }
        canvas {
            border: 1px solid black;
            position: fixed;
        }
    </style>
    <body>
        <canvas id="canvas"></canvas>

        <script type="text/javascript">
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
        </script>
    </body>
    </html>
    ```

    Design the website further as per your requirements by adding more HTML, CSS, and JavaScript.

## 5. Downloading and Importing Your Map
11. Download the map you created in the editor. This map will be saved as `map.js`.
12. Ensure `map.js` is located in the same directory as your HTML file or update the path if it’s in a different location.
13. In your HTML file, add the following line inside the `<head>` section or before your main script:

    ```html
    <script type="text/javascript" src="./map.js"></script>
    ```

    Make sure the path to `map.js` is correct to avoid loading issues.
## 6. Downloading and Importing Your Map
11. Download and install `cdn.zip`, then extract its contents.
12. Connect all files in the `cdn` folder to your simple website by adding the following lines inside the `<head>` section or before your main script:

    ```html
    <script type="text/javascript" src="./cdn/Vector.js"></script>
    <script type="text/javascript" src="./cdn/circle.js"></script>
    <script type="text/javascript" src="./cdn/imgObj.js"></script>
    <script type="text/javascript" src="./cdn/rectangle.js"></script>
    <script type="text/javascript" src="./cdn/polygon.js"></script>
    <script type="text/javascript" src="./road.js"></script>
    ```
Make sure the path is correct to avoid loading issues.

## 7. Viewing Your Game Map
14. Stop the server for _PDSengine_ and select the folder where your game website files are saved (including `map.js` and your main HTML file).
15. Start the server again with this new game folder.
16. Open Chrome and navigate to `http://127.0.0.1:8080/` to see your game with the loaded map.
17. Your game map should now be visible, and you can start interacting with it.
