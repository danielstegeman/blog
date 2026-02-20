The problems we face when developing with the assistance of AI are not new, they are simply of another scale. This is something I repeatedly say to colleagues. It is something that was highlighted again when I dove into the concept of Domain Driven Design over the course of a three day training. At the start of the training I set a secondary goal for myself: Figure out if and how Domain Driven Design could benefit agentic development.



Domain Driven Design is all about tackeling complexety and deviding it into meaningfull, managable chunks. During the course, we used chess as an example of a domain we worked in.

LLM's lack understanding of your specific domain. This understanding can be provided as context through meaningfull code. The use of value objects provides the same benefit as for human dev

Better separation of concerns limits nessecary context windows for specific problems. Instead of having to tackle a large complex problems, you can more easily devide it in chunks.

The concept of bounded contexts make the understanding of your subdomain more manageble by agents. Even the similaries in naming should be noted. With agentic development we are always talking about context as well. Since bounded contexts are (in principle) independent from eachother, there is little need to provide knowledge of other bounded contexts to the agent.

DDD is beneficial with a sufficiently complex domain, but for agents the bar of what qualifies as complex is much lower. So when using agentic development, you will benefit from DDD much sooner.

