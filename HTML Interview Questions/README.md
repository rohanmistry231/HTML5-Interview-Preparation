# HTML Interview Questions for AI/ML Roles

This README provides **170 HTML interview questions** tailored for AI/ML students preparing for technical interviews, focusing on HTML’s role in web development for AI/ML applications (e.g., building dashboards, model deployment interfaces, and data visualizations). The questions are categorized into **HTML Basics**, **Semantic HTML**, **Forms and Validation**, **Multimedia**, **HTML APIs**, **Accessibility**, **Performance Optimization**, and **Integration with AI/ML**. Each category is divided into **Basic**, **Intermediate**, and **Advanced** levels, with practical code snippets to illustrate concepts. This resource supports candidates aiming for roles that combine web development with AI/ML workflows, such as creating interactive interfaces for model outputs or deploying ML models via web applications.

## HTML Basics

### Basic
1. **What is HTML, and how is it used in web development?**  
   HyperText Markup Language structures web content.  
   ```html
   <!DOCTYPE html>
   <html>
   <body>
       <h1>Hello, World!</h1>
   </body>
   </html>
   ```

2. **How do you create a basic HTML document structure?**  
   Uses `<!DOCTYPE>`, `<html>`, `<head>`, and `<body>`.  
   ```html
   <!DOCTYPE html>
   <html lang="en">
   <head>
       <meta charset="UTF-8">
       <title>My Page</title>
   </head>
   <body>
       <p>Content here</p>
   </body>
   </html>
   ```

3. **What is the purpose of the `<!DOCTYPE html>` declaration?**  
   Specifies HTML5 standard.  
   ```html
   <!DOCTYPE html>
   <html>
   <body>
       <p>HTML5 page</p>
   </body>
   </html>
   ```

4. **How do you add a comment in HTML?**  
   Uses `<!-- -->` syntax.  
   ```html
   <!-- This is a comment -->
   <p>Visible content</p>
   ```

5. **What are HTML attributes, and how are they used?**  
   Provide additional information to elements.  
   ```html
   <img src="image.jpg" alt="Description">
   ```

6. **How do you visualize HTML structure?**  
   Plots element hierarchy (mock example).  
   ```python
   import matplotlib.pyplot as plt
   def plot_html_structure():
       plt.figure(figsize=(8, 6))
       plt.plot([1, 2, 3], [3, 2, 1], 'o-', label='DOM Tree')
       plt.title('HTML Structure')
       plt.savefig('html_structure.png')
   ```

#### Intermediate
7. **Write a function to generate a dynamic HTML list.**  
   Creates a list dynamically.  
   ```html
   <ul id="dynamic-list"></ul>
   <script>
   function createList(items) {
       const ul = document.getElementById('dynamic-list');
       items.forEach(item => {
           const li = document.createElement('li');
           li.textContent = item;
           ul.appendChild(li);
       });
   }
   createList(['Item 1', 'Item 2']);
   </script>
   ```

8. **How do you link an external CSS file in HTML?**  
   Uses `<link>` tag.  
   ```html
   <head>
       <link rel="stylesheet" href="styles.css">
   </head>
   ```

9. **Write a function to validate HTML attributes.**  
   Checks attribute presence.  
   ```html
   <img id="my-image" src="image.jpg">
   <script>
   function validateAttributes(elementId, attribute) {
       const element = document.getElementById(elementId);
       return element.hasAttribute(attribute);
   }
   console.log(validateAttributes('my-image', 'alt')); // False
   </script>
   ```

10. **How do you embed JavaScript in HTML?**  
    Uses `<script>` tag.  
    ```html
    <script>
        console.log("Hello, JavaScript!");
    </script>
    ```

11. **Write a function to toggle visibility of an HTML element.**  
    Changes display style.  
    ```html
    <button onclick="toggleVisibility()">Toggle</button>
    <div id="content">Content</div>
    <script>
    function toggleVisibility() {
        const div = document.getElementById('content');
        div.style.display = div.style.display === 'none' ? 'block' : 'none';
    }
    </script>
    ```

12. **How do you create a hyperlink in HTML?**  
    Uses `<a>` tag.  
    ```html
    <a href="https://example.com">Visit Example</a>
    ```

#### Advanced
13. **Write a function to parse HTML content.**  
    Extracts element data.  
    ```html
    <div id="data">Model Output: 0.95</div>
    <script>
    function parseHTMLContent(elementId) {
        const element = document.getElementById(elementId);
        return element.innerHTML;
    }
    console.log(parseHTMLContent('data')); // Model Output: 0.95
    </script>
    ```

14. **How do you optimize HTML file size?**  
    Minifies HTML code.  
    ```html
    <!-- Before -->
    <html>
        <body>
            <p>  Content  </p>
        </body>
    </html>
    <!-- After -->
    <html><body><p>Content</p></body></html>
    ```

15. **Write a function to dynamically update HTML attributes.**  
    Modifies attributes at runtime.  
    ```html
    <img id="dynamic-img" src="old.jpg">
    <script>
    function updateAttribute(elementId, attribute, value) {
        const element = document.getElementById(elementId);
        element.setAttribute(attribute, value);
    }
    updateAttribute('dynamic-img', 'src', 'new.jpg');
    </script>
    ```

16. **How do you implement HTML5 data attributes?**  
    Uses `data-*` attributes.  
    ```html
    <div data-model-id="123">Model Data</div>
    <script>
    const div = document.querySelector('[data-model-id]');
    console.log(div.dataset.modelId); // 123
    </script>
    ```

17. **Write a function to measure HTML rendering time.**  
    Logs rendering performance.  
    ```html
    <script>
    function measureRenderTime() {
        const start = performance.now();
        document.body.innerHTML += '<p>Test</p>';
        return performance.now() - start;
    }
    console.log(measureRenderTime());
    </script>
    ```

18. **How do you handle HTML entities?**  
    Encodes special characters.  
    ```html
    <p>Copyright &copy; 2025</p>
    ```

## Semantic HTML

### Basic
19. **What is semantic HTML, and why is it important?**  
   Uses meaningful tags for structure.  
   ```html
   <header>
       <nav>
           <ul>
               <li><a href="#home">Home</a></li>
           </ul>
       </nav>
   </header>
   ```

20. **How do you use the `<article>` element?**  
   Represents independent content.  
   ```html
   <article>
       <h2>AI Model Results</h2>
       <p>Accuracy: 95%</p>
   </article>
   ```

21. **What is the purpose of the `<section>` element?**  
   Groups related content.  
   ```html
   <section>
       <h2>Data Visualization</h2>
       <canvas id="chart"></canvas>
   </section>
   ```

22. **How do you use the `<nav>` element?**  
   Defines navigation links.  
   ```html
   <nav>
       <a href="/dashboard">Dashboard</a>
   </nav>
   ```

23. **What is the `<footer>` element used for?**  
   Contains footer content.  
   ```html
   <footer>
       <p>Contact: ai@example.com</p>
   </footer>
   ```

24. **How do you visualize semantic structure?**  
   Plots semantic hierarchy.  
   ```python
   import matplotlib.pyplot as plt
   def plot_semantic_structure():
       plt.plot([1, 2, 3], [3, 2, 1], 'o-', label='Semantic DOM')
       plt.title('Semantic HTML Structure')
       plt.savefig('semantic_structure.png')
   ```

#### Intermediate
25. **Write a function to validate semantic HTML usage.**  
    Checks for semantic tags.  
    ```html
    <main>
        <article>Content</article>
    </main>
    <script>
    function validateSemantic() {
        return document.querySelectorAll('main, article, section, nav').length > 0;
    }
    console.log(validateSemantic()); // True
    </script>
    ```

26. **How do you use the `<aside>` element?**  
    Represents supplementary content.  
    ```html
    <aside>
        <h3>Model Metadata</h3>
        <p>Version: 1.0</p>
    </aside>
    ```

27. **Write a function to dynamically add semantic elements.**  
    Appends semantic tags.  
    ```html
    <main id="container"></main>
    <script>
    function addSemanticElement(tag, content) {
        const main = document.getElementById('container');
        const element = document.createElement(tag);
        element.textContent = content;
        main.appendChild(element);
    }
    addSemanticElement('section', 'New Section');
    </script>
    ```

28. **How do you use the `<figure>` and `<figcaption>` elements?**  
    Represents captioned media.  
    ```html
    <figure>
        <img src="chart.png" alt="Model Accuracy">
        <figcaption>Accuracy over epochs</figcaption>
    </figure>
    ```

29. **Write a function to extract semantic content.**  
    Retrieves content from semantic tags.  
    ```html
    <article id="model-data">Accuracy: 95%</article>
    <script>
    function getSemanticContent(selector) {
        return document.querySelector(selector).textContent;
    }
    console.log(getSemanticContent('#model-data')); // Accuracy: 95%
    </script>
    ```

30. **How do you combine semantic HTML with CSS?**  
    Styles semantic elements.  
    ```html
    <style>
        header { background: #f0f0f0; padding: 10px; }
    </style>
    <header>
        <h1>AI Dashboard</h1>
    </header>
    ```

#### Advanced
31. **Write a function to enforce semantic HTML structure.**  
    Validates required semantic tags.  
    ```html
    <main><section>Content</section></main>
    <script>
    function enforceSemantic(tags) {
        return tags.every(tag => document.querySelector(tag));
    }
    console.log(enforceSemantic(['main', 'section'])); // True
    </script>
    ```

32. **How do you optimize semantic HTML for SEO?**  
    Uses semantic tags and metadata.  
    ```html
    <head>
        <meta name="description" content="AI Model Dashboard">
    </head>
    <main>
        <h1>Model Results</h1>
        <article>Accuracy: 95%</article>
    </main>
    ```

33. **Write a function to generate a semantic dashboard.**  
    Creates a dynamic dashboard layout.  
    ```html
    <main id="dashboard"></main>
    <script>
    function createDashboard(data) {
        const main = document.getElementById('dashboard');
        const section = document.createElement('section');
        section.innerHTML = `<h2>Model: ${data.model}</h2><p>Accuracy: ${data.accuracy}</p>`;
        main.appendChild(section);
    }
    createDashboard({ model: 'BERT', accuracy: '95%' });
    </script>
    ```

34. **How do you implement microdata in semantic HTML?**  
    Adds structured data.  
    ```html
    <article itemscope itemtype="http://schema.org/AIModel">
        <h2 itemprop="name">BERT</h2>
        <p itemprop="description">Accuracy: 95%</p>
    </article>
    ```

35. **Write a function to audit semantic HTML compliance.**  
    Checks semantic best practices.  
    ```html
    <main><article>Content</article></main>
    <script>
    function auditSemantic() {
        const hasSemantic = document.querySelectorAll('main, article, section').length;
        return hasSemantic > 2 ? 'Compliant' : 'Non-compliant';
    }
    console.log(auditSemantic());
    </script>
    ```

36. **How do you integrate semantic HTML with JSON-LD?**  
    Embeds structured data.  
    ```html
    <script type="application/ld+json">
    {
        "@context": "http://schema.org",
        "@type": "AIModel",
        "name": "BERT",
        "description": "Accuracy: 95%"
    }
    </script>
    ```

## Forms and Validation

### Basic
37. **How do you create an HTML form?**  
   Uses `<form>` and input elements.  
   ```html
   <form>
       <input type="text" name="username">
       <button type="submit">Submit</button>
   </form>
   ```

38. **What is the purpose of the `action` attribute in a form?**  
   Specifies form submission URL.  
   ```html
   <form action="/submit" method="POST">
       <input type="text" name="data">
       <button type="submit">Send</button>
   </form>
   ```

39. **How do you use the `<input>` element?**  
   Captures user input.  
   ```html
   <input type="number" name="model-epoch" min="1">
   ```

40. **What is the `required` attribute in forms?**  
   Enforces input before submission.  
   ```html
   <input type="text" name="email" required>
   ```

41. **How do you create a dropdown menu?**  
   Uses `<select>` and `<option>`.  
   ```html
   <select name="model">
       <option value="bert">BERT</option>
       <option value="gpt">GPT</option>
   </select>
   ```

42. **How do you visualize form submission metrics?**  
   Plots submission counts.  
   ```python
   import matplotlib.pyplot as plt
   def plot_form_metrics(submissions):
       plt.plot(submissions, label='Submissions')
       plt.title('Form Submission Metrics')
       plt.savefig('form_metrics.png')
   ```

#### Intermediate
43. **Write a function to validate form inputs.**  
    Checks input values.  
    ```html
    <form id="model-form">
        <input type="number" name="epochs" id="epochs">
        <button type="submit">Submit</button>
    </form>
    <script>
    function validateForm() {
        const epochs = document.getElementById('epochs').value;
        return epochs > 0 ? true : alert('Invalid epochs');
    }
    document.getElementById('model-form').addEventListener('submit', validateForm);
    </script>
    ```

44. **How do you use HTML5 validation attributes?**  
    Enforces input patterns.  
    ```html
    <input type="email" name="email" pattern="[a-z0-9._%+-]+@[a-z0-9.-]+\.[a-z]{2,}$">
    ```

45. **Write a function to handle form submissions.**  
    Processes form data.  
    ```html
    <form id="data-form">
        <input type="text" name="model-name">
        <button type="submit">Submit</button>
    </form>
    <script>
    function handleSubmit(event) {
        event.preventDefault();
        const formData = new FormData(event.target);
        console.log(formData.get('model-name'));
    }
    document.getElementById('data-form').addEventListener('submit', handleSubmit);
    </script>
    ```

46. **How do you create a file upload form?**  
    Uses `<input type="file">`.  
    ```html
    <form enctype="multipart/form-data">
        <input type="file" name="model-file">
        <button type="submit">Upload</button>
    </form>
    ```

47. **Write a function to reset a form.**  
    Clears form inputs.  
    ```html
    <form id="reset-form">
        <input type="text" name="data">
        <button type="button" onclick="resetForm()">Reset</button>
    </form>
    <script>
    function resetForm() {
        document.getElementById('reset-form').reset();
    }
    </script>
    ```

48. **How do you use radio buttons in forms?**  
    Allows single selection.  
    ```html
    <input type="radio" name="model" value="bert"> BERT
    <input type="radio" name="model" value="gpt"> GPT
    ```

#### Advanced
49. **Write a function to implement custom form validation.**  
    Validates complex rules.  
    ```html
    <form id="custom-form">
        <input type="number" id="learning-rate" name="lr">
        <button type="submit">Submit</button>
    </form>
    <script>
    function customValidate() {
        const lr = document.getElementById('learning-rate').value;
        if (lr < 0.0001 || lr > 0.1) {
            alert('Learning rate out of range');
            return false;
        }
        return true;
    }
    document.getElementById('custom-form').addEventListener('submit', customValidate);
    </script>
    ```

50. **How do you integrate forms with Fetch API?**  
    Submits form data asynchronously.  
    ```html
    <form id="api-form">
        <input type="text" name="model-name">
        <button type="submit">Submit</button>
    </form>
    <script>
    document.getElementById('api-form').addEventListener('submit', async (e) => {
        e.preventDefault();
        const formData = new FormData(e.target);
        const response = await fetch('/api/submit', {
            method: 'POST',
            body: formData
        });
        console.log(await response.json());
    });
    </script>
    ```

51. **Write a function to serialize form data.**  
    Converts form to JSON.  
    ```html
    <form id="serialize-form">
        <input type="text" name="model" value="BERT">
        <button type="submit">Submit</button>
    </form>
    <script>
    function serializeForm(formId) {
        const form = document.getElementById(formId);
        const data = {};
        new FormData(form).forEach((value, key) => data[key] = value);
        return JSON.stringify(data);
    }
    document.getElementById('serialize-form').addEventListener('submit', () => console.log(serializeForm('serialize-form')));
    </script>
    ```

52. **How do you implement autocomplete in forms?**  
    Uses `datalist`.  
    ```html
    <input list="models" name="model">
    <datalist id="models">
        <option value="BERT">
        <option value="GPT">
    </datalist>
    ```

53. **Write a function to monitor form submission performance.**  
    Logs submission latency.  
    ```html
    <form id="perf-form">
        <input type="text" name="data">
        <button type="submit">Submit</button>
    </form>
    <script>
    async function monitorSubmission() {
        const start = performance.now();
        const response = await fetch('/api/submit', { method: 'POST' });
        return performance.now() - start;
    }
    document.getElementById('perf-form').addEventListener('submit', async (e) => {
        e.preventDefault();
        console.log(await monitorSubmission());
    });
    </script>
    ```

54. **How do you secure HTML forms?**  
    Uses CSRF tokens and validation.  
    ```html
    <form method="POST">
        <input type="hidden" name="csrf_token" value="token123">
        <input type="text" name="data">
        <button type="submit">Submit</button>
    </form>
    ```

## Multimedia

### Basic
55. **How do you embed an image in HTML?**  
   Uses `<img>` tag.  
   ```html
   <img src="model-output.png" alt="Model Output">
   ```

56. **How do you add a video to an HTML page?**  
   Uses `<video>` tag.  
   ```html
   <video controls>
       <source src="demo.mp4" type="video/mp4">
   </video>
   ```

57. **What is the `<audio>` element used for?**  
   Embeds audio content.  
   ```html
   <audio controls>
       <source src="podcast.mp3" type="audio/mpeg">
   </audio>
   ```

58. **How do you use the `<canvas>` element?**  
   Renders graphics dynamically.  
   ```html
   <canvas id="chart" width="200" height="200"></canvas>
   <script>
   const ctx = document.getElementById('chart').getContext('2d');
   ctx.fillRect(50, 50, 100, 100);
   </script>
   ```

59. **How do you add alternative text to media?**  
   Uses `alt` attribute.  
   ```html
   <img src="chart.png" alt="Accuracy Chart">
   ```

60. **How do you visualize multimedia rendering?**  
   Plots rendering times.  
   ```python
   import matplotlib.pyplot as plt
   def plot_multimedia_metrics(times):
       plt.plot(times, label='Render Time')
       plt.title('Multimedia Rendering')
       plt.savefig('multimedia_metrics.png')
   ```

#### Intermediate
61. **Write a function to dynamically load images.**  
    Adds images via JavaScript.  
    ```html
    <div id="image-container"></div>
    <script>
    function loadImage(src, alt) {
        const img = document.createElement('img');
        img.src = src;
        img.alt = alt;
        document.getElementById('image-container').appendChild(img);
    }
    loadImage('model.png', 'Model Output');
    </script>
    ```

62. **How do you implement responsive images?**  
    Uses `srcset` and `sizes`.  
    ```html
    <img src="small.png" srcset="large.png 1024w, small.png 640w" sizes="(max-width: 600px) 640px, 1024px" alt="Model">
    ```

63. **Write a function to control video playback.**  
    Manages video controls.  
    ```html
    <video id="demo-video" controls>
        <source src="demo.mp4" type="video/mp4">
    </video>
    <button onclick="toggleVideo()">Play/Pause</button>
    <script>
    function toggleVideo() {
        const video = document.getElementById('demo-video');
        video.paused ? video.play() : video.pause();
    }
    </script>
    ```

64. **How do you draw on a canvas for data visualization?**  
    Renders a simple chart.  
    ```html
    <canvas id="data-chart" width="300" height="200"></canvas>
    <script>
    const ctx = document.getElementById('data-chart').getContext('2d');
    ctx.beginPath();
    ctx.moveTo(0, 100);
    ctx.lineTo(300, 50);
    ctx.stroke();
    </script>
    ```

65. **Write a function to preload multimedia content.**  
    Improves loading performance.  
    ```html
    <link rel="preload" href="model.mp4" as="video">
    <script>
    function preloadMedia(src, type) {
        const link = document.createElement('link');
        link.rel = 'preload';
        link.href = src;
        link.as = type;
        document.head.appendChild(link);
    }
    preloadMedia('chart.png', 'image');
    </script>
    ```

66. **How do you embed SVG in HTML?**  
    Uses `<svg>` tag.  
    ```html
    <svg width="100" height="100">
        <circle cx="50" cy="50" r="40" fill="blue" />
    </svg>
    ```

#### Advanced
67. **Write a function to animate a canvas chart.**  
    Animates data visualization.  
    ```html
    <canvas id="anim-chart" width="300" height="200"></canvas>
    <script>
    function animateChart(data) {
        const ctx = document.getElementById('anim-chart').getContext('2d');
        let x = 0;
        function draw() {
            ctx.clearRect(0, 0, 300, 200);
            ctx.fillRect(x, 100, 10, data[x % data.length]);
            x += 5;
            if (x < 300) requestAnimationFrame(draw);
        }
        draw();
    }
    animateChart([50, 100, 75, 120]);
    </script>
    ```

68. **How do you optimize multimedia loading?**  
    Uses lazy loading.  
    ```html
    <img src="placeholder.png" data-src="model.png" loading="lazy" alt="Model">
    <script>
    document.querySelectorAll('img[loading="lazy"]').forEach(img => {
        img.src = img.dataset.src;
    });
    </script>
    ```

69. **Write a function to handle video streaming.**  
    Manages video chunks.  
    ```html
    <video id="stream-video"></video>
    <script>
    async function streamVideo(url) {
        const video = document.getElementById('stream-video');
        const response = await fetch(url);
        video.src = URL.createObjectURL(await response.blob());
        video.play();
    }
    streamVideo('/stream.mp4');
    </script>
    ```

70. **How do you implement WebGL with canvas?**  
    Renders 3D graphics.  
    ```html
    <canvas id="webgl-canvas"></canvas>
    <script>
    const canvas = document.getElementById('webgl-canvas');
    const gl = canvas.getContext('webgl');
    gl.clearColor(0, 0, 1, 1);
    gl.clear(gl.COLOR_BUFFER_BIT);
    </script>
    ```

71. **Write a function to monitor multimedia performance.**  
    Logs rendering latency.  
    ```html
    <canvas id="perf-canvas"></canvas>
    <script>
    function monitorCanvasRender() {
        const start = performance.now();
        const ctx = document.getElementById('perf-canvas').getContext('2d');
        ctx.fillRect(0, 0, 100, 100);
        return performance.now() - start;
    }
    console.log(monitorCanvasRender());
    </script>
    ```

72. **How do you integrate multimedia with AI/ML outputs?**  
    Displays model visualizations.  
    ```html
    <canvas id="ml-chart"></canvas>
    <script>
    function renderMLChart(data) {
        const ctx = document.getElementById('ml-chart').getContext('2d');
        data.forEach((val, i) => ctx.fillRect(i * 20, 200 - val, 15, val));
    }
    renderMLChart([50, 100, 75]); // Model accuracy
    </script>
    ```

## HTML APIs

### Basic
73. **What is the DOM, and how is it accessed in HTML?**  
   Document Object Model for manipulation.  
   ```html
   <p id="text">Hello</p>
   <script>
   document.getElementById('text').textContent = 'World';
   </script>
   ```

74. **How do you use the History API?**  
   Manages browser history.  
   ```html
   <button onclick="goBack()">Back</button>
   <script>
   function goBack() {
       history.back();
   }
   </script>
   ```

75. **What is the Fetch API used for?**  
   Makes HTTP requests.  
   ```html
   <script>
   fetch('https://api.example.com/data')
       .then(response => response.json())
       .then(data => console.log(data));
   </script>
   ```

76. **How do you use the Geolocation API?**  
   Retrieves user location.  
   ```html
   <button onclick="getLocation()">Get Location</button>
   <script>
   function getLocation() {
       navigator.geolocation.getCurrentPosition(pos => console.log(pos.coords));
   }
   </script>
   ```

77. **What is the purpose of the Web Storage API?**  
   Stores data locally.  
   ```html
   <script>
   localStorage.setItem('model', 'BERT');
   console.log(localStorage.getItem('model')); // BERT
   </script>
   ```

78. **How do you visualize API response times?**  
   Plots API latency.  
   ```python
   import matplotlib.pyplot as plt
   def plot_api_metrics(times):
       plt.plot(times, label='API Latency')
       plt.title('API Response Times')
       plt.savefig('api_metrics.png')
   ```

#### Intermediate
79. **Write a function to fetch AI model data.**  
    Retrieves model outputs via API.  
    ```html
    <div id="model-output"></div>
    <script>
    async function fetchModelData(url) {
        const response = await fetch(url);
        const data = await response.json();
        document.getElementById('model-output').textContent = data.accuracy;
    }
    fetchModelData('/api/model');
    </script>
    ```

80. **How do you use the WebSocket API?**  
    Enables real-time communication.  
    ```html
    <script>
    const ws = new WebSocket('ws://example.com');
    ws.onmessage = event => console.log(event.data);
    </script>
    ```

81. **Write a function to store ML metadata locally.**  
    Uses Web Storage.  
    ```html
    <script>
    function storeMetadata(metadata) {
        localStorage.setItem('ml-metadata', JSON.stringify(metadata));
    }
    storeMetadata({ model: 'BERT', accuracy: 0.95 });
    </script>
    ```

82. **How do you implement drag-and-drop with HTML5?**  
    Uses Drag and Drop API.  
    ```html
    <div draggable="true" ondragstart="drag(event)">Model</div>
    <div ondrop="drop(event)" ondragover="allowDrop(event)"></div>
    <script>
    function allowDrop(e) { e.preventDefault(); }
    function drag(e) { e.dataTransfer.setData('text', e.target.textContent); }
    function drop(e) {
        e.preventDefault();
        e.target.textContent = e.dataTransfer.getData('text');
    }
    </script>
    ```

83. **Write a function to use the Clipboard API.**  
    Copies text to clipboard.  
    ```html
    <button onclick="copyText()">Copy</button>
    <script>
    async function copyText() {
        await navigator.clipboard.writeText('Model: BERT');
        console.log('Copied!');
    }
    </script>
    ```

84. **How do you use the Notification API?**  
    Displays browser notifications.  
    ```html
    <button onclick="showNotification()">Notify</button>
    <script>
    function showNotification() {
        Notification.requestPermission().then(perm => {
            if (perm === 'granted') new Notification('Model Trained!');
        });
    }
    </script>
    ```

#### Advanced
85. **Write a function to stream ML model outputs.**  
    Uses Server-Sent Events.  
    ```html
    <div id="stream-output"></div>
    <script>
    function streamModelOutput(url) {
        const source = new EventSource(url);
        source.onmessage = event => {
            document.getElementById('stream-output').textContent = event.data;
        };
    }
    streamModelOutput('/api/stream');
    </script>
    ```

86. **How do you implement Web Workers for ML tasks?**  
    Runs tasks in background.  
    ```html
    <script>
    const worker = new Worker('ml-worker.js');
    worker.postMessage({ model: 'BERT' });
    worker.onmessage = e => console.log(e.data);
    </script>
    <!-- ml-worker.js -->
    <!-- self.onmessage = e => self.postMessage({ result: 'Processed' }); -->
    ```

87. **Write a function to use the Intersection Observer API.**  
    Detects element visibility.  
    ```html
    <div id="model-section">Model Data</div>
    <script>
    function observeElement(elementId) {
        const element = document.getElementById(elementId);
        const observer = new IntersectionObserver(entries => {
            if (entries[0].isIntersecting) console.log('Visible');
        });
        observer.observe(element);
    }
    observeElement('model-section');
    </script>
    ```

88. **How do you integrate the WebRTC API for video?**  
    Enables real-time video.  
    ```html
    <video id="local-video" autoplay></video>
    <script>
    async function startVideo() {
        const stream = await navigator.mediaDevices.getUserMedia({ video: true });
        document.getElementById('local-video').srcObject = stream;
    }
    startVideo();
    </script>
    ```

89. **Write a function to monitor API performance.**  
    Logs API call metrics.  
    ```html
    <script>
    async function monitorAPICall(url) {
        const start = performance.now();
        await fetch(url);
        return performance.now() - start;
    }
    monitorAPICall('/api/model').then(time => console.log(time));
    </script>
    ```

90. **How do you implement the Service Worker API?**  
    Enables offline functionality.  
    ```html
    <script>
    if ('serviceWorker' in navigator) {
        navigator.serviceWorker.register('/sw.js');
    }
    </script>
    <!-- sw.js -->
    <!-- self.addEventListener('fetch', e => e.respondWith(fetch(e.request))); -->
    ```

## Accessibility

### Basic
91. **What is web accessibility in HTML?**  
   Ensures content is usable by all.  
   ```html
   <img src="model.png" alt="Model Accuracy Chart">
   ```

92. **How do you use ARIA attributes?**  
   Enhances accessibility.  
   ```html
   <button aria-label="Run Model">Run</button>
   ```

93. **What is the purpose of the `alt` attribute?**  
   Provides image descriptions.  
   ```html
   <img src="chart.png" alt="Accuracy over epochs">
   ```

94. **How do you create accessible links?**  
   Uses descriptive text.  
   ```html
   <a href="/dashboard" aria-label="View AI Dashboard">Dashboard</a>
   ```

95. **What is the `role` attribute in ARIA?**  
   Defines element purpose.  
   ```html
   <div role="alert">Model training complete!</div>
   ```

96. **How do you visualize accessibility metrics?**  
   Plots accessibility scores.  
   ```python
   import matplotlib.pyplot as plt
   def plot_accessibility_metrics(scores):
       plt.plot(scores, label='Accessibility Score')
       plt.title('Accessibility Metrics')
       plt.savefig('accessibility_metrics.png')
   ```

#### Intermediate
97. **Write a function to check for alt attributes.**  
    Validates image accessibility.  
    ```html
    <img src="model.png" id="model-img">
    <script>
    function checkAltAttributes() {
        const images = document.querySelectorAll('img');
        return Array.from(images).every(img => img.hasAttribute('alt'));
    }
    console.log(checkAltAttributes()); // False
    </script>
    ```

98. **How do you make forms accessible?**  
    Uses `<label>` and ARIA.  
    ```html
    <form>
        <label for="model-name">Model Name</label>
        <input id="model-name" type="text" aria-required="true">
    </form>
    ```

99. **Write a function to add ARIA landmarks.**  
    Enhances navigation.  
    ```html
    <div id="main-content"></div>
    <script>
    function addAriaLandmark(elementId, role) {
        const element = document.getElementById(elementId);
        element.setAttribute('role', role);
    }
    addAriaLandmark('main-content', 'main');
    </script>
    ```

100. **How do you ensure keyboard navigation?**  
     Uses `tabindex`.  
     ```html
     <button tabindex="0">Run Model</button>
     ```

101. **Write a function to test focus management.**  
     Checks focusable elements.  
     ```html
     <button id="focus-btn">Click</button>
     <script>
     function testFocus() {
         const btn = document.getElementById('focus-btn');
         btn.focus();
         return document.activeElement === btn;
     }
     console.log(testFocus()); // True
     </script>
     ```

102. **How do you make multimedia accessible?**  
     Adds captions and descriptions.  
     ```html
     <video controls>
         <source src="demo.mp4" type="video/mp4">
         <track src="captions.vtt" kind="captions" srclang="en" label="English">
     </video>
     ```

#### Advanced
103. **Write a function to audit accessibility compliance.**  
     Checks ARIA and alt attributes.  
     ```html
     <img src="model.png" alt="Model">
     <script>
     function auditAccessibility() {
         const images = document.querySelectorAll('img');
         const aria = document.querySelectorAll('[role]');
         return images.length > 0 && aria.length > 0 ? 'Compliant' : 'Non-compliant';
     }
     console.log(auditAccessibility());
     </script>
     ```

104. **How do you implement dynamic ARIA states?**  
     Updates ARIA attributes.  
     ```html
     <button id="toggle-btn" aria-expanded="false">Toggle</button>
     <script>
     function updateAriaState() {
         const btn = document.getElementById('toggle-btn');
         btn.setAttribute('aria-expanded', btn.getAttribute('aria-expanded') === 'false' ? 'true' : 'false');
     }
     document.getElementById('toggle-btn').addEventListener('click', updateAriaState);
     </script>
     ```

105. **Write a function to enhance screen reader support.**  
     Adds ARIA live regions.  
     ```html
     <div id="live-region" aria-live="polite"></div>
     <script>
     function updateLiveRegion(message) {
         document.getElementById('live-region').textContent = message;
     }
     updateLiveRegion('Model training complete');
     </script>
     ```

106. **How do you test accessibility with automated tools?**  
     Simulates tool output (mock).  
     ```html
     <script>
     function simulateA11yTest() {
         const issues = document.querySelectorAll('img:not([alt])').length;
         return issues === 0 ? 'Pass' : 'Fail';
     }
     console.log(simulateA11yTest());
     </script>
     ```

107. **Write a function to manage focus for modals.**  
     Traps focus in modal.  
     ```html
     <div id="modal" role="dialog" aria-hidden="true">
         <button id="close-btn">Close</button>
     </div>
     <script>
     function trapFocus(modalId) {
         const modal = document.getElementById(modalId);
         const focusable = modal.querySelectorAll('button');
         focusable[0].focus();
     }
     trapFocus('modal');
     </script>
     ```

108. **How do you ensure color contrast for accessibility?**  
     Uses high-contrast colors.  
     ```html
     <style>
         .high-contrast { background: #000; color: #fff; }
     </style>
     <div class="high-contrast">Model Results</div>
     ```

## Performance Optimization

### Basic
109. **How do you optimize HTML loading?**  
     Minifies HTML and uses async.  
     ```html
     <script async src="script.js"></script>
     ```

110. **What is lazy loading in HTML?**  
     Delays loading of non-critical resources.  
     ```html
     <img src="placeholder.png" loading="lazy" alt="Model">
     ```

111. **How do you reduce HTTP requests in HTML?**  
     Combines resources.  
     ```html
     <link rel="stylesheet" href="combined.css">
     ```

112. **What is the purpose of the `defer` attribute?**  
     Defers script execution.  
     ```html
     <script defer src="script.js"></script>
     ```

113. **How do you preload critical resources?**  
     Uses `<link rel="preload">`.  
     ```html
     <link rel="preload" href="model.css" as="style">
     ```

114. **How do you visualize performance metrics?**  
     Plots page load times.  
     ```python
     import matplotlib.pyplot as plt
     def plot_performance_metrics(times):
         plt.plot(times, label='Load Time')
         plt.title('Page Performance')
         plt.savefig('performance_metrics.png')
     ```

#### Intermediate
115. **Write a function to lazy load images.**  
     Loads images on scroll.  
     ```html
     <img data-src="model.png" class="lazy" alt="Model">
     <script>
     function lazyLoadImages() {
         document.querySelectorAll('.lazy').forEach(img => {
             if (img.getBoundingClientRect().top < window.innerHeight) {
                 img.src = img.dataset.src;
             }
         });
     }
     window.addEventListener('scroll', lazyLoadImages);
     </script>
     ```

116. **How do you optimize CSS delivery?**  
     Uses critical CSS.  
     ```html
     <style>
         .critical { font-size: 16px; }
     </style>
     <link rel="stylesheet" href="styles.css">
     ```

117. **Write a function to measure page load time.**  
     Logs load performance.  
     ```html
     <script>
     function measurePageLoad() {
         const loadTime = performance.timing.domContentLoadedEventEnd - performance.timing.navigationStart;
         console.log(loadTime);
     }
     window.addEventListener('load', measurePageLoad);
     </script>
     ```

118. **How do you implement browser caching?**  
     Sets cache headers (mock).  
     ```html
     <meta http-equiv="Cache-Control" content="max-age=3600">
     ```

119. **Write a function to defer non-critical scripts.**  
     Dynamically loads scripts.  
     ```html
     <script>
     function deferScript(src) {
         const script = document.createElement('script');
         script.src = src;
         script.defer = true;
         document.head.appendChild(script);
     }
     deferScript('non-critical.js');
     </script>
     ```

120. **How do you optimize font loading?**  
     Uses `font-display`.  
     ```html
     <style>
         @font-face {
             font-family: 'Custom';
             src: url('font.woff2') format('woff2');
             font-display: swap;
         }
     </style>
     ```

#### Advanced
121. **Write a function to implement code splitting.**  
     Loads scripts dynamically.  
     ```html
     <script>
     async function loadModule(module) {
         const { default: mod } = await import(module);
         mod.init();
     }
     loadModule('./module.js');
     </script>
     ```

122. **How do you optimize critical rendering path?**  
     Prioritizes above-the-fold content.  
     ```html
     <style>
         .hero { display: block; }
     </style>
     <div class="hero">AI Dashboard</div>
     ```

123. **Write a function to monitor resource loading.**  
     Logs resource timings.  
     ```html
     <script>
     function monitorResources() {
         const resources = performance.getEntriesByType('resource');
         return resources.map(r => ({ name: r.name, duration: r.duration }));
     }
     window.addEventListener('load', () => console.log(monitorResources()));
     </script>
     ```

124. **How do you implement progressive enhancement?**  
     Ensures core functionality.  
     ```html
     <form action="/submit">
         <input type="text" name="data">
         <button type="submit">Submit</button>
     </form>
     <script>
     document.querySelector('form').addEventListener('submit', e => {
         e.preventDefault();
         fetch('/submit', { method: 'POST' });
     });
     </script>
     ```

125. **Write a function to reduce DOM reflows.**  
     Minimizes layout changes.  
     ```html
     <div id="content"></div>
     <script>
     function optimizeDOM() {
         const fragment = document.createDocumentFragment();
         for (let i = 0; i < 100; i++) {
             const p = document.createElement('p');
             p.textContent = 'Data';
             fragment.appendChild(p);
         }
         document.getElementById('content').appendChild(fragment);
     }
     optimizeDOM();
     </script>
     ```

126. **How do you use Resource Hints?**  
     Optimizes resource fetching.  
     ```html
     <link rel="dns-prefetch" href="https://api.example.com">
     <link rel="preconnect" href="https://cdn.example.com">
     ```

## Integration with AI/ML

### Basic
127. **How do you display ML model outputs in HTML?**  
     Renders predictions in DOM.  
     ```html
     <div id="prediction">Loading...</div>
     <script>
     fetch('/api/predict').then(res => res.json()).then(data => {
         document.getElementById('prediction').textContent = data.prediction;
     });
     </script>
     ```

128. **How do you create a dashboard for ML metrics?**  
     Uses semantic HTML and canvas.  
     ```html
     <section>
         <h2>Model Metrics</h2>
         <canvas id="metrics-chart"></canvas>
     </section>
     ```

129. **What is the role of HTML in ML deployment?**  
     Provides user interface for models.  
     ```html
     <form action="/predict">
         <input type="text" name="input">
         <button type="submit">Predict</button>
     </form>
     ```

130. **How do you embed TensorFlow.js in HTML?**  
     Runs ML models in browser.  
     ```html
     <script src="https://cdn.jsdelivr.net/npm/@tensorflow/tfjs"></script>
     <script>
     tf.ready().then(() => console.log('TensorFlow.js ready'));
     </script>
     ```

131. **How do you display data visualizations in HTML?**  
     Uses `<canvas>` for charts.  
     ```html
     <canvas id="data-vis"></canvas>
     <script>
     const ctx = document.getElementById('data-vis').getContext('2d');
     ctx.fillRect(0, 0, 100, 50);
     </script>
     ```

132. **How do you visualize ML integration metrics?**  
     Plots model performance.  
     ```python
     import matplotlib.pyplot as plt
     def plot_ml_metrics(accuracies):
         plt.plot(accuracies, label='Accuracy')
         plt.title('ML Model Performance')
         plt.savefig('ml_metrics.png')
     ```

#### Intermediate
133. **Write a function to render ML predictions.**  
     Updates DOM with predictions.  
     ```html
     <div id="ml-output"></div>
     <script>
     async function renderPrediction(url) {
         const response = await fetch(url);
         const data = await response.json();
         document.getElementById('ml-output').textContent = `Prediction: ${data.result}`;
     }
     renderPrediction('/api/predict');
     </script>
     ```

134. **How do you integrate HTML with Flask for ML?**  
     Serves ML model via Flask.  
     ```html
     <form action="/predict" method="POST">
         <input type="text" name="input">
         <button type="submit">Predict</button>
     </form>
     ```

135. **Write a function to visualize ML model outputs.**  
     Renders chart with model data.  
     ```html
     <canvas id="ml-chart"></canvas>
     <script>
     function visualizeModelOutput(data) {
         const ctx = document.getElementById('ml-chart').getContext('2d');
         data.forEach((val, i) => ctx.fillRect(i * 20, 200 - val, 15, val));
     }
     visualizeModelOutput([0.5, 0.9, 0.7]);
     </script>
     ```

136. **How do you use HTML to display real-time ML results?**  
     Uses WebSocket for updates.  
     ```html
     <div id="real-time"></div>
     <script>
     const ws = new WebSocket('ws://example.com/ml');
     ws.onmessage = event => {
         document.getElementById('real-time').textContent = event.data;
     };
     </script>
     ```

137. **Write a function to load ML model in browser.**  
     Uses TensorFlow.js.  
     ```html
     <script src="https://cdn.jsdelivr.net/npm/@tensorflow/tfjs"></script>
     <script>
     async function loadModel(url) {
         const model = await tf.loadLayersModel(url);
         console.log('Model loaded');
     }
     loadModel('/model.json');
     </script>
     ```

138. **How do you create an interactive ML interface?**  
     Uses forms and canvas.  
     ```html
     <form id="ml-input">
         <input type="number" name="input">
         <button type="submit">Predict</button>
     </form>
     <canvas id="result-chart"></canvas>
     ```

#### Advanced
139. **Write a function to integrate ML with Web Workers.**  
     Runs model inference in background.  
     ```html
     <script>
     const worker = new Worker('ml-worker.js');
     worker.postMessage({ input: [1, 2, 3] });
     worker.onmessage = e => console.log(e.data.prediction);
     </script>
     <!-- ml-worker.js -->
     <!-- self.onmessage = async e => {
         const model = await tf.loadLayersModel('model.json');
         const prediction = model.predict(tf.tensor(e.data.input));
         self.postMessage({ prediction });
     }; -->
     ```

140. **How do you deploy ML models with HTML interfaces?**  
     Uses Flask and HTML.  
     ```html
     <form action="/predict" method="POST">
         <input type="file" name="image">
         <button type="submit">Classify</button>
     </form>
     ```

141. **Write a function to stream ML predictions.**  
     Uses Server-Sent Events.  
     ```html
     <div id="ml-stream"></div>
     <script>
     function streamPredictions(url) {
         const source = new EventSource(url);
         source.onmessage = event => {
             document.getElementById('ml-stream').textContent = event.data;
         };
     }
     streamPredictions('/api/predict-stream');
     </script>
     ```

142. **How do you optimize ML model rendering in HTML?**  
     Uses WebGL for fast rendering.  
     ```html
     <canvas id="ml-render"></canvas>
     <script>
     const canvas = document.getElementById('ml-render');
     const gl = canvas.getContext('webgl');
     gl.clear(gl.COLOR_BUFFER_BIT);
     </script>
     ```

143. **Write a function to monitor ML interface performance.**  
     Logs rendering metrics.  
     ```html
     <canvas id="ml-perf"></canvas>
     <script>
     function monitorMLRender(data) {
         const start = performance.now();
         const ctx = document.getElementById('ml-perf').getContext('2d');
         ctx.fillRect(0, 0, data, 100);
         return performance.now() - start;
     }
     console.log(monitorMLRender(100));
     </script>
     ```

144. **How do you secure ML model interfaces?**  
     Uses authentication and validation.  
     ```html
     <form method="POST">
         <input type="hidden" name="csrf_token" value="token123">
         <input type="text" name="input">
         <button type="submit">Predict</button>
     </form>
     ```

## Security

### Basic
145. **How do you prevent XSS in HTML?**  
     Sanitizes user input.  
     ```html
     <div id="output"></div>
     <script>
     function sanitizeInput(input) {
         return input.replace(/</g, '&lt;').replace(/>/g, '&gt;');
     }
     document.getElementById('output').textContent = sanitizeInput('<script>alert("XSS")</script>');
     </script>
     ```

146. **What is a CSRF token, and how is it used?**  
     Prevents cross-site request forgery.  
     ```html
     <form method="POST">
         <input type="hidden" name="csrf_token" value="token123">
         <button type="submit">Submit</button>
     </form>
     ```

147. **How do you secure file uploads in HTML?**  
     Validates file types.  
     ```html
     <input type="file" accept=".png,.jpg" name="upload">
     ```

148. **What is the `rel` attribute for links?**  
     Prevents phishing attacks.  
     ```html
     <a href="https://example.com" rel="noopener noreferrer">Link</a>
     ```

149. **How do you use Content Security Policy (CSP)?**  
     Restricts resource loading.  
     ```html
     <meta http-equiv="Content-Security-Policy" content="default-src 'self'">
     ```

150. **How do you visualize security metrics?**  
     Plots security incidents.  
     ```python
     import matplotlib.pyplot as plt
     def plot_security_metrics(incidents):
         plt.plot(incidents, label='Incidents')
         plt.title('Security Metrics')
         plt.savefig('security_metrics.png')
     ```

#### Intermediate
151. **Write a function to sanitize HTML inputs.**  
     Prevents injection attacks.  
     ```html
     <input id="user-input">
     <script>
     function sanitizeHTML(input) {
         const div = document.createElement('div');
         div.textContent = input;
         return div.innerHTML;
     }
     document.getElementById('user-input').addEventListener('input', e => {
         console.log(sanitizeHTML(e.target.value));
     });
     </script>
     ```

152. **How do you implement secure form submissions?**  
     Uses HTTPS and tokens.  
     ```html
     <form action="https://api.example.com/submit" method="POST">
         <input type="hidden" name="csrf_token" value="token123">
         <input type="text" name="data">
         <button type="submit">Submit</button>
     </form>
     ```

153. **Write a function to validate file uploads.**  
     Checks file extensions.  
     ```html
     <input type="file" id="file-upload">
     <script>
     function validateFile() {
         const file = document.getElementById('file-upload').files[0];
         return /\.(png|jpg)$/i.test(file.name) ? 'Valid' : 'Invalid';
     }
     document.getElementById('file-upload').addEventListener('change', () => console.log(validateFile()));
     </script>
     ```

154. **How do you prevent clickjacking?**  
     Uses X-Frame-Options.  
     ```html
     <meta http-equiv="X-Frame-Options" content="DENY">
     ```

155. **Write a function to log security events.**  
     Tracks suspicious activity.  
     ```html
     <script>
     function logSecurityEvent(event) {
         console.log(`Security event: ${event}`);
         // Send to server
     }
     window.addEventListener('error', () => logSecurityEvent('Script error'));
     </script>
     ```

156. **How do you secure API calls from HTML?**  
     Uses authentication tokens.  
     ```html
     <script>
     fetch('/api/secure', {
         headers: { 'Authorization': 'Bearer token123' }
     }).then(res => res.json()).then(data => console.log(data));
     </script>
     ```

#### Advanced
157. **Write a function to implement input validation.**  
     Prevents malicious inputs.  
     ```html
     <input id="secure-input">
     <script>
     function validateInput(input) {
         const regex = /^[a-zA-Z0-9\s]*$/;
         return regex.test(input) ? input : '';
     }
     document.getElementById('secure-input').addEventListener('input', e => {
         e.target.value = validateInput(e.target.value);
     });
     </script>
     ```

158. **How do you implement secure session management?**  
     Uses secure cookies.  
     ```html
     <meta http-equiv="Set-Cookie" content="session=abc123; HttpOnly; Secure">
     ```

159. **Write a function to monitor XSS attempts.**  
     Logs suspicious inputs.  
     ```html
     <input id="xss-input">
     <script>
     function monitorXSS(input) {
         if (/[<>\"\';]/.test(input)) {
             console.log('Potential XSS detected');
         }
     }
     document.getElementById('xss-input').addEventListener('input', e => monitorXSS(e.target.value));
     </script>
     ```

160. **How do you secure WebSocket connections?**  
     Uses wss:// protocol.  
     ```html
     <script>
     const ws = new WebSocket('wss://example.com');
     ws.onmessage = event => console.log(event.data);
     </script>
     ```

161. **Write a function to enforce CSP dynamically.**  
     Applies security policies.  
     ```html
     <script>
     function setCSP(policy) {
         const meta = document.createElement('meta');
         meta.httpEquiv = 'Content-Security-Policy';
         meta.content = policy;
         document.head.appendChild(meta);
     }
     setCSP("default-src 'self'");
     </script>
     ```

162. **How do you integrate OAuth2 in HTML interfaces?**  
     Uses redirect for authentication.  
     ```html
     <a href="https://example.com/oauth2/authorize">Login with OAuth2</a>
     ```

## Testing and Validation

### Basic
163. **How do you test HTML structure?**  
     Validates DOM elements.  
     ```html
     <div id="test">Content</div>
     <script>
     function testStructure() {
         return document.getElementById('test') ? 'Valid' : 'Invalid';
     }
     console.log(testStructure());
     </script>
     ```

164. **How do you validate HTML code?**  
     Uses W3C validator (mock).  
     ```html
     <!DOCTYPE html>
     <html lang="en">
     <body>
         <p>Valid HTML</p>
     </body>
     </html>
     ```

165. **How do you test form functionality?**  
     Simulates form submission.  
     ```html
     <form id="test-form">
         <input type="text" name="data">
         <button type="submit">Submit</button>
     </form>
     <script>
     function testForm() {
         const form = document.getElementById('test-form');
         return form.checkValidity() ? 'Valid' : 'Invalid';
     }
     console.log(testForm());
     </script>
     ```

166. **How do you test multimedia rendering?**  
     Checks media load.  
     ```html
     <img id="test-img" src="model.png">
     <script>
     function testMedia() {
         const img = document.getElementById('test-img');
         return img.complete ? 'Loaded' : 'Not loaded';
     }
     console.log(testMedia());
     </script>
     ```

167. **How do you mock API responses for testing?**  
     Simulates API data.  
     ```html
     <script>
     function mockAPI() {
         return Promise.resolve({ data: 'Mocked response' });
     }
     mockAPI().then(res => console.log(res));
     </script>
     ```

168. **How do you visualize test results?**  
     Plots test pass rates.  
     ```python
     import matplotlib.pyplot as plt
     def plot_test_results(passes):
         plt.plot(passes, label='Pass Rate')
         plt.title('Test Results')
         plt.savefig('test_results.png')
     ```

#### Intermediate
169. **Write a function to test DOM manipulation.**  
     Verifies element changes.  
     ```html
     <div id="dynamic">Initial</div>
     <script>
     function testDOM() {
         const div = document.getElementById('dynamic');
         div.textContent = 'Updated';
         return div.textContent === 'Updated';
     }
     console.log(testDOM());
     </script>
     ```

170. **How do you test accessibility compliance?**  
     Checks ARIA and alt attributes.  
     ```html
     <img src="model.png" alt="Model">
     <script>
     function testAccessibility() {
         const images = document.querySelectorAll('img');
         return Array.from(images).every(img => img.hasAttribute('alt'));
     }
     console.log(testAccessibility());
     </script>
     ```