# netlogo-diversity.github.io

# WHAT IS IT?
This project models how men, women, and people of color move through organizations. 

I wanted to see if I could replicate the statistics we see in companies using simple modeling techniques like homophily and preferential attachment. The gist of the model is: people network, they act or they don't, they have confidence and a well-connectedness score, which determines whether or not they get promoted. 

# HOW IT WORKS
Turtles are either men or women and either a person of color or not. The number of women and people of color are exposed to the interface and can vary from 0-100. People have an echelon between 0-4, which represents their place within the company. The echelons are visually represented in circles; the lower the number and the smaller the circle, the higher in power the person is, and the more exclusive the echelon. Links represent relationships between people.

On SETUP, the model assigns men, women, and people of color into echelons. The agents go to their respective places based on their echelons, unless that echelon is full, in which case they are demoted.

Then, on GO, agents either act or do not act depending on their confidence level. People who have relationships with the acting people judge them on this action. Then, the acting people self-assess, which affects their ability to act next time. If they do not act, they lose some confidence.

Once at least 10% of the people are up for promotion, the highest scoring 10% are promoted. The lowest scoring 10% are demoted. People re-calculate and update their score based on similarity, prestige, and the age (where new relationships are more powerful) of their relationships.

People also network with the people around them; they prefer to form relationships with people similar to them, but also those people with the highest score above them. If people have more relationships than the maximum, a random relationships is eliminated. If they have more links than can be shown, the links fade into white links that eventually die.

# HOW TO USE IT
First, customize the number and type of people in the organization. The PEOPLE-IN-ORG slider determines how many people total are shown The %-OF-WOMEN slider determines what percentage of the total people are women. The %-OF-COLOR slider determines what percentage of the total people are people of color. All of these take effect each time you click SETUP.

Click the SETUP button to set up the agents. The agents should be randomly scattered into different circles.

Click GO to start the simulation. People start networking with each other, moving around the circles, and the scores chart starts changing.

The LINK-MAX slider controls the maximum number of links allowed, which makes it so that people are constantly creating new links. The LINK-FADE slider controls how many ticks the links are visible for, and the links gradually turn white as they approach this many ticks. For example, if the LINK-FADE slider is set to 20 and LINK-MAX is set to 30, a link that is 15 ticks old will be nearly faded away, and has 15 ticks of life left.

The DIFFERENCE-CAP slider shows the maximum similarity score a person can be given when they are either a different color or a different gender from a another person. Similarly, the SIMILARITY-CAP slider shows the maximum similarity score a person can be given when they are either a different color or a different gender from a another person. So for example, if the DIFFERENCE-CAP is 30 and the SIMILARITY-CAP is 50, and if a white female meets a colored male, the highest similarity score one can give to the other is 60. If a white female meets a colored female, the highest similarity score one can give to another is 80, and so on.

The NO-ACT-LOSS slider shows the percentage of confidence that is lost each time a person does not act.

The SCORES monitor shows the average score of each type of person at each tick. It starts at 0, and rapidly builds up and stabilizes, because the scores stay roughly the same.

The CONFIDENCE monitor shows the average confidence of each type of person at each tick. It starts at 100, and decreases and stabilizes, because the confidence stays roughly the same.

The TOP %, MID %, and BOTTOM % monitors all correspond to the percentage of each type of person in each category. TOP represents echelons 0 and 1, MID represents echelons 2 and 3, and BOTTOM represents echelon 4. For example, if the TOP % monitors show 26 under WOMEN, 50 under MEN, and 24 under POC, then the echelons 0 and 1 have 26% women, 50% men, and 24% people of color.

# THINGS TO NOTICE
When you execute SETUP, people are randomly distributed throughout the organization. But once you click GO, people will almost immediately sort themselves based on how high the DIFFERENCE-CAP is and how many people look similar to them.

Notice the variability of the confidence when you change the %-OF-COLOR and %-OF-WOMEN sliders. The higher the percentages, the more confident those categories tend to be.

Notice the variability of the scores when you change the SIMILARITY-CAP and the DIFFERENCE-CAP. The more equal the two caps, the more similar the scores.

Notice how the model rapidly stabilizes after a few ticks, and how the SCORE monitor still shows an increase in score.

Try changing the %-OF-COLOR and %-OF-WOMEN in the model. Where do most agents of color end up?

Try changing the SIMILARITY-CAP and the DIFFERENCE-CAP. Make the DIFFERENCE-CAP larger. Does this change the way the model runs?

Try changing the percentages of the types of people in the model and the similarity-cap and difference-cap. Where do most agents of color end up?

Try different values for %-OF-WOMEN and leave %-of-color lower. Where do women of color end up?

Can you set sliders so that the model never finishes running, and agents keep moving echelons?

# MAKING THE MODEL BETTER

A future iteration of the model would: 

- Have the initial configuration mimic real-world data. Much of the model relies on the initial configuration, which is determined randomly. 
- Integrate social networks into this model, like having personal relationships and professional relationships be different things with different values. 
- Include standard racial categories, and change the definition of underrepresented minority in realtime. 
- Factor age, where certain positions are only available to people with a certain amount of experience; e.g., people can be too old or too young for a position?
