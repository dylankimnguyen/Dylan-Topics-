# Dylan-Topics-
Topics in Computer Science, Adelaide University, Dylan Nguyen

Link to more orangutang videos: https://uao365.sharepoint.com/:f:/r/sites/AnimalbehaviourobservationusingArtificialIntelligence/Shared%20Documents/File%20and%20data%20sharing/Orangutan%20Videos?csf=1&web=1&e=tzE0vp

1: Install DeepLabCut: https://github.com/DeepLabCut/DeepLabCut/blob/main/docs/installation.md
2: Install SimBA: https://github.com/sgoldenlab/simba

3: How to use DeepLabCut: https://deeplabcut.github.io/DeepLabCut/docs/standardDeepLabCut_UserGuide.html
4: Follow those steps above on how to use DeepLabCut then by using the videos and data within my files, the same result can be matched.

Look to the paper, in the methods on a rough rundown on how to use the system.
In deeplabcut, create a project, then adjust the config.yaml file, change the bodyparts to 4, name them head, center, leftleg and rightleg. (Alternate: You can choose my preconfigured config file in the orangutang-Dylan folder.
Then "add videos" and add all the videos found in the "orangutang-Dylan" folder which has a videos folder.
Then keep everything on default settings and then use "select videos" and select all the videos then extract frames for all the videos.
Then go to label frames, and annotate all the frames correctly, look to the DeepLabCut user guide on how to do this process correctly.
Then create training dataset on default settings, then train network, do as many iterations as possible.
Then Evaluate the network and click all the check boxes.


Next create analyse videos, and select all the videos you want to use, and click all the check boxes. Once down you can view many results.

Optional: Use create videos and you can test how your model works on new videos.

Next SimBA:
Open Simba and load project.
In the final folder, then in the project folder, there is a project configuration file, open this in Simba.
In The first part, further imports
Import all nessercay data, if doing this project from scratch, import all the CSV files from the deeplabcut folder, you can find these in the orangutang-dylan -> videos folder.
Then import all the videos from this folder too.

Then go to Video paramteresm and known distance to 200mm then conifgure video paramteres, and change distance in mm of your videos to 200mm then do calculate distance and tap on the two sides of the orangutangs head as on average the width is 200mm.

Then do outlier correction and change the settings, change the criteon values to whatever you think is correct, you can understand it by viewing Simba guide, it is however many mm multiplied by something and if it is over a certain value, a frame can be conisdered an outlier. 30mm or so is good. Then run outlier correction, then extract features and run that.
Then label behaviour: Label all the videos accordingly, if the animal is walking, check the walking box and if not then don't. After train machine model, adjust the settings to as needed, then run it  by doing train single model.
Then in validation you can select the .sav file which is walking or walk.sav and select it and select a csv file which corresponds to a video, then you can run the now trained model on the video. You can then view the results.

Then finally in visualization you can create graphs and plots which show the results.



