  This program is used to test the performance of the 11 object detect algorithms, including DAEAR-DETR, RT-DETR, DINO-DETR, DAB-DETR, Conditional DETR, Deformable DETR, DETR, YOLOv8, YOLOv9, Swin Transformer, Faster Rcnn, etc., on the Caltech Pedestrian Dataset (built with a frame interval of 30) 

1.Running environment

  After testing, the code can run normally in  Matlab2023a (Mac Monterey)  and Matlab2013a (Windows 7 64 bit) environments, but Matlab2019a (Windows 10 64 bit) fails to run.

2.Content structure

2.1CaltechPedestrian_Dataset

  The "CaltechPedestrian_Dataset" directory contains the training set, test set, and their annotation files. The train.json and test.json files store the annotation information in COCO format (with seg indicating segmentation annotation information).

2.2CocoEvalResults

  The JSON files in the "CocoEvalResults" directory are the test results for each model. Subdirectories named after the algorithms contain the test results converted into TXT format (used for calculating and plotting the Log Average Miss Rate (LAMR) curve).

2.3FinalResult

  The "FinalResult" directory stores the final LAMR curves plotted under different test conditions.

2.4ResultsEval

  The "ResultsEval" directory contains the intermediate files and calculation results generated during the evaluation process.

2.5test_annotations_txt

  The "test_annotations_txt" directory contains the test set annotation files in TXT format.

3.Running methods

3.1 run dbEval(1,'(a)') to calculate and display LAMR curves on Reasonable subset

3.2 run dbEval(3,'(b)') to calculate and display LAMR curves  on Small subset

3.3 run dbEval(10,'(c)') to calculate and display LAMR curves  on Occ=heavy subset

