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
To prove our clustering works, let's experiment with a history. Our world is constantly changing, but do our favourite characters?

Take a look at the past to find what people used to like and compare to what they like now.

## Cultural preferences
The main place of the film industry, its Mecca is Hollywood. Other countries make films aimed mostly at local audiences. But it’s all the more interesting to look at them!

To prove or refute stereotypes, to look at cultures from a different angle - we consider our archetypes depending on the country of the film production.


##  Movie success
Ok, we learn our differences and similarities, but can we predict the success of the movie based on the scenario and more specifically on the characters who are involved?



## Actors success
The same goes for actors - we know that it is possible to become famous by playing in the first or secondary roles, villains or good-natured people, strong-willed leaders or decent citizens, but who has *statistically* more chances?
