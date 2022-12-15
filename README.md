# yolov5-with-SE

  
　&ensp; 　&ensp; The mechanism of attention stems from the study of human vision. In cognitive science, humans selectively focus on a portion of all information while ignoring other visible information due to bottlenecks in information processing. The reason for achieving this ability is that different parts of the human retina have different information processing capabilities, that is, different parts have different acuities, and the fovea of the human retina has the highest acuity. In order to make rational use of limited visual information processing resources, humans need to select a specific part of the visual area and then focus on it. For example, when people use the computer screen to watch movies, they will focus on and deal with the vision within the scope of the computer screen, and the vision outside the computer screen, such as the keyboard, computer background, etc., will be ignored.
  
　&ensp; 　&ensp; There are many ways to introduce attention mechanisms in neural networks, taking convolutional neural networks as an example, you can increase the introduction of attention mechanisms in the spatial dimension and you can also increase the attention mechanism in the channel dimension, of course, there are also mixed dimensions, that is, adding attention mechanisms in the spatial dimension and channel dimensions at the same time.
  ![image](https://user-images.githubusercontent.com/120677884/207951728-b85f94dd-e95f-42c9-a681-5b3293f15b8d.png)　&ensp; 　&ensp; 　&ensp; 　&ensp; 　&ensp; 　&ensp; 　&ensp; 　&ensp; 　&ensp; 　&ensp; 　&ensp; 　&ensp; The structure of the SE building block
  
　&ensp; 　&ensp; Squeeze: Encodes the entire spatial feature on a channel into a global feature, and uses global average pooling to compress the two-dimensional feature (H×W) of each channel into a real number.
  
　&ensp; 　&ensp; Excitation: Dynamically generates a weight value for each feature channel. It uses two fully connected layers to form a Bottleneck structure to model the correlation between channels and outputs the same number of weight values as the input features.
  
　&ensp; 　&ensp; Scale: The normalized weights learned by the excitation are weighted to the features of each channel. 
