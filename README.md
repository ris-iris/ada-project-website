In our daily lives, we naturally categorize everything we encounter, including the characters in the movies we love. The characters that capture our collective imagination often mirror our aspirations, fears, and evolving values. This project aims to employ a data-driven approach to cluster movie characters into archetypes. By using these archetypes, we aim to uncover valuable insights into people's preferences for character traits. Using this knowledge, we can not only help filmmakers to create more appealing stories but also look into the prevailing cultural and psychological dynamics in society.

## Characters clustering
We were given the plots of the movies. Let's cluster characters based on their attributes and actions that they did or was done to them.

To do so, we use Latent Dirichlet allocation, a model, that allows us to interpret the resulting clusters of characters based on the topics of their attrubutes and actions. You can look at the topics with the highest probabilities for each archetype:

{% include_relative assets/js/cluster_slider.html %}

And some examples of characters with particular archtype:

| Character|                                         Film     |Archetype(cluster)|
|----------|--------------------------------------------------|------------------|
|Dumbledore|~~Harry Potter and the Goblet of Fire, Harry Potter and the Half-Blood Prince|~~13|
|   Gandalf|             The Lord of the Rings: The Two Towers|              ~~13|
|   Gandalf| The Lord of the Rings: The Fellowship of the Ring|              ~~25|
|     Harry|     Harry Potter and the Deathly Hallows – Part 2|              ~~25|
|    Gollum|     The Lord of the Rings: The Return of the King|              ~~39|
| Voldemort|         Harry Potter and the Order of the Phoenix|              ~~46|
| Bellatrix|          Harry Potter and the Half-Blood Prince  |              ~~46|

We can see, that the clusters obtained with our method group characters with the similar roles in their movies (sometimes this leads to one character being in different clussters, e.g. having a different role in different parts of the story).

## Historical trends
What are the prevailing archtypes trough the history.

## Cultural preferences
Difference in archtypes in different countries.
