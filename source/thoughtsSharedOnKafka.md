# Thoughts Shared on Kafka

### A developer goes over his favorite resources on Apache Kafka, giving a brief synopsis of each. Hopefully you'll find something to add to your library!


This is a collection of interesting articles, best practices, case studies, and some books (on data and logs) I came across while working with Kafka.

## Articles

1.  [Kafka in a Nutshell](https://sookocheff.com/post/kafka/kafka-in-a-nutshell/). Published on September 25, 2015, by Kevin Sookocheff. Kevin’s article is all about Kafka in a nutshell. He says “Kafka is quickly becoming the backbone of many organization’s data pipelines — and with good reason. By using Kafka as a message bus we achieve a high level of parallelism and decoupling between data producers and data consumers, making our architecture more flexible and adaptable to change.” If you have not read about Kafka yet, you must go through it. This is more like an executive summary of the what, where, and why of Kafka.
2.  [Should you put several event types in the same Kafka topic?](http://martin.kleppmann.com/2018/01/18/event-types-in-kafka-topic.html)  Published by Martin Kleppmann on January 18, 2018. Martin Kleppmann has focused on why the number of partitions matters. He says, "as a rule of thumb, if you care about latency, you should probably aim for (order of magnitude) hundreds of topic-partitions per broker node. If you have thousands or even tens of thousands of partitions per node, your latency will suffer. Most of the time we get confused about whether it’s a good practice to have multiple events on the same topic or we should have one is to one. When you use different topics for similar events you might end up with ordering issues." Kleppmann has discussed all the points about latency, performance, ordering and best practices in this article.
3.  [How to choose the number of topics/partitions in a Kafka cluster?](https://www.confluent.io/blog/how-choose-number-topics-partitions-kafka-cluster)  Published by  [Jun Rao](https://www.confluent.io/blog/author/jun-rao/ "View all posts by Jun Rao"), who said “the degree of parallelism in the consumer (within a consumer group) is bounded by the number of partitions being consumed. Therefore, in general, the more partitions there are in a Kafka cluster, the higher the throughput one can achieve.” A partition is directly mapped to the file system in the broker. This article is having views on how the file system behaves with the increase in the partition. Also, the discussion is on the latency getting affected by the number of partitions.
4.  [Why I am not a fan of Apache Kafka](https://gist.github.com/markrendle/26e423b6597685757732). Published by  [Mark Rendle](https://gist.github.com/markrendle). Mark has some points like “If you are using Java/Scala/Clojure/Kotlin/whatever and can use the Official Java Client then I’m sure Kafka is a perfectly reasonable choice for a message bus, although there are plenty of others that seem to me to be far less bloody-minded.” Kafka cannot solve all the problems you have. This blog post is more about why Kafka is not a good choice for some scenarios and what the alternatives are.
5.  [Best practices](https://blog.newrelic.com/engineering/kafka-best-practices/)  by  [Tony Mancill](https://blog.newrelic.com/author/tonymancill/), August 1, 2018. Tony says, "Kafka has gained popularity with application developers and data management experts because it greatly simplifies working with data streams. But Kafka can get complex at scale." This is one of the great articles on best practices if you are really worried about the industry standard and the adaptability of Kafka. The article has a different section of best practices like partitions, consumers, producers, and brokers.

## Case Studies

I went through different case studies where companies have used Kafka at a large scale and have written about their experience with this streaming technology.

1.  [New York Times](https://www.confluent.io/blog/publishing-apache-kafka-new-york-times/): Boerge Svingen has authored this post in the Confluent blog and has focused on the backend systems and described the new approach they developed to solve a problem, based on a log-based architecture powered by Apache Kafka. They call it the**_Publishing Pipeline_**. This is all about how Kafka is used for storing all the articles ever published by The New York Times.
2.  [Keystone Pipeline](https://medium.com/netflix-techblog/kafka-inside-keystone-pipeline-dd5aeabaf6bb)  at Netflix, by the  [Netflix Technology Blog](https://medium.com/@NetflixTechBlog?source=post_header_lockup). This case study is about Netflix’s data pipeline called the Keystone pipeline, which is a unified event for publishing, collecting, and routing infrastructure for both batch and stream processing.
3.  [Linkedin’s Scale](https://engineering.linkedin.com/kafka/running-kafka-scale): How Big is Big? This has been answered by the creator of Kafka, you will get a view on the experience of running Kafka at a scale. Kafka provides reliability, resiliency, and retention, all while performing at high throughput.

## Books on Data and Logs

  

![Image title](https://images-na.ssl-images-amazon.com/images/I/51e0O8eNQ6L._SX386_BO1,204,203,200_.jpg)

[Designing Data-Intensive Applications by Martin Kleppmann](https://learning.oreilly.com/library/view/designing-data-intensive-applications/9781491903063/cover.html)

[Amazon](https://www.google.com/aclk?sa=L&ai=DChcSEwicye25_NHfAhVLHSsKHWXZAIQYABABGgJzZg&sig=AOD64_0x5Va1uenjoHj4R-rOYgFm6qiQ9w&ctype=5&q=&ved=0ahUKEwi2i-a5_NHfAhVGMI8KHTikAPYQ9A4IjwE&adurl=)

“Data outlives code.” - Martin Kleppmann

This book comes to your rescue when you are really concerned about your data which is the biggest challenge in system design and you are worried about issues such as scalability, consistency, reliability, efficiency, and maintainability.

  

![Image title](https://covers.oreillystatic.com/images/0636920034339/lrg.jpg)

[I ♥ Logs by Jay Kreps](https://learning.oreilly.com/library/view/i-heart-logs/9781491909379/titlepage01.html)


[O'REILLY](http://shop.oreilly.com/product/0636920034339.do) | [Amazon](https://www.amazon.in/Heart-Logs-Stream-Processing-Integration-ebook/dp/B00NUGHIU6/ref=sr_1_1?s=books&ie=UTF8&qid=1546531554&sr=1-1&keywords=I+Heart+Logs)

This is a book on logs and how they work on distributed systems. Jay has given practical ideas on data integration, enterprise architecture, real-time stream processing, data system design, and abstract computing models.

N.B: These are some of my favorite articles, case studies or books. If you have any worth sharing, please put that in the comment section.

Until next time, keep smiling!
