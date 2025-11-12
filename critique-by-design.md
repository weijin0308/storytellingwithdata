| [home page](https://cmustudent.github.io/tswd-portfolio-templates/) | [data viz examples](dataviz-examples) | [critique by design](critique-by-design) | [final project I](final-project-part-one) | [final project II](final-project-part-two) | [final project III](final-project-part-three) |

# Title
How Each State and County Contributes to the U.S. Economy (2001 – 2018)

## Step one: the visualization
For this project, I selected “3D Map: The U.S. Cities With the Highest Economic Output” from Visual Capitalist (Makeover Monday).Link：https://www.visualcapitalist.com/3d-map-the-u-s-cities-with-the-highest-economic-output/
I chose it because it immediately caught my eye — the 3D bar design looked engaging and modern. However, after studying it more carefully, I realized the chart raised a lot of questions. The 3D perspective distorted perception and made it difficult to compare cities accurately. The visual appeal was strong, but the underlying data story was not easy to understand. That motivated me to explore how I could redesign it to keep the appeal but make the message clearer and more accurate.

## Step two: the critique
I evaluated the visualization using Stephen Few’s Data Visualization Effectiveness Profile.
In my critique (submitted through the Google form), I noted that the visualization worked well in terms of visual appeal and initial engagement — the design captured attention quickly. However, it failed in clarity and accuracy. The 3D effects distorted perception, the vertical bars overlapped, and the labeling was inconsistent. The color gradient wasn’t meaningful, and there was no clear sense of total economic contribution by region.

Compared to the Good Charts method, the Stephen Few framework helped me analyze more precisely why the visualization was ineffective — focusing on perception, clarity, and accessibility rather than just aesthetics. It encouraged me to think systematically about audience understanding instead of visual design alone.

## Step three: Sketch a solution
My initial redesign idea was to keep the same information but make it more readable.
I wanted to keep the states colored by total GDP and highlight the top 10 cities with circles in a different color. The concept was to make a cleaner, flatter version of the 3D map, with consistent color contrast and better readability.

I went straight into Tableau rather than sketching by hand, because I already had a clear visual in mind. However, while building, I faced several challenges:
-I tried to overlay two maps (one for state-level GDP and one for city dots), but they didn’t align properly.
-Dual-axis maps caused issues with zoom synchronization.
-Filters applied to both layers together, even when I wanted them to apply only to one (for example, only to the top 10 cities).
-The top layer completely covered the background, and I couldn’t make it transparent enough to reveal the base map.
<img width="933" height="642" alt="Screenshot 2025-11-11 at 11 29 39 PM" src="https://github.com/user-attachments/assets/20957c97-4979-4241-8105-ec8107fde014" />
<img width="930" height="647" alt="Screenshot 2025-11-11 at 11 31 27 PM" src="https://github.com/user-attachments/assets/e7cbdb8d-bfaf-4c1c-b4df-943e9bdf9629" />


After several iterations, I realized the approach was not practical. The combined city-state layout was visually overloaded and technically unstable in Tableau. It became clear that I needed a simpler, more purposeful redesign that prioritized clarity over complexity.

## Step four: Test the solution
During the feedback session, I shared my prototype map and initial design ideas with my classmates. I prepared a short feedback script, asking questions like:

“Can you tell me what you think this visualization is showing?”
"Do you have any recommendation for me based on my current struggles techinically?"
"Do you think it's better to disregard the city thing and focus on states?"

Feedback Summary

Peer 1 : said the map looked interesting at first, but once they tried to read it, they got confused by having both cities and states together. They mentioned that showing everything at once made the message harder to follow and recommended simplifying the scope.

Peer 2 : focused on the technical side and acknowledged that layering maps in Tableau can be tricky. They suggested it might be more efficient to separate the information by geography and build interactions instead of overlays — for example, letting users click on a state to see details instead of showing both levels at once.

Peer 3 : agreed that focusing on states might make the dashboard more readable and audience-friendly. They encouraged me to rethink the audience — rather than replicating the Visual Capitalist chart, I could aim for policymakers, economists, or students who want to explore regional contributions clearly.

My Reflection and Design Changes:
This feedback helped me realize that I was trying too hard to preserve the structure of the original visualization instead of improving its communication. Everyone agreed that clarity mattered more than showing everything. Based on their input, I made several major design decisions:

-Removed the city layer completely to eliminate clutter and confusion.

-Refocused on state-level GDP and added county-level contribution charts as an optional drill-down for users who want more detail.

-Replaced overlapping map layers with an interactive filter system, where clicking a state updates a bar chart instead.

-Simplified the color ramp to one sequential blue palette for readability.

-Added a dynamic title and year slider, so users can interact with the map smoothly and track changes over time.

These adjustments made the design not only simpler but also more purposeful. My peers’ advice shifted my mindset — instead of fighting the technical constraints, I learned to redesign around them and focus on user understanding.

## Step five: build the solution

My final dashboard focuses on how each state and county contributes to the U.S. economy over time.
The design includes:
-A state-level filled map colored from light to dark blue based on GDP ranking.

-A year slider that allows users to move between 2001 and 2018 to see how economic patterns evolve.

-A county-level bar chart that automatically updates when a user clicks on a state, showing that state’s internal GDP composition.

-A clear title and dynamic text to highlight the selected year.

I deliberately removed unnecessary city labels, 3D effects, and excessive legends. The goal was to create a clean, data-driven story that anyone can read easily. Each interaction guides the user from a national overview to state-specific insights without visual clutter. Overall, this redesign transformed a flashy but confusing 3D map into a clear, interactive, and data-focused dashboard. It emphasizes the story of how different regions contribute to the U.S. economy over time — simple, insightful, and easy to explore.

<div class='tableauPlaceholder' id='viz1762920101613' style='position: relative'><noscript><a href='#'><img alt='How Each State and County Contributes to the U.S. Economy (2001 – 2018) ' src='https:&#47;&#47;public.tableau.com&#47;static&#47;images&#47;US&#47;US_GDP_WJ&#47;Dashboard1&#47;1_rss.png' style='border: none' /></a></noscript><object class='tableauViz'  style='display:none;'><param name='host_url' value='https%3A%2F%2Fpublic.tableau.com%2F' /> <param name='embed_code_version' value='3' /> <param name='site_root' value='' /><param name='name' value='US_GDP_WJ&#47;Dashboard1' /><param name='tabs' value='no' /><param name='toolbar' value='yes' /><param name='static_image' value='https:&#47;&#47;public.tableau.com&#47;static&#47;images&#47;US&#47;US_GDP_WJ&#47;Dashboard1&#47;1.png' /> <param name='animate_transition' value='yes' /><param name='display_static_image' value='yes' /><param name='display_spinner' value='yes' /><param name='display_overlay' value='yes' /><param name='display_count' value='yes' /><param name='language' value='zh-CN' /><param name='filter' value='publish=yes' /></object></div>
<script type='text/javascript'>
  var divElement = document.getElementById('viz1762920101613');
  var vizElement = divElement.getElementsByTagName('object')[0];
  if ( divElement.offsetWidth > 800 ) { vizElement.style.width='1000px';vizElement.style.height='827px';} else if ( divElement.offsetWidth > 500 )
  { vizElement.style.width='1000px';vizElement.style.height='827px';} else { vizElement.style.width='100%';vizElement.style.height='827px';}
  var scriptElement = document.createElement('script');
  scriptElement.src = 'https://public.tableau.com/javascripts/api/viz_v1.js';
  vizElement.parentNode.insertBefore(scriptElement, vizElement);
</script>

## References
Visual Capitalist. (2022, July 12). 3D Map: The U.S. Cities With the Highest Economic Output. Retrieved from https://www.visualcapitalist.com/3d-map-the-u-s-cities-with-the-highest-economic-output/

Underlying GDP data obtained from the U.S. Bureau of Economic Analysis (BEA) via Makeover Monday open dataset, GDP by County, 2001–2018.

## AI acknowledgements
Use Chatgpt to help me with techinical problems in tableau
