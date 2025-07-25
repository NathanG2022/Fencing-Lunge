# Fencing-Lunge

Abstract 

Background/Objective: Fencing, a sport requiring precise movements and rapid decision-making, utilizes various techniques, with the lunge being fundamental across all weapons. The study aims to address the gap in optimizing lunge techniques to reduce injury risks and enhance performance. This research explores the use of Artificial Intelligence (AI) and Virtual Reality (VR) technologies to analyze and improve fencing lunges. 

Methods: The methodology involved a multi-stage analysis, beginning with 2D analysis using Google Video Intelligence API for initial posture assessment. Subsequently, a more comprehensive 3D analysis was conducted using DeepMotion's AI motion capture, allowing detailed examination of body mechanics. The data was then visualized in an immersive environment using an Oculus VR application developed with Unreal Engine, enabling real-time feedback and adjustment. 

Results: Findings indicate significant improvements in lunge technique, with a reduction in movements that could lead to knee injuries. The 3D analysis provided detailed insights into optimal body positions for power and safety. The VR application demonstrated its effectiveness in offering an interactive platform for technique refinement. 

Conclusions: The integration of AI and VR in sports training, specifically in fencing, shows promising potential for enhancing athletic performance and reducing injury risks. This study contributes to the broader field by demonstrating the applicability of advanced technologies in sports training and opens avenues for further research in other sports techniques. 

Keywords: Fencing Performance, Artificial Intelligence, Virtual Reality, Lunge Technique, Biomechanical Analysis, Injury Prevention, Sports Training, 3D Motion Capture, Video Intelligence API, Unreal Engine. 

Introduction 

Fencing is a sport that demands pinpoint accurate movements with quick on-the-fly decision-making. Many different skills and techniques are present in fencing but the lunge is a fundamental footwork technique employed in all three fencing weapons - foil, epee, and sabre - and is considered essential to contemporary fencing styles. It involves a forward movement with the front foot while the body is propelled forward with the back leg, forming the foundation for offensive actions and combos. Hence, improving the lunge is crucial for success in fencing. 
Unfortunately, many young fencers, including myself, experience sport-related injuries, such as knee pain. One factor that can contribute to knee pain in fencing is an incorrect lunge technique. Using 2D and 3D data analysis, we are able to examine the specific positions and angles which can help fencers to adjust their lunges to prevent future injuries. 

This study aimed to explore the utilization of advanced artificial intelligence (AI) (J. Kim, "Artificial Intelligence in Sports Training," AI Review, vol. 7, pp. 23-30, (2018).) and virtual reality (VR) (S. Su, Y. Zhang, and L. Wang, "A Virtual Reality System for Fencing Training," Journal of Virtual Reality, vol. 18, pp. 5-12, (2013).) technologies in improving fencing performance, with a particular focus on the technique of a lunge. Our journey began with a 2D machine learning model using Google Video Intelligence APIs (Google, "Video Intelligence API documentation," Google Cloud. https://cloud.google.com/video-intelligence/docs (2022).), followed by the implementation of a more advanced 3D AI model using DeepMotion 3D Animation APIs (DeepMotion, "Animate 3D," DeepMotion. https://www.deepmotion.com/animate-3d (2022).). Lastly, the 3D animation model was imported into Unreal Engine and used to create an Oculus VR application for visualizations. 

 

Analyze 2D Posture with GCP Video Intelligence API 

 

Advice from my fencing coach 

To commence my research, I began by capturing some video footage of my lunges. During practices and tournaments, I would video my actions to begin analyzing my lunges. Afterwards, I sent the clip to my fencing coach, an international fencer and coach Mario Jelev, who provided me with valuable feedback that read as follows: 

Nathan’s upper body needs to be lower, which means that the front leg should form an angle closer to 90-degrees. 

Nathan’s back leg needs to be fully extended to form a stronger push forward. The majority of the power in a lunge comes from the back leg and leaving it not fully extended is wasting speed and power. 

Nathan’s lunge moves too much on the vertical plane while lunges are more horizontal. For stability purpose, the upper body needs to move in the horizontal direction and not as much movement vertically. This is because the bouncing in the vertical direction decreases tip accuracy. Additionally, the upwards movement is wasting time and can cause a greater force to be applied to the knee increasing the chances of injury. 

When looking at Nathan’s training and tournament lunges, they are noticeably different. This can be due to nervousness but there is a second jittery action that follows. This creates unnecessary stress and strain in the knee. Fixing this habit and making the lunge more fluid and a one-tempo action will improve speed, power, accuracy, and knee health. 

This feedback brought up few questions that I would like to analyze using machine learning technologies: 

Are the positions of my front and back knee optimal for power, speed, and knee health? 

Could the positions of my body be improved? (Hip, Shoulder, ect.) 

Did my front arm fully extend? 

How was far does my lunge travel? (Positions of hand and leg) 

How does a tournament lunge compare with one in practice and one from an Olympic champion? 

 

Pose Detection using Person Detection Feature  

The GCP Video Intelligence API offers a wide range of variety of features for Person Detection. From among the available tools, I chose to utilize it to determine the angle of my knees and arms. According to the Person Detection API documentation (Google, "Video Intelligence API documentation," Google Cloud. https://cloud.google.com/video-intelligence/docs (2022).), the following are specific attributes that the Person Detection feature can identify: 
