# Advanced Quiz Answers

**1. When should you use 'replicas'?**

- [:heavy_check_mark:] When you want to run multiple executors in parallel to increase throughput and availability.
- &#x2610; When you want to partition big indices
- &#x2610; When you need to segment large texts into smaller chunks
- &#x2610; When you need to segment large texts into smaller chunks

**2. What is a valid signature for a function that uses the  @requests decorator?**

- &#x2610; def foo(self, docs, *args)
- &#x2610; def foo(docs, **kwargs)
- [:heavy_check_mark:] def foo(self, docs, parameters, **kwargs)
- &#x2610; def foo(cls, docs, docs_matrix, **kwargs)

**3. How to control mesage overflow at the Executor?**

- &#x2610; Use prefetch>0 with the Client
- [:heavy_check_mark:] Use prefetch>0 while starting the Flow
- &#x2610; Use shards>1 with the Executor
- &#x2610; Use overload=0 environment variable in the Executor

**4. How to override the `with` configurations when using an Executor from Jina Hub?**

- [:heavy_check_mark:] Use uses_with argument
- &#x2610; Use overide_with argument
- &#x2610; Use with argument
- &#x2610; Use customized_with argument

**5. How to provide custom models to containerized Hub encoders?**

- [:heavy_check_mark:] Use the volumes parameter to specify a disk volume that contains the model files and specify the custom model path in the Executor parameters
- &#x2610; Upload the custom model to HuggingFace
- &#x2610; Specify the custom model path in the Executor parameters
- &#x2610; It is not possible with Jina

**6. Which amongst these is not a right syntax to use an already existing Executor from Hub?**

- &#x2610; Executor.from_hub('jinahub://DummyHubExecutor')
- &#x2610; Flow().add(uses='jinahub+docker://DummyHubExecutor')
- [:heavy_check_mark:] DocumentArray.load_from('jinahub://DummyHubExecutor')
- &#x2610; Flow().add(uses='jinahub://DummyHubExecutor')

**7. Which is correct about the retention policy for the Flows deployed on JCloud?**

- &#x2610; Flows are kept forever.
- &#x2610; By default Flows will be removed after 24 hrs, regardless of whether it's in use / has been used or not.
- [:heavy_check_mark:] You can configure the Flow retention days in Flow YAML.

**8. How can I make sure Executors only receive Documents meeting certain conditions?**

- &#x2610; Adding Flow().add(condition=...) with condition beind defined with DocArray query language
- &#x2610; Adding Flow().add(when=...) with condition being defined with DocArray query language
- [:heavy_check_mark:] Adding Flow().add(when=...) with condition being defined with your own query language
- &#x2610; Adding Flow().add(condition=...) with condition beind defined with your own query language

**9. What is the way Jina exposes to check the readiness of a Flow from a Client?**

- [:heavy_check_mark:] client.dry_run()
- &#x2610; client.health_check()
- &#x2610; client.post()
- &#x2610; client.index()

**10. How can you monitor the Flow?**

- [:heavy_check_mark:] Flow(monitoring=True, port_monitoring=9090) and scrape metrics using Prometheus
- &#x2610; Send a HTTP request to each Executor
- &#x2610; Flow(monitoring=True, port_monitoring=9090) and client.monitor(port=9090)
- &#x2610; Monitoring is available only in JCloud
