# Room-Layout-Estimation-in-AR-MR2024-
Course Project for ETH Zurich - Mixed Reality - Autumn Semester 2024

## 1. Environment Setup
1. Clone this repository to your local machine.
2. Ensure you have Python installed (e.g., 3.8+).
3. Create or activate a Python virtual environment (e.g., `conda` or `venv`).
4. Install dependencies with:
   ```bash
   pip install -r requirements.txt

## 2. Testing the Workflow Locally

1. Open and run **`test.ipynb`** to see the entire process demonstrated with an example dataset.
2. This notebook walks through:
   - Initializing the environment
   - Loading images and metadata
   - Estimating 2D layouts
   - Aligning depth and color images
   - Estimating 3D lines
   - Rendering results for inspection

## 3. Running on Magic Leap 2

For real-world usage on Magic Leap 2, follow these steps:

1. **Start the Monitoring Script**  
   Run **`run_monitor.bat`** to begin monitoring for new images. This script continuously checks for fresh data coming from the Magic Leap 2 device.

2. **Run the Data-Capture Script**  
   Execute **`newtxt.py`** in parallel. This script handles capturing new images from the device.

3. **Automatic Indexing**  
   Each newly captured image is automatically assigned an index in **`index.json`** located under the **`received_data`** folder, alongside:
   - The color image  
   - The depth image  
   - Associated metadata  

4. **Rendering**  
   Once the new images and metadata are received, the room layout estimation and rendering pipeline will process them for visualization.

**Enjoy exploring room layout estimation for AR/MR applications!**
