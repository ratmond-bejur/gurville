<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Text Transformation</title>
</head>
<body>
    <h1>Text Transformation Tool</h1>
    
    <label for="sentenceInput">Enter a sentence:</label><br>
    <input type="text" id="sentenceInput" placeholder="Enter your sentence here"><br><br>
    
    <button onclick="transformSentence()">Transform</button><br><br>
    
    <h2>Transformed Sentence:</h2>
    <p id="result"></p>

    <script>
        function transformSentence() {
            // Get the input sentence
            let sentence = document.getElementById('sentenceInput').value;
            let words = sentence.split(' ');
            let transformedWords = [];
            
            // Apply transformation to each word
            for (let i = 0; i < words.length; i++) {
                let word = words[i] + 'vir';  // Add 'vir' at the end of every word
                if (i % 2 === 1) {  // Add 'gur' to every other word
                    word = 'gur' + word;
                }
                transformedWords.push(word);
            }

            // Add 'gill' at the beginning and end of the sentence
            let result = 'gill ' + transformedWords.join(' ') + ' gill';
            
            // Display the result
            document.getElementById('result').innerText = result;
        }
    </script>
</body>
</html>
