# Deep Learning Playground 🧪

A repository containing Jupyter Notebooks used for quick testing, running code snippets, and experimenting during my Deep Learning studies. 

## 🚀 The Workflow: GitHub + Colab + Drive

To keep the code version-controlled while utilizing cloud GPUs and storage for large datasets, this project follows a specific workflow:

### 1. Open and Run Code (Colab)
We use Colab purely as the compute engine (RAM/GPU).
1. Go to [Google Colab](https://colab.research.google.com/).
2. Select **File > Open notebook > GitHub**.
3. Paste this repository's URL and open the desired `.ipynb` file.
4. Go to **Runtime > Change runtime type** and select **T4 GPU** if you need hardware acceleration.

### 2. Manage Data (Google Drive)
**Do not** commit large datasets, model weights, or output files to GitHub. Instead, use Google Drive as a mounted "data drive". 

Run this in your notebook to access your data:
```python
from google.colab import drive
drive.mount('/content/drive')
```
Recommendation: Keep all your data organized in a specific folder on your Drive (e.g., /content/drive/MyDrive/AI_Data/).

### 3. Save Changes (GitHub)
❌ **DO NOT** select File > Save a copy in Drive. This will create a detached deep copy.

✅ **DO** select **File > Save a copy in GitHub** when you finish your session. This acts as a direct commit to this repository, saving your code and outputs cleanly.

### 💻 Local Setup (Optional)
If you prefer to test code locally (e.g., in VS Code) rather than on Colab:
```
Bash
# Create and activate a virtual environment
python -m venv .venv
.venv\Scripts\activate

# Install Jupyter and required libraries
pip install jupyterlab torch torchvision numpy pandas matplotlib
```
