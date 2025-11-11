### Simulation of public emotional reactions to news using LLM

This project was completed as part of a BSP course at the University.
The goal was to develop a system capable of analyzing news events and modeling the emotional responses of different social groups to these events using Large Language Models (LLMs) and iterative prompt engineering methodology.

1. ### **Project objective**

Traditional methods of analyzing public opinion (surveys, focus groups) are time-consuming, expensive, and do not reflect the immediate reactions of society.
LLMs allow this task to be solved quickly, scalably, and flexibly—but their behavior must be controlled, otherwise the results will be:

- **too generalized,**

- **contradictory,**

- **prone to stereotypes.**

The project aims to create a controllable model capable of producing realistic and interpretable emotional assessments.

2. ### Social groups (Avatars)

The system models the reactions of three main social classes, each represented by male and female variants.
This is important because the perception of news often depends not only on social status, but also on gender, level of stability, and life priorities.

**Lower class:**
People with limited economic opportunities and unstable sources of income.

- Men: concerned about financial stability and personal safety. Low level of trust in institutions.
- Women: burdened with domestic and social responsibilities, emotional reactions often related to the theme of daily survival.

**Middle class:**
A group with a relatively stable standard of living and access to services and information.

- Men: financially stable, interested in socio-economic trends, but do not directly link self-fulfillment with work.
- Women: have a stable lifestyle, form opinions through social values and the social context.

**Upper class:**
People with long-term financial security and influence in the social structure.

- Men: focused on stability, cultural capital, reputation, and long-term consequences.
- Women: view news through the prism of maintaining social balance, social status, and cultural norms.

> Important:
In upper-class reactions, there is no automatic assumption that any event is perceived through the lens of money.
Their emotions are often linked to social order, reputation, cultural changes, and long-term stability, rather than direct benefit.

3. ### Emotional scale

The system uses 10 categories of emotions, ranked by intensity:

"emotions": [
    {
      "id": 1,
      "label": "Disgust",
      "description": "A strong feeling of aversion or rejection toward something perceived as offensive, dirty, immoral, or revolting.",
      "score": 1
    },
    {
      "id": 2,
      "label": "Anger",
      "description": "A heated emotional response to perceived injustice, offense, or frustration. Often includes tension and a desire to protest or act.",
      "score": 2
    },
    {
      "id": 3,
      "label": "Fear",
      "description": "A sense of danger, threat, or anxiety about a possible negative outcome. Often includes mental unease or physical tension.",
      "score": 3
    },

...

{
      "id": 9,
      "label": "Excitement",
      "description": "A high-energy positive emotion. Includes enthusiasm, stimulation, or eagerness about something happening or upcoming.",
      "score": 9
    },
    {
      "id": 10,
      "label": "Joy",
      "description": "A strong feeling of happiness and emotional uplift. Deep satisfaction, delight, or celebration.",
      "score": 10
    }
  ]
}

4. ### Emotional Integrity Rules

To ensure that reactions are realistic, the model follows a number of principles:

- If the news involves human suffering, the initial reaction should be emotional rather than analytical.
- You cannot replace “Sadness” or ‘Fear’ with words like “Interest” just to make the response sound nicer.
- If a character is emotionally distant, this should be explained, not simply labeled as “Neutral.”
 
The reaction should be proportional to the significance of the event.
For example:
- News about war → strong emotions.
- News about a music show → moderate emotions.
- Values 9–10 are only assigned if the event is personally and culturally significant.
 
These rules help to avoid:
- caricatured reactions,
- excessive emotions “out of nowhere,”
- and automatic stereotypes.
 
5. ### Interface
The project uses Gradio to work via the web.

<img width="1470" height="836" alt="Image" src="https://github.com/user-attachments/assets/cad7fda6-57a0-4250-84d5-1882a0ddd7ed" />

 6. ### Conclusion 
 
**What was particularly important in the project:**
- Using role prompting to set a professional tone for the analysis.
- Creating social avatars that reflect different worldviews.
- Introducing rules of emotional integrity to prevent excessive reactions.
- Combating stereotypes, especially in groups with pronounced status differences.
- Transitioning to a JSON structure for machine interpretation and visualization.
