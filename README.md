Lab Result OCR Web Application
This is a simple web application that allows users to upload images or PDF files of lab test results and attempts to extract key information (test name, result, unit, and normal range) using client-side Optical Character Recognition (OCR) with Tesseract.js.

Features
File Upload: Easily upload image files (JPG, PNG) or PDF documents.

Image Preview: See a preview of the uploaded image.

Client-Side OCR: Utilizes Tesseract.js to perform OCR directly in the browser.

Data Parsing: Attempts to parse the raw OCR text into structured data (test name, result, unit, normal range).

Display Results: Shows the extracted lab results in a user-friendly format.

JSON Download: Allows downloading the extracted structured data as a JSON file.

Responsive Design: Optimized for various screen sizes using Tailwind CSS.

RTL Support: Designed for right-to-left languages (Persian).

How to Use
Open index.html: Simply open the index.html file in your web browser.

Upload File:

Click on the "برای آپلود کلیک کنید یا فایل را اینجا بکشید و رها کنید." (Click to upload or drag and drop your file here) area.

Select an image (JPG, PNG) or a PDF file of a lab test result.

Alternatively, drag and drop your file directly onto the upload area.

Process Image: Once the file is uploaded, a "پردازش تصویر" (Process Image) button will appear. Click this button to start the OCR process.

View Results: After the OCR is complete, the extracted results will be displayed on the page.

Download Data: Click the "دانلود JSON" (Download JSON) button to save the extracted data as a JSON file.

Technical Details
Frontend: HTML, CSS (Tailwind CSS), JavaScript

OCR Library: Tesseract.js (Client-side OCR engine)

Languages Supported for OCR: English (eng) and Farsi/Persian (fas)

Limitations and Future Improvements
OCR Accuracy: Client-side OCR with Tesseract.js, especially for complex documents like lab results with varying layouts, fonts, and image quality, might not always be 100% accurate. For higher precision, a server-side OCR solution (e.g., Google Cloud Vision API, AWS Textract) combined with advanced machine learning models for data extraction would be more robust.

Parsing Logic: The parseLabResults function uses regular expressions and heuristics to extract structured data from the raw OCR text. This logic is simplified and may not correctly parse all lab result formats.

Improvement: To enhance parsing accuracy, consider implementing more sophisticated NLP techniques, training custom models for specific lab report layouts, or using a rules-based engine that can be configured for different report structures.

PDF Handling: While Tesseract.js can process PDFs, its performance is generally better with image-based PDFs (scanned documents). Text-based PDFs might require different handling or conversion to images first for optimal OCR.

Error Handling: Basic error handling is in place, but a more comprehensive system for identifying and allowing manual correction of OCR errors would greatly improve usability.

No Backend: This is a purely client-side application. For a full Micro SaaS, you would typically need a backend for user management, persistent storage, more powerful OCR processing, and potentially advanced analytics.

Privacy: Since all processing happens client-side, no data leaves the user's browser, which is a privacy benefit. However, if you plan to introduce server-side components, ensure strict data privacy and security measures (e.g., HIPAA compliance for medical data) are in place.

Development
To run this project locally, simply save the code as an .html file (e.g., index.html) and open it with your web browser. No server setup is required for the basic functionality.
