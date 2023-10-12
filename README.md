# Fake Resume Attacks: Data Poisoning on Online Job Platforms

This repository contains the code for our fake resume attack model, FRANCIS. 


## Abstract 
While recent studies have exposed various vulnerabilities incurred from data poisoning attacks in many web services, little is known about the vulnerability on online professional job platforms (e.g., LinkedIn and Indeed). In this work, first time, we demonstrate the critical vulnerabilities found in the common HR task of matching job seekers and companies on online job platforms. Capitalizing on the unrestricted format and contents of job seekers’ resumes and easy creation of accounts on job platforms, we demonstrate three attack scenarios: (1) company promotion attack to increase the likelihood of target companies being recommended, (2) com- pany demotion attack to decrease the likelihood of target companies being recommended, and (3) user promotion attack to increase the likelihood of certain users being matched to certain companies. To this end, we develop an end-to-end “fake resume” generation frame- work, titled FRANCIS, that induces systematic prediction errors via data poisoning. Our empirical evaluation on real-world datasets reveals that data poisoning attacks can markedly skew the results of matchmaking between job seekers and companies, regardless of underlying models, with vulnerability amplified in proportion to poisoning intensity. These findings suggest that the outputs of various services from job platforms can be potentially hacked by malicious users. 


## Running the code
The code is based on python and will be stored in this repository.
