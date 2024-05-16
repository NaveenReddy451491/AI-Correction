# AI-Correction


The code performs several NLP (Natural Language Processing) tasks to assess the similarity between a main sentence (Ohm's Law definition) and a student's answer. Here's an explanation of its workflow and how it executes:

1. **Importing Libraries and Downloading Resources:**
   - The code begins by importing necessary libraries such as `SentenceTransformer`, `nltk`, and `numpy`.
   - It also downloads required resources from NLTK using `nltk.download()`.

2. **Semantic Similarity Calculation (`calculate_semantic_similarity`):**
   - The `calculate_semantic_similarity` function initializes a pre-trained model (`paraphrase-distilroberta-base-v1`) from `SentenceTransformer`.
   - It encodes the main sentence and the student's answer into numerical embeddings using the model.
   - It calculates the cosine similarity between the embeddings to determine the semantic similarity score.

3. **Sentiment Analysis (`calculate_polarity_score`):**
   - The `calculate_polarity_score` function uses `SentimentIntensityAnalyzer` from NLTK to determine the sentiment polarity (positive, negative, or neutral) of the text.
   - It returns a numerical score representing the overall sentiment polarity.

4. **Grammatical Similarity Check (`check_grammatical_similarity`):**
   - The `check_grammatical_similarity` function tokenizes the main sentence and the student's answer into words using `word_tokenize` from NLTK.
   - It computes the path similarity between WordNet synsets of corresponding words in both sentences.
   - It calculates the average similarity score as the grammatical similarity between the sentences.

5. **Input Sentences and Scores Calculation:**
   - The code defines the main sentence and the student's answer as strings.
   - It calculates the sentiment polarity scores for both sentences using `calculate_polarity_score`.

6. **Execution and Output:**
   - The code prompts the user to input the maximum marks for the question.
   - Based on the semantic similarity, grammatical similarity, and sentiment polarity scores, it calculates the final marks using a predefined logic.
   - It then prints the polarity scores, grammatical and semantic similarity scores, and awarded marks along with the maximum marks.

7. **Explanation of Marks Calculation:**
   - If both sentences have positive polarity and meet certain similarity thresholds, marks are assigned based on the semantic similarity score.
   - If the sentences have negative polarity or do not meet the similarity thresholds, a lower mark is assigned.

8. **Overall Workflow:**
   - The code utilizes various NLP techniques to assess the similarity between the main sentence and the student's answer, considering both meaning (semantic similarity) and structure (grammatical similarity) of the sentences, along with sentiment analysis.

To execute the code, ensure that you have installed the required libraries and NLTK resources. Run the code in a Python environment, and follow the prompts to input the maximum marks and view the assessment results.
