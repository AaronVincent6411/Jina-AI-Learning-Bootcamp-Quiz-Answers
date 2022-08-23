# Intermediate Quiz Answers

**1. What does an Executor do?**

- [ ] An Executor is the tool you use to execute your Flow from the CLI: execute jina_app.py
- [ ] An Executor is a processing pipeline for indexing or querying a dataset
- [x] An Executor performs a single task on a Document or DocumentArray, like segmenting or encoding it.

**2. What does a Flow do?**

- [x] The Flow ties Executors together into a processing pipeline to perform a bigger task, like indexing or querying a dataset.
- [ ] The Flow is a graphical interface that lets users see how their Documents are flowing into the processing pipeline.
- [ ] The Flow is short for "fast, low-resource" and is a special kind of Executor for low-powered machines.
- [ ] The Flow helps you visualize the input and the output flow of data.

**3. What's the recommended way to share Executors with a colleague?**

- [ ] Send them a link to the repo
- [ ] Dockerize your Executor and push directly to Docker Hub
- [ ] Push your Executor to Pypi and ask them to install via pip
- [x] Push your Executor to Jina Hub and share

**4. Given a Document doc, what does doc.content refer to?**

- [ ] doc.tensor
- [ ] doc.blob
- [ ] doc.text
- [x] Any of the above as long as the field is not empty

**5. What is the best way to embed Documents in a DocumentArray**

- [ ] loop over Documents and compute embeddings
- [ ] Iterate over batches of Documents and compute embeddings in batches
- [x] Use method DocumentArray.embed
- [ ] Create a new DocumentArray with computed embeddings

**6. What formats are supported for creating Executors?**

- [ ] YAML
- [ ] JSON
- [ ] Python
- [x] YAML and Python

**7. What function decorator is used to invoke an Executor?**

- [x] @requests
- [ ] @start
- [ ] @invoke
- [ ] @jina_invoke

**8. What are the different ways to send request data in a Flow?**

- [ ] Document, DocumentArray, and None
- [ ] An iterator of Document
- [ ] A generator of Document
- [x] All of them

**9. How can I store a DocumentArray in a database?**

- [x] Use a different DocumentArray store
- [ ] Serialize the DocumentArray and store it in a database
- [ ] Create a relational database table for Document and use an ORM to persist Document to the table

**10. Which communication protocol(s) does the Flow support?**

- [ ] HTTP, ZMQ and Sockets
- [x] GRPC, Websockets and HTTP
- [ ] GRPC, HTTP and ZMQ
- [ ] Websockets, GRPC and FTP
