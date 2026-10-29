### Why Multi-stage Pipelines Matter
* Cannot have one massive model that generates predicts for all at speed and scale. 

### Anatomy of a Multi-stage Pipeline

1. Candidate Generation
- Candidate generation is the first and widest stage of the pipeline. Its job is to retrieve a manageable subset of items from the full catalog—typically reducing hundreds of millions of items down to tens of thousands.
- The output of this stage is a candidate pool: a large but tractable set of items that are plausibly relevant to the user.

2. Filtering L0 and L1
- L0 filtering applies hard rules. These are binary, non-negotiable exclusions executed via fast bitmask operations or key-value lookups
- L1 filtering applies softer, contextual constraints. These rules are still relatively lightweight but require some awareness of live user context

3. Light Ranking
- Light ranking is the first stage where a machine learning model scores candidates. The model used here is intentionally simple—fast to evaluate, with a low memory footprint, and capable of processing thousands of candidates within a few milliseconds.

- Typical light ranking models use logistic regression, gradient-boosted decision trees (such as XGBoost or LightGBM), or small neural networks with sparse feature inputs. The goal is not to produce a perfect ranking—it is to make a fast, reasonably accurate cut from thousands of candidates down to hundreds.

4. Heavy Ranking
- Heavy ranking is where the most sophisticated model in the pipeline runs. By this stage, the candidate pool has been reduced to hundreds of items—a size that makes it feasible to run deep neural networks, transformer-based models, or large multi-task learning architectures.

5. Business Rules and Diversity Constraints 
- The final stage of the pipeline is not a model—it is a strict business-rule layer. After a heavy ranking produces a scored and ordered list, deterministic business rules are applied to shape the final output layout.

### Formulating Pipeline Architecture 
- Don't want to put all the notes and images into notes. 

### Explore Funnel Reduction Logic 
