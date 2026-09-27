## Matthew Clinton

I'm a Lead Machine Learning Engineer at [Dstillery](https://dstillery.com/). Most of my
work there is data engineering, MLOps, and the pipelines behind our models. I have a
master's in computer science from UMass Amherst, with a concentration in data science.

Outside of work I make games for fun, and I've released around 20 of them at
[unitedfailures.itch.io](https://unitedfailures.itch.io/).

### Games and prototypes

- [burning-wood-versus](https://github.com/mfclinton/burning-wood-versus) is an online
  arena game I wrote in Rust over a summer. I built the multiplayer netcode, with an
  authoritative server, client prediction, and delta updates.
- [its-caturday](https://github.com/mfclinton/its-caturday) runs GPT-2 and RoBERTa
  locally inside a Unity game through ONNX Runtime. I wrote the inference and the
  tokenizers in C#. GPT-2 suggests and autocompletes words as you type, and RoBERTa
  scores how well each tweet fits the trending topic.
- [card-tree-puzzle](https://github.com/mfclinton/card-tree-puzzle) is a deckbuilding
  prototype played on a randomly generated tree. The game logic is plain C# with no
  Unity dependency, and it's unit tested.
- [diggity-diggity-dash](https://github.com/mfclinton/diggity-diggity-dash) is a mole
  racing game where you dig through terrain built on marching squares. The terrain is
  split into chunks, and digging only rebuilds the ones it touches. The AI racers use A*
  to find their way as the tunnels change.
- [pikmin-squad-prototype](https://github.com/mfclinton/pikmin-squad-prototype) is a
  Pikmin inspired prototype built on an entity component system I wrote on top of Unity.
- [say-cheese](https://github.com/mfclinton/say-cheese) is a game about spotting
  suspects in a crowd through security cameras. I built the procedural crowds, where everyone is put together
  from layered sprites and the suspects hide among decoys.
- [courier-crusaders](https://github.com/mfclinton/courier-crusaders) is a management
  game about running a fantasy courier company. I wrote the probability model behind
  events on the road, which shows your party's exact odds before you send them out.

### Machine learning

- [DISAPERE](https://aclanthology.org/2022.naacl-main.89/) is a NAACL 2022 paper I
  co-authored as a research assistant in the
  [Information Extraction and Synthesis Lab](https://www.iesl.cs.umass.edu/). It's a
  dataset of peer review discussions annotated with their discourse structure. I built
  early BERT baselines on the review data.
- [implicit_reward_optimization](https://github.com/mfclinton/implicit_reward_optimization)
  is reinforcement learning research I did with a PhD student in the
  [Autonomous Learning Laboratory](https://all.cs.umass.edu/). It learns a reward
  function and a discount function that keep an agent on the real goal. That lets
  hand-made helper rewards speed up learning without leading it astray when they're
  wrong. I wrote it in PyTorch and ran the hyperparameter sweeps on a Slurm cluster with
  Hydra and Nevergrad.
- [GANDataGeneration](https://github.com/andstu/GANDataGeneration) is a paper I co-wrote
  on training classifiers with synthetic data from GANs, to anonymize a dataset or to
  balance one. I wrote most of the GAN code, including the conditional convolutional
  GAN that worked best.
- [Image2Minecraft](https://github.com/andstu/Image2Minecraft) is a group project that
  turns a single image into a Minecraft build. I wrote the voxelizer, the matching of
  block textures to each voxel, and a CMA-ES search over block choices that scores
  each attempt by comparing renders.
- [Subreddit-Stock-Prediction](https://github.com/mfclinton/Subreddit-Stock-Prediction)
  was a group project for my NLP class on whether sentiment in subreddits like
  wallstreetbets tracks the market. I built the pipeline that pulls seven years of posts
  and comments from Reddit and labels them with stock prices. I also turned the
  sentiment of each post and its comments into features for a PyTorch classifier that
  predicts whether the stock a post mentions rises over the following week.
- [rl-policy-improvement](https://github.com/mfclinton/rl-policy-improvement) was a
  project for my reinforcement learning class. It searches for new policies with CMA-ES
  and keeps the ones that beat the old policy with high confidence, using importance
  sampling bounds on the old policy's data.

### Open source

- I've had fixes merged into the [Turbo](https://github.com/super-turbo-society/turbo-genesis-sdk)
  game SDK, like a [bounds check on network reads](https://github.com/super-turbo-society/turbo-genesis-sdk/pull/17)
  and [tinting for nine slice sprites](https://github.com/super-turbo-society/turbo-genesis-sdk/pull/21).
- For burning-wood-versus I added [2D point lights](https://github.com/mfclinton/burning-wood-versus/blob/main/shaders/light-shader.wgsl)
  to my fork of the Turbo engine, from the renderer and runtime bindings up through the
  SDK.
