# Titanic-Passangers
## Predicting Wheather passangers on the Titanic would have survived or not from the Train and Test datasets.
## Contents:
      1.Import the libraries![libraries_](https://user-images.githubusercontent.com/75600702/117145790-e8099900-ad89-11eb-82d0-d936dc86fd64.PNG)


      2.Get the data sets ![Datasets](https://user-images.githubusercontent.com/75600702/117145978-1a1afb00-ad8a-11eb-8307-7447374700ac.PNG)


      3.Drop the cabin Feature:#Drop the cabin feature

        train = train.drop(['Cabin'], axis = 1)
        test = test.drop(['Cabin'], axis = 1)
      4.Do the data Exploration/Analysis![Analysis](https://user-images.githubusercontent.com/75600702/117146770-ed1b1800-ad8a-11eb-8879-246a4c9442c9.PNG)

      5.Describe the training dataset![Describe train](https://user-images.githubusercontent.com/75600702/117146967-26538800-ad8b-11eb-838a-2934ac593ca9.PNG)

      6.Clean the dataset ![Data cleaning](https://user-images.githubusercontent.com/75600702/117147318-85190180-ad8b-11eb-9d89-2e7597b85c99.PNG)

      7.Display the head upto 10 rows ![Train Head](https://user-images.githubusercontent.com/75600702/117147573-c27d8f00-ad8b-11eb-8064-31ed18441576.PNG)

      8.Convert the features into numerals so that machine learning algorithms can process them.![Embark feature](https://user-images.githubusercontent.com/75600702/117148094-4a639900-ad8c-11eb-91a5-7c0ae8681bbd.PNG)

      9.Sport additional features with missing (NaN=not a number) fill them in.![Age feature](https://user-images.githubusercontent.com/75600702/117148527-adedc680-ad8c-11eb-904d-b2e7bd78c664.PNG)

      10.determine the Age and sex of Passengers.![pp](https://user-images.githubusercontent.com/75600702/117149223-687dc900-ad8d-11eb-9ef8-8541914bf845.PNG)

      11.Determine the class of passanger(1,2 and 3rd class and their survival rates) ![NN](https://user-images.githubusercontent.com/75600702/117149506-a975dd80-ad8d-11eb-9229-ac698cbafb92.PNG)

      12.Create categories based on Age![random](https://user-images.githubusercontent.com/75600702/117149009-2ce2ff00-ad8d-11eb-9c27-3b189fac4d1c.PNG)

      13.Do the same as for Fare as you did for Age on #12 
           #map each Age value to a numerical value
             age_mapping = {'Baby': 1, 'Child': 2, 'Teenager': 3, 'Student': 4, 'Young Adult': 5, 'Adult': 6, 'Senior': 7}
              train['AgeGroup'] = train['AgeGroup'].map(age_mapping)
              test['AgeGroup'] = test['AgeGroup'].map(age_mapping)
      14.Build the machine model and compare the results.We need to use the predictions on the training set to compare the algorithms with each other and use the cross validation.
      a)Do Stochastic Gradient Descent (SDG):![Sto](https://user-images.githubusercontent.com/75600702/117151443-76344e00-ad8f-11eb-9a76-f33676f9916a.PNG)

      b)Do a Random Forest![random](https://user-images.githubusercontent.com/75600702/117151310-54d36200-ad8f-11eb-96ab-53ae22576834.PNG)

      c)Do a logistic Regression![logistic](https://user-images.githubusercontent.com/75600702/117149903-08d3ed80-ad8e-11eb-8c43-76d0536cedf2.PNG)

      d)Do a K Nearest Neighbour ![Ke](https://user-images.githubusercontent.com/75600702/117151081-1b025b80-ad8f-11eb-82f3-599db9928f71.PNG)

      e)Do a Gaussian Naive Bayes ![Gausi](https://user-images.githubusercontent.com/75600702/117149760-e2ae4d80-ad8d-11eb-85d0-e5c43aed9d84.PNG)

      f)Do a support Vector Machine ![Support](https://user-images.githubusercontent.com/75600702/117150244-58b2b480-ad8e-11eb-961f-678045ccf682.PNG)

      g)Do a perceptron ![Pre](https://user-images.githubusercontent.com/75600702/117150675-bcd57880-ad8e-11eb-95bc-9f968a249de2.PNG)

      h)Do a Decision Tress ![Decision Tree](https://user-images.githubusercontent.com/75600702/117150814-e0002800-ad8e-11eb-8d5d-3e45f8d81af3.PNG)

      i)Do a Linear regression ![Linear](https://user-images.githubusercontent.com/75600702/117150492-944d7e80-ad8e-11eb-9273-84783bdf7f47.PNG)

   ## Conclude the best Model.
     ![Comparison](https://user-images.githubusercontent.com/75600702/117151659-aaa80a00-ad8f-11eb-8aa3-7076dcb9783a.PNG)

      my conclusion Gradient Boosting Classifier is the best.This is because Gradient boosting is a greedy algorithm and can overfit a training dataset quickly. It can benefit from regularization methods that penalize various parts of the algorithm and generally improves the performance of the algorithm by reducing overfitting.
