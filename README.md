# Can I detect and predict facial keypoints?
(or how to deal with images)

This is my project work for couse "Machine Lerning" at SoftUni during the September-November2022.

Here I try to demonstrate my skilles and knowledge I've lerned during the course which is analog to an upper level compared to a beginner.

## 1.General Description

My work aimes the detection and the predicttion of keypoint positions on face images. This can be used as a building block in several applications, such as:

 1. tracking faces in images and video
 2. analysing facial expressions
 3. detecting dysmorphic facial signs for medical diagnosis
 4. biometrics / face recognition

Detecing facial keypoints is a very challenging problem.  Facial features vary greatly from one individual to another, and even for a single individual, there is a large amount of variation due to 3D pose, size, position, viewing angle, and illumination conditions. Computer vision research has come a long way in addressing these difficulties, but there remain many opportunities for improvement.


## 2.Dataset Description

The data set for this work was graciously provided to [kaggle]('kaggle.com') by [Dr. Yoshua Bengio]('https://yoshuabengio.org/') of the University of Montreal and is in kaggle.com at disposal. 

There is a benchmark data set.

Each predicted keypoint is specified by an (x,y) real-valued pair in the space of pixel indices. There are 15 keypoints, which represent the following 15 elements of the face:

 - left_eye_center,
 - right_eye_center, 
 - left_eye_inner_corner, 
 - left_eye_outer_corner, 
 - right_eye_inner_corner, 
 - right_eye_outer_corner, 
 - left_eyebrow_inner_end, 
 - left_eyebrow_outer_end, 
 - right_eyebrow_inner_end,
 - right_eyebrow_outer_end,
 - nose_tip, 
 - mouth_left_corner, 
 - mouth_right_corner, 
 - mouth_center_top_lip, 
 - mouth_center_bottom_lip

Left and right here refers to the point of view of the subject.

In some examples, some of the target keypoint positions are misssing (encoded as missing entries in the csv, i.e., with nothing between two commas).

The input image is given in the last field of the data files, and consists of a list of pixels (ordered by row), as integers in (0,255). The images are $96$x$96$ pixels.

### Data files

**training.csv:** list of training 7049 images. Each row contains the (x,y) coordinates for 15 keypoints, and image data as row-ordered list of pixels.

**test.csv:** list of 1783 test images. Each row contains ImageId and image data as row-ordered list of pixels

**submissionFileFormat.csv:** list of 27124 keypoints to predict. Each row contains a RowId, ImageId, FeatureName, Location. FeatureName are "left_eye_center_x," "right_eyebrow_outer_end_y," etc. Location is what you need to predict.

## 3.Contents

### 3.1. Hypothesis 
### 3.2. Data processing
### 3.3. Modeling
### 3.4. Conclusion

## 4.References

 4.1. kaggle datesets: 'https://www.kaggle.com/competitions/facial-keypoints-detection'

 4.2. dataset autor is [Dr. Yoshua Bengio]('https://yoshuabengio.org/').
 
 4.3. https://matplotlib.org/
