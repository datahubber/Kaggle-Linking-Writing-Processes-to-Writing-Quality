# Feature Performance
## Baseline
https://www.kaggle.com/mianwang1024/baseline/edit
### CV:
Composition OOF score = 0.60851 
Composition best W = 0.472 
current_RMSE:0.6133531196220571 
blending_weights:{'lgbm': 0.459, 'catboost': 0.246, 'svr': 0.295}
### LB:
0.5784x ?

5. 2 + 3 + 4 

6. 3 + 4 

7. Text_change_nunique / event_id_max/up_time_max/action_time_sum 

8. Activity_nunique/Event_id_max / action_time_sum 

9. 10% - 90% 

10. Word_count_max / action_time_sum  

11. Down_event_nunique / up_time_max 

12. Sent_len_sum ratio

13. down_event_8_count/down_event_3_count / up_time_max/event_id_max

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

## (Based on feature 1) Feature 2 add activity_nunique / time/event
        feats['net_word_time_ratio'] = feats['word_count_max'] / (feats['up_time_max'] - feats['action_time_gap1_sum'])
        feats['net_event_time_ratio'] = feats['event_id_max']  / (feats['up_time_max'] - feats['action_time_gap1_sum'])
### CV
Composition OOF score = 0.60718
Composition best W = 0.517
current_RMSE:0.6135213015827492
blending_weights:{'lgbm': 0.472, 'catboost': 0.244, 'svr': 0.284}
### LB
0.5780x ?

## (Based on feature 1) Feature 3 add cursor_position_nunique / time/event
        feats['cursor_time_ratio'] = feats['cursor_position_nunique'] / feats['up_time_max']
        feats['cursor_event_ratio'] = feats['cursor_position_nunique'] / feats['event_id_max']
### CV
Composition OOF score = 0.60734
Composition best W = 0.510
current_RMSE:0.6125888480526304
blending_weights:{'lgbm': 0.416, 'catboost': 0.318, 'svr': 0.266}
### LB
0.5777x ?

## (Based on feature 1) Feature 4 add activity_nunique / time/event
        feats['activity_time_ratio'] = feats['activity_nunique'] / feats['up_time_max']
        feats['activity_event_ratio'] = feats['activity_nunique'] / feats['event_id_max'] 
### CV
Composition OOF score = 0.60709
Composition best W = 0.521
current_RMSE:0.6116264188789808
blending_weights:{'lgbm': 0.5, 'catboost': 0.256, 'svr': 0.244}
### LB
0.5773x ?

## Feature 5 2 + 3 + 4

### CV
Composition OOF score = 0.60781
Composition best W = 0.501
current_RMSE:0.6131531920028749
blending_weights:{'lgbm': 0.436, 'catboost': 0.253, 'svr': 0.311}
### LB
> 0.5780

## Feature 6 3 + 4

### CV
Composition OOF score = 0.60742
Composition best W = 0.505
current_RMSE:0.6122198260314985
blending_weights:{'lgbm': 0.521, 'catboost': 0.223, 'svr': 0.256}
### LB
0.578

## Feature 4 + 7

### CV
current_RMSE:0.6134721235494489
blending_weights:{'lgbm': 0.472, 'catboost': 0.247, 'svr': 0.281}
### LB

## Feature 4 + 8

### CV
current_RMSE:0.612013548583005
blending_weights:{'lgbm': 0.477, 'catboost': 0.275, 'svr': 0.248}
### LB

## Feature 4 + 9

### CV
current_RMSE:0.6118376863066016
blending_weights:{'lgbm': 0.434, 'catboost': 0.305, 'svr': 0.261}
### LB

## Feature 4 + 10

### CV
current_RMSE:0.6130396836008632
blending_weights:{'lgbm': 0.453, 'catboost': 0.277, 'svr': 0.27}
### LB

## Feature 4 + 11

### CV
current_RMSE:0.6117052130602196
blending_weights:{'lgbm': 0.377, 'catboost': 0.361, 'svr': 0.262}
### LB

## Feature

### CV

### LB

## Feature

### CV

### LB

## Feature

### CV

### LB
