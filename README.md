# 🌿 Plant Disease Detection using YOLOv11

A deep learning-based plant disease detection system trained using the **YOLOv11** object detection model. The model identifies various plant leaf diseases in crops such as **tomato and corn**.


---

##  Classes Detected

The model is trained to detect **7 plant classes**:

1. Corn rust leaf  
2. Tomato Brown Spots  
3. Tomato Bacterial Wilt  
4. Tomato Blight Leaf  
5. Tomato Healthy  
6. Tomato Leaf Mosaic Virus  
7. Tomato Leaf Yellow Virus  

---

## 🚀 How to Use

### 🖥️ 1. Clone the repo

```bash
git clone https://github.com/your-username/plant-disease-yolo.git
cd plant-disease-yolo


📦 2. Install dependencies

pip install ultralytics


🧪 3. Run inference

from ultralytics import YOLO

model = YOLO("Field-plant-2/training_results/run_finetuned_v3/weights/best.pt")
results = model("path_to_your_image.jpg", show=True)


📊 Sample Performance (from final validation)
Class	Precision	Recall	mAP50	mAP50-95
Tomato Brown Spots	0.558	0.884	0.842	0.679
Tomato Blight Leaf	0.562	0.707	0.705	0.497
Tomato Leaf Yellow Virus	1.000	0.089	0.416	0.315
Others (see logs)	...	...	...	...


📝 Speed: 0.9ms preprocessing, 28.5ms inference


📌 Notes
Training was done using YOLOv11 with yolov8l.pt as the base model.

The dataset is not included due to size — use the folder Field-plant-2/ structure for reference.

This project was part of a mini project focused on agriculture-based AI solutions.
