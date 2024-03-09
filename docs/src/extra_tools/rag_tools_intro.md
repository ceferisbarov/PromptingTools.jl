```@meta
CurrentModule = PromptingTools.Experimental.RAGTools
```

# RAG Tools Introduction

`RAGTools` is an experimental module that provides a set of utilities for building Retrieval-Augmented Generation (RAG) applications, ie, applications that generate answers by combining knowledge of the underlying AI model with the information from the user's knowledge base.

Import the module as follows:

```julia
# required dependencies to load the necessary extensions!!!
using LinearAlgebra, SparseArrays 
using PromptingTools.Experimental.RAGTools
# to access unexported functionality
const RT = PromptingTools.Experimental.RAGTools
```


## Highlights

The main functions to be aware of are:
- `build_index` to build a RAG index from a list of documents (type `ChunkIndex`)
- `airag` to generate answers using the RAG model on top of the `index` built above
- `annotate_support` to highlight which parts of the RAG answer are supported by the documents in the index vs which are generated by the model
- `build_qa_evals` to build a set of question-answer pairs for evaluation of the RAG model from your corpus

See example `examples/building_RAG.jl` for an end-to-end example of how to use these tools.

The hope is to provide a modular and easily extensible set of tools for building RAG applications in Julia. Feel free to open an issue or ask in the `#generative-ai` channel in the JuliaLang Slack if you have a specific need.

## References

```@docs; canonical=false
build_index
airag
annotate_support
build_qa_evals
```