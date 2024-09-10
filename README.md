# Spelling Corrector

The **Spelling Corrector** project is an advanced spell-checking solution designed to analyze text, detect spelling errors, and provide accurate correction suggestions. It goes beyond traditional spell-checking by addressing challenges such as homonyms, common typos, and out-of-dictionary words.

## Key Features

- **Advanced Spell-Checking**: Detects and corrects misspelled words using  Natural Language Processing (NLP) techniques.
- **Contextual Awareness**: Incorporates the surrounding text to offer relevant and precise corrections.
- **Real-Time Performance**: Delivers spelling suggestions with minimal latency, ensuring seamless user experience.

  
## Methodology

1. **Text Segmentation**: The input text containing spelling errors is first segmented into smaller units (words) for efficient processing. This segmentation allows the model to focus on specific parts of the text.

2. **Transformer-Based Encoding**: The segmented text is processed using a Transformer encoder, which converts the text into numerical vectors, capturing relationships between words and phrases using the **Attention** mechanism.

3. **Transformer-Based Decoding**: The decoder takes the encoded vectors and generates a corrected version of the text, applying knowledge gained during fine-tuning on spelling correction datasets.

## proposed solutions 

In our project, we explore two distinct solutions to address spelling correction:

-**Solution 1**: Using the **HappyTextToText** class from the **Happy Transformer** package, we fine-tuned the **T5-base** model, which demonstrated promising results with fast and efficient spelling correction. The model was fine-tuned using the **JFLEG (Joint Foreign Language Evaluation Corpus)**. You can access the JFLEG dataset [here](https://github.com/keisks/jfleg).

-**Solution 2**: We employed a more manual approach to fine-tuning the **T5-small** model. This approach allowed for a deeper exploration of the underlying mechanics of the Transformer model, providing more granular control and insight into its capabilities.
In this solution, we used a different dataset, the **Grammar Correction Dataset**, which can be downloaded [here](https://www.kaggle.com/datasets/pranav082001/grammaratical-error-correction-dataset/data).  
We used Hugging Face Spaces to create a user interface. Users can input their text, and the corrected text produced by our model will be displayed below. You can access our space on Hugging Face [here](https://huggingface.co/douha/T5_SpellCorrector2).

