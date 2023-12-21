In our daily lives, we naturally categorize everything we encounter, including the characters in the movies we love. The characters that capture our collective imagination often mirror our aspirations, fears, and evolving values. Although every movie is unique, we still can notice that there are often protagonists and antagonists; the main character and her/his beloved, and many many more patterns.

So we invite you on a journey to reveal archetypes of movie characters, to uncover insights into people's preferences for character traits. 
We hope everyone will discover something interesting here: movie historians will see global trends; geographers will obtain a perspective of the cultural preferences of every country; filmmakers will learn the characters they need for success; psychologists will create a portrait of modern human and their desires and Potterheads will be mad to know why Draco and Harry ended up in the same cluster. 

Still not interested? Give us a chance by looking at the visuals and allow us to entertain you for the next couple of minutes.


## Characters clustering
We were given the plots of the movies. Let's cluster characters based on their attributes and actions that they did or was done to them.

To do so, we use Latent Dirichlet allocation, a model, that allows us to interpret the resulting clusters of characters based on the topics of their attributes and actions. You can look at the topics with the highest probabilities for each archetype:

{% include_relative assets/js/cluster_slider.html %}

And some examples of characters with particular archetypes:

| Character |                                         Film     |Archetype(cluster)|
|-----------|--------------------------------------------------|------------------|
|Dumbledore |  Harry Potter and the Goblet of Fire, Harry Potter and the Half-Blood Prince|  13|
|   Gandalf |             The Lord of the Rings: The Two Towers|                13|
|   Gandalf | The Lord of the Rings: The Fellowship of the Ring|                25|
|     Harry |     Harry Potter and the Deathly Hallows – Part 2|                25|
|    Gollum |     The Lord of the Rings: The Return of the King|                39|
| Voldemort |         Harry Potter and the Order of the Phoenix|                46|
| Bellatrix |          Harry Potter and the Half-Blood Prince  |                46|

We can see, that the clusters obtained with our method group characters with similar roles in their movies (sometimes this leads to one character being in different clusters, e.g. having a different role in different parts of the story).

## Historical trends
To prove our clustering works, let's experiment with a history. Our world is constantly changing, but do our favourite characters?``

Take a look at the past to find what people used to like and compare to what they like now.

## Cultural preferences
The main place of the film industry, its Mecca is Hollywood. Other countries make films aimed mostly at local audiences. But it’s all the more interesting to look at them!

To prove or refute stereotypes, to look at cultures from a different angle - we consider our archetypes depending on the country of the film production.


##  Movie success
Ok, we learn our differences and similarities, but can we predict the success of the movie based on the scenario and more specifically on the characters who are involved?



## Actors success
The same goes for actors - we know that it is possible to become famous by playing in the first or secondary roles, villains or good-natured people, strong-willed leaders or decent citizens, but who has *statistically* more chances?

<h5> Measurement of success</h5>
We were conflicted about how to measure the success of the actors, whether to use their average ratings or normalized revenue. By plotting the histogram chart between the two metric and calculating the Pearson correlation coefficient, we noticed certain correlation between the average ratings and normalized revenue. In order to measure the success of an actor, we decided to combine both metrics and use the sum of normalized log revenue and rating of the film as the metric for success.

![Alt Text](assets/img/ActorSuccess/histogram1.png)

We are interested in figuring out who are the top actors that in the film industry. To assess the success of actors, we established specific criteria to determine the significance of each actor. 

Firstly, actors were assigned varying levels of importance based on their roles in different movies. We determined the importance of each actor by analyzing plot summaries and counting the number of associations made to them. The total associations were then summed up to quantify the overall importance of each actor. The overall success of the actors are calculated based on the importance value what was assigned to them. Following this, actors in various movies exhibited different archetypes, with these archetypes grouped into clusters. Actors are deemed successful when they have participated in multiple movies; this criterion filters out those who take on smaller or lesser roles. By sorting the actors according to their associated success values, we plot the chart below according to the success of the actors.

![Alt text](assets/img/ActorSuccess/topactors.png)

<h5> Does the number of architypes lead to an actor’s success? </h5>
We are now interested in determining if the number of architypes acted by the actors contributed to their success. We took the number of clusters of the actors and divided it by the number of films they have acted in, which gives us the clusters to film ratio. According to our analysis, the median is 0.8, which suggests that taking a more diverse role may lead to the actor’s success.

![Alt text](assets/img/ActorSuccess/clusttofilmratio.png)
<p align="center"> Histogram chart for cluster to film ration</p>

Further analysis was conducted to determine if the claim of taking a more diverse role in may lead to the actor’s success is true. We consider an actor who assumes many archetypes to have a cluster-to-film ratio exceeding 0.7. We set the treatment group as actors who take on many architypes and the control group as actors who take on less architypes.

Propensity score matching was conducted, using the propensity score similarity to construct a graph where nodes represent instances from the control and treatment groups, and edges reflect the similarity between instances. The matched results were extracted and further grouped into treatment and control. This was done to reduce the selection bias. 

According to the chart on success distribution comparison, the results we obtained are intriguing. We can now assert that actors who have portrayed fewer archetypes are statistically significantly more successful than those who have played a greater variety of archetypes.

![Alt text](assets/img/ActorSuccess/successdistribution.png)

