# ML-hw1
----------პროექტის სათაური და მოკლე მიმოხილვა------------
House Prices - Advanced Regression Techniques - კონკურსი, რომლის მიზანია სახლების
მონაცემებზე დაყრდნობით საბოლოო გაყიდვის ფასის პროგნოზირება. მონაცემები მოცემულია 
train.csv და test.csv ფაილებში და მოიცავს როგორც რიცხვით ასევე კატეგორიულ ცვლადებს.

----------ჩემი მიდგომა--------------
1. მონაცემების წმენდა და Null მნიშვნელობების დამუშავება
2. Feature Selection
3. დატრენინგება
4. შეფასება ლოგარითმულად გარდაქმნილი მნიშვნელობებით
5. და საუკეთესო შედეგის პოვნა
   
----------Feature Engineering-----------
გამოვიყენე WeightOfEvidence და OneHotEncoding მეთოდები, კატეგორიული ცვალდების
რიცხვითში გადასაყვანად
Nan მნიშვნელობის დასამუშავლებად გამოვიყენე handle_nulls ფუნქცია,რომელმაც ცვლადები
შეავსო 0 ებით ან NO-ებით
ასევე ამოვიღე ისეთი column-ები რომელსაც 80%-ზე მეტი მონაცემები არ ქონდა

----------Feature Selection-------------
გამოვიყენე estimator-ები:
LinearRegression, RandomForestRegressor, XGBRegressor, GradientBoostingRegressor
ამათი მნიშვნელობა შეფასდა სკალირების შემდეგ და scatter plot-ების აგება დამეხმარა მათი
ვიზუალურად შეფასებისთვის

----------Training---------------
ზემოთ ჩამოთვლილი მოდელები არის ტესტირებული მოდელები.
საბოლოო მოდელის შერჩევა მოხდა RMSE-მეტრიკით, რომელიც გამოთვლილია ლოგარითმული
გარდაქმნის შემდეგ. არჩევანი გაკეთდა მინიმალური bias-ისა და variance-ის მქონე მოდელზე

----------MLflow Tracking-----------
https://dagshub.com/lkhok22/ML-hw1.mlflow/#/experiments/0?searchFilter=&orderByKey=attributes.start_time&orderByAsc=false&startTime=ALL&lifecycleFilter=Active&modelVersionFilter=All+Runs&datasetsFilter=W10%3D
(იმედია სწორადაა ეს ლინკი)

საბოლოოდ საუკეთესო შედეგი მიიღო GradientBoostingRegressor-მა 
თითოეული მიდგომის შედეგები Mlflow-ზეა

