---

title: "addendum to initiation"

date: 2023-04-20

---

<!-- more -->

In "initiation", I neglected to supply the broad strokes of my critique of the [Yuddites](/definitions#yuddites). This was intentional. "initiation" was intended as a syllabus, not a real post. While I promised [Residual Streams, Stochastic Depth Regularization, and Gradient Hacking](https://ajl.bio/2023/04/20/residual-streams-and-gradient-hacking.html) and [Zipfian Distributions and Yemlem Alignment](https://ajl.bio/2023/04/22/zipfian-distributions-and-yemlem-alignment.html) as the inaugural posts, I don't foresee there being room in those upcoming technical screeds for an overview of my thinking on realistic A(G)I threats. In lieu of including it in future publication's, I've outlined it below:

# Critique of the Yuddites
All natural sequence data we know of follows a Zipfian distribution, when ordered by the intelligence required to model them (see [this stub](https://ajl.bio/2023/04/20/intelligence-as-prediction-difficulty.html) for how intelligence is measured in (y/z)emlems). A Zipfian distribution is just lingo for a power law distribution over some naturally ordered set, where the frequency of an element is inversely proportional to its ranking under the natural ordering. The distribution of token sequences in language modeling follows a Zipfian distribution, where the ordering is given by the "difficulty" of modeling a given subset of sequences. For a beautiful and profoundly cogent exposition on this property of natural language, read [this work](https://arxiv.org/pdf/2303.13506.pdf).  

The Zipfian nature of natural language is what produces generalization-over-model-scale power laws. As you increase model size and data size, generalization (as measured by test perplexity) goes up. The Yuddites understand this, and repeat it ad nauseum. They cite it as the principal cause for AGI alarmism, claiming that model intelligence gains are outpacing model alignment gains. That claim is preposterous.  

Zipfian laws do not only apply to the pre-training behavior - they also apply to the learning of the reward function from human feedback that is eventually used to align the original instruction-tuned foundation model with human preferences. In terms of sample complexity, it is far easier to learn to label malicious token sequences as malicious than it is to generate them.  

The OpenAI API, to the best of my knowledge, does not employ input or output rejection safeguards to prevent malicious outputs. It relies on the sequence distribution used to train the policy being a superset of the test distribution (ie, the distribution over sequences that users input). Because of the Zipfian distribution over natural language sequences, the probability of a user discovering a malicious sequence decreases exponentially with the amount of user interactions collected, assuming each interaction is i.i.d. The ChatGPT free trial yielded billions of user interactions, all of which were used when optimizing the GPT-4 policy. OpenAI said as much in their technical report, and it is the principal reason for their competitive lead over Google and Anthropic.  

To summarize, the Yuddites' argument that capability is outpacing alignment is nonsense, assuming their own presuppositions. Alignment is actually outpacing capability, at least at OpenAI. The simplest way to ensure that holds for other labs' AI systems is to pressure OpenAI to make public an anonymized version of their user interaction data, so that it can be used to align other labs' models.

# The actual AGI danger
There is a syntactically similar version of the Yuddites' capability-outpacing-alignment claim that is veritable: capability is outpacing security. OpenAI's API is a sieve, and their model checkpoints are stored in Azure, which is also a sieve. It is second only to GCP in the porousness of its security measures.  

A breach leading to the leak of the foundation GPT-4 model would be catastrophic. Such an event is not without precedent. LLaMA was a family of large language models released publicly by FAIR, ostensibly for research purposes. A St. Louis-based hacker downloaded them legally, just as other researchers had, but he then proceeded to make them available through a torrent. The LLaMA models are now freely available on the dark web. They are foundation models; they are completely unaligned with human feedback. Any sequence fed to them will be completed. If you feed a foundation model the opening lines of ISIS monthly's June 2015 edition, it will proceed to tell you how to make a truck bomb far more sophisticated than anything some Levantine radical could build. Bombs aside, the largest of the leaked LLaMA models is only a tad smarter than GPT-3. It's potentially dangerous, but it'll probably fail to do long division. It certainly won't be able to write Stuxnet.  

In contrast, GPT-4 probably can write a novel in-memory virus, especially if it's fine-tuned on a database of malicious files. It is difficult to put into words how catastrophic a leak of a foundation [Yemlem](/definitions#yemlems) would be. Once it's hosted on the un-indexed web, it becomes impossible to claw back. A leak would force policymakers to introduce accelerator hardware permits to prevent unauthorized inferencing of Yemlems. While it's a terribly undemocratic measure, there would be no choice but to enact it in the event of a security breach of OpenAI/Anthropic/Google Deepmind's VPCs. Legislating security regulations is of the utmost priority, if we are to avoid the totalitarian measures a model leak would necessitate. I would even go so far as to temporarily support the Yuddites' calls to ban yottascale+ training runs until the appropriate security measures have been taken.

