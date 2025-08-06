# Int.2D-3D-CNN
The Int.2D-3D-CNN integrates 2D-CNN and 3D-CNN architectures for video violence recognition. The architecture of Int.2D-3D-CNN is divided into three main components:
1. Deep feature extraction at the frame level: Each frame is processed by two pre-trained lightweight 2D-CNN models, namely MobileNetV1 and MobileNetV2, to extract rich spatial features.
2. Fusion of frame-level features: The features extracted from both CNN models are aggregated to enhance the accuracy and distinctiveness of the resulting feature representations. These aggregated features are subsequently used to construct representative frame-level features.
3. Spatio-temporal feature learning using 3D-CNN: The proposed 3D-CNN performs two primary functions. First, it refines the learning of spatial features at the individual frame level. Second, it captures temporal dependencies by analyzing patterns across consecutive frames. The 3D-CNN architecture comprises a batch normalization layer, a 3D convolution layer, a dropout layer, and a global average pooling layer.

File Detail:
1. TrainCNNModel.ipynb: for train the dataset with transfer learning before extracted deep feature by using MobileNetV1 and MobileNetV2.
2. FeatureExtraction.ipynb: for extract deep feature frame-by-frame using trained MobileNetV1 and MobileNetV2. Then fusion the features extracted from MobileNetV1 and MobileNetV2 with concatenate operation.
3. Train3DCNN.ipynb: for train the fused features to classify violent video dataset.
