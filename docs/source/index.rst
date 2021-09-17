Link to my non-Sphinx HTML file
===============================

To get to my standalone, non-generated HTML file,
just `click here </_static/tinker_all.html>`_ now!


.. raw:: html

    <embed>
    <blockquote class="twitter-tweet"><p lang="en" dir="ltr">Tomography visualized! (Link to full video below) <a href="https://t.co/nHwHsXuLIB">pic.twitter.com/nHwHsXuLIB</a></p>&mdash; Kolibril (@kolibril13) <a href="https://twitter.com/kolibril13/status/1430249252199018496?ref_src=twsrc%5Etfw">August 24, 2021</a></blockquote> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>
    </embed>

.. raw:: html

    <html>
    <body>

    <h2>HTML Iframes</h2>
    <p>You can use the height and width attributes to specify the size of the iframe:</p>

    <iframe src="https://kolibril13.github.io/mobject-gallery/" height="1000" width="500" title="Iframe Example"></iframe>

    </body>
    </html>

.. raw:: html

    <html lang="en">

    <head>
    <meta name="viewport" content="width=device-width, initial-scale=1">
    <style>
        .image {
            opacity: 1;
            display: inline-block;
            border: 2px solid darkcyan;
            width: 80px;
            height: auto;
            margin: 1px;
            transition: .1s ease;
            backface-visibility: hidden;
            border-radius: 8px;
        }
        .image:hover {
            opacity: 0.4;
        }


    </style>
        <title>Hello Manim</title>

    </head>

    <body>

    <div style="text-align:center">
        <h2>All manim Mobjects</h2>
        <a href="https://github.com/kolibril13/mobject-gallery">https://github.com/kolibril13/mobject-gallery</a>
        <p><a href="debugging_page.html">Debugging Page</a></p>
        <p>Click on the images below to copy the code snippet:</p>

    </div>
    <p id="info_field"> Here will come the text that you copied.</p>



    <script>
        var request = new XMLHttpRequest();
        request.open("GET", "name_snippet_pairs.json", false);
        request.send(null);
        var jsonData = JSON.parse(request.responseText);
        document.writeln(' <h1>Basic Shapes</h1>')
        for (let key of Object.keys(jsonData)) {
            document.write(`<img src='images/${key}' alt= '${jsonData[key]}' onclick='myFunction(this);' class='image'> `);
        }
        var request = new XMLHttpRequest();
        request.open("GET", "name_snippet_pairs_text.json", false);
        request.send(null);
        var jsonData = JSON.parse(request.responseText);
        document.writeln(' <h1>Text</h1>')
        for (let key of Object.keys(jsonData)) {
            document.write(`<img src='images/${key}' alt= '${jsonData[key]}' onclick='myFunction(this);' class='image'> `);
        }





        // add copy button to images
        function myFunction(imgs) {
            var name = imgs.alt;
            navigator.clipboard.writeText(name);
            document.getElementById("info_field").innerHTML = "'" + name + "'" + " is now copied to clipboard"
        }
    </script>


    </body>
    </html>