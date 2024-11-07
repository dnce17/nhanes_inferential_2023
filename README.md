# nhanes_inferential_2023

Key Notes
* Make sure SEQN is treated as an obj/str before merging
    * e.g. code
```python
anova2way_iv1 = demographics_df[['SEQN', 'RIDAGEYR']]
anova2way_iv1['SEQN'] = anova2way_iv1['SEQN'].astype(str)
```