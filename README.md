# ERisk2023
EARLY RISK PREDICTION ON THE INTERNET

Task 1: Search for symptoms of depression

The task consists of ranking sentences from a collection of user writings according to their relevance to a depression symptom. The participants will have to provide rankings for the 21 symptoms of depression from the BDI Questionnaire. A sentence will be deemed relevant to a BDI symptom when it conveys information about the user's state concerning the symptom. That is, it may be relevant even when it indicates that the user is ok with the symptom.

We would release a TREC formatted sentence-tagged dataset (based on eRisk past data) together with the BDI questionnaire. Participants would be free to decide on the best strategy to derive queries from describing the BDI symptoms in the questionnaire.

After receiving the runs from the participating teams, we would create the relevance judgements with the help of human assessors using pooling. We will use the resulting qrels to evaluate the systems with classical ranking metrics (e.g. MAP, nDCG, etc.). This new corpus with annotated sentences would be a valuable resource with multiple applications beyond eRisk.
