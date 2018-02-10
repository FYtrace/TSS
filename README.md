import cv2
import numpy as np
'''
image = cv2.imread("/home/surging/Desktop/test.jpg")
cv2.imshow("test",image)
'''

cap = cv2.VideoCapture("/home/surging/Desktop/test.mp4")
#cap = cv2.VideoCapture(0)
while(cap.isOpened()):
    # get a frame
    ret, frame = cap.read()
    print "imshow"
    # show a frame
    if ret == False:
        print "over"
        break
    cv2.imshow("capture", frame)
    if cv2.waitKey(100) & 0xFF == ord('q'):
        break
    
cap.release()
cv2.destroyAllWindows()
