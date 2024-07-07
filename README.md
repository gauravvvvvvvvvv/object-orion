# Object Orion v1.0

Object Orion is a machine learning model for real-time object detection, trained on the Pascal VOC dataset. Named after the constellation Orion, it is designed to identify 20 classes of objects efficiently, with the flexibility to expand to more classes in future versions.

## Key Features

- **Real-time Detection**: Perform object detection in real-time.
- **Pascal VOC Dataset**: Trained on the Pascal VOC dataset for reliable performance.
- **20 Object Classes**: Capable of identifying a variety of objects, from common to specific categories.
- **Easy Integration**: Simple integration into existing applications and projects.

## Getting Started

### Creating Predictions with Object Orion 

To use Object Orion for object detection in your own applications, follow these steps to create a function for making predictions:

1. **Initialize Object Orion**:
   - Load your ONNX model and YAML file containing class labels and metadata.

2. **Preprocess the Input Image**:
   - Resize the input image to a suitable size for your model (e.g., square image).

3. **Prepare Input for Inference**:
   - Convert the preprocessed image into a format compatible with your model (e.g., using `cv2.dnn.blobFromImage()`).

4. **Perform Inference**:
   - Set the input to your model using `model.setInput()` and obtain predictions with `model.forward()`.

5. **Process Predictions**:
   - Extract relevant information from the model's output, such as bounding boxes, confidence scores, and class IDs.

6. **Filter and Visualize Results**:
   - Apply thresholds (e.g., confidence score) and Non-Maximum Suppression (NMS) to filter detections.
   - Draw bounding boxes and labels on the image based on the filtered predictions.

7. **Return Results**:
   - Optionally, return the annotated image and the list of detected class names for further processing.

---
