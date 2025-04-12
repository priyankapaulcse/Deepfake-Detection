# Deepfake-Detection
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Purple</title>
    Multi Model Deepfake Detection Assistant</h1>
    <!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Deepfake Detection Assistant</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      background-color: #f4f6f8;
      margin: 0;
      padding: 20px;
    }

    .container {
      max-width: 800px;
      margin: auto;
      background-color: white;
      padding: 30px;
      box-shadow: 0 0 10px rgba(0,0,0,0.1);
      border-radius: 8px;
    }

    h1 {
      text-align: center;
      color: #333;
    }

    input, textarea, select {
      width: 100%;
      padding: 10px;
      margin: 15px 0;
      border: 1px solid #ccc;
      border-radius: 5px;
    }

    button {
      background-color: #007bff;
      color: white;
      padding: 12px;
      border: none;
      border-radius: 5px;
      cursor: pointer;
    }

    button:hover {
      background-color: #0056b3;
    }

    .results {
      margin-top: 20px;
      padding: 15px;
      background-color: #eef1f5;
      border-left: 5px solid #007bff;
    }
  </style>
</head>
<body>
  <div class="container">
    <h1>Multi-Modal Deepfake Detection Assistant</h1>

    <label for="mediaType">Choose Content Type:</label>
    <select id="mediaType">
      <option value="image">Image</option>
      <option value="video">Video</option>
      <option value="text">Text</option>
    </select>

    <div id="uploadSection">
      <input type="file" id="fileInput" accept="image/,video/" />
    </div>

    <div id="textSection" style="display:none;">
      <textarea id="textInput" rows="6" placeholder="Paste suspicious text here..."></textarea>
    </div>

    <button onclick="submitContent()">Analyze</button>

    <div class="results" id="resultSection" style="display:none;">
      <h3>Detection Results:</h3>
      <p id="confidenceScore">Confidence Score: --%</p>
      <p id="explanation">Explanation: --</p>
    </div>
  </div>

  <script>
    const mediaTypeSelector = document.getElementById('mediaType');
    const uploadSection = document.getElementById('uploadSection');
    const textSection = document.getElementById('textSection');

    mediaTypeSelector.addEventListener('change', () => {
      const selected = mediaTypeSelector.value;
      if (selected === 'text') {
        uploadSection.style.display = 'none';
        textSection.style.display = 'block';
      } else {
        uploadSection.style.display = 'block';
        textSection.style.display = 'none';
      }
    });


    function submitContent() {
      const mediaType = mediaTypeSelector.value;
      const resultSection = document.getElementById('resultSection');
      const confidence = document.getElementById('confidenceScore');
      const explanation = document.getElementById('explanation');

      // Placeholder for real backend logic
      resultSection.style.display = 'block';
      confidence.textContent = "Confidence Score: 87% (Mock)";
      explanation.textContent = "Explanation: Detected visual anomalies in facial texture and unnatural blinking patterns.";
    }
</head>
<body>
    
</body>
</html>
