# Leukemia-classification-project
Cell image classification is implemented 3 algorithms: 

- Naïve Bayes
- Logistic regression
- Neural network

Details and Methods

- Since the images of the normal white blood cells and the immature leukemic blasts appear similar, therefore the process of identifying them is challenging.

- During their data acquisition, some staining noise and illumination errors remain in the microscopic images of these cells even though they have been mostly fixed.

- The dataset comprises of 7,271 Leukemia white blood cell images and 3,389 normal white blood cell images.

- Set diagnosis = 1 for ALL (Acute lymphoblastic leukemia) and diagnosis = 0 for HEM (Normal white blood cell)

- Naïve Bayes and Logistic regression: prepared dataset by extracting features from the white blood cell images.

  - Pixel values
  
      - Max_NM_pixel: Normalized Pixel values in the range of 0-1 and take the maximum value
      
      - Mean_global: Calculated and subtracted the mean pixel value across color channels
      
      - SD_global: Calculated standard deviation across all color channels
      
  - Circle detection: Used function cv2.minEnclosingCircle() to detect circle which completely covers the object with minimum area and find the radius and 
  center X, Y of the white blood cell. Since I think that leukemia white blood cells will be blasted, this should have an effect on the radius of the cell image.
  
Conclusion

    This project’s dataset fits better with Naïve Bayes with categorical model which gives the F1 score of 0.798, while the Neural network generated the lowest F1 score, which is 0.76. The Naïve Bayes and Logistic regression are the powerful supervised algorithm used for binary classification problems. A neural network is more complex and must train the model carefully and it will produce better performance when you have sufficient training data
