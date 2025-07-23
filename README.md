Image Downloader and Converter

This Python script downloads images from URLs listed in an Excel file, converts them from GIF to JPG format, and saves them to a specified folder. If any images fail to download or convert, the script logs the details in a file named failed_images.log.
Requirements

    Python 3.x

    requests library

    openpyxl library

    Pillow (PIL) library

    tkinter library (usually pre-installed with Python)

You can install the required libraries using pip if not already installed:

pip install requests openpyxl pillow

Script Overview

    Excel File Input: The script reads an Excel file with two columns—SKU and image URL.

    Image Download and Conversion: The script downloads the images from the URLs, saves them as temporary GIF files, and converts them to JPG format.

    Error Logging: Any failed downloads or conversions are logged in a failed_images.log file within the specified save folder.

    File Saving: Processed images are saved in the selected folder with the SKU as the filename.

How to Use
Step 1: Run the Script

python image_downloader.py

Step 2: Select Excel File

A file dialog will appear asking you to select the Excel file that contains the SKUs and image URLs. The Excel file should have two columns:

    Column 1: SKU (Product identifier)

    Column 2: Image URL (Direct URL to the image)

Step 3: Select Folder to Save Images

A folder dialog will appear where you can select the folder to save the images. The script will save the images as .jpg files named by their corresponding SKU.
Step 4: View Output

    The images are saved in the selected folder with .jpg extension.

    A failed_images.log file will be created in the same folder, listing any SKUs that failed to download or convert, along with the error details.

Sample Output

Processed SKU: 12345
Processed SKU: 67890
Error processing SKU: 11223, URL: https://example.com/image.gif. Error: 404 Not Found

Troubleshooting

    If the script fails to process an image, check the failed_images.log for details on the error.

    Make sure that the image URLs in the Excel file are direct links to the image files and are accessible.

License

This project is licensed under the MIT License - see the LICENSE file for details.
