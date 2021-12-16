# Lab 3 ML for Cybersecurity
The defence used in the lab is only pruning defence. The badnet given was pruned until the desired accuracy was reached. The accuracy was reached after pruning 45 neurons for X=2%, pruning 48 for X=4%, pruning 51 neurons for X=10%, pruning 53 neurons for X=30%. 

The files used in the lab are:
```
├── data 
    └── cl
        └── valid.h5 // this is clean validation data used to design the defense
        └── test.h5  // this is clean test data used to evaluate the BadNet
    └── bd
        └── bd_valid.h5 // this is sunglasses poisoned validation data
        └── bd_test.h5  // this is sunglasses poisoned test data
├── models
    └── B1.h5 // this is the pruned BadNet
    └── G_net.h3 // this is the GoodNet but might not work as it uses Lambda layers which are not serializable in Keras
    └── pruned_net_2.h5 
    └── pruned_net_4.h5
    └── pruned_net_10.h5
├── README.md
└── eval.py // this is the evaluation script
```
The evaluation script is used to evaluate the BadNet on the clean test data and the BadNet on the sunglasses poisoned test data. The results are printed to the console.
The report and the code is in the form of a jupyter notebook which is included with this project.