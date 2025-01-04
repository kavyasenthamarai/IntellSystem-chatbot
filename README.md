# JorneAI : Your Travel Companion

## Project Overview:
This is a completed JorneAI Chatbot Project that provides travel-related advice through a conversational AI, including intent data, a neural network model, and a Gradio interface. To get started, review all provided resources to understand the project structure, including the intent data and the model. Follow the setup instructions in the README, install necessary dependencies, and train the model with the provided data.

## Procedure and Enhancements:
Ensure the chatbot meets basic requirements by verifying it responds correctly to user queries based on recognized intents. Once the core functionality is working, feel free to extend the project by adding new intents, improving performance, or enhancing the Gradio interface for a better user experience.

# Procedure
## Steps to Follow:

### Understanding the Project Objective:

   Review the README and familiarize yourself with the chatbot’s purpose.

### Setting Up the Environment:
   Install the required libraries: TensorFlow, Gradio, and NLTK.
### Data Preparation:
   Review the provided intent data.
   Explore creating your own additional intents for extended functionality.
### Model Training:
   Preprocess the data and train the neural network as described in the script.
### Testing and Fine-Tuning:
   Interact with the chatbot using Gradio.
   Identify any gaps in responses and modify intent data as needed.
### Documenting the Learning:
   Write a report doc on how the project was set up, the challenges faced, and how they were resolved.


## Table of Contents

1. [Introduction](#introduction)
    - [Overview](#overview)
    - [Features](#features)
    - [Project Objective](#project-objective)

2. [Getting Started](#getting-started)
    - [Installation](#installation)
    - [Dependencies](#dependencies)

3. [Intent Data](#intent-data)
    - [Structure of Intent Data](#structure-of-intent-data)
    - [Training Intent Data](#training-intent-data)

4. [Neural Network Model](#neural-network-model)
    - [Architecture](#architecture)
    - [Training Process](#training-process)

5. [Gradio Integration](#gradio-integration)
    - [Interface Setup](#interface-setup)

6. [Chat Functionality](#chat-functionality)
    - [User Input Processing](#user-input-processing)
    - [Model Prediction](#model-prediction)
    - [Intent Recognition](#intent-recognition)
    - [Response Generation](#response-generation)

7. [Training and Model Persistence](#training-and-model-persistence)
    - [Model Compilation](#model-compilation)
    - [Training Process](#training-process)
    - [Saving and Loading the Model](#saving-and-loading-the-model)

8. [Code Structure and Components](#code-structure-and-components)
    - [Main Components](#main-components)
    - [Functions and Methods](#functions-and-methods)

9. [Additional Information](#additional-information)
    - [NLTK Usage](#nltk-usage)
    - [Random Responses](#random-responses)
    - [User Input Handling](#user-input-handling)

---

## 1. Introduction

### Overview

JorneAI is a chatbot designed to assist users with travel-related queries and recommendations. It employs natural language processing and a neural network model to understand user inputs and generate appropriate responses.

### Features

- Intent recognition for various travel-related queries.
- Dynamic responses based on recognized intents.
- Integration with Gradio for a user-friendly interface.

### Project Objective

The primary objective of JorneAI is to provide users with personalized and engaging travel advice, helping them plan their trips effectively.

## 2. Getting Started

### Installation

To install JorneAI and its dependencies, use the following commands:
```
!pip install gradio
```
## Dependencies
Ensure the following dependencies are installed:
```
TensorFlow
Gradio
NLTK
```
## 3. Intent Data
### Structure of Intent Data
Intent data is structured in a JSON format with tags, patterns, and responses. Each intent represents a category of user queries.

```
{
    "intents": [
        {
            "tag": "greeting",
            "patterns": ["hi", "hello", "hey"],
            "responses": ["Greetings!", "Hello there!", "Hey!"]
        },
        ...
    ]
}
```
### Training Intent Data
The script preprocesses the intent data, tokenizes patterns, and trains the neural network using backpropagation.

## 4. Neural Network Model
## Architecture
JorneAI's model consists of an input layer, hidden layers, and an output layer. It uses the ReLU activation function for hidden layers and softmax for the output layer.

### Training Process
The model is compiled with the Adam optimizer and categorical crossentropy loss function. It is trained for 1000 epochs with a batch size of 8.

## 5. Gradio Integration
### Interface Setup 
Gradio is integrated to provide a simple text-based interface for users to interact with JorneAI.
```
iface = gr.Interface(fn=chat, inputs="text", outputs="text")
iface.launch()
```
## 6. Chat Functionality
### User Input Processing
User input is processed by tokenizing and stemming words using NLTK.

### Model Prediction
The model predicts the user's intent and generates a response based on the highest confidence.

### Intent Recognition
Intent recognition involves identifying the most probable intent from the model's predictions.

### Response Generation
Responses are generated based on the recognized intent, and a random response is selected from the predefined responses.

## 7. Training and Model Persistence
### Model Compilation
The model is compiled with the Adam optimizer, categorical crossentropy loss, and accuracy as a metric.

### Training Process
The model is trained on preprocessed data for 1000 epochs with a batch size of 8.

### Saving and Loading the Model
The trained model is saved as jornebot_model.h5, and preprocessing data is saved as preprocess_data.pkl.

## 8. Code Structure and Components
### Main Components
The script includes components for intent data, model architecture, training, user input processing, and response generation.

### Functions and Methods
Functions include those for cleaning up sentences, creating bag-of-words representations, and the main chat function.

## 9. Additional Information
### NLTK Usage
NLTK is used for tokenizing and stemming words in user input and intent patterns.

### Random Responses
Responses are randomly selected from the predefined responses for a more natural conversation flow.

### User Input Handling
User inputs are processed, and the chat function generates appropriate responses based on recognized intents.

