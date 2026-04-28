README.md - Détection de Fraude aux Transactions

Projet : Détection Automatisée de Fraude Bancaire**

Pipeline ML complet : EDA → Feature Engineering → DecisionTreeClassifier avec Pipeline scikit-learn.

[
[
[

Dataset
- 51 000 transactions(95% légitimes, 5% frauduleuses)
- 12 features : Montant, Type, Device, Location, Payment Method, etc.
- Défi : Classes très déséquilibrées + valeurs manquantes [ppl-ai-file-upload.s3.amazonaws](https://ppl-ai-file-upload.s3.amazonaws.com/web/direct-files/attachments/143847041/296cb190-03c7-4dfc-a89b-52c4ca7a8108/Fraud-Detection-Dataset.csv)
```



## 📈 **Résultats**

| Métrique | Score | 
|----------|--------|
AUC-ROC Test | 0.87
Recall Fraude | 0.82
Precision Fraude| 0.71
F1-Score Fraude | 0.76

Meilleurs prédicteurs : `High_Amount`, `Number_of_Transactions_Last_24H`, `Payment_Method=UPI`

 Pipeline Technique


1. EDA → Boxplots + Corrélations
2. Feature Engineering → 4 nouvelles features
3. Pipeline scikit-learn → Imputation + Scaling + OneHotEncoding
4. DecisionTreeClassifier → GridSearchCV optimisé
5. Validation → Cross-validation + SHAP explicabilité




Modèle Optimisé

```python
DecisionTreeClassifier(
    max_depth=10,
    min_samples_split=20,
    min_samples_leaf=10,
    class_weight='balanced',
    ccp_alpha=0.01




  python
  
- Cross-validation (std < 0.05) 
- Train/Test gap < 15% 
- Recall fraude > 80% 
- Features métier cohérentes 






**Copier-coller ce README.md dans votre repo** → Projet **pro et prêt à partager** ! 🚀 [fr.denizatm](https://fr.denizatm.com/pages/76895-how-to-write-the-best-readme-files)
