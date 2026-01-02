
**PROMPT 1 - TECHNICAL SUMMARISATION**
Summarize the following paragraph into a concise 3–4 sentence summary,
highlighting the main concepts and their relationships, but do not omit
technical details:

"Transformers have become the standard architecture for natural language
processing tasks. They rely on a mechanism called self-attention, which
allows the model to weigh the importance of different words in a sequence
relative to each other. Unlike recurrent neural networks (RNNs) or long
short-term memory networks (LSTMs), transformers process all tokens
simultaneously, enabling more parallelism and faster training.
Transformers are widely used in tasks like translation, text
summarization, question answering, and language modeling."


**PROMPT 2 - RESEARCH UNDERSTANDING**
Read the following research description and provide a structured summary
in 3–5 sentences. Include key methods, results, and applications:

"Recent research in computer vision has shown that vision transformers
(ViTs) can outperform convolutional neural networks (CNNs) on image
classification tasks when trained on large datasets. ViTs divide an
image into patches, embed each patch into a vector, and then apply
transformer layers to learn relationships between patches. This allows
the model to capture long-range dependencies and global context better
than CNNs. Experiments show that with sufficient data, ViTs achieve
higher accuracy and are more robust to occlusion and image
transformations."


**PROMPT 3 - CODE EXPLANATION (BEGINNER FRIENDLY)**
Explain the following Python function in clear, beginner-friendly
language. Include what it does, its inputs, outputs, and any important
edge cases.

def is_prime(n):
    if n < 2:
        return False
    for i in range(2, int(n**0.5)+1):
        if n % i == 0:
            return False
    return True


**PROMPT 4 - CODE REFACTORING**
Refactor the following Python function to improve readability,
efficiency, and Python best practices. Explain the changes you made.

def fibonacci(n):
    if n <= 0:
        return []
    elif n == 1:
        return [0]
    seq = [0, 1]
    while len(seq) < n:
        seq.append(seq[-1] + seq[-2])
    return seq

**PROMPT 5 - UNIT TEST GENERATION**
Write Python unit tests for the function below using the unittest
framework. Include at least 3 test cases covering normal, edge, and
invalid inputs.

def factorial(n):
    return 1 if n==0 else n*factorial(n-1)


**PROMPT 6 - TEXT TO JSON CONVERSION**
Convert the following text into a structured JSON object with fields:
name, age, occupation, location. Ensure the JSON is properly formatted.

Text:
"John Doe is a 34-year-old software engineer living in San Francisco,
California. He enjoys hiking and photography in his free time."


**PROMPT 7 - SOFTWARE TEST CASE GENERATION**
Read the following software requirement and produce a JSON array of test
cases. Each test case should have a "title", "input", and
"expected_output".

Requirement:
"The login page must accept an email and password. If the credentials
are correct, the user is redirected to the dashboard. If the
credentials are incorrect, an error message is displayed."


**Prompt 8 - Summarising json from paragraph**
Read the paragraph below and produce a JSON object summarizing the main points, including: topic, key_concepts, and potential_applications.
 "Neural networks are a set of algorithms modeled loosely after the human brain, designed to recognize patterns. Theyinterpret sensory data through a kind of machine perception, labeling, or clustering raw input. Deep learning, a subset of machine learning, uses multi-layered neural networks to learn complex patterns in large datasets, enabling applications like speech recognition, image classification, and autonomous vehicles."


**PROMPT 9 - CONCEPTUAL COMPARISON**
Compare the strengths and weaknesses of transformers versus recurrent
neural networks (RNNs) in natural language processing. Provide a concise
summary with at least three points for each.

