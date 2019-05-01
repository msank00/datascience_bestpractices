# Deep Learning Best Practices - Mistakes and Tips

The purpose of this repo is to consolidate all the **Best Practicies** for building neural network model curated over the internet

- Try to overfit a single batch first
  - It's a very quick sanity test of your wiring; i.e. if you can't overfit a small amount of data you've got a simple bug somewhere 
  - it's by far the most "bang for the buck" trick that noone uses that exists.
5 replies 7 retweets 219 likes
- Forgot to toggle train/eval mode for the net
- Forgot to `.zero_grad()` (in pytorch) before `.backward()`.
- Passed `softmaxed outputs` to a loss that expects `raw logits`.
- You didn't use `bias=False` for your `Linear/Conv2d` layer when using `BatchNorm`, or conversely forget to include it for the output layer .This one won't make you silently fail, but they are spurious parameters
- Thinking `view()` and `permute()` are the same thing (& incorrectly using view)
- starting with `small model` + `small amount of data` & growing both together; I always find it really insightful
  - I like to start with the simplest possible sanity checks - e.g. also training on all zero data first to see what loss I get with the base output distribution, then gradually include more inputs and scale up the net, making sure I beat the previous thing each time.
- ...
  
------

**Read the below references**

These are pure gold.

#### Reference

- [tweet_andrej_karpathy](https://twitter.com/karpathy/status/1013244313327681536)
- [Recipe for training neural network](https://karpathy.github.io/2019/04/25/recipe/)
- [What should I do when my neural network doesn't learn?](https://stats.stackexchange.com/questions/352036/what-should-i-do-when-my-neural-network-doesnt-learn)
- [Practical Advice for Building Deep Neural Networks](https://pcc.cs.byu.edu/2017/10/02/practical-advice-for-building-deep-neural-networks/) 