# Fake Resume Attacks: Data Poisoning on Online Job Platforms

![workflow_figure](https://github.com/mickeymst/FRANCIS/blob/main/workflow.png)

## Abstract 
While recent studies have exposed various vulnerabilities incurred from data poisoning attacks in many web services, little is known about the vulnerability on online professional job platforms (e.g., LinkedIn and Indeed). In this work, first time, we demonstrate the critical vulnerabilities found in the common Human Resources (HR) task of matching job seekers and companies on online job platforms. Capitalizing on the unrestricted format and contents of job seekers’ resumes and easy creation of accounts on job platforms, we demonstrate three attack scenarios: (1) company promotion attack to increase the likelihood of target companies being recommended, (2) company demotion attack to decrease the likelihood of target companies being recommended, and (3) user promotion attack to increase the likelihood of certain users being matched to certain companies. To this end, we develop an end-to-end “fake resume” generation framework, titled FRANCIS, that induces systematic prediction errors via data poisoning. Our empirical evaluation on real-world datasets reveals that data poisoning attacks can markedly skew the results of matchmaking between job seekers and companies, regardless of underlying models, with vulnerability amplified in proportion to poisoning intensity. These findings suggest that the outputs of various services from job platforms can be potentially hacked by malicious users.


## Description
This repository contains the code for our fake resume attack framework, FRANCIS. The code will be stored in this repository.


## Attack Scenarios
Our attack objects and scenarios are highlighted in red color within the above figure. Our fake resume attack focuses on the delivery phase of a model's prediction result. Specifically, the aim is to alter the original predicted companies X into target}companies Y, thereby influencing Y's visibility to job seekers and the prominence of specific users in recruiters' shortlists. The foundation of these attacks lies in the unrestricted nature of resumes and account creation on online job platforms. We demonstrate three attack scenarios below:

1. Company Promotion Attack
  - This approach targets specific companies X and artificially increases the likelihood of X to be recommended to job seekers. Imagine a small company that struggles to attract talents as job seekers are often gravitated toward larger and well-known companies. Then, an attacker may offer a promotion service to such a small company, claiming that "for some $, I can make your company to be twice more matched to job seekers than before." That is, the attacker's goal is to maximize the hit ratio of  target companies. Suppose the career prediction model recommends N companies to each user. We denote the fraction of users whose top-N recommendations include the target company after the attack. Essentially, after the attack, a significantly larger portion of users would find these target companies among their top-N company recommendations.

2. Company Demotion Attack
  - This approach is the inverse of the company promotion attack. Instead of increasing the likelihood, the aim is to decrease the likelihood and demote target companies. A plausible motivation is a corporate rivalry, where one company wishes to undermine the other company's presence on the platform.

3. User Promotion Attack
  - Some users, despite being keenly interested in working for specific companies, say Google or Microsoft, may lack the necessary qualifications or experience. Consequently, these job seekers are unlikely to be recommended to the recruiters of Google or Microsoft. To promote such users for specific companies, therefore, this attack seeks to manipulate model outputs, ensuring target users to be featured in the shortlists provided to target companies. Shortlist systems consist of K users for each company. The goal is to maximize the averaged display rate on the shortlist, which denotes the fraction of target companies whose top-K recommendations include target users.


## Citation
```bibtex
@inproceedings{yamashita2023fake,
  title={{Fake Resume Attacks: Data Poisoning on Online Job Platforms}},
  author={Yamashita, Michiharu and Tran, Thanh and Lee, Dongwon},
  booktitle={Proceedings of the ACM Web Conference 2024},
  year={2024},
}
