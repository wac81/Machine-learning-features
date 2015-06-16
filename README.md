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
    
# Result
在苹果4跟G14之间，哥也会果断选14，不在乎价格，而是综合判定。玩机还是大屏的好啊，那样才有感觉。

pos probability score: 0.998996

neg probability score: 0.001004

总之机无完机，瑕不掩瑜。

pos probability score: 0.639381

neg probability score: 0.360619

