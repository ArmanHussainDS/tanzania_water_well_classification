
# Module 3 Project


## Introduction

In this lesson, we'll review all the guidelines and specifications for the final project for Module 3.


## Objectives

* Understand all required aspects of the Module 3 project
* Understand all required deliverables
* Understand what constitutes a successful project

## Project Summary

Congratulations! You've made it through another _intense_ module, and now you're ready to show off your newfound Machine Learning skills!

![awesome](https://raw.githubusercontent.com/learn-co-students/mod3-project-london-dsc/master/smart.gif)

All that remains for Module 3 is to complete the project!

## The Project

The main goal of this project is to create a classification model. For this project you'll have your choice of dataset (see below). Each comes with its own advantages and disadvantages, and, of course, its own associated business problem and stakeholders. It may be desirable to flesh out your understanding of the audience or the business proposition more than we have sketched out here.

## The Data

1. [Chicago Car Crash Data](https://data.cityofchicago.org/Transportation/Traffic-Crashes-Crashes/85ca-t3if). Note this links also to [Vehicle Data](https://data.cityofchicago.org/Transportation/Traffic-Crashes-Vehicles/68nd-jvt3) and to [Driver/Passenger Data](https://data.cityofchicago.org/Transportation/Traffic-Crashes-People/u6pd-qa9d).

Build a classifier to predict the primary contributory cause of a car accident, given information about the car, the people in the car, the road conditions etc. You might imagine your audience as a Vehicle Safety Board who's interested in reducing traffic accidents, or as the City of Chicago who's interested in becoming aware of any interesting patterns. Note that there is a **multi-class** classification problem. You will almost certainly want to bin or trim or otherwise limit the number of target categories on which you ultimately predict. Note e.g. that some primary contributory causes have very few samples.

2. [Terry Stops Data](https://catalog.data.gov/dataset/terry-stops).
In [*Terry v. Ohio*](https://www.oyez.org/cases/1967/67), a landmark Supreme Court case in 1967-8, the court found that a police officer was not in violation of the "unreasonable search and seizure" clause of the Fourth Amendment, even though he stopped and frisked a couple of suspects only because their behavior was suspicious. Thus was born the notion of "reasonable suspicion", according to which an agent of the police may e.g. temporarily detain a person, even in the absence of clearer evidence that would be required for full-blown arrests etc. Terry Stops are stops made of suspicious drivers.

Build a classifier to predict whether an arrest was made after a Terry Stop, given information about the presence of weapons, the time of day of the call, etc. Note that this is a **binary** classification problem.

Note that this dataset also includes information about gender and race. You **may** use this data as well. You may, e.g. pitch your project as an inquiry into whether race (of officer or of subject) plays a role in whether or not an arrest is made.

If you **do** elect to make use of race or gender data, be aware that this can make your project a highly sensitive one; your discretion will be important, as well as your transparency about how you use the data and the ethical issues surrounding it.

3. [Customer Churn Data](https://www.kaggle.com/becksddf/churn-in-telecoms-dataset)

Build a classifier to predict whether a customer will ("soon") stop doing business with SyriaTel, a telecommunications company. Note that this is a **binary** classification problem.

Most naturally, your audience here would be the telecom business itself, interested in losing money on customers who don't stick around very long. Are there any predictable patterns here?

4. [Tanzanian Water Well Data](https://www.drivendata.org/competitions/7/pump-it-up-data-mining-the-water-table/page/23/) (*active competition*!)
Tanzania, as a developing country, struggles with providing clean water to its population of over 57,000,000. There are many waterpoints already established in the country, but some are in need of repair while others have failed altogether.

Build a classifier to predict the condition of a water well, using information about the sort of pump, when it was installed, etc. Note that this is a **ternary** classification problem.

## DELIVERABLES

1. A public GitHub repository.
2. An `environment.yml` file that contains all the necessary packages needed to recreate your conda environment.
3. A standalone `src/` directory that stores all relevant source code.
    - All functions have docstrings that act as [professional-quality documentation](http://google.github.io/styleguide/pyguide.html#381-docstrings). 
    - If applicable, [well documented](https://www.sqlstyle.guide/) SQL queries with appropriate single-line or multiline comments.
    - Quality classification model
       - Be prepared for questions about model and hyperparameter choice
4. A standalone `data/` directory that stores all relevant raw and processed data files
    - Be sure to include how the data was obtained!
    - All large files are labeled in the `.gitignore` file to avoid having them accidentally live in your commit history.
5. A standalone `references/` directory that stores all relevant literature, data dictionaries, or useful references that were used to help you during the project.
    - Use this directory to store physical copies of the `.pdf` files; or
    - Create a `README.md` file that cites external resources that were used.
6. A standalone `reports/` directory that stores your `memo.md` and `presentation.pdf` files
7. A user-focused `README.md` file that explains your process, methodology and findings.
    - Take the time to make sure that you craft your story well, and clearly explain your process and findings in a way that clearly shows both your technical expertise and your ability to communicate your results!
8. One Jupyter Notebook file that focuses on EDA, visualization, and presentation. 
    - The very beginning of the notebook contains a description of the purpose of the notebook.
       - This is helpful for your future self and anyone of your colleagues that needs to view your notebook. Without this context, you’re implicitly asking your peers to invest a lot of energy to help solve your problem. Help them by enabling them to jump into your project by providing them the purpose of this Jupyter Notebook.
    - Explanation of the data sources and where one can retrieve them
       - Whenever possible, link to the corresponding data dictionary
    - Custom functions and classes are imported from Python modules and are not created directly in the notebook.
    - At least 4 meaningful data visualizations, with corresponding interpretations. All visualizations are well labeled with axes labels, a title, and a legend (when appropriate)
9. A one-page memo written exclusively for a non-technical stakeholder with a file name `memo.md`.
    - This memo should describe:
       - A summary of the business problem you are trying to solve
       - Key takeaways from your solution
       - A section on next steps if you had more time (i.e. one additional week)
10. An "Executive Summary" Keynote/PowerPoint/Google Slide presentation (delivered as a PDF export) that explains what you have found.
    - Make sure to also add and commit this file as presentation.pdf of your non-technical presentation to your repository with a file name of `presentation.pdf`.
    - Contain between 5-10 professional quality slides detailing:
       - A high-level overview of your methodology
       - The results you’ve uncovered
       - Any real-world recommendations you would like to make based on your findings (ask yourself--why should the executive team care about what you found? How can your findings help the company/stakeholder?)
       - Avoid technical jargon and explain results in a clear, actionable way for non-technical audiences.
    - The slides should use visualizations whenever possible, and avoid walls of text

**_Organization/Code Cleanliness_**

* The notebook should be well organized, easy to follow, and code is commented where appropriate.  
    * Level Up: The notebook contains well-formatted, professional looking markdown cells explaining any substantial code. All functions have docstrings that act as professional-quality documentation.  
* The notebook is written to technical audiences with a way to both understand your approach and reproduce your results. The target audience for this deliverable is other data scientists looking to validate your findings.  

**_Process, Methodology, and Findings_**

* Your notebook should contain a clear record of your process and methodology for exploring and preprocessing your data, building and tuning a model, and interpreting your results.
* We recommend you use the CRISP-DM process to help organize your thoughts and stay on track (see below for a refresher).

## THE PROCESS

These steps are informed by Smart Vision's<sup>1</sup> description of the CRISP-DM process.

### 1. Business Understanding

Start by reading this document, and making sure that you understand the kinds of questions being asked.  In order to narrow your focus, you will likely want to make some design choices about your specific audience, rather than addressing all of the "many people" mentioned in the background section.  Do you want to emphasize affordability, investment, or something else?  This framing will help you choose which stakeholder claims to address.

Three things to be sure you establish during this phase are:

1. **Objectives:** what questions are you trying to answer, and for whom?
2. **Project plan:** you may want to establish more formal project management practices, such as daily stand-ups or using a Trello board, to plan the time you have remaining.  Regardless you should determine the division of labor, communication expectations, and timeline.
3. **Success criteria:** what does a successful project look like?  How will you know when you have achieved it?

### 2. Data Understanding

Write a script to download the data (or instructions for future users on how to manually download it), and explore it.  Do you understand what the columns mean?  How do the three data tables relate to each other?  How will you select the subset of relevant data?  What kind of data cleaning is required?

It may be useful to generate visualizations of the data during this phase.

### 3. Data Preparation

Through SQL and Pandas, perform any necessary data cleaning and develop a query that pulls in all relevant data for analysis in a linear regression model, including any merging of tables.  Be sure to document any data that you choose to drop or otherwise exclude.  This is also the phase to consider any feature scaling or one-hot encoding required to feed the data into a classification model.

### 4. Modeling

The focus this time is on prediction. Good prediction is a matter of the model generalizing well. Steps we can take to assure good generalization include: testing the model on unseen data, cross-validation, and regularization. What sort of model should you build? A diverse portfolio is probably best. Classification models we've looked at so far include logistic regression, naive bayes,k nearest neighbors, decision trees, bagging, and boosting, each of these with different flavors. You are encouraged to try any or all of these.
This section is made of 2 steps:
- Fit a baseline model:
  - Pick a learner and train it without optimisation. Then measure its performance to know. This will be your benchmark to beat during the next step.
- Learner training and optimisation:
  - Try multiple learners (minimum 3) and apply hyperparameter optimisation to them. Pick the best model of each learner to analyse in the next section.

### 5. Evaluation

There are many different metrics we might use for evaluating a classification model. Accuracy is intuitive, but can be misleading, especially if you have class imbalances in your target. Perhaps, depending on you're defining things, it is more important to minimize false positives, or false negatives.<br>
We recommend you implement the following process (if you decide to do something different make sure you explain your logic):
- Model *discrimination* comparison (using ROC_AUC):
  - Compare the results of the previous step. Declare a winner and explain the logic behind your decision. (Remember, you get paid to solve problems. Your scoring metric is not everything)
- Threshold selection:
  - Estimate prevalence for the deployment environment
  - Estmate the costs associated to each element of the confusion matrix and explain your logic
  - Select the threshold with the highest score (Zweig and Campbell formula)
  - Show the associated confusion matrix
- Final interpretation:
  - Show importances / coefficients
  - Show the quantitative impact of that the top variables have on your target
  - Explain in non-technical terms the results that you obtained for power / alpha / precision and any other metric that could be interesting to your audience



### 6. Deployment

In this case, your "deployment" comes in the form of the deliverables listed above. Make sure you can answer the following questions about your process:

 - "How did you pick the question(s) that you did?"
 - "Why are these questions important from a business perspective?"
 - "How did you decide on the data cleaning options you performed?"
 - "Why did you choose a given method or library?"
 - "Why did you select those visualizations and what did you learn from each of them?"
 - "Why did you pick those features as predictors?"
 - "How would you interpret the results?"
 - "How confident are you in the predictive quality of the results?"
 - "What are some of the things that could cause the results to be wrong?"
 
And most importantly:
- Actionable problem solving recommendations:
  - What recommendations can you give to your stakeholders? Make sure is something they can directly act on. For example: 'Refer to a doctor any patient with glucose higher than x'

## Citation

1. "What is the CRISP-DM Methodology?" Smart Vision Europe. Available at: https://www.sv-europe.com/crisp-dm-methodology/
