# Media Content Analysis

## Description
Description Generator Concept; CV Concept

## Content
1. [Complete] Image Data input (jpg, etc.…)
2. [Complete] Object detection: Fine-tune VGG166 Image Classification (subject, verb and confidence value)
    * Build
    * Train
    * Predict
3. [Complete] Scene detection: Keras + VGG16 + Places365 (place and confidence value)
4. [incomplete] Category Filter
    * [Complete] Fasttext & Textgrocery (Text Category and confidence value)
    * [Progressing] LCS Confidence + Subject Confidence 
5. [incomplete] NLP - Generate Sentence & Probabilistic
    * n-gram: [S V O P]
    * NLTK

## Outputs Data model
Recognization Data Format:  

    "Description": {
        "tags": [{
            "obj": "string",
            "label": "string",
            "confidence": value
        }, …],
        "caption": [{
            "text": "string",
            "confidence": value
        }],
        "category": [{
            "name": "string",
            "score": value
        }]
    }

## Detection&Recognition:
Keras + CRFasRNN
+ MaskRNN(attempt)...[Failed]
+ subject + facial + action + scene
 
## NLG(Natural Language Generation):  
n-gram + NLTK  
1. Raw text Processing
2. Sentence Segmentation (lists of strings)
3. Tokenization (sentences)
4. Categorizing and Tagging words (tokenized sentences)
5. Extracting, recognize the entities (pos-tagged sentences)
6. Analyzing sentence structure (chunked sentences)
7. Build grammars (relations)
 
Result:  

    Subject & score  
    +  
    Verb & score  
    +  
    Object & score  
    +  
    Context & score  
    +  
    Place & score  
  
Reference  
* https://keras.io
* https://github.com/matterport/Mask_RCNN
* https://github.com/sadeepj/crfasrnn_keras
* https://github.com/oswaldoludwig/Human-Action-Recognition-with-Keras
* https://github.com/jalajthanaki/Facial_emotion_recognition_using_Keras
* https://github.com/GKalliatakis/Keras-VGG16-places365/blob/master/vgg16_places_365.py
* https://github.com/keras-team/keras-contrib