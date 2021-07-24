## City Persons Data

#### - Interpret and analyze your results. Did the model performance exhibit a particular trend?

I first ran into issues and some errors running my model because I tried a lot of complex column feature types (I think I used every column feature type there was).

I then tried a simple model with size, age, and edu as numeric columns and gender as an indicator column, and got the following results:

___

wealth (2) Accuracy 0.9853658676147461

wealth (3) Accuracy 0.890731692314148

wealth (4) Accuracy 0.6517072916030884

wealth (5) Accuracy 0.5502439141273499

___

Then I tried changing up the types of feature columns a little, and found that setting size, age, and edu as numeric columns, age as a bucketized column, and age and size together as crossed columns gave me _**slightly**_ better values:

---

wealth (2) Accuracy 0.9941463470458984

wealth (3) Accuracy 0.9043902158737183

wealth (4) Accuracy 0.6565853953361511

wealth (5) Accuracy 0.5697560906410217

---

In both cases, there was a trend that as the wealth class got higher, the model did worse in predictions. That is probably because wealthier classes have varying features such as education level attainments, and household sizes that are very different and inconsistent, which makes it harder for the models to train on. More data will probably be needed to be better able to predict wealthier classes.