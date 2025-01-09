# Review of "Do Transformers Really Perform Bad for Graph Representation?"

## Summary
This paper tackles the challenge of using Transformers for graph representation learning, a domain where they traditionally struggle. The authors introduce **Graphormer**, a Transformer-based model that incorporates graph-specific information through three clever techniques: 
- **Centrality Encoding** (to capture node importance)
- **Spatial Encoding** (to account for relationships between nodes)
- **Edge Encoding** (to leverage features on graph edges).

Their approach not only makes Transformers work for graphs but achieves state-of-the-art results on several benchmark datasets, like the OGB Large-Scale Challenge.

![Graphormer Encodings](https://github.com/user-attachments/assets/24d61fc6-cc86-48e1-810c-c4d9f7545e96)

*Figure 1: An illustration of Centrality Encoding, Spatial Encoding, and Edge Encoding in Graphormer.*

---

## Strengths
1. **Creative Solution**: The paper creatively adapts Transformers for graphs by introducing structural encodings, which is a smart and innovative approach.
2. **Strong Results**: Graphormer achieves excellent performance, often beating traditional graph neural networks (GNNs), showing its potential as a game-changer.
3. **Solid Theoretical Backing**: The authors explain how Graphormer can match or even surpass the capabilities of popular GNNs, which adds a lot of credibility to their work.
4. **Practical Focus**: The fact that they’ve shared their code and pre-trained models is a huge plus—it shows they’re committed to helping others use and build on their work.
5. **Thorough Experiments**: The evaluation on multiple datasets and the detailed comparisons with existing methods make the results feel robust and trustworthy.

---

## Weaknesses
1. **Scalability Issues**: Like other Transformer models, Graphormer has a quadratic complexity in its self-attention, which makes it harder to use for very large graphs.
2. **Risk of Overfitting**: With its large model size and the small size of some datasets, there’s a real risk of overfitting, which they had to address with extra data augmentation.
3. **Heavy Dependence on Pretraining**: The model shines with pretraining on big datasets, but that’s not always an option for smaller teams or less common use cases.
4. **Limited Exploration of Alternatives**: While the encodings are great, it would’ve been nice to see a discussion of other possible ways to adapt Transformers for graphs.

---

## Suggestions
1. **Make it Scalable**: To handle large graphs, it would be great to explore more efficient attention mechanisms or ways to sample graphs effectively.
2. **Broaden Comparisons**: Comparing Graphormer with other Transformer-based GNNs across a wider variety of datasets could give a fuller picture of its strengths and weaknesses.
3. **Deeper Ablation Studies**: The ablation studies are helpful but could dive even deeper into how much each component contributes to performance.
4. **Domain-Specific Tweaks**: Tailoring the encodings for specific fields like molecular chemistry or social networks could unlock even better results.
5. **Simplify Pretraining**: Finding ways to reduce the cost and complexity of pretraining would make this model more accessible to everyone.

---

## Closing Remarks
This paper is an exciting leap forward for using Transformers in graph learning. Graphormer’s ability to integrate structural graph information makes it a strong alternative to traditional GNNs. While there are still challenges like scalability and the need for heavy pretraining, the work opens up a lot of possibilities.

---

## Contributors

- **1805017 - Rizvan Jawad Ruhan**
- **1905020 - Gazi Fardin Zafor Suvro**
- **1905021 - Sakib Mohammed Sobaha**
