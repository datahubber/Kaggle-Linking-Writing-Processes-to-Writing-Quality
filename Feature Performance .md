# Feature Performance
## Baseline
https://www.kaggle.com/mianwang1024/baseline/edit
CV:
Composition OOF score = 0.60851
Composition best W = 0.472

current_RMSE:0.6133531196220571
blending_weights:{'lgbm': 0.459, 'catboost': 0.246, 'svr': 0.295}

LB:
0.5784x ?

## Feature 1 reduce sentences separation
delete '|\\?|\\!':
delete ', '_', '+'' 3 times:
### CV
Composition OOF score = 0.60729
Composition best W = 0.509

current_RMSE:0.6137741648796663
blending_weights:{'lgbm': 0.404, 'catboost': 0.314, 'svr': 0.282}
### LB
0.5782x ?

## Feature 2 add activity_nunique / time/event
        feats['net_word_time_ratio'] = feats['word_count_max'] / (feats['up_time_max'] - feats['action_time_gap1_sum'])
        feats['net_event_time_ratio'] = feats['event_id_max']  / (feats['up_time_max'] - feats['action_time_gap1_sum'])
### CV
Composition OOF score = 0.60718
Composition best W = 0.517

current_RMSE:0.6135213015827492
blending_weights:{'lgbm': 0.472, 'catboost': 0.244, 'svr': 0.284}
### LB
0.5780x ?

## Feature 3 add activity_nunique / time/event
        feats['cursor_time_ratio'] = feats['cursor_position_nunique'] / feats['up_time_max']
        feats['cursor_event_ratio'] = feats['cursor_position_nunique'] / feats['event_id_max']
### CV
Composition OOF score = 0.60734
Composition best W = 0.510

current_RMSE:0.6125888480526304
blending_weights:{'lgbm': 0.416, 'catboost': 0.318, 'svr': 0.266}
### LB
0.5777x ?

## Feature 4 add activity_nunique / time/event
        feats['activity_time_ratio'] = feats['activity_nunique'] / feats['up_time_max']
        feats['activity_event_ratio'] = feats['activity_nunique'] / feats['event_id_max'] 
### CV
Composition OOF score = 0.60709
Composition best W = 0.521

current_RMSE:0.6116264188789808
blending_weights:{'lgbm': 0.5, 'catboost': 0.256, 'svr': 0.244}
### LB
0.5773x ?

## Feature

### CV

### LB
