# Long_video_qa


Long Video question answering(LVQA) is a challenging task for vision language models(VLMs). Long Videos contain thousand of frames. LVQA generally requires a frame selection or token reduction strategy to reduce the number of input frames to VLMs. In this project, we take a state of the art frame selection method [Videotree](https://arxiv.org/abs/2405.19209) and improve it in a training free manner for the [egoschema](https://arxiv.org/abs/2308.09126) test set.

## Method

1. First, frames are selected using depth-expansion and breadth-expansion to create frame clusters with the Videotree method.  
2. Videotree selects a number frames using clusters and then pass to an LLM to generate answer. We took the same approach, with a VLM. Since there are too many frames to pass directly to the VLM, we further iteratively find similarity between two frames and reduce redundant frames


## Result

Our method outperforms Videotree by 7 percent on the egochema dataset.

## This is a work in progress. Further ablation and result will be released in the future
