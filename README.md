# Bloc_Change_Experiments

## Project Idea 
[Excalidraw.](https://excalidraw.com/#json=09XI-m-Om_-GWmV-J_2lh,GGIASaqsJp9ZX4LA-Ng7yA)
If the link is unavailable, open the local Excalidraw file [figures/final.excalidraw](figures/final.excalidraw)

## Project Resources

- [Final Notebook](ml_approaches/Final.ipynb)
- [Project Proposal](presentation/Project%20idea.pdf)
- [Final Presentation](presentation/Isuru_Ariyarathne_AML%20.pdf)

## Introduction
**Goal**: Demonstrate that measuring change and diversity are useful in identifying suspicious accounts.

**Suspicious account**: Accounts at extremes of change and diversity spectrum. In other words, accounts with very high change and diversity or very low change and diversity are the most suspicious.

Figure 1 and Figure 2, shows extremes have more bot-like behavior.

<div style="display: flex; justify-content: space-around; align-items: center;">
  <figure style="text-align: center;">
    <img src="figures/action.png" alt="Action Behavior">
    <figcaption><em>Figure 1: Action behavior indicating bot-like extremes.</em></figcaption>
  </figure>
  <figure style="text-align: center;">
    <img src="figures/content.png" alt="Content Behavior">
    <figcaption><em>Figure 2: Content behavior illustrating diversity trends.</em></figcaption>
  </figure>
</div>

After normalizing(Figure 5 shows how to calculate the change dynamic score), we can get an idea of how we can classify accounts using change and diversity, considering both action and content.

<figure style="text-align: center;">
  <img src="figures/change_dynamic_score.png" alt="Change Dynamic Score" style="width: 60%;">
  <figcaption><em>Figure 3: Change dynamic score showing account classification potential.</em></figcaption>
</figure>


## Dataset

Data
<figure style="text-align: center;">
  <img src="figures/data.png" alt="Data Overview" style="width: 60%;">
  <figcaption><em>Figure 4: Overview of the data used for analysis.</em></figcaption>
</figure>

Features
<figure style="text-align: center;">
  <img src="figures/user_data_point.png" alt="User Data Features" style="width: 60%;">
  <figcaption><em>Figure 5: Features for one user</em></figcaption>
</figure>


## Classification

**Model Accuracies**

<table>
  <tr>
    <th>Model</th>
    <th style="width: 100px;">Only Two Features</th>
    <th style="width: 100px;">Using All Features</th>
  </tr>
  <tr>
    <td>Random Forest</td>
    <td>0.6807</td>
    <td>0.8263</td>
  </tr>
  <tr>
    <td>Logistic Regression</td>
    <td>0.6807</td>
    <td>0.8263</td>
  </tr>
  <tr>
    <td>KNN</td>
    <td>0.6778</td>
    <td>0.8024</td>
  </tr>
  <tr>
    <td>XGBoost</td>
    <td>0.7192</td>
    <td>0.8299</td>
  </tr>
  <tr>
    <td>SVM - linear</td>
    <td>0.6840</td>
    <td>0.8016</td>
  </tr>
  <tr>
    <td>SVM - nonlinear</td>
    <td>0.7179</td>
    <td>0.8084</td>
  </tr>
</table>


**Randome Forest**

By analyzing the feature importance using Random Forest, it was observed that change_dynamic_score for change and diversity holds significant importance, as illustrated in Figure 6.
<figure style="text-align: center;">
  <img src="figures/feature_importance.png" alt="Feature Importance" style="width: 60%;">
  <figcaption><em>Figure 6: Feature importance</em></figcaption>
</figure>

## Logistic Regression - Results

**Decision Boundary**
<figure style="text-align: center;">
  <img src="figures/output.png" alt="Decision Boundary" style="width: 60%;">
  <figcaption><em>Figure 7: Decision Boundary</em></figcaption>
</figure>

**Confusion Matrix**
<figure style="text-align: center;">
  <img src="figures/cm_for_all.png" alt="Confusion Matrix" style="width: 60%;">
  <figcaption><em>Figure 8: Confusion Matrix</em></figcaption>
</figure>

## Acknowledgment

- [BLOC Framework](https://github.com/anwala/bloc)
- [BLOC Change Experiments](https://github.com/anwala/bloc-change-experiments)

