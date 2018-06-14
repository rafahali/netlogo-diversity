# netlogo-diversity.github.io

# WHAT IS IT?
This project models how men, women, and people of color move through organizations. People sometimes act, and they have confidence that changes based on how they feel after acting. They also have a score based on their relationships. All types of people network with each other, and they prefer to have relationships with people who are similar to them and have higher scores with them. The simulation shows how these individual preferences and homophily can move different types of people to different echelons within the company.

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

# THINGS TO TRY
Try changing the %-OF-COLOR and %-OF-WOMEN in the model. Where do most agents of color end up?
Try changing the SIMILARITY-CAP and the DIFFERENCE-CAP. Make the DIFFERENCE-CAP larger. Does this change the way the model runs?
Try changing the percentages of the types of people in the model and the similarity-cap and difference-cap. Where do most agents of color end up?
Try different values for %-OF-WOMEN and leave %-of-color lower. Where do women of color end up?
Can you set sliders so that the model never finishes running, and agents keep moving echelons?
# EXTENDING THE MODEL
Much of the model relies on the initial configuration, which is determined randomly. Can you create an initial configuration that matches the real world more closely?
Incorporate social networks into this model. For instance, have personal relationships and professional relationships be different things with different values. Does this change the model significantly?
Currently, the model considers only people of color and people not of color. Expand the model to include standard racial categories. Would it be possible to tell which categories are underrepresented minorities.
Age of people is not a factor in the model, but is certainly a factor in the real world. Create rules where certain positions are only available to turtles with a certain amount of experience; e.g., Can you make it so turtles can be too old or too young for a position?
