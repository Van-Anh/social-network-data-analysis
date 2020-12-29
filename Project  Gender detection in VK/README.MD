
# Project  Gender detection in VK
Students:  Le Thanh Van Anh, Karataeva Azhar

## Downloading and data processing
   - Downloading data via VK API - [VK_scraph.ipynb](https://github.com/Van-Anh/social-network-data-analysis/blob/main/Project%20%20Gender%20detection%20in%20VK/VK_Scraph.ipynb).
	    1. id members 
	    2. id friends of members 
	    3. data about members of group and their friends: [user_data_all.pickle](https://github.com/Van-Anh/social-network-data-analysis/blob/main/Project%20%20Gender%20detection%20in%20VK/user_data_all.pickle), [user_connections_all.pickle](https://github.com/Van-Anh/social-network-data-analysis/blob/main/Project%20%20Gender%20detection%20in%20VK/user_connections_all.pickle)
   -  Find and save the largest connected component: [connected_components-all.ipynb](https://github.com/Van-Anh/social-network-data-analysis/blob/main/Project%20%20Gender%20detection%20in%20VK/connected_components-all.ipynb).
	    1. All male user in the largest connected component: [male_all.txt](https://github.com/Van-Anh/social-network-data-analysis/blob/main/Project%20%20Gender%20detection%20in%20VK/male_all.txt)
	    2. All female user in the largest connected component: [female_all.txt](https://github.com/Van-Anh/social-network-data-analysis/blob/main/Project%20%20Gender%20detection%20in%20VK/female_all.txt)
	    3. Visualization of gender distribution 
	    4. All information of users in the largest connected component: [more_infomation_user_data_all.pickle](https://github.com/Van-Anh/social-network-data-analysis/blob/main/Project%20%20Gender%20detection%20in%20VK/more_infomation_user_data_all.pickle)
	    5. Save graph [G_subgraph_all.gz](https://github.com/Van-Anh/social-network-data-analysis/blob/main/Project%20%20Gender%20detection%20in%20VK/G_subgraph_all.gz)

## Classification based on static features
  - Implemention: [classification_on_static_features.ipynb](https://github.com/Van-Anh/social-network-data-analysis/blob/main/Project%20%20Gender%20detection%20in%20VK/classification_on_static_features_all.ipynb)
  - Best model ROC AUC - 0.65
  - Save best model in file: [best_static_model_all.pickle](https://github.com/Van-Anh/social-network-data-analysis/blob/main/Project%20%20Gender%20detection%20in%20VK/best_static_model_all.pickle)

## Classification based on Node2vec
  - Implemention: [classification_on_node2vec_all.ipynb](https://github.com/Van-Anh/social-network-data-analysis/blob/main/Project%20%20Gender%20detection%20in%20VK/classification_on_node2vec_all.ipynb)
  - Best model ROC AUC - 0.52
  - Save best model in file: [best_node2vec_model_all.pickle](https://github.com/Van-Anh/social-network-data-analysis/blob/main/Project%20%20Gender%20detection%20in%20VK/best_node2vec_model_all.pickle)

## Classification based on Node2vec embeddings and static features
   - Implemention: [classification_on_node2vec_and_static_features_all.ipynb](https://github.com/Van-Anh/social-network-data-analysis/blob/main/Project%20%20Gender%20detection%20in%20VK/classification_on_node2vec_and_static_features_all.ipynb)
    - Best model ROC AUC - 0.55

## Summary
We trained the models with best results: 
    - Classifiers on static features – 0.65
    - Classifiers on the concatenation of static features and Node2Vec embeddings – 0.55
    - Classifiers on embeddings Node2Vec – 0.52

## Future work
   - Get more users 
   - Collect other information such as followers, subscriptions, public pages, …
   - Collect and add image recognition
