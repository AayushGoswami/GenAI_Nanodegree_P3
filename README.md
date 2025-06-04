# AI Photo Editing with Inpainting Project

This project is part of the **BERTELSMANN next Gen Tech Booster Generative AI Nanodegree Program by Udacity**.

This project demonstrates an AI-powered photo editing tool that enables users to perform advanced image inpainting—removing or replacing backgrounds and objects in photos using state-of-the-art deep learning models. The solution combines the Segment Anything Model (SAM) for object segmentation and Stable Diffusion for inpainting, all accessible through an interactive web app.

## Table of Contents
- [Project Overview](#project-overview)
- [Features](#features)
- [Setup Instructions](#setup-instructions)
- [How It Works](#how-it-works)
- [Example Usage](#example-usage)
- [Customization](#customization)
- [License](#license)

## Project Overview
This project allows users to:
- Upload an image and select the subject to keep using point-based segmentation (SAM).
- Automatically generate a mask for the selected subject or background.
- Use a text prompt to generate a new background or inpaint selected regions with AI (Stable Diffusion).
- Preview and download the edited image.

The project is implemented in Python using Jupyter Notebook for experimentation and Gradio for the interactive web app.

## Features
- **Interactive Web App:** Upload images, select regions, and edit photos in your browser.
- **AI-Powered Inpainting:** Replace or remove backgrounds/objects using Stable Diffusion.
- **Flexible Prompts:** Guide the inpainting process with custom text prompts and negative prompts.
- **Segmentation with SAM:** Precisely select subjects or backgrounds for editing.
- **Example Gallery:** Try out preloaded examples for inspiration.

## Setup Instructions
1. **Clone the repository or download the project files.**
2. **Install dependencies:**
   ```bash
   pip install -r requirements.txt
   ```
3. **Ensure you have a compatible GPU and the necessary drivers installed.**
4. **Open `starter.ipynb` in VS Code or Jupyter Notebook.**
5. **Run the notebook cells to experiment with the models and launch the web app.**

## How It Works
- The user uploads an image and selects points on the subject to keep using the web app.
- The Segment Anything Model (SAM) generates a segmentation mask based on the selected points.
- The user provides a text prompt describing the desired background or object to inpaint.
- Stable Diffusion inpaints the masked region according to the prompt, producing a new, edited image.
- The app displays the original, mask, and inpainted images side by side for comparison.

## Example Usage
- Replace the background of a car with a Martian landscape.
- Add fantasy elements to classic artworks (e.g., dragons in the Mona Lisa).
- Remove unwanted objects from photos with natural-looking results.

Example workflow in the app:
1. Upload `car.png` and select the car.
2. Enter prompt: `a car driving on planet Mars. Studio lights, 1970s`.
3. Enter negative prompt: `artifacts, low quality, distortion`.
4. Click "Run inpaint" to generate the edited image.

## Customization
- You can modify the segmentation and inpainting pipelines in `starter.ipynb` and `app.py`.
- Adjust the prompt, negative prompt, guidance scale, and random seed for different results.
- Add your own example images to the app for experimentation.

## License
See [LICENSE](LICENSE) for details.