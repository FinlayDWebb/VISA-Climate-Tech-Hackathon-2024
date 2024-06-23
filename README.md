# VISA-Climate-Tech-Hackathon-2024
The mission is to  revolutionize the use of payments data, to create groundbreaking solutions that drive  sustainable outcomes and enable consumers to make informed choices. Our idea is Airide, a chrome extension/app that allows people to hire local drivers to move 1 or 2 pieces of furniture (boot space permitting). This allows avoiding surcharges and minimum amounts that moving companies levy on the customers. The system would also priority rank more carbon efficient cars over less carbon efficient ones too.

#progress log

--------------------------------------------------------------------------------

18th May - 

Today I met (on a google meet) with Rbhu Gandhi, Shresht Venkatraman and Ayushi Bhandari. This is the provisional team for the hackathon, we formed through networking on Linkedin. Rbhu has a background in software development, NLP and chemical engineering and is based in the US. Shresht has a background in economics and more recently data science and is also in the US. Ayushi has a background in chemistry, pursusing a data science masters, with a more strategic consulting direction and is based in Paris. My background is in pure and applied math, with some elementary data science. We spoke about which of the three challenges that are proposed we would pursue, as well as how we could communicate. We decided on challenge #2 "Remixing Data and Recommerce". As this seemed to give the largest opportunity to create a unique solution due to its open-endedness. WhatsApp was chosen as the mode of communication. We also decided that since we don't have information on what data will be given to us by VISA, when the competition opens (28th of May), we would each choose an area of recommerce to conduct market research and try and find gaps in the market that we could capitalise on. The areas given by VISA are repair, resale, rent, resdistribute, refill, return. I chose to go after repair and refill. 

Main takeaways: 
1. Weekly meetings on Saturdays at 6pm (GMT).
2. Conduct research on the industry of repair and the indsutry of refill
3. Stay in contact with the team on WhatsApp.

--------------------------------------------------------------------------------

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

--------------------------------------------------------------------------------

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

--------------------------------------------------------------------------------

Sunday 16th June - Uploaded MinBoxBounding.md, FurnitureFitStep.md, FuelEmissionRanking.md

A lot has happened since the last log, with the deadline steadily approaching there is an increase in the intensity of work with the project. Throughout last week I added lots to the PPTX, including multiple demo scripts and flowcharts to explain/pitch the idea to the viewer of the PPTX. This included details around how the app works, what inputs are needed from the consumer and the driver, and how the app could go about processing and utilising the data to ensure a swift and seamless process for both parties. A USP of our idea is the ease of use, so it is imperative that clunkiness is left out of it. I will upload the PPTX once I have finished it. Now to discuss the issues and how I resolved them as they cropped up:

Problem 1: Furniture fitting imperfections
  
  In the previous log entry I outlined a process that scraped the dimensions of the driver's cargo space off a website online. This was
  handy and solved the problem of requiring the driver to do that themselves. But, following that there was the problem of using that data
  successfully. A big issue to consider is that the boot or cargo space of cars is rarely ever a strict box, and is normally one that curves
  in places, along with other obstructing parts. After mindmapping some possible solutions and drawing up rough flowcharts I settled on a
  fix.
  
  Solution: The idea would be to add a margin of error to the bounded box estimation, this way we are accounting for imperfections in the
  shape of the cargo space. Deciding on the value for the margin of error was done by doing some research into the most common car shapes.
  As such, 10cm was added to rigid furniture entries, and 5cm for flexible furniture pieces. The demo script created added these values, as
  well as printing out the minimum size needed given the customer's furniture entry.

  However, this did not work. Upon talking with the team, we collectively found that 'flexible' furniture was rarely ever a thing, so that
  extra step of computation (adding different values for the margin of error based on if the product was flexible or not) was unnecessary.
  Furthermore, the script simply printed the needed size for the furniture, it didn't find if the furniture would fit based on the car model
  and make, which is what is needed.

    So how do I deal with this new information? That my previous solution was incorrect.

  I went back to the original app flowchart, and consulted with my other teammates. Isha had created a prototype for the front-end on Figma,
  which I utilised to completely re-write the flowchart from scratch. This allowed me to make sure my other solutions, my other steps,
  didn't have the same shortfall (unneccesary and not actually solving the issue). This allowed me to see exactly what the demo script
  should be, as well as where other demo scripts were needed too. From this I created a new script, with inputs for the cargo space
  dimensions (found in the data scraping script), inputs for the furniture as well as input for the type of furniture too. Along with this,
  I scrapped the 10cm margin of error and applied a universal 5cm margin of error to the dimensions. Then I found the script so that it
  would check not only volume, but also length, height, and width, and that all those values were smaller than the cargo space, in order to
  return a Yes or a No, on whether the furniture would fit. This is all shown in the file 'FurnitureFitStep.md', attached in the repo. This
  solves the issues that the previous demo script had. And for now, is a good solution to the overall issue of checking if the furniture
  will fit.

  Conclusion: in future, check that the overall picture of the program or process is sound and detailed, in order to prevent shortcomings
  in future scripts and solutions in general.

Problem 2: Priority ranking step/algo

  One thing that had really interested me from the start was developing this ranking idea. Taking inspiration from ELO algos in chess and
  from holding ourselves accountable for climate change, I knew I could come up with a novel process to carry this out. So the issue is, I
  feel as though the ranking of eligible drivers on the page is important, as the customer is likely to pick the top option. Furthermore, I
  think that a ranking based on proximity is too one-dimensional, other things to be considered are the emissions that the driver's car
  gives off, and, the ratings of the driver. Each of these is too be discussed below within the solution paragraph.

  Solution: To write this succinctly, I'll delve into each factor to be considered below. First is the proximity/distance. 
    
    Bolt is an example of a successful realisation of what we want to implement, they utilise Google Maps and Mapbox APIs. Drivers are
    ranked based on their proximity to the rider and their ETA. The closer a driver is, the higher they are ranked. This is a good solution     for the issue as it lays out the idea of what could be implemented in the future, perhaps in deployment of the app, but at the moment       and with the current time frame, it is not feasible to actually build this idea.

  Now moving to fuel emissions or carbon emissions.

    I could implement a data scraping system that would find the emissions statistics on the driver’s car. After standardizing the metrics, 
    we could calculate averages and carry out a simple ranking system, that put the cars with the least emissions at the top, and the most 
    emissions at the bottom. The main issue here would be finding a website with the data available for every car, I think once again, it
    is more feasible to leave it as a thought out process rather than a technically working solution for this factor. So we are done here.

  Finally, we move to driver's reviews and ratings.

    On deployment of the app, this would not be a possible factor due to the lack of data to effectively consider it. However, once the
    data was collected we could follow as such. Use Laplace’s rule of succession to take into account the number of reviews as well as the
    overall rating of the driver. This is leveraging Bayesian statistics to properly inform the customer of their expected utility gain by 
    using Driver A over Driver B, I got this idea from a 3Blue1Brown video, and is tangentially related to chess ELO rankings (something I
    was very interested in). Using these figures derived, again, simply rank the drivers from best to worst.

  Once all of these are formed, and we have each eligible driver on a ranking from #1 to #x, where x is the number of eligible options for
  drivers. We then assign a weighting to each factor, say 0.3 for rankings, 0.2 for emissions and 0.5 to proximity. Finally, ranking the
  drivers with the lowest score (a driver who has is #1 for all factors would have a score of 3) at the top of the list and the highest
  score at the bottom. This successfully ranks the drivers from top to bottom in a way that reinforces ease of use, our project missions
  to make recommerce more appealing, and create a project that helps the environment.

  Conclusion: make sure to do proper reading in order to allow you to explore your options when creating a process.

These were the issues that cropped up whilst forming the PPTX. The goal now is to finalise all the formatting and the other teammates entries into the PPTX, and begin to create the video pitch along with the other mandatory components of the competition.

Main problem:
There were two of these, and discussed in detail above.

Main takeaways:
1. I successfully dealt with multiple issues as they came up, implementing novel ideas to solve them.
2. I was able to take on board criticism on a solution, take a step back, re-inform myself and correct my solution.
3. I was able to draw away two key points to bear in mind when pursuing future endeavours (under "Conclusion:" in each problem section).
4. Keep moving forward, to secure the project before the deadline.

--------------------------------------------------------------------------------

Sunday 23rd June - 1/2

Having got the powerpoint pitch completed, and working with Isha on the front-end Figma prototype (I designed the selecting driver page and the carbon tracking calculator page), the deadline was coming up (21st June). But the competition organisers pushed it back to the 1st of July; as they want us to look at the resources they uploaded in their full. These resources include a new API that can be used to contract payment data and the carbon emissions connected with that payment. As such, I have organised another team meeting where we will pitch our ideas of how to incorporate this new API in our already well established app. I will update this log later on after the meeting. 
  Going back to what's already happened (the PPTX and the Figma prototype), the PPTX was a smooth process since the last log, I simply added some formatting and edited my teammates entries into the pitch slides. The Figma software was something I had never used before so it involved me doing some preliminary research into the tools and how to go about navigating it. I ended up designing two pages, as listed earlier. A problem I had found was not getting the navigation bar to stay at the bottom whilst the user scrolled, although I quickly fixed this issue. The end goal is to get the prototype to a stage where we can overlay it onto an iPhone screen and it replicate what the user would see from start to finish (login to completed order). I have utilised other websites such as a carbon footprint calculator into the prototype so that we can urge the customer to stay accountable. Other than this, there is not much to update before the meeting.

Main problem: Navigating the app development software Figma, particularly issues within keeping buttons in their place whilst the user scrolls. Solution: Background research and asking my peers, helped me to understand the steps to properly fix a button whilst scrolling. Outcome: A good replication of what us (the team) want the app to look like.

Main takeaways:
1. I successfully learned and implemented basic Figma skills to help build a front-end prototype for our app AirRide
2. I was able to coordinate with peers to get the powerpoint pitch finished before the initial deadline, this included delegating research to others.
3. I smoothly took on board moved deadline and re-directed our efforts to be more ambitious, as well as organising a meeting to discuss my peers' thoughts on the new API.

--------------------------------------------------------------------------------

Sunday 23rd June - 2/2 (after meeting)

We discussed the new API resources that were given to us in the meeting, which help us keep track of carbon emissions. Deciding that (after reading the general chat) that we wouldn't get permission from the resource in time before the deadline. Also, we lack a back-end in the prototype app, it is very much an idea. So therefore, I decided to propose we instead just put an idea of how to use the API in developing the app fully, into the future forecast section of the slides. 
  After discussing this, we talked about how we would go about doing the video pitch. Rbhu is creating a YouTube account for AirRide, and everyone else is sending me their pitches. Their individual sections will go over what they did in the powerpoint and in the project. I'll edit them all together into a coherent pitch. Including some public interview excerpts. As well as this I need to finish the prototype with Isha, I just let her know that I can take charge of the proposed section for API integration, and general formatting. Leaving her the payments page to design.

Main takeaways:
1. I successfully coordinated the team to discuss a new issue that arose (the API resource and extended deadline).
2. Finish the front-end prototype with Isha, working on finding a place to let the customer use the API system (proposed), dimensions of each page and the top iPhone bar.
3. Add the proposed system of utilising the API to the flowchart within the PPTX.
4. Design a script for the video pitch and self-record my section, conduct and film public interviews, and edit it all together to create an overall pitch.


