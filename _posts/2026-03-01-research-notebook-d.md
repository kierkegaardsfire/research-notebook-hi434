---
layout: post
title: "Research Notebook D"
date: 2026-03-01
---

<style>
/* Background image fills the whole browser window */
body.notebook-d-bg {
  background-image: url("{{ '/assets/images/coins.png' | relative_url }}");
  background-size: cover;
  background-position: center top;
  background-attachment: fixed;
  background-repeat: no-repeat;
}

/* Dark overlay over the image for readability */
body.notebook-d-bg::before {
  content: "";
  position: fixed;
  top: 0; left: 0; right: 0; bottom: 0;
  background: rgba(0, 0, 0, 0.40);
  z-index: 0;
  pointer-events: none;
}

/* Make Minima's wrappers transparent so the image shows through */
body.notebook-d-bg .site-header,
body.notebook-d-bg .page-content,
body.notebook-d-bg .wrapper,
body.notebook-d-bg .site-footer {
  background: transparent !important;
  position: relative;
  z-index: 1;
}

/* Make the site nav and footer readable against the image */
body.notebook-d-bg .site-header {
  background: rgba(255, 255, 255, 0.92) !important;
}

body.notebook-d-bg .site-footer {
  background: rgba(255, 255, 255, 0.92) !important;
  color: #1a1a1a;
}

/* The translucent white panel for post content */
.bg-content-panel {
  position: relative;
  z-index: 1;
  max-width: 760px;
  margin: 30px auto;
  background: rgba(255, 255, 255, 0.88);
  padding: 40px 50px;
  border-radius: 4px;
  box-shadow: 0 4px 20px rgba(0, 0, 0, 0.3);
  backdrop-filter: blur(2px);
  -webkit-backdrop-filter: blur(2px);
}

.bg-content-panel,
.bg-content-panel p,
.bg-content-panel li,
.bg-content-panel h1,
.bg-content-panel h2,
.bg-content-panel h3 {
  color: #1a1a1a;
}

.bg-content-panel img {
  max-width: 100%;
  height: auto;
}
</style>

<script>
document.body.classList.add('notebook-d-bg');
</script>

<div class="bg-content-panel" markdown="1">

# Research Notebook D - History 434
## Jonas Goodwin
### March 1st, 2026

For my RAWGraph project I went online to find sample data because my own data wasn't suited for this yet. I found a large excel file with thousands of rows of data mimicking the personnel list of a major company. Each person in the file had a variety of information about them, their Job Title, Department, Gender, Ethnicity, Age, Salary. Originally, my idea was to visualize the correlation between age and salary in the company. I figure this would show a clear correlation between the two, with average salary throughout the company rising with age. I initially wanted to do a bar graph before I spoke with Professor Carty, who suggested a scatter plot instead. With a scatterplot not being offered by RAWGraphs, I figured that a line graph would be the next best option. I put my data into the line graph, with age on the x axis and salary on the Y.

Here I ran into a problem, as RAWGraphs was categorizing my salary data as if it was qualitative, not quantitative. After googling I realized that this was because of the "$" in the dataset. So, I opened my original dataset in Google Sheets and attempted to get rid of the dollar sign. First I tried using the "search and replace" tool, but that was not working. The dollar signs remained there inexplicably. Some more research revealed that this was because it was a formatting issue, and the solution was to find the "number format" setting within Sheets. I turned off the "automatic" formatting, which removed the dollar sign. Then I downloaded the Sheet file as a new CSV, and started over in a new RAWGraphs.

Having resolved this problem, I was free to create my line graph. However, this did not turn out as I expected:

![PEI Forests]({{ "/assets/images/expectedd.png" | relative_url }})

As you can see, there was not the correlation I anticipated, although the very highest salary was indeed also one of the highest ages. I am not sure if the dataset I got was generated somehow, or if it was taken from real corporate data and anonymized in some way. In any case, I decided to look at other variables to try. I thought about swapping out "age" for "department" to see any pay disparity between the 7 divisions of the company: IT, Engineering, Sales, HR, Finance, Accounting, and Marketing. The results here, while not shocking, were more satisfying:

I sorted the bars in ascending order for better visualization. The results showed that marketing led the pack with an average salary of about $130,000, while IT trailed behind their co-workers, coming in at just under $100,000.

<h1 align="center"><em>Research Notebook D Revision</em></h1>
<h2 align="center">Jonas Goodwin</h2>
<h2 align="center">May 5th, 2026</h2>

While reviewing these readings on visualization, I had newfound interest in its discussion of museum collections as a result of my experience volunteering at the Joel Lane Museum House in downtown Raleigh throughout this semester. As my work has progressed and I have delved deeper into the collections systems, I now have a better understanding with which to approach the experiences of Davis, Vane, and Krautli. The Davis article opened my eyes to to the potential for bias in the type of collections work that I been engaged with throughout this semester. Between my experience on museum collections and my work on Omeka, I am involved in every stage of the process at which data problems can occur. While working on Unjust Deeds, I select what data to use for my own project. Then, I digitize, upload, and apply metadata. I do this as well at the JLMH - but there I am obligated to be cautious to adhere to existing forms. In my own project that responsibility is up to me. And finally, in Unjust Deeds I play a direct role in its visualization. I probably play an indirect role in the visualization of the collections at the museum, but I hadn't really considered that before. The photos I digitize and upload are not my own, but someone did have a form of narrative control when they were originally taken. For context, you can view excerpts from the collection I work with [here, on Joel Lane Museum House website.](https://www.joellane.org/history/collection).

While struck by the new implications Davis' article had drawn about my personal work, Amiée Knight's article filled me with hope about the possibilities of digital history and visualization. I related strongly to the sense of optimism pervading Knight's discussion of data visualization. In particular, "Data Stories," Knights fifth mode of inquiry, describes exactly what my intention is with my project on Unjust Deeds. I love the idea of using data and technology to create a narrative that guides the user through the historical experience rather than sending them off on their own. With that in mind, the guiding questions Knight poses are extremely useful to me as ways to keep me grounded in my research.

In the Davis article one issue that I related to from my own experience was the ever-changing nature of institutional names. A particular problem when dealing with a multitude of governmental agencies and non-profits, as I am with Unjust Deeds. In my own research project, I found name variation, whether over time or across sources, to be particularly frustrating when navigating my Amicus Curiae documents, court petitions filed on behalf of third parties such as the ACLU, NAACP, and more obscure examples like the American Indian Citizens League of California, Inc. Jeffrey Gonda decided to cite the latter organization as "Amici," having never referenced it previously. Resulting in the following citation:

106. The complete list of amici is as follows:...California Amici,

As you can see "amici" is also the plural of "amicus."

The only logical explanation I can consider is that Gonda was copying a list of amici (small a), without context, and misinterpreted something. The only reason I am confident I am correct in my assumption that Gonda was referring to the American Indian Citizens League is that after looking through multiple lists of the parties to the case, it is the only one with any connection to California.

These differences in classification, as we saw in Rosenberg and Erickson's articles in the Historical Data unit, can be just as much from human error or carelessness as from evolution over time. However, I myself am of course guilty of inconsistency in naming as well. I believe this phenomenon is a natural human tendency that we must learn to mitigate rather than trying to prevent at the individual level.

</div>
