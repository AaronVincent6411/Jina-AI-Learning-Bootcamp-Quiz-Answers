# Intermediate Quiz Answers

**1. What does an Executor do?**

- &#x2610; An Executor is the tool you use to execute your Flow from the CLI: execute jina_app.py
- &#x2610; An Executor is a processing pipeline for indexing or querying a dataset
- [:heavy_check_mark:] An Executor performs a single task on a Document or DocumentArray, like segmenting or encoding it.

**2. What does a Flow do?**

- [:heavy_check_mark:] The Flow ties Executors together into a processing pipeline to perform a bigger task, like indexing or querying a dataset.
- &#x2610; The Flow is a graphical interface that lets users see how their Documents are flowing into the processing pipeline.
- &#x2610; The Flow is short for "fast, low-resource" and is a special kind of Executor for low-powered machines.
- &#x2610; The Flow helps you visualize the input and the output flow of data.

**3. What's the recommended way to share Executors with a colleague?**

- &#x2610; Send them a link to the repo
- &#x2610; Dockerize your Executor and push directly to Docker Hub
- &#x2610; Push your Executor to Pypi and ask them to install via pip
- [:heavy_check_mark:] Push your Executor to Jina Hub and share

**4. Given a Document doc, what does doc.content refer to?**

- &#x2610; doc.tensor
- &#x2610; doc.blob
- &#x2610; doc.text
- [:heavy_check_mark:] Any of the above as long as the field is not empty

**5. What is the best way to embed Documents in a DocumentArray**

- &#x2610; loop over Documents and compute embeddings
- &#x2610; Iterate over batches of Documents and compute embeddings in batches
- [:heavy_check_mark:] Use method DocumentArray.embed
- &#x2610; Create a new DocumentArray with computed embeddings

**6. What formats are supported for creating Executors?**

- &#x2610; YAML
- &#x2610; JSON
- &#x2610; Python
- [:heavy_check_mark:] YAML and Python

**7. What function decorator is used to invoke an Executor?**

- [:heavy_check_mark:] @requests
- &#x2610; @start
- &#x2610; @invoke
- &#x2610; @jina_invoke

**8. What are the different ways to send request data in a Flow?**

- &#x2610; Document, DocumentArray, and None
- &#x2610; An iterator of Document
- &#x2610; A generator of Document
- [:heavy_check_mark:] All of them

**9. How can I store a DocumentArray in a database?**

- [:heavy_check_mark:] Use a different DocumentArray store
- &#x2610; Serialize the DocumentArray and store it in a database
- &#x2610; Create a relational database table for Document and use an ORM to persist Document to the table

**10. Which communication protocol(s) does the Flow support?**

- &#x2610; HTTP, ZMQ and Sockets
- [:heavy_check_mark:] GRPC, Websockets and HTTP
- &#x2610; GRPC, HTTP and ZMQ
- &#x2610; Websockets, GRPC and FTP
