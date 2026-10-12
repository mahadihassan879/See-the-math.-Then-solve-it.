# Dimensa (free version, no API key)

One file: `index.html`. It reads photos in your browser with Tesseract.js and solves with math.js. Nothing is sent to any AI service, and no key is needed.

## Run it in VS Code

1. Put `index.html` in a folder and open the folder in VS Code (File > Open Folder).
2. Install the "Live Server" extension (search for it in the Extensions panel, the one by Ritwick Dey).
3. Right-click `index.html` and choose **Open with Live Server**.

You need an internet connection. The page loads two libraries (math.js and Tesseract.js) from a CDN, and Tesseract downloads its English text data the first time you read a photo.

## What it can solve

- Equations with one unknown: `2x + 3 = 11`, `x^2 - 5x + 6 = 0`. Linear and quadratic equations get algebra steps. Other equations, like `sin(x) = 0.5`, get approximate answers found numerically between -20 and 20.
- Derivatives: `derivative of x^3 - 4x`, `d/dx(sin(x)*cos(x))`, `derivative of x^2 + y^2 at (1, 2) with respect to x`.
- Functions and surfaces: `y = x^2`, `z = sin(x)*cos(y)`.
- Plain arithmetic and simplifying: `2 + 3*4`, `simplify 2(x+3) - 4`.

It does not solve word problems, inequalities, systems of equations, integrals, geometry diagrams or anything that is mostly a picture.

## Reading photos

Photo reading is the weak part, so the page always shows the text it found and lets you fix it before solving.

- Printed text works well. Neat handwriting works sometimes. Messy handwriting often fails.
- Take the photo close up, in good light, with one problem filling the frame.
- Powers are the usual mistake. A written x² is often read as x2. Change it to `x^2`.
- A written x is sometimes read as a times sign. Fix it in the text box.

## Troubleshooting

- Nothing happens on Solve, or a message says the solver didn't load: you are offline, or a network blocks cdn.jsdelivr.net. Press F12 in the browser and look at the Console tab for the exact error.
- Photo reading fails when you double-click `index.html` to open it: use Live Server instead.
<img width="1105" height="1268" alt="Screenshot 2026-10-12 211112" src="https://github.com/user-attachments/assets/934eb406-bdf3-4233-af24-3b88637e2016" />
<img width="1234" height="1057" alt="Screenshot 2026-10-12 211101" src="https://github.com/user-attachments/assets/1c0fc2a3-24fc-400d-9654-c7793beef13c" />
<img width="687" height="989" alt="Screenshot 2026-10-12 211056" src="https://github.com/user-attachments/assets/096aeb4c-1494-44ae-933e-b1ff6463c1ec" />
<img width="659" height="1004" alt="Screenshot 2026-10-12 211047" src="https://github.com/user-attachments/assets/dee19955-7ca1-4477-8a09-362c6bf3e18c" />
<img width="1262" height="1059" alt="Screenshot 2026-10-12 211028" src="https://github.com/user-attachments/assets/87d6a6f7-3007-4c74-83c7-9668a75aa219" />
