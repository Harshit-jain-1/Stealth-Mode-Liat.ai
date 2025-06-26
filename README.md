# Stealth-Mode-Liat.ai
#  Cross-Camera Player Mapping

##  Objective

This project matches and assigns **consistent player IDs** across two camera angles:
- `broadcast.mp4`: Main view (wide angle)
- `tacticam.mp4`: Alternate angle (low or tactical view)

Each player detected in the **tacticam** video is matched to their corresponding identity in the **broadcast** video using **visual embeddings** and **cosine similarity**.

##  How It Works

1. **YOLOv8** detects players in both videos.
2. **ResNet50** extracts a 2048-dimensional visual feature (embedding) for each player crop.
3. Players in `tacticam` are matched to those in `broadcast` by comparing embeddings using **cosine similarity**.
4. A consistent mapping of player IDs is created and saved.

## Dependencies
1. Library	Use
2. ultralytics	YOLOv8 detection
3. torch	PyTorch backend
4. torchvision	ResNet50 pretrained model
5. opencv-python	Video and image processing
6. numpy	Vector operations
7. scikit-learn	Cosine similarity computation
8. pandas	Output mapping to CSV
________________________________________
## Files Included
1. broadcast.mp4	Broadcast view of the game
2. tacticam.mp4	Tactical camera angle
3. best.pt	YOLOv8 player detection model
4. cross_camera_match.py	Full source code
5. player_id_mapping.csv	Output of player ID correspondences
6. Cross-Camera Player Mapping.pdf	Theory and explanation
7. README.md	How to run and install dependencies
________________________________________
