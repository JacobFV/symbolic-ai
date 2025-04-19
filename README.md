# Symbol AI

## Core assumptions

1. Compositional symbolic abstraction and generalization--including the symbol of the self--is the principle objective of AGI

2. System dynamics and problem objectives are usually defined at differennt layers of abstraction. Abstrcations defined under a given context provide a low dimensional representation of system dynamics and the more faithful an abstraction is to the underlying latent structure it represents, the more stable it remains through Bayesian update (ie, the generalizble context increases).

3. Equivalently for model-based agents (not necesarily model-based RL), abstractions provide a low dimensional handle their world model which allows directly exploring and manipulating the latent structure of its cognition, and again, the closer these abstractions aligns with its underlying dynamics, the better they generalize. World models used to be constructed directly in symbolic form allow perfect representation fidelity and reduce abstractions to symbolic identities. However subsymbolic methods like embedding representations minimizes the exponential complexity of increasing symbolic dimensionality and are more grounded in the underlying latent structure of the universe anyways.

4. Compositional symbolic abstraction iteratively decomposes the fronteir of a bulk representation into discrete symbolic constituients, ie, subgraphs factored from the bulk. (Pairwise embeddings like token embeddings are implicit representations of individual nodes in their metric space but internal embeddings are subject to other competing objectives which decreases the utiltiy of this interpretation.

5. When working with already abstrcated graph structures, factorization enables isolating the locus of attention to a minimial set of nodes of manageable complexity as well as composing multiple symbols into new ones of exponentially increasing complexity (eg, joining two subgraphs into one graph). The imprecision/infidelity of individual constituients also factored which limits how useful compositions of increasing scale are but error factorization property can also be useful for peeling off uncertainty or for joining constituients in a way such that their individual imprecisions marginalize each other out.

6. Tokens are subsymbolic. Even though they are much sharper expressions of patterns than pixels or touch sensor observations, tokens are usually not identicle to symbolic identities themselves! Symbolic reasoning is still at a higher plane of abstraction than the token completion process.

7. LLMs don't "think" symbolically; they predict tokens based on patterns, not over persistent object-level state. The symbolic graph is formed by the pattern of attention and interaction across embeddings — not stored in a single token or layer. But this graph is weakly defined and exists in a noisy space with competing mechanisms operating in the same activation space. LLMs appear to have strong short-term memory via attention, but fail to maintain consistent symbolic state. 

8. ENgineers currently compensate for the imperfect ability of LLMs to think symbolically with external mechasnisms that require the LLM to pass a threshold of 

## Initial Experiments on symbolic reasoning

1. How much symbolic load can different LLMs handle?
    1. How does parameter count affect performance under differnt symbolic loads?
    2. How does qualitatively distinct architectures affect performance under different symbolic loads?
        1. Attention vs. SSM vs external memory
        2. Different attnetion variants: vanilla, sparse, w/o PEs, w/ RoPe, ...
        3. Number of attention heads
        4. Attention head dimensionality
        5. Internal embedding dimensionality
    3. What are signs that an LLM is saturating its abstraction ability
2. How much symbolic load do different tasks require?
    1. How can I build a compressed reprentation of a task complexity? (Maaybe this isn't important)
3. Identifying symbolic processing mechanisms in existing architectures
    1. How much of the middle layer activations of an LLMs can be explained as building an implicit graph representation (formed by the dynamic interplay of all the successive 'instructions' for each middle token, ie, add-edge, remove-edge)?
4. How can I synthesize symbolic compositions of increasing depth without loosing realism (ie, not just procedurally generated syntax trees of increasing depth)

## Initial practical application: long context reasoning and many-symbol reasoning

1. What long context reasoning tasks benefit from taking a symbolic perspective? (as opposed to needle-in-haystack tests)
2. When long context reasoning fails, is it usually that hte symbols were never propperly abstracted from the subsymbolic token representation or that the symbolic retreival itself failed or that the symbolic transofmration itself failed?
3. How can transformers architecture and weights be modified to concentrate attention on symbols rather than subsymbolic features
4. How can I test LLMs on tracking and manipulating increasingly many symbols

## Practical objectives toward stronger AI

1. It seems like a lot of tasks and benchmarks are trying to teach LLMs to perform compositional symbolic abstraction and generalization using proxy tasks, but the LLMs mostly prefer to memorize subsets of the patterns rather than grok the underlying latent structure of learning itself
2. If we could directly quantify symbolic abstractions and generalization capability of a given token completion engine, we would be able to build more general reward functions

## Quantifying symbolic self-awareness

1. The self as a symbol is distinct from the self as a subsymbolic zombie
2. What experiment measure symbolic abstraction of the self as opposed to just parrot-level understanding
