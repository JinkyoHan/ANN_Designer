# ANN_Designer

            ######################
            #    ANN Designer    #
            #     ver 0.9.7      #
            ######################

# Written by Jinkyo Han, OST, SNU NAOE
# 38jinkyo@snu.ac.kr
# Supervised by Do Kyun Kim, OST, SNU NAOE

# Input : 
    # 1) your dataset
    # 2) parameters for optimization - search space, threshold, n_calls, ...
# Output : 
    # 1) hyperparameters-model performance set, by csv file
    # 2) full-trained optimal model by '.h5'
    # 3) convergence plot for BOwGP optimization

# Algorithm
    # Search Space : manually defined
    # Search Strategy : BOwGP - "n_calls" should be adjusted as needed
    # Estimation : Early Stopping, by nu-SVR, at 25% learning curve - "threshold" should be adjusted as needed
        # ref: Baker et al. (2017), Accelerationg NAS using performance prediction.
        # NuSVR would be pretrained, with "n_samples" of dataset.
            # Learning Curve at 25% epochs - Final val_loss
