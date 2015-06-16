# Machine-learning-for-text

# import
in pos_neg_ml_feature.py file

#  Load classifier
clf = pickle.load(open('wac_classifier.pkl'))   

# Testing single review
pred = clf.prob_classify_many(extract_features(sentiment_review[:2])) # An object contian positive and negative probabiliy
# Testing single sentence
pred = clf.prob_classify_many(extract_features("这个车啥都不行真讨厌。"))

# Spilt positive and negative info to output
pred2 = []  


for i in pred:


    pred2.append([i.prob('pos'), i.prob('neg')])
