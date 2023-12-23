
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Show and Play Video or GIF on Text Match</title>
    <style>
        body {
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            height: 100vh;
            margin: 0;
        }

        #videoContainer {
            display: none;
        }

        #alternativeContentContainer {
            display: none;
        }
    </style>
    <link href="https://cdn.jsdelivr.net/npm/daisyui@4.4.20/dist/full.min.css" rel="stylesheet" type="text/css" />
    <script src="https://cdn.tailwindcss.com"></script>
</head>
<body>

    <div class="flex flex-col h-screen justify-center items-center">
        <label for="textInput">Enter text:</label>
        <input type="text" id="textInput" placeholder="Type specific text">
        <button onclick="checkAndDisplayContent()" class="btn btn-primary">thala for reason </button>
    </div>

    <div id="videoContainer">
        <video id="myVideo" width="640" height="360" controls>
            <!-- Replace 'YOUR_VIDEO_SOURCE' with the actual video source URL -->
            <source src="3b37a044.mp4" type="video/mp4">
            Your browser does not support the video tag.
        </video>
    </div>

    <div id="alternativeContentContainer">
        <!-- Replace 'ALTERNATIVE_GIF_SOURCE' with the actual alternative GIF source URL -->
        <img id="alternativeGif" src="sad-kid.gif" alt="Alternative GIF">
        <audio id="alternativeAudio">
            <!-- Replace 'ALTERNATIVE_AUDIO_SOURCE' with the actual alternative audio source URL -->
            <source src="moye-moye.mp3" type="audio/mp3">
    </div>

    <script>
        var videoContainer = document.getElementById("videoContainer");
        var video = document.getElementById("myVideo");

        var alternativeContentContainer = document.getElementById("alternativeContentContainer");
        var alternativeGif = document.getElementById("alternativeGif");
        var alternativeAudio = document.getElementById("alternativeAudio");
        function checkAndDisplayContent() {
            var inputText = document.getElementById("textInput").value.toLowerCase();

            // Replace 'YOUR_TEXT_CONDITION' with the desired text condition
            if (inputText === '7') {
                // Display the video container
                videoContainer.style.display = "block";
                alternativeContentContainer.style.display = "none";

                // Play the video
                video.muted = false;
                video.play();
            } else {
                // Display the alternative content container (GIF)
                videoContainer.style.display = "none";
                alternativeContentContainer.style.display = "block";

                // Display the alternative GIF
                alternativeGif.style.display = "block";
                 // Play the alternative audio
                 alternativeAudio.play();
            }
        }
    </script>

</body>
</html>
