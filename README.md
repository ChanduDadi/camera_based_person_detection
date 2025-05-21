# Multi-Camera-Based Queue Analysis in an Amusement Park

This project detects and tracks people across two video cameras using **YOLOv8** and **TorchReID** (Re-Identification). It assigns each person a consistent ID, even when they move from one camera to another.

You can find full folder in drive(some files are missing which are having more than 25mb, so you can find everything here): https://drive.google.com/drive/folders/1iEGfpo96BX2WrhPXmUShXsxxwDw2_0K_?usp=sharing

---

## Folder & File Descriptions

### Folders

- **`.ipynb_checkpoints/`**  
  → Auto-save files from Jupyter Notebook. *(Can be ignored)*

- **`logs/`**  
  → Training or runtime logs (e.g., ReID training progress).

- **`reid_dataset/`**  
  → Custom dataset used for person re-identification training.

- **`images_from_2_cameras/`**  
  → main images taken in queue from 2 cameras.

- **`video/`**  
  → Contains input videos which are having same fps:
  - `cam1_fps.mp4`
  - `cam2_fps.mp4`  
  Used as input for detection and tracking.

- **`output/`**  
  → (Optional) Directory for saving additional output data (like images or results).

---

### Important Files

- **`output_tracking.xlsx`**  
  → Logs frame-by-frame tracking data: person IDs in Cam1 and Cam2, and count of unique people.

- **`output.avi`**  
  → Final output video with visual tracking results (IDs and bounding boxes).

- **`reid_osnet.pt`**  
  → Finetuned model for person re-identification (OSNet).

- **`yolov8s.pt / yolov8n.pt`**  
  → YOLOv8 models for detecting people.  
  - `s` = small version  
  - `n` = nano version (faster, lighter)

- **`Task-2-Main_Notebook.ipynb`**  
  → Main Jupyter Notebook where detection and tracking happens.  
  Run this to perform multi-camera person tracking.

- **`Task-2-Main_Notebook.html`**  
  → Main Jupyter Notebook in html where detection and tracking happens.  
  HTML file is useful to check directly without runing notebook. 

- **`training_reid.ipynb`**  
  → Notebook used to fine-tune the ReID model using custom dataset.

---

## How It Works (Overview)

1. **YOLOv8** detects people in both video streams.
2. **TorchReID** compares features to match the same person across both cameras.
3. Each person is assigned a unique **ID**.
4. Outputs include:
   - A **video** with drawn boxes and IDs.
   - An **Excel** log of who appeared where.
   - Optional **waiting time** report.

## Team Members
1. Anagha Manikathuparambil Baby
2. Anusha Vishwanath Salimath
3. Chandu Dadi
4. Pratik Nichite
5. Tharun Kumar Korine Palli
