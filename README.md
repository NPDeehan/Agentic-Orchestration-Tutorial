
# Message Delivery Service

## Overview

This BPMN process represents a Message Delivery Service that uses AI and human intervention to deliver messages effectively.

## Process Flow

1. **Start Event**: The process begins when a message needs to be delivered.

2. **AI Task Agent**: An AI agent processes the message, improving tone, spelling, and grammar. It also decides on the best delivery method.

3. **Decision Gateway**: The process checks if any tools need to be run.

4. **Niall's Tools**: If tools are needed, the process enters an ad-hoc subprocess with various delivery options:
   - **Deliver Message by Hand**: A human can be asked to deliver the message personally.

5. **End Event**: The process ends when the message is successfully delivered.

## Key Components

- **AI Task Agent**: Uses Bedrock's Claude 3 Sonnet model for message processing and decision-making.
- **Ad-hoc Subprocess**: Allows for flexible execution of delivery tools based on the AI agent's decision.
- **User Task**: Enables human intervention for hand-delivering messages when necessary.

## Technical Details

- The process uses Camunda Cloud for execution.
- AI integration is achieved through Bedrock's Claude 3 Sonnet model.
- The process includes error handling and retry mechanisms for the AI task.

## Forms

- A form is associated with the start event to capture initial message details.
- Another form is used for the "Deliver Message by Hand" user task.

This process combines AI capabilities with human intervention to ensure efficient and appropriate message delivery based on the context and requirements of each situation.

## Prerequisites
First you need a Camunda 8 SaaS account - you can use a trial account for free here: https://modeler.camunda.io/ 

Set up your LLM model provider and authentication	
Prior to using this connector, you must have previously set up an account with access and authentication details for the supported LLM model provider you want to use.

For example:
* To use an LLM model provided by Amazon Bedrock, you must have an AWS account with an access key and secret key to execute Converse actions.
* For OpenAI, you must configure the OpenAI model and obtain an OpenAI API key to use for authentication.