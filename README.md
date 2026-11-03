# Sobel Edge Lab

A browser-only demo of grayscale conversion and Sobel edge detection. Upload a JPEG or PNG to compare the original, grayscale, horizontal edges, vertical edges, and combined edges. Download each result as a PNG.

No Python, Streamlit, dependencies, accounts, or server-side image uploads. Processing happens locally in the visitor's browser.

## Publish on GitHub Pages

1. Create a new **public** GitHub repository, for example `sobel-edge-lab`.
2. Extract this ZIP. Upload the extracted `index.html`, `README.md`, and `LICENSE` to the **top level** of the repository. Do not upload the ZIP as one file.
3. Go to **Settings → Pages → Build and deployment**. Select **Deploy from a branch**, `main`, `/(root)`, then save.
4. Once published, copy the website link under **Settings → Pages**. It is typically `https://YOUR-USERNAME.github.io/sobel-edge-lab/`. Use the website link, not the repository link, for your QR code.
5. Test the link in a private browser window and on a phone.

Use a separate repository from the Streamlit version: GitHub Pages serves `index.html` but cannot run Python `app.py`.

## Try it locally

Open `index.html` in a modern browser. No installation needed.

## How it works

The page resizes large images to a maximum side length of 1400 pixels for responsive processing and converts RGB pixels to grayscale. Standard 3×3 Sobel kernels measure horizontal and vertical brightness changes. The horizontal-edge image uses the vertical derivative; the vertical-edge image uses the horizontal derivative. The combined image uses both. Each edge result is independently scaled for display. Downloads use the processed resolution, so the downloaded original PNG may be resized.

## License

MIT; see [LICENSE](LICENSE).
