This project integrates the concepts of Internet of Things with Python. The project was developed thorugh the follwoing phases:
  
1. A Raspberry Pi was used to capture images of an eomployee who would have access. 30 images were captured using an Open-CV pre-trined classifier. 
PiRGBArray() gave us a 3-dimensional RGB array from the captures. The advantage is that it has the ability to read from the Raspberry Pi camera as a Numpy       array. A directory is created with the name of the employee and the 30 images are stored inside it.

2. A recognizer was trained accoring to the data gathered. the Local Binary Patterns Histogram (LPBH) face recognizer was used. It comes included in the OpenCV package. A dictionary is created which contains the employee name and the Label ID associated with the employee.

3. The recoginzer trained can now be used to detect faces and activate the lock to open the door if the emplyee is recognised by the model. It gives a confidence level for each face it detecs and upon crossing a certain threshold, the lock opens.
