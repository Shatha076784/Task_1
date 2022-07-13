# Task_1
<!DOCTYPE html>
<html lang="ar">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="initial-scale=3,maximum-scale=3,user-scalable=3">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>SpeechRecognition</title>
    <link rel="stylesheet"type="text/css"href="css/style.css">
</head>
<body>
    <h1>
    <!-- Input area -->
    <label for="Click and start talking">Click and talking Dear ...</label>

    <input type="text" name="" id="speechToText" placeholder="Speak Something" onclick="record()"></input>

    <!-- Below is the script for voice recognition and conversion to text-->
    </h1>
    <script>
        function record() {
            var recognition = new webkitSpeechRecognition();
            recognition.lang = "ar";

            recognition.onresult = function(event) {
                // console.log(event);
                document.getElementById('speechToText').value = event.results[0][0].transcript;
            }
            recognition.start();

        }

        
    </script>
    <!-- end of script -->
</body>
</html>
