Local 3D Depth Map Generator

A client-side web application that converts 2D images into interactive 3D meshes using Monocular Depth Estimation and WebGL.

Runs entirely in the browser—no server-side compute required. Images never leave your device.

🚀 Live Demo

[Insert your GitHub Pages link here, e.g., https://www.google.com/search?q=https://yourusername.github.io/your-repo-name/]

✨ Features

100% Local Inference: Powered by Transformers.js (v3) running the depth-anything-v2-base ONNX model via WebAssembly/WebGPU.

Real-time 3D Rendering: Uses Three.js to generate a high-density PlaneGeometry dynamically displaced by the generated depth map.

Interactive Controls: Trackball globe widget for intuitive 3D rotation and an adjustable slider to scale depth (0-100cm).

Export: Download the raw generated grayscale depth map for external use (e.g., in Blender or After Effects).

🛠 Tech Stack

Frontend: HTML5, CSS, vanilla JavaScript (ES Modules)

Styling: Tailwind CSS (via CDN)

3D Engine: Three.js

Machine Learning: @huggingface/transformers (v3)

💻 Local Development

Since the application uses ES modules (<script type="module">), you cannot open the index.html file directly via the file:// protocol due to browser CORS restrictions.

You must serve it via a local HTTP server:

Using Python:

python -m http.server 8000


Using Node.js (npx):

npx serve .


Then navigate to http://localhost:8000 (or the port provided by your tool).

Note: On the first run, the browser will download the ~380MB ONNX model and cache it in IndexedDB. Subsequent loads will be nearly instant.

🌐 Deployment to GitHub Pages

This project is fully static and perfect for GitHub Pages.

Commit index.html (and this README.md) to your main branch.

Go to your repository Settings > Pages.

Under Build and deployment, select Deploy from a branch.

Select the main branch and / (root) folder, then click Save.

Your app will be live in a few minutes!

👨‍💻 Author

Serhii Lavrenov
