# Relative Needs Entropy (RNE) Agent Trust Model
## Abstract

Cooperation in multi-agent and multi-robot systems can help agents build various formations, shapes, and patterns presenting corresponding functions and purposes adapting to different situations. Relationship between agents such as their spatial proximity and functional similarities could play a crucial role in cooperation between agents. Trust level between agents is an essential factor in evaluating their relationships' reliability and stability, much as people do. This paper proposes a new model called Relative Needs Entropy (RNE) to assess trust between robotic agents. RNE measures the distance of needs distribution between individual agents or groups of agents. To exemplify its utility, we implement and demonstrate our trust model through experiments simulating a heterogeneous multi-robot grouping task in a persistent urban search and rescue mission consisting of tasks at two levels of difficulty. The results suggest that RNE trust-Based grouping of robots can achieve better performance and adaptability for diverse task execution compared to the state-of-the-art energy-based or distance-based grouping models.

> Paper: https://ieeexplore.ieee.org/abstract/document/9659187

## Relative Needs Entropy Based Agent Trust Models
Similar to the information entropy, we define the needs entropy as the difference or distance of needs distribution between agents in a specific scenario for an individual or groups. Here, needs of the robots are regarded as their motivations. From a statistical perspective, the RNE can be regarded as calculating the similarity of high-dimensional samples from the robot needs vector. 
> A lower RNE value means that the trust level between agents or groups is higher because their needs are well-aligned and there is low difference (distance) in their needs distributions. Similarly, a higher RNE value will mean that the needs distributions are diverse, and there exists a low trust level between the agent or groups because of their misalignment in their motivations, which are similar to each other.

### Trust between Agents
<img src="http://latex.codecogs.com/svg.latex? Supposing~the~needs'~vectors~of~R_1~and~R_2~are~N_{R_1}(n_{11},~\dots,~n_{1j})~and~N_{R_2}(n_{21},~\dots,~n_{2j}),~where"/>
<img src="http://latex.codecogs.com/svg.latex? j~is~the~number~of~specific~needs~(categories)~in~the~needs~space.~Then,~through~the~corresponding~"/>
<img src="http://latex.codecogs.com/svg.latex? weight~vector~W(w_1,~\dots,~w_j),~we~get~the~needs'~distribution~of~two~agents~are~D_{R_1}(d_{11},~\dots,~d_{1j})~and"/>
<img src="http://latex.codecogs.com/svg.latex? D_{R_2}(d_{21},~\dots,~d_{2j})~respectively.~We~can~present~the~RNE~based~Trust~value~from~R_1~to~R_2~as~below."/>
<img src="http://latex.codecogs.com/svg.latex? Here,~d_{1k}~and~d_{2k}~are~calculated~as~below.~(j,~k~\in~Z^+)."/>

<div align = center>
<img src="http://latex.codecogs.com/svg.latex?\mathop{\mathbb{T}(R_1||R_2)} = \sum_{k=1}^{j} D_{R_{1_k}} \cdot \log \frac{D_{R_{1_k}}}{D_{R_{2_k}}}"/>
</div>

<div align = center>
<img src="http://latex.codecogs.com/svg.latex?D_{R_{1/2}} \ni \mathop{d_{1k/2k}} "/>
</div>

> Note: Please check the [paper](https://ieeexplore.ieee.org/abstract/document/9659187) for more details about the definitions of Trust between Agent and Groups and Trust between Groups.

Comparing with the natural intelligent agent, when the artificial intelligence (AI) agent becomes more advanced and smart, it also represents more complex, multilayered, and diverse needs in evolution such as individual security, health, friendship, love, respect, recognition, and so forth. When we consider intelligent agents, like robots, working as a team or cooperating with human beings, organizing their needs building certain reliable and stable relationships such as trust is a precondition for robot-robot and human-robot collaboration in complex and uncertain environments

## Numerical Evaluation
### Experiment Setting


### Demonstration
> The simulation of two heterogeneous robot teams cooperative achieving tasks in USAR with Unity:
    <div align = center>
    <img src="https://github.com/RickYang2016/PhD-Dissertation-SASS/blob/main/figures/rne.png" height="225" alt="Hopper-V2 3SABC">   <img src="https://github.com/RickYang2016/PhD-Dissertation-SASS/blob/main/figures/rne.gif" height="225" alt="Hopper-V2 3SABC Video"/>
    </div>



## Conclusion

In this paper, we introduce a general agent trust model based on Relative Needs Entropy (RNE) to measure and analyze the trust levels between agents and groups, representing the similarity of their diverse needs in a specific situation for heterogeneous multi-robot cooperation. Then, we illustrate how the RNE trust can be used in multiagent decision-making applications. Specifically, we propose an RNE trust-based effective heterogeneous multi-robot cooperation method to form multiple robot groups based on trust levels within the groups. The proposed model is evaluated through extensive simulations under different difficulty tasks in a post-nuclear radiation leak-like urban search and rescue scenario. We also developed a dynamic priority switching mechanism to solve conflicts in multi-robot cooperation. 

The experimental analysis showed that the RNE trust-based grouping model outperformed state-of-the-art energy-based and distance-based methods in maximizing group utilities and represented lower system costs. Trust based on relative needs distributions presents opportunities for improvements and interesting applications. Ultimately, we envision a harmonious team of robots in future multi-robot missions in which each robot values trust on each other robot.
