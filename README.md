![Screenshot 2024-05-23 220950](https://github.com/Safe-bet/CV-TASK3/assets/149116096/3a034b18-2e0a-4598-b617-57b166b392ad)
![Screenshot 2024-05-23 220839](https://github.com/Safe-bet/CV-TASK3/assets/149116096/370b3c86-6c73-4a96-8b10-7180d68abe31)
# CV-TASK3
Link to DATASET="https://drive.google.com/file/d/1dJieB7idMxv94ILeNEpOgr0KXa407lQi/view?usp=drive_link"

Link to Colab Notebook="https://colab.research.google.com/drive/1ci0StH_352vNHS3ntZCwA7QMJUEz9XbR?usp=sharing

So I have created dataset by finding masked photos from internet and other similar datasets, I have done this for both train and test dataset. After that I cropped the photos so that only face is present in it. I have also used "mask snapchat filter" on my wingies to get photos for testing set.

So the main difficulty after dataset creation was training of model. For this I used several approachs like using my custom CNN models, then some standard architectures like VGG16, Alexnet, etc. , these model didn't gave a quite significant accuracy. I have not shown these models in my CODE file it was not final model. After experimenting with previous models I shifted to YOLOv8, although it was quite a big model and took around 8 mins to train on normal CPU(no GPU), it gave 98% accuracy on unseen testing set. I had trained YOLO on "20 epochs" with "image size 224". Before Passing to YOLO I had used sharpening filter upon images to enhance its features like eye, eyebrow, hair, etc. as YOLO was primarly using them for classification. I also tested on increasing brightness and contrast but that didn't helped much so I removed them so save computation.

It is requested to run the code in GOOGLE COLAB, as I have preset the path to get prediction from model in that interface, else you will have to modify path to best model.
So to run the code firstly upload dataset on your drive in MyDrive section and then mount drive. Then run the blocks in up to down order. To predict your own photo, give path to your photo(If you are running in COLAB firstly upload your own photo) in input and check result.

NOTE- Try to run in COLAB, I have given link to COLAB notebook and also editor access.
![Screenshot 2024-05-23 215427](https://github.com/Safe-bet/CV-TASK3/assets/149116096/b19c1b4b-a73e-4736-a7a0-2c4c5f7587ef)
