# Enhancing Fencing Lunge Performance through AI and VR Analysis

## Abstract

**Background/Objective**: Fencing, a sport requiring precise movements and rapid decision-making, utilizes various techniques, with the lunge being fundamental across all weapons. The study aims to address the gap in optimizing lunge techniques to reduce injury risks and enhance performance. This research explores the use of Artificial Intelligence (AI) and Virtual Reality (VR) technologies to analyze and improve fencing lunges.

**Methods**: The methodology involved a multi-stage analysis, beginning with 2D analysis using Google Video Intelligence API for initial posture assessment. Subsequently, a more comprehensive 3D analysis was conducted using DeepMotion's AI motion capture, allowing detailed examination of body mechanics. The data was then visualized in an immersive environment using an Oculus VR application developed with Unreal Engine, enabling real-time feedback and adjustment.

**Results**: Findings indicate significant improvements in lunge technique, with a reduction in movements that could lead to knee injuries. The 3D analysis provided detailed insights into optimal body positions for power and safety. The VR application demonstrated its effectiveness in offering an interactive platform for technique refinement.

**Conclusions**: The integration of AI and VR in sports training, specifically in fencing, shows promising potential for enhancing athletic performance and reducing injury risks. This study contributes to the broader field by demonstrating the applicability of advanced technologies in sports training and opens avenues for further research in other sports techniques.

**Keywords**: Fencing Performance, Artificial Intelligence, Virtual Reality, Lunge Technique, Biomechanical Analysis, Injury Prevention, Sports Training, 3D Motion Capture, Video Intelligence API, Unreal Engine.

---

## 1. Introduction

Fencing is a sport that demands pinpoint accurate movements with quick on-the-fly decision-making. Many different skills and techniques are present in fencing but the lunge is a fundamental footwork technique employed in all three fencing weapons - foil, epee, and sabre - and is considered essential to contemporary fencing styles. It involves a forward movement with the front foot while the body is propelled forward with the back leg, forming the foundation for offensive actions and combos. Hence, improving the lunge is crucial for success in fencing.

Unfortunately, many young fencers, including myself, experience sport-related injuries, such as knee pain. One factor that can contribute to knee pain in fencing is an incorrect lunge technique. Using 2D and 3D data analysis, we are able to examine the specific positions and angles which can help fencers to adjust their lunges to prevent future injuries.

This study aimed to explore the utilization of advanced artificial intelligence (AI) and virtual reality (VR) technologies in improving fencing performance, with a particular focus on the technique of a lunge. Our journey began with a 2D machine learning model using Google Video Intelligence APIs, followed by the implementation of a more advanced 3D AI model using DeepMotion 3D Animation APIs. Lastly, the 3D animation model was imported into Unreal Engine and used to create an Oculus VR application for visualizations.

---

## 2. Analyze 2D Posture with GCP Video Intelligence API

### 2.1. Advice from my fencing coach

To commence my research, I began by capturing some video footage of my lunges. During practices and tournaments, I would video my actions to begin analyzing my lunges. Afterwards, I sent the clip to my fencing coach, an international fencer and coach Mario Jelev, who provided me with valuable feedback:

1. Nathan’s upper body needs to be lower, which means that the front leg should form an angle closer to 90-degrees.  
2. Nathan’s back leg needs to be fully extended to form a stronger push forward.  
3. Nathan’s lunge moves too much on the vertical plane while lunges are more horizontal.  
4. Nathan’s training and tournament lunges are noticeably different, likely due to nervousness and resulting in a jittery second action.

This feedback brought up a few questions that I would like to analyze using machine learning technologies:

- Are the positions of my front and back knee optimal for power, speed, and knee health?  
- Could the positions of my body be improved?  
- Did my front arm fully extend?  
- How far does my lunge travel?  
- How does a tournament lunge compare with one in practice and one from an Olympic champion?

### 2.2. Pose Detection using Person Detection Feature

The GCP Video Intelligence API offers person detection that can identify angles of knees and arms. I trimmed the video to isolate the lunge and used the API to analyze it. The results were visualized with 2D skeleton models.

### 2.3. Further Data Analysis of Position and Angle Movement

Using Python and the Law of Cosines, I computed angles for my knees, elbows, and shoulders. This allowed me to identify specific motion inefficiencies and compare them with Olympic-level fencers.

---

## 3. Analyze the 3D Posture Using DeepMotion AI Motion Capture API

DeepMotion Animate 3D enables video-to-3D animation conversion. I uploaded the same footage to generate an FBX file representing my lunge in 3D. The platform provided features such as foot locking and facial tracking, enhancing the accuracy of the motion capture.

The FBX format allowed for detailed capture of motion, which I then used to inspect biomechanics in a more comprehensive way than 2D.

---

## 4. Create Oculus Quest 2 VR App using the 3D model with Unreal Engine

Using Unreal Engine 4, I built an immersive VR application to visualize the lunge. Steps included:

1. Creating a new VR project in UE4  
2. Importing and retargeting the DeepMotion FBX animation  
3. Setting up Android and Oculus build environments  
4. Deploying the app to Oculus Quest 2 using SideQuest  

This environment allowed me to observe and correct my posture interactively in real-time.

---

## 5. Conclusion

This study gathered and analyzed movement data using 2D and 3D AI to identify and improve fencing lunge technique. VR was used to simulate and visualize performance, enabling real-time feedback. Sharing the results with fellow fencers and my coach confirmed that AI and VR tools can significantly improve lunge performance while minimizing injury risk.

---

## 6. Future Work

1. Apply this framework to other sports techniques.  
2. Expand to analyze more complex fencing movements.  
3. Develop ML models that predict lunge success from joint data.

---

## Acknowledgements

I wish to express my sincere gratitude to Coach Mario for his valuable comments on this manuscript. I deeply appreciate the time and effort from all the reviewers dedicated to reviewing my work:

- Mr. Kevin He, CEO of DeepMotion  
- Dr. Fengnian Xia, Professor of EE at Yale University  
- Mr. Mario Jelev, Coach of South Florida Fencing Club

---

## References

1. J. Kim, "Artificial Intelligence in Sports Training," AI Review, vol. 7, pp. 23–30, 2018.  
2. S. Su, Y. Zhang, and L. Wang, "A Virtual Reality System for Fencing Training," Journal of Virtual Reality, vol. 18, pp. 5–12, 2013.  
3. Google, "Video Intelligence API documentation," Google Cloud. https://cloud.google.com/video-intelligence/docs  
4. DeepMotion, "Animate 3D." https://www.deepmotion.com/animate-3d  
5. "Tutorial on Building Quest 2 VR apps with Unreal Engine (Win)," YouTube. https://www.youtube.com/watch?v=veKyDnzb7-k  
6. "Tutorial on using Deepmotion AI motion capture animation retargeting on Unreal Engine," YouTube. https://www.youtube.com/watch?v=j5wfOF1JrJA&t=0s
