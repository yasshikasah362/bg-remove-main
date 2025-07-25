Image Background Remover in the browser
A powerful React + Vite application that removes backgrounds from images directly in your browser. This app leverages machine learning models through Transformers.js to process media locally, ensuring your files never leave your device.

Features
🎯 One-click background removal for images
🎨 Custom background color and image selection
💾 Download options for both transparent and colored backgrounds
🏃‍♂️ Local processing - no server uploads needed
🔒 Privacy-focused - all processing happens in your browser
⚡ Optional WebGPU acceleration for supported browsers
Technical Implementation
The app implements a cross-browser approach to background removal with optional WebGPU acceleration:

Default Implementation (All Browsers)
Uses RMBG-1.4, a robust background removal model
Ensures consistent performance across all modern browsers
Processes images efficiently using WebAssembly
Optional WebGPU Acceleration
For browsers with WebGPU support, offers MODNet as an alternative
Can be enabled through a dropdown when WebGPU is available
Leverages GPU acceleration for potentially faster processing
Both implementations use Transformers.js to run the machine learning models directly in the browser, eliminating the need for server-side processing.

How It Works
File Selection: Upload any image file
Model Selection:
By default, uses RMBG-1.4 for maximum compatibility
If WebGPU is available, offers option to switch to MODNet
Background Removal: The selected ML model processes your media, creating an alpha mask
Customization: Choose a custom background color, image or keep transparency
Export: Download your processed media with either transparent or colored background
Getting Started
Clone the repository:
git clone https://github.com/mahanaatma1/bg-remove.git
Install dependencies:
npm install
Start the development server:
npm run dev
Browser Support
Default Experience: All modern browsers (Chrome, Firefox, Safari, Edge)
Optional WebGPU: Available in browsers with WebGPU support (Chrome Canary with WebGPU flags enabled)
Technical Stack
React + Vite for the frontend framework
Transformers.js for ML model inference
RMBG-1.4 as the default cross-browser model
Optional WebGPU acceleration with MODNet
IndexedDB (via Dexie.js) for local file management
TailwindCSS for styling
