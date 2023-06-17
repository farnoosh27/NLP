
## MLflow

```import matplotlib.pyplot as plt
import mlflow

# Load and plot the image
image_path = "path/to/image.jpg"
image = plt.imread(image_path)
plt.imshow(image)
plt.axis("off")

# Log the image as an artifact in MLflow
with mlflow.start_run():
    mlflow.log_artifact(image_path, artifact_path="images")```
