**Subreddit Hyperlink Network**: the subreddit-to-subreddit hyperlink network is extracted from the posts that create hyperlinks from one subreddit to another. We say a hyperlink originates from a post in the source community and links to a post in the target community.

Note that each post has a **title** and a **body**. The hyperlink can be present in **either the title** of the post or **in the body**. Therefore, we provide one network file for each.

The first step will be to concatenate those two datasets and provide w full dataset containing all directed and signed connexions between subreddits

The data contains 40 months of Reddit comments and posts



**BALANCE THEORY** :

- Considers the possible ways in which triangles on three individuals can be signed.
- it posits that triangles with **three positive signs** (3 mutual friends), and those with **one positive sign** (2 friends with common enemy) are more plausible (more prelevent) than triangles with **two positive signs** (2 enemies with common friend) or **none** (mutual enemies)


**STATUS THEORY** :

- We need to define our proper way of formulating the status theory. Given the low pourcentage of negative links (10% in all the links) we can say that a negative link from community A to community B may mean that community B is my enemy / wrong  and a positive link from A to B may be I get along well with community B


	Max Weber developed the idea of "status group" which is a translation of the German Stand (pl. Stände). Status groups are communities that are based on ideas of lifestyles and the honor the status group both asserts, and is given by others. Status groups exist in the context of beliefs about relative prestige, privilege, and honor and can be of both a positive and negative sort.

We can therefore say that a positive link from A to B means that A agrees/respect B's ideas/lifestyle , and a negative link from A to B means that A disagrees/disrespect B's ideas/lifestyle.



## SOURCES :

#### Data : 
S. Kumar, W.L. Hamilton, J. Leskovec, D. Jurafsky. Community Interaction and Conflict on the Web. World Wide Web Conference, 2018.
(BibTex Citation:
@inproceedings{kumar2018community,
  title={Community interaction and conflict on the web},
  author={Kumar, Srijan and Hamilton, William L and Leskovec, Jure and Jurafsky, Dan},
  booktitle={Proceedings of the 2018 World Wide Web Conference on World Wide Web},
  pages={933--943},
  year={2018},
  organization={International World Wide Web Conferences Steering Committee}
}
)



