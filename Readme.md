# Machine Learning Based Fault Diagnosis of Electric Drives

AC Electric Drives or Variable Speed Drives (VSDs), enjoy extensive application in industrial, domestic, & commercial fields. This is due to their ability to generate desired torque, power levels & control for various external load requirements. The Three Phase Induction Motor is frequently employed as part of the drive, due to its simplicity and robustness. The drive part, hosting the induction motor is prone to faults. This results in expensive maintenance, down-time, and a potential threat to human safety.

This project presents a time-series analysis of some critical and non-critical faults i.e., electrical and mechanical, using statistical feature extraction techniques to extract information rich regions from the motor output data. This is followed by Machine Learning based multi-class classification to optimally identify various faults with high accuracy and short diagnosis time for appropriate corrective action. 

## Dataset Generation

### Model
A Variable Frequency Drive model was simulated using Simulink, MATLAB. 

![model](https://user-images.githubusercontent.com/97694796/226060876-17c98265-e27a-4150-8449-10ce15aa9cb9.png)

### Faults
There are five faults that have been selected and subsequently simulated for this project:
1) Under Voltage Fault
2) Over Voltage Fault
3) Phase to Ground Short Circuit Fault
4) Phase to Phase Short Circuit Fault
5) Over Loading Fault

These faults along with the normal operating condition form the six target/label categories to be predicted by the ML model. 

Data is generated for multiple loading conditions, with regard to the full load torque. Data generated is transformed from signal/waveform to data matrix, stored in
csv files.

### Feature Selection
Six output parameters/features were selected for further processing.

![Feature set](https://user-images.githubusercontent.com/97694796/226059923-7e90da4b-9b09-4971-a4c3-59fd356dbae4.png)

## Data Preprocessing
A number of steps have been taken under this phase to transform the dataset into the desired form:
1) Steady-state Data Segregation
2) Data Imputation
3) Label Encoding
4) Feature Scaling
5) Data Shuffling

## Model Building
Three supervised machine learning models were chosen for this multi-class classification problem. They are:
1) K-Nearest Neighbor
2) Support Vector Machine
3) Random Forest

All models are trained using K-fold cross validation and subsequently optimized using grid search over a range of possible values for their respective hyperparameters.

## Model Evaluation
There a number of evaluation metrics employed to assess performance:
1) Accuracy
2) Confusion Matrix
3) Training Time

Results obtained revealed that the K-Nearest Model performs the best out of the three models i.e., 93.13%  classification accuracy on the testing set.

## Conclusion
The results obtained showed high correct classification accuracy in comparison to other diagnosis techniques and an in-house comparison between multiple machine learning algorithms was conducted to identify the most optimal results.
The project has enabled a comprehensive study of the use of ML in the field of motor conditioning and response generation. Since the use of ML in this particular 
field is relatively new, there exists a plethora of opportunities, one of which we have tried to explore during the course of our project.

Moreover, on the lines of novelty, we reviewed multiple supervised classification algorithms to gauge results in a more comprehensive manner. All in all, we were able to generate a robust and significantly accurate methodology for fault diagnosis of AC electric drives being employed in the industry and elsewhere.
