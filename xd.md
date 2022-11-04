# Homework

We will use what we have learned so far in a real life applications.

## Instructions
- Release date: **3/11/20222**.
- Due date: **10/11/2022**
- Your should submit a `.zip` file to Moodle with your name,
  like `YusufMesbah.zip`. All the files inside should have a meaningful names,
  like `task_1.ipynb`. Don't name your file `untitled.ipynb`.
- You are expected to follow the best practices for code writing and model
training. Poor coding style will be penalized.
  [PEP8](https://peps.python.org/pep-0008/) is one of the most common style guides.
- You are allowed to discuss ideas with your peers, but no sharing of code.
Plagiarism in the code will result in failing. If you use code from the
internet, cite it.
- If the instructions seem vague, use common sense.


## Task 1: Genetic Algorithms (50%)
For this task you need to solve a scheduling problem for food spices company.
They have a machine that produces multiple spice mixes, and they have a weekly
demand. The problem is that switching between mixes requires cleaning the machine.

Also, there are different cleaning protocols depending on the mix you were
making and the  mix you want to make. This is because some mixes can cause
allergies, so the machine has to be well cleaned.

Here are the cleaning protocols:
- Allergens - Wet Cleaning required: 3 hr
- Different Flavor/color/odor - Dry Cleaning with salt is required: 1 hr		
- Similar recipes - Scraping of previous batch residuals only is required: 20 min		
- Same Mix - No need for cleaning: 0 min

Your task it to find an optimal way to produce the total demand for the week.
Assume that it takes 20 minutes to produce any mix without the cleaning process.
Also, there is a maintenance process at the end of each day that requires the
3hr wet cleaning + 1hr maintenance. So, you can manufacture for 20hr a day.

### Data
Read `NIC GA matrix.xlsx` you will find the cost matrix between mixs and the
total demand of each for this week.


## Task 2: Genetic Programming (50%)
This task is based on this [competition](https://www.kaggle.com/competitions/quora-question-pairs/overview).
We will be checking duplicate questions from quora.com.

### Data fields
- **id** - the id of a training set question pair
- **qid1, qid2** - unique ids of each question (only available in train.csv)
- **question1, question2** - the full text of each question
- **bot?** - If one of the questions was posted by a bot
- **number_likes** - how many likes the questions had at the time of data collection
- **is_duplicate** - the target variable, set to 1 if question1 and question2 have essentially the same meaning, and 0 otherwise.


### Task
Your goal is to achieve the highest accuracy using GP. You should evaluate your model
using [balanced accuracy score](https://scikit-learn.org/stable/modules/generated/sklearn.metrics.balanced_accuracy_score.html).

You can use TPOT or GPLearn. These of course don't support text input out
of the box. However, you can add your own modules, feel free to be creative
with your preprocessing modules.

At the end report the best pipeline you got.

You are not allowed to directly drop or preprocess the data,
except for dropping the IDs.
the GP algorithm should do everything.
