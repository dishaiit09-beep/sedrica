# Section A — General / Common Questions

## A1. What are your short-term and long-term goals?

In the short term, I want to strengthen my practical skills in computer vision, machine learning and autonomous systems through hands-on projects rather than only coursework. I have already explored AI/ML through projects in sentiment analysis, object detection, deep learning and quantitative applications, and I now want to understand how these ideas work when they become part of a real physical system.

I also want to improve my ability to take a problem from understanding the data and building a baseline to testing failures and improving the final system.

In the long term, I want to work in AI/ML and related research-driven areas where software interacts with real-world engineering constraints. I am especially interested in perception, intelligent decision-making and reliable systems, and I hope to pursue challenging research or development roles in these areas.

---

## A2. What motivates you to join UMIC SeDriCa?

What attracts me most to UMIC SeDriCa is that it combines AI and computer vision with an actual autonomous vehicle.

Most AI projects I have worked on so far end with a model, accuracy score or software output. SeDriCa is different because the final output has to influence a real vehicle, where perception, planning and control all depend on each other and mistakes have real consequences.

I am particularly interested in perception because even apparently simple tasks such as lane detection become difficult when there are shadows, missing markings, misleading lines or conflicting sensor information. Working on the assignment made this much more clear to me.

I also want to learn through implementation, debugging and testing on a team where the work eventually becomes part of a complete autonomous system rather than remaining an isolated coding exercise.

---

## A3. A campus driving scenario

One difficult situation for the autonomous buggy would be a busy pedestrian crossing or road near an academic or hostel area during class-change time.

A group of students may be walking close to the road while one person suddenly changes direction and starts crossing. At the same time, cycles or scooters may pass nearby, and parked vehicles or other pedestrians can partially block the camera's view.

The difficulty is that simply detecting a person is not enough. A pedestrian walking beside the road does not always require the buggy to stop, while someone beginning to enter the vehicle's path may require an immediate response. The system has to understand both the person's location and how that person is moving.

This mainly challenges perception, prediction and planning. Perception must detect pedestrians despite occlusion and changing lighting. Prediction must estimate whether their motion is likely to intersect the buggy's path, and planning must decide whether to continue, slow down or stop.

A practical approach would be to define the drivable or crossing region and combine pedestrian position, recent motion and distance from the buggy. If the predicted pedestrian path begins to overlap the buggy's path, the vehicle should first reduce speed and request STOP when the conflict becomes significant.
