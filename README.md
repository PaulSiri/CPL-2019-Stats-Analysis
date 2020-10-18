# CPL-2019-Stats-Analysis
2019 marked the inaugural season of the Canadian Premier League, Canada's new top division soccer/football league. Alongside the end of the season, the league announced that they were making all the game and player data from 2019 public through [Centre Circle Data.](https://canpl.ca/centre-circle-data/)

Recently, I decided to take a look at the database and analyze it using R to identify attacking prospects from across the league!

## Expected Goals and Assists
The database holds a variety of [Opta's advanced statistics](https://www.optasports.com/insight-for-fans/opta-s-event-definitions/), two of the most important being Expected Goals (xG) and Expected Assists (xA). These stats represent the number of goals or assists a player should be expected to make, given the location and type of the shots/passes that a player made (among many other factors).

To make these numbers more comparable across players, I converted them to xG/90 minutes played and xA/90 minutes played so I could see how many goals and assists players should have made per game. I also excluded players who had less than 450 minutes of league play to make sure there was sufficient data.

### Putting this together, I came up with this graph with the names of high performing players
![Expected Goals and Assists](https://i.imgur.com/RbwFm1t.png)

#### Some standouts from this figure include:
 - Tristan Borges, the league MVP, top scorer, and top assister, who although undoubtedly performed well, is placed lower in xG/90 and xA/90 than several others
 - Dominique Malonga, the second top scorer and by far the leader in pure xG (15.56 compared to 2nd with 9.35), is the leader in xG/90 as well
 - Julian Büscher, the leader in xA/90 and teammate of Malonga on the Cavalry
 - While the players above (as well as most of the high performing players in general) play for the dominating forces in the league with either the Cavalry or Forge, there are two standouts on notably weaker sides who still pull ahead of the pack
   - Mohamed Kourouma, the leader in pure xA and truly a creative juggernaut in the league while playing on a struggling Halifax side
   - Easton Ongaro, only 21 years old during the season and a massive goal threat in the limited minutes that he played with Edmonton

Those last two players especially stood out to me, so I looked to further understand their creative and goal-scoring contributions.

## Chances and Big Chances Created
To delve deeper into the creative aspect of the game, I took a look at how many chances and big chances players created every 90 minutes. A "chance" is a pass which leads to a shot by the recipient, and creating a "**big** chance" means a pass that leads to a very high probability goal scoring opportunity. Either way, these statistics track with how well a player provides opportunities for their teammates to shoot (and hopefully score).

### I once again converted them to per 90-minute stats and charted them as such
![Chances and Big Chances](https://i.imgur.com/zElylnw.png)

#### Lo and behold, our boys Büscher and Kourouma lead the pack again, but with a surprise performance by Ryan Telfer!
So here we have an instance of how looking further in the data can reveal more qualities in players, and in this case some truly insane superiority in chances created by Ryan Telfer. He plays on a York9 team that had the most shots in the league, and judging by this graph he is largely responsible for that stat. However, this huge gap in-between Telfer and other players could indicate that his York9 teammates are shooting excessively from low-quality areas. In fact, York9 took the most shots from outside the box with 50 in 2019. So, while Telfer is an exceptional passer and creator, his team's tactical approach could probably make better use of his talents by progressing nearer the goal before taking shots.

## Shots on Target and Touches, Both in the Box
Shifting focus to the goalscoring aspect of the game, we have the more straightforward statistics of shots on target in the box, and touches in the box, which are both exactly what they sound like. Though this doesn't mean that they aren't powerful indicators of a player's ability and habits inside the goalscoring danger-zone! 

By their nature, shots from inside the box are usually high-quality chances, and getting them means a player is putting themselves in dangerous areas, either from their off-the-ball movement, or ability to dribble into good positions. Making sure these shots are on target means both that the chances were probably of even higher quality, and that the player has half-decent aim. Combining this stat with touches made inside the box gives insight as to how a player is behaving once they receive the ball in the box. For example, a high number of shots with fewer touches implies a poacher style approach with one-touch finishes, while low shots and high touches could indicate a more pass-first mentality.

Of course, this sort of analysis is more case-by-case and requires more context, so let's look for interesting cases to look at!

### Again, making sure all stats are per 90 minutes and charting, we get...
![Shots on Target and Touches in the Box](https://i.imgur.com/OqVpPMv.png)
#### The dotted regression line gives a rough guide as to the typical shots to touches ratio

At the top end of the graph, we have our clinical strikers such as Ongaro and Malonga, who are usually on the receiving end of high-quality chances and aren't afraid to take a shot. 

Rodrigo Gattas also makes an appearance, I suspect that he enjoyed a lot of the service we saw Telfer was dishing out in the last graph. 

On the other end of the spectrum we have Zach Verhoven, a tricky winger for Pacific FC who is often dribbling his way into the box and squaring the ball for teammates. 

There is also Emery Welshman on the far right side, although he is a centre forward, he seems to struggle to get good shots off given the number of touches he is taking in the box. Looking more into his stats, he had 7 big goalscoring chances across the season, and he is underperforming his xG by 2 goals (expected to score 5, only scored 3). Overall, it seems like Welshman's shot taking could be much more efficient. This doesn't mean that Welshman is a bad player by any means, just that he could probably improve his shot volume in the future if coached properly.

## Conclusion
Going back to the original goal of this post (_get it_), I would have to say that from the players I assessed, the number one attacking prospect from the 2019 CPL season would have to be Easton Ongaro! He's tall, young, Canadian, and has some of the best goalscoring indicators in the league. If I had to put money on any of the players from this season becoming a real talent in the MLS or Europe, I would put it on Ongaro.

It turns out that he actually has already gotten a loan to the Danish 2nd division with an option to buy in the winter! Best of luck to him.

### Conclusion for Real
I hope that whoever is reading enjoyed this brief look into the 2019 CPL stats! 

Personally, I had a great time analyzing the data and I'm sure that I'll continue to learn more about football analytics and the power that it has for scouting and coaching!
