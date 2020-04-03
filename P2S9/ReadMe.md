# Assignment

---

## **Phase 2 Session 9: Assignment**

1. Well, there is a reason why this code is in the image, and not pasted.
2. You need to:
    1. write this code down on a Colab file, upload it to GitHub.
    2. write a Readme file explaining all the 15 steps we have taken:
        1. read me must explain each part of the code
        2. each part of the code must be accompanied with a drawing/image (you cannot use the images from the course content)
    3. Upload the link.

---
## **Twin Delayed DDPG (TD3)**
* **DDPG** stands for **Deep Deterministic Policy Gradient** and is a recent breakthrough in AI, particularly in the case of environments with continuous action spaces.
* To be able to apply Q-learning to continuous tasks, the authors introduced the Actor-Critic model.
* Actor-Critic has 2 neural networks that the following way:
    1. The Actor is the policy that takes as input the State and outputs Actions
    2. The Critic takes as input States and Actions concatenated together and outputs a Q-value
* The Critic learns the optimal Q-values which are then used to for gradient ascent to update the parameters of the Actor.
* By combining learning the Q-values (which are rewards) and the parameters of the policy at the same time, we can maximize expected reward.

