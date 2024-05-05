# Video Analytics for Environmental Spatial Intelligence

Waste Management in a city is one of the most challenging tasks that needs to be overcome for sustainable progression. The issue of garbage is a global challenge with growing concerns over its intense effects on public health, environmental degradation, and sustainable development. Rapid urbanization, industrialization, and population growth have only worsened the situation, exerting increasing pressure on existing waste management facilities. Problems such as littering, illegal dumping, inadequate disposal techniques, and insufficient and inefficient dumping spaces worsen management capacities and also pollutes soil, water bodies, and the air, threatening local ecosystems and biodiversity. Furthermore, the decomposition of organic waste in landfills generates greenhouse gases that contribute to climate change. Thus, efficient waste management is critical to preserving clean and sustainable habitats. In this project, we present a smart waste monitoring system that addresses the difficulty of tracking waste accumulation in specified localities and performing timely cleaning and installation measures. The proposed framework uses a Faster RCNN network to detect and recognize garbage heaps in the locality through CCTV footage or video cameras in real-time. Data from these videos is processed by the model in real-time over several frames and used to analyze the growth of the garbage heaps. The output from the collected data can be used to indicate long-term waste accumulation. Following such analysis automatic notifications are configured to be issued, contacting the proper authorities or waste management organizations to begin cleaning operations and or install more garbage bins as required. The project work by implementing Faster RCNN is able to detect garbage heaps with reasonable accuracy and bounding box measurements which is to be repeated over the real-time processing of the footage to execute the objective task. 

## Methodology
**Data Collection:** The data required for this project is a customized dataset
that comprises of videos of garbage heaps taken from across the internet. Sites such as Story-
blocks.com, Pexels.com, Pixaby.com, iStockphoto.com, Videezy.com, and youtube.com.
We have collected data of garbage heaps on various locations like the roadside,
in buildings, open spaces, and also video data of individual throwing garbage
around.

**Data Compression:** The video data being large is compressed to a desired
aspect ratio and file size using opencv. The file size is set to 4 MB and dimen-
sions to 640x480.

**Data Augmentation and Noise Reduction:** To increase diversity and vari-
ation in data we perform data augmentation. Several techniques like flipping,
rotations, colour change, resolution change, dimension alteration, noise reduc-
tion and addition have been employed to many data points.

**Frame Extraction:** We extract keyframes from the video data for processing
and feeding to the model. The frames contain our target object, i.e. garbage heaps or dumps. We set sampling at every 25th frame for this project. Once we extract the frames they are stored separately.

**Frame Normalization:** We then normalize the data frames to enhance the
accuracy of the model. We analyze the results of normalization following the
conversion of frames to grayscale and standard color channels.

**Data Annotation:** Once we have pre-processed our video frames, we define
bounding boxes on the garbage so it can be annotated to a csv or xml file that
can be accepted by the model for detection. Bounding box definition can be
declared by open-source data annotation tools or manually declare axis points.
The annotated data shall contain bounding box axis, path to the respective
frames and the labels. For this project, we have used ‘labelImg’ to define bounding boxes over the garbage heaps.

**Data Preparation:** Import the annotated data into the environment. Parse the xml file and associate the bounding box information with the images and form a data frame. The data frame is fed into the Faster R-CNN model after splitting the data into train and test data frames. The Faster R-CNN framework has been described in the previous section.

Training Garbage Detection Model – Faster R-CNN Model:
1. Backbone CNN
2. RPN – Region Proposal Network
3. Fast R-CNN

**Periodic Analysis:** Based on the bounding boxes present following the detection, we estimate the need for garbage cans in the neighbourhood. If the size of the bounding box of detection increases over time or is persistent for a long period, we can infer that garbage management is an issue in this place. This can be done by many methods like frame differencing, or comparing the size of the bounding boxes of successive frames and fitting it over a model to analyse the growth. We alert the cleaning units or MCD of that region that this area needs to be cleaned or they need to install more garbage cans as this region is frequently littered or there is staggering amount of garbage. Take actions as necessary such as installing dustbins in the region as it is a requirement.

Waste management remains a significant concern for local authorities in many urban cities. Inadequate waste management procedures have negative consequences for human health, environmental integrity, and climate change, hence it is important that we necessitate new solutions that are efficient and take advantage of the modern digital era. Our study adds to this progression by proposing framework that can monitor trash dumping in a locality by employing a Faster RCNN network for precise identification, recognition, and temporal analysis. The technology successfully identifies garbage heaps or buildup in specific regions this is to be extended to analysing CCTV footage or video streams in real time, allowing for early intervention and resource allocation and installation for optimal waste management.  By embracing new technologies of computer vision in the form of Intelligent Video Analytics, we can potentially prevent and suppress the negative consequences of garbage accumulation, improve operational efficiency, and promote cleaner, healthier communities for future generations.

