---
layout: page
title: Algorithmic Bidding in Procurement Auctions
description: Deep-learning algorithms can bid above cost to inflate the price, leading to critical efficiency losses on supply chains. 
img: assets/img/Deep_Learning_Applications.jpg
importance: 1
category: working papers
related_publications: false
---

**Status: Submitted to _Management Science_** (with Meng Li & Saunak Kumar Panda)

(Full draft is available <a href="https://drive.google.com/file/d/1UVDtQDdVut3rDfC-NN9zEkXM-YCm99f6/view?usp=share_link">here</a>)

Abstract  

As online auction platforms evolve, bidders' use of artificial intelligence (AI) has become increasingly prevalent for strategic advantages. This paper investigates the algorithmic bidding behavior in second-price procurement auctions, focusing on AI bidders trained by a model-free value-based reinforcement learning algorithm: the Deep Q-Network (DQN). Our experiments reveal a distinct tendency for overbidding (to bid above the cost) as the algorithm converges, shown in the Figure 1 below. 

<div class="row">
    <div class="col-sm-12 d-flex justify-content-center mt-1 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/comparebid.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Figure 1. Average Bids at Stable Convergences with N=2 and 10
</div>

The extent of overbidding intensifies with increased competition, captured by the N as the number of the bidders, exposing a discrepancy between the algorithmic behavior and the strategy predicted by the Nash equilibrium. To explain the underlying mechanism, we develop an analytical model that characterizes an algorithmic equilibrium within the DQN framework, as the Figure 2 below depicts, demonstrating how overbidding arises from internalizing the positive externalities it generates on opponents' rewards.

<div class="row">
    <div class="col-sm-12 d-flex justify-content-center mt-1 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/idqn.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Figure 2. Deep Q-Neural Network Learning Mechanism
</div>

In particular, we show that the "incentive" to overbid arises whenever the positive externalities of overbidding internalized through the feedbacks observed from the environment outweigh the direct negative impact it has on the bidder's reward, illustrated by the Figure 3 below: 

<div class="row">
    <div class="col-sm-12 d-flex justify-content-center mt-1 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/overbideffects.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Figure 3. "Incentive" to Overbid Generated through DQN
</div>

We further study conditions that promote overbidding, underscoring the challenges posed to existing antitrust regulations. In response, apart from reducing the competition intensity by limiting the number of bidders, we propose strategies for refining market environments and adjusting information input to mitigate overbidding, supported by assessments through further experiments with specific treatments. In the results shown in Figure 4 and Figure 5 below, we can see that the inflation in the bids (or the price in the procurement auction) can be effectively mitigated when there is a lower reserve as the price ceiling and whenever there is a limited number of bidders with an additional information about the previous lowest bid observed by DQN every round. 

<div class="row">
    <div class="col-sm-6 d-flex justify-content-center mt-1 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/comparebidmax2.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm-6 d-flex justify-content-center mt-1 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/comparebidmax10.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Figure 4. Average Bids with Lower Reserve
</div>

<div class="row">
    <div class="col-sm-6 d-flex justify-content-center mt-1 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/information2.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm-6 d-flex justify-content-center mt-1 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/information10.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Figure 5. Average Bids with Additional Information to Bidders 
</div>

We also extend to the case where the auctioneer adaptively anchors the reserve to prevent overpaying. However, it shows, in the Figure 6 below, this would not reduce the risk of overbidding as the DQN bidders can learn about this anchoring on reserve and overbid to fix it at a high level. 

<div class="row">
    <div class="col-sm-6 d-flex justify-content-center mt-1 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/anchor2.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm-6 d-flex justify-content-center mt-1 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/anchor10.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Figure 6. Average Bids with Anchoring on Reserves
</div>

Based on these findings, the study offers critical implications for regulatory oversight, advocating for the careful integration of AI in procurement auction markets to foster technological innovation while maintaining effective governance.

