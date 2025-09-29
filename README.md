# 👁️ Practical Drowsiness Detection System Using Computer Vision and Eye Aspect Ratio
A computer vision-based system that detects drowsiness in real-time using eye aspect ratio (EAR) analysis. Features live webcam monitoring, audio alerts, data logging, and comprehensive analytics for safety applications. Perfect for driver safety, workplace monitoring, or personal alertness tracking.

## Features
- **Real-time Detection**: Monitor drowsiness through webcam feed
- **Audio Alerts**: Automatic sound warnings when drowsiness is detected
- **Visual Indicators**: On-screen alerts and status displays
- **Data Logging**: CSV logs with timestamps and drowsiness episodes
- **Video Recording**: Save detection sessions for later review
- **Configurable Thresholds**: Adjustable sensitivity settings
- **Analytics**: Comprehensive data analysis and visualization

## Technologies Used
- **Python 3.x**
- **OpenCV**: Computer vision and image processing
- **Dlib**: Facial landmark detection
- **SciPy**: Distance calculations
- **Pandas** - Data manipulation and analysis
- **Matplotlib & Seaborn** - Data visualization
- **Threading** - Audio alert management
- **CSV** - Data logging

**Note**: You'll need to download the dlib wheel file for Windows:
- `dlib-19.24.99-cp312-cp312-win_amd64.whl`

## How It Works

<video width="640" height="480" controls>
  <source src="Demo/drowsiness_session.mp4" type="video/mp4">
  Your browser does not support the video tag.
</video>

### Eye Aspect Ratio (EAR)
The system uses the Eye Aspect Ratio formula to detect when eyes are closed:
```
EAR = (|p2-p6| + |p3-p5|) / (2 * |p1-p4|)
```
- **Normal EAR**: ~0.3 (eyes open)
- **Low EAR**: <0.25 (eyes closing/closed)
- **Threshold**: 0.25 (configurable)

### Detection Process
1. Capture video from webcam
2. Detect faces using Dlib's face detector
3. Extract 68 facial landmarks
4. Calculate EAR for both eyes
5. Monitor EAR values over consecutive frames
6. Trigger alerts when drowsiness is detected

## Output Files
The system generates several output files:

- **`drowsiness_log_YYYYMMDD.csv`** - Detailed event logs
- **`drowsiness_session_YYYYMMDD_HHMMSS.avi`** - Recorded video session
- **Analysis plots** - Various visualization charts

## Analytics Features
The system includes comprehensive analytics:

- **Timeline Visualization** - When drowsiness episodes occurred
- **Duration Analysis** - How long each episode lasted
- **EAR Trends** - Eye aspect ratio changes over time
- **Cumulative Tracking** - Total drowsiness duration
- **Statistical Summary** - Average, maximum, and total metrics

## Use Cases
- **Driver Safety**: Prevent accidents due to drowsy driving
- **Workplace Monitoring**: Monitor alertness in safety-critical jobs
- **Medical Research**: Study sleep patterns and fatigue
- **Personal Wellness**: Track your own alertness levels
- **Security Applications**: Monitor security personnel alertness

**Disclaimer**: This system is for research and educational purposes. For safety-critical applications, additional validation and testing are recommended.
