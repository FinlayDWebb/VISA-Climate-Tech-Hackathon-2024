# VISA-Climate-Tech-Hackathon-2024
The mission is to  revolutionize the use of payments data, to create groundbreaking solutions that drive  sustainable outcomes and enable consumers to make informed choices.

#progress log

18th May - 

Today I met (on a google meet) with Rbhu Gandhi, Shresht Venkatraman and Ayushi Bhandari. This is the provisional team for the hackathon, we formed through networking on Linkedin. Rbhu has a background in software development, NLP and chemical engineering and is based in the US. Shresht has a background in economics and more recently data science and is also in the US. Ayushi has a background in chemistry, pursusing a data science masters, with a more strategic consulting direction and is based in Paris. My background is in pure and applied math, with some elementary data science. We spoke about which of the three challenges that are proposed we would pursue, as well as how we could communicate. We decided on challenge #2 "Remixing Data and Recommerce". As this seemed to give the largest opportunity to create a unique solution due to its open-endedness. WhatsApp was chosen as the mode of communication. We also decided that since we don't have information on what data will be given to us by VISA, when the competition opens (28th of May), we would each choose an area of recommerce to conduct market research and try and find gaps in the market that we could capitalise on. The areas given by VISA are repair, resale, rent, resdistribute, refill, return. I chose to go after repair and refill. 

Main takeaways: 
1. Weekly meetings on Saturdays at 6pm (GMT).
2. Conduct research on the industry of repair and the indsutry of refill
3. Stay in contact with the team on WhatsApp.

28th May - Relevant document is "Project file (1)"

Yesterday, we had another meeting on Google Meet where we all presented our findings and thoughts of the direction of the project. I presented my thoughts on the repair and refill industry, concluding that a couple good ideas I had were as such: 
(1.) a forward predicting repair model and directory combined that works with the consumer and utilises companies like IFIXIT to keep the appliance working and sustainable. 
(2.) a pricing and repair model to assess the most cost-effective and sometimes eco-friendly method to deal with a crashed/written-off car.
  the first idea would utilise ML and web-development skills, to provide an incentive for consumers to explore the idea of repairing before they 'default' to purchasing a new car. The second idea would also use ML and web-development skills, this one focussing more on a niche market of consumers who have recently written-off their car (this refers to damaging a car so badly that the insurance company gives you money rather than repairing the car). Both ideas align with the goal of making re-commerce more appealing to the consumers. Perhaps the first idea has a larger market cap. However, in the meeting we all discussed the other areas of re-commerce like recycle, redistribute, resale, etc. Coming away with an idea that we weren't sure which direction to go in, but with a clear goal to really think about what our ideal end consumer was. Shresht's idea of using image recognition to classify the stage in which a household appliance was in, in it's lifecycle. The idea being that with a clear classification system, we could help fix the issues of waste at the source, the companies. Furthermore, image recognition was something that the group was keen to explore, one novel idea was as such:
  We use image recongition to allow the consumer to scan their household appliance/furniture that they don't need anymore, it classifies the state of it, and then finds the exact amount of packaging needed to pack it up once dissambled. We could then assign a connection to a delivery service, so that people locally would be able to get the appliance/furniture instead of buying off Amazon. I am not so sure about this type of idea, it seems a little too optimistic and I voiced these thoughts, that we should focus on a niche that could then be adapted to be widely applicable, but to really just hone in on one thing. From this we knew what we had to do for the next meeting, listed in the MT (Main takeaways):

Main takeaways:
1. Come up with an idea of a product/service with a clear set of end users. If I can find data on the end-users like scale, size, market penetration, competitors that would be ideal.
2. For the idea, come up with a clear set of use-cases that illustrates the need for the idea
3. Go over the Dataset they release and come up with observations, ideas or questions
4. If possible, do some research into the Machine Learning/Data Science literature on your idea to get an idea of the technical steps involved

Sunday 9th June - Uploaded DimensionFetcher.md to the repo

I just got back from abroad, we have had two meetings (2nd and the 8th) and after pitching my idea for building a model to determine longevity of specific household appliances, we decided to go in a different direction. After some brainstorming on the 2nd of June, we decided to commit to the idea of a moving company prioritising the environment and ease of use. Almost like Uber for moving, there is a company that does this already named Dolly so to be careful in order to not repeat what is already been done, but we feel as though there isn't a market for small items. Dolly requires drivers with vans and usually involves moving the entire contents of a house. Our idea would involve moving, just one or two pieces of furniture and moving it with anybody with a car big enough. After deciding on this idea it was time to go away and find data and articles backing this up. I found 4 relevant datasets, 2 of which included car model/make and the dimensions of the boot, cargo space, etc. And the other 2 of which included emissions data for those cars. These would be incredibly useful as the idea would also to be rank priority to more fuel efficient cars for the 'movee', to really emphasise the climate consideration. 
  We then met again on the 8th (yesterday) and decided that we need to hurry up our progress. We needed to focus on the presentation more than the product being 'perfect'. The tasks were delegated to each person, some front end and back end, some research, some presentation, some data scraping, etc. I was tasked with writing the presentation slides on the data scraping as I had been most successful with finding data up to that point. So we skip to today, and I wanted to find a way so that the driver could put in their car model and make, and a script would return the dimensions, so that the movee could match their requirements with a car big enough. This would involve first data scraping from sites with this information, and then building a script to calculate whether the movee's furniture would fit. Starting with the scraping data task:
  I dont have much experience with Python so this was extremely challenging, I first watched multiple videos and read some articles about the package BeautifulSoup, deciding that it would be best to use this. I then layed out a plan for the script, it as such:
      1. Create a function that would in turn create a URL possessing the data for the dimensions.
      2. Define a function to scrape the boot dimensions from the constructed URL.
      3. Define the main function that gets user input, constructs the URL, fetches the dimensions, and prints them.
  Using StackOverflow, videos, articles and the Python OpenAI model, I was able to construct all three parts, with some tweaking to make sure it worked. One issue was the dashes in the car model, with the website that I used for the dimensions, "How Many Bags Fit", the url obviously turns Honda Accord Executive 2 into honda-accord-executive-2, so that was handled by prompting the driver to put their own dashes in. As well as running a make.lower.replace(" ", "-") in the construct URL branch to sort out the make input too. And this all worked. Next I have to tackle finding a way to check if furniture fits now.

Main problem:
I found it extremely hard to find and think of a way to scrape the dimensions of a car boot from the internet. Solution: searching over 10 websites to find data, and researching into BeautifulSoup to try and form a script. Outcome: utilised OpenAI, articles and videos to help me build a script that worked in scraping this data.

Main takeaways:
1. I successfully navigated building an initial data scraping script (with help from the internet)
2. Continue to build a script that can check if furniture can fit in the back of a car. And share this script with Isha who is working on the back and front end.
3. Put together multiple slides in the group's presentation going over data scraping, ahead of the next weekend.



