---
title: Frequently asked questions (FAQ) for document processing - AI Builder | Microsoft Docs
description: This topic provides answers to frequently asked questions about the document processing model in AI Builder.
author: JoeFernandezMS
ms.topic: conceptual
ms.custom: 
ms.date: 05/31/2022
ms.author: jofernan
ms.reviewer: angieandrews
---

# FAQ for document processing

This topic consists of frequently asked questions about the document processing model in AI Builder. If you don't find your question here, review the [overview of the document processing AI model](form-processing-model-overview.md) or submit your question to the [Power Automate Community for AI Builder](https://powerusers.microsoft.com/t5/AI-Builder/bd-p/AIBuilder).

## Functionality

### What can I do with document processing?

With document processing, you can build a custom AI model to extract information from documents. Document processing supports extracting data from structured, semi-structured documents like invoices, purchase orders, delivery orders, tax forms as well as unstructured documents such as contracts, statement of work, letters and others. Learn more: [Overview of the document processing model](form-processing-model-overview.md)

### What types of documents can document processing handle?

Supported file types are PDF, JPG, and PNG.

### What data can I extract from documents by using document processing?

document processing can extract fields, tables, and checkboxes from documents. Learn more: [Define information to extract](create-form-processing-model.md#define-information-to-extract)

### Can I extract handwritten text from documents?

Yes. Document processing can extract printed and handwritten text from your documents.

<!-- Can I extract tables that span across multiple pages?
Coming soon -->

### How many samples do I need to train a document processing model?

For high-quality documents that use the same layout, five sample documents should be sufficient. For low-quality documents (for example, scans of poor quality<!--note from editor: Suggested.-->), more sample documents might be necessary. To improve results, use 15 to 20 sample documents.

### Can a single form-processing model extract information from documents that have different layouts or templates?

Yes. By using the collections feature, you train a single form-processing model to handle documents that have different layouts. Learn more: [Group documents by collections](create-form-processing-model.md#group-documents-by-collections)

### Can document processing handle *multiple* forms in a *single* document?

Each form needs to be in a separate file. For example, if you have a PDF document with multiple invoices in it, create a separate file for each invoice before you send it to the document processing model.

You can also specify pages for the document processing model to handle. This way you can take advantage of the model's functionality to loop page by page, and process one form at a time. Learn more: [Page range](form-processing-model-in-flow.md#page-range)

### I've trained a document processing model but I'm not getting good results when it comes to extracted data. How can I improve the model?

If your model is returning poor results after you've trained it, edit the model and provide more samples for training. The more samples you provide, the more the AI model will learn how to extract data from your documents. Learn more: [Improve the performance of your document processing model](improve-form-processing-performance.md)

## Limitations

### What is the maximum number of documents I can process?

You can process up to 360 documents per environment, every 60 seconds.

### Can I use contracts and letters in my documents processing model?

Yes, unstructured documents like contracts and letters are supported by document processing. 

## Comparisons

### What are the differences among document processing, invoice processing, receipt processing, identity document reader, business card reader, and text recognition?

Depending on your situation, you might need to use a particular model or a combination of them.

Use [text recognition](prebuilt-text-recognition.md) when you want to extract all the text present in an image or a PDF. You can then, for example, search for a keyword in the text that's extracted or build some fixed rules to extract certain items.
 
If you want to extract information from invoices, receipts, passports, driver's licenses, or business cards, start with the corresponding prebuilt model:

- [Invoice processing](prebuilt-invoice-processing.md)
- [Receipt processing](prebuilt-receipt-processing.md)
- [Identity document reader](prebuilt-id-reader.md) (passports and driver's licenses)
- [Business card reader](prebuilt-business-card.md)

You can use these prebuilt models immediately, without having to create a new model. These models can extract common information found in their corresponding document type.

For any other document type, you can create a custom document processing model to extract the fields and tables you need. This also applies if you need additional information not provided by the prebuilt model. Learn more: [Custom document processing model](form-processing-model-overview.md)

### What is the difference between AI Builder document processing and Azure Form Recognizer?

AI Builder document processing is built on top of Azure Form Recognizer. This provides both products with the latest advancements in Microsoft AI.

- AI Builder is part of [Microsoft Power Platform](/power-platform/). This enables anyone to add AI into apps and automation with an easy-to-use interface. *You don't need to be a developer or data scientist*.

- [Azure Form Recognizer](/azure/applied-ai-services/form-recognizer/overview) is *targeted to professional developers*. They can use simple REST APIs to add AI capabilities to their custom code solutions.  

## Cost options

### How much does AI Builder document processing cost?

You can start trying out document processing for free by starting a [trial](administer-licensing.md). After you've evaluated it, you'll need to purchase AI Builder credits to use document processing. Every page you process with document processing will consume AI Builder credits. AI Builder credits can be purchased through AI Builder add-ons. Learn more: [AI Builder licensing](administer-licensing.md)
