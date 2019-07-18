# Results
## Part 1 Derviations
Please see "Homework_2_p1.pdf".

## Cart Pole
### Large Batch
<p float="left">
  <img src="./results/lb_cartpole.png" width="350"/>
</p>

### Small Batch
<p float="left">
  <img src="./results/sb_cartpole.png" width="350"/>
</p>

## Inverted Pendulum
### Batch 1000, LR varied
<p float="left">
  <img src="./results/ip_b1000_lrvaried.png" width="350"/>
</p>
LR = 0.01 was best

### Batch 2000, LR varied
<p float="left">
  <img src="./results/ip_b2000_lrvaried.png" width="350"/>
</p>
LR = 0.01 was best

### Tiny batch, LR .02
<p float="left">
  <img src="./results/ip_bvaried_small_lr02.png" width="350"/>
</p>
Did this as a fun exercise to see how small the batch could go while still spiking to the score of 1000. This mainly demonstrates that having a good seed can lead to great results much faster (10x) than a bad one.

## Half Cheetah
### Batch 10k, LR varied
<p float="left">
  <img src="./results/hc_b10k_lrvaried.png" width="350"/>
</p>
LR .02 was best

### Batch varied, LR .02
<p float="left">
  <img src="./results/hc_bvaried_lr02.png" width="350"/>
</p>
Batch 50000 was best

### RTG/NN Baseline Comparison
<p float="left">
  <img src="./results/hc_rtg_nn_comparison.png" width="350"/>
</p>

## Lunar Lander
This was a challenge. After getting the most recent version of Box2D to work, fixing an issue with the continuous log prob (one that the inverted pendulum did not pick up), setting gamma to .9999, and the actions properly clipped, the learning was still collapsing:
<p float="left">
  <img src="./results/ll_failure_ll_copy.png" width="350"/>
</p>

Supposing that the learning rate was too high, turning down the learning rate helped, but then the high score (180) wasn't reached by the end of the 100 iterations:
<p float="left">
  <img src="./results/ll_b40k_lr002.png" width="350"/>
</p>

Trying again with same learning rate, but with a batch size of 50k, it's a little worse. (Thanks, cat, for terminating my experiment early, even though it was dying anyway. Just because it is made of warm doesn't mean it is meant for sits.)
<p float="left">
  <img src="./results/ll_b50k_lr002.png" width="350"/>
</p>
