---
layout: page
title: Student Needs in Engineering Design Capstones
description: I studied the relationship between support students received from their teammates and industry mentors and learning outcomes in design capstones.
img: /assets/img/capstone2.jpeg
importance: 2
category: work
---

The purpose of this study is to examine the relationship between the support students receive from their peers (teammates) and industry mentors during an industry sponsored engineering design capstone and their perceptions about technical and non-technical learning outcomes. Capstone design courses are an important requirement for undergraduate engineering programs, and industry sponsored capstone programs are one way to provide students with the opportunity to work on real-world problems. However, these programs vary widely in implementation, and there is a gap in understanding the influence of peer and industry mentor support on student learning outcomes in the capstone experience.

 <div class="row">
                <div class="col-3">
                  <h3 class="fact-title">Role</h3>
                  <p class="fact-fact">Primary Researcher</p>
                </div>
                <div class="col-3">
                  <h3 class="fact-title">Company</h3>
                  <p class="fact-fact">Research Project</p>
                </div>
                <div class="col-3">
                  <h3 class="fact-title">Timeline</h3>
                  <p class="fact-fact">June 2022 - March 2023</p>
                </div>
                 <div class="col-3">
                  <h3 class="fact-title">Study Design</h3>
                  <p class="fact-fact">Mixed-Methods</p>
                </div>
              </div>
<hr>

# Key Questions
<br>
- What are the relevant factors necessary to explore student learning outcomes?
- How were (industry and teammate) support linked to student learning outcomes?
- How and why were student learning outcomes impacted by instructional support?
<hr>
# Participants
The study involved a cohort of students who enrolled in the industry sponsored engineering design capstone (ENGINE) during the 2021-2022 academic year. The capstone is a two (ten week) quarter program spanning winter and spring quarters for a total of 20 weeks. In 2021-2022, the program hosted 184 students, 177 of which were electrical and computer engineering majors. Students had an opportunity to select from about 48 projects. Approximately 80% of the projects were sponsored by industry, while the remaining were sponsored by government organizations.
<hr>

# Methodology

I designed a self-reflection survey to collect large-scale quantitative data on students' perceptions of support and learning. The self-reflection survey contained 36 closed-ended (Likert type questions) and 5 open-ended questions. The close-ended questions were adapted from different scales developed to assess engineering design performance, entrepreneurial and students' innovation competencies and faculty support along with items that I newly developed for this study. 

## Close-Ended Questions (Quantitative)
### Purpose
The goal of using close-ended questions was to pinpoint the essential factors needed to investigate student learning outcomes and their relationship with students' views on teammate and industry mentor support.

### Method
Since all survey items were either adapted to or newly developed for this capstone setting, an exploratory factor analysis (EFA) was conducted in R. The EFA helped to identify learning outcomes, independent variables, and control variables. A linear regression model was then utilized to investigate the relationship between the dependent, independent, and control variables identified from the EFA.

### Outcomes
The outcome of the exploratory factor analysis (EFA) revealed two distinct factors related to student learning in the capstone setting. The first factor, named "Engineering Design and Decision-Making," highlighted students' perceptions of their ability to learn more about systems engineering, ethical implications of design, and decision-making. The second factor, labeled "Adaptability," focused on students' ability to manage changes in project scope, deal with ambiguity, and obtain necessary information to move forward. Together, these two factors accounted for a total variance of 70.5%, which exceeded the desired threshold of 60%.

The EFA also resulted in four factors associated with students' sense of support and other controlling variables: design self-efficacy, preparedness, teammate support, and industry mentor support. These factors represented a total variance of 72.1%, exceeding the desired threshold of 60%. The analysis identified specific areas where students perceived their skills and support to be strongest, providing valuable insight for improving the capstone experience.

Once the factors were identified, the relationship between them was investigated using a linear regression model. 
- The independent variables were teammate support and industry mentor support
- The controlling variables were design self-efficacy and preparedness
- The dependent variables were engineering design and decision-making and adaptability.

Two regression models were created for each of the dependent variables. The final model for engineering design and decision-making had an adjusted R^2 of 0.50, meaning that the independent variables and interactions between them explained 50% of the variance in the data. All independent variables were significantly and positively associated with engineering design and decision-making, except for industry mentor support.

Similarly, the final model for adaptability had an adjusted R^2 of 0.55, indicating that the independent variables and interactions between them collectively explained 55% of the variance in the data. All independent variables were significantly and positively linked to adaptability.

The analysis also identified two significant interaction effects between the independent variables. In the first model (for engineering design and decision-making), interactions between preparedness and teammate support were significant, indicating that teammate support played a more significant role in students' engineering design and decision-making skills when they did not feel well-prepared for the project. Likewise, in the second model (for adaptability), the interaction between preparedness and industry support was significant, indicating that industry mentor support had a stronger impact on students' adaptability skills when they felt less prepared for their projects. These findings provide valuable insights into the factors that influence students' engineering design and decision-making and adaptability in the capstone setting.


## Open-Ended Questions (Qualitative)
### Purpose
To understand and explain the relationship between the independent, dependent and controlling variables, a qualitative analysis of the open-ended survey questions was conducted. 

### Method
The method used for the thematic analysis of the qualitative data involved a deductive coding process, which categorized student responses into perceptions of support, design self-efficacy, and preparedness for each of the learning outcomes. This was followed by frequency analyses to generate counts within different categories for each learning outcome, allowing for a better understanding of the relationship between the dependent and independent variables. 

### Outcomes
- **Teammate support:** The study found that in engineering design and decision-making, students rely heavily on teammate support for solving technical problems, achieving goals, brainstorming ideas, balancing designs, and adapting to challenges. Students emphasized the importance of effective project management, organizational structure, and communication among team members. 
- **Industry mentor support:** Industry mentor support played a significant role in students' adaptability, with technical feedback and flexibility being the two most prominent aspects. Having an involved mentor who could provide feedback and approve out-of-the-box ideas helped students adapt to changes and solve problems effectively. However, delayed mentor support could also negatively impact project outcomes. While not statistically significant, students also looked to mentors for high-level support and well-defined expectations, allowing them to design with more clarity.
- **Preparedness:** Two aspects of preparedness - technical and project plan - are important to students' perceptions of engineering design, decision-making, and adaptability. Students who felt more prepared for their project were able to organize their team's direction more effectively. Preparedness also mediated the relationship between teammate support and engineering design and decision-making such that students who felt more technically prepared for the project could better support their team. Also, Industry mentor support emerged as being vital to preparing students to
adapt to unforeseen changes by providing a concrete vision of the project goals.
- **Design self-efficacy:** The ability to self-learn and apply new knowledge was found to be key to positive perceptions of engineering design, as students were able to pivot their problem framing and access online resources to overcome technical challenges. However, some students expressed frustration with the burden of self-learning and a lack of teammate or industry mentor support. 
<hr>

# Limitations
The study focuses on the role of support, design self-efficacy, and preparedness on learning outcomes in a single institution, which limits its generalizability to other academic settings. The qualitative analysis is subject to researcher subjectivity, but the use of open-ended questions serves as triangulation. One of the authors' positionality as a teaching assistant may have influenced the interpretation of the themes. Despite these limitations, the study offers valuable insight into how teammate and industry mentor support influence students' perceptions of the technical and non-technical skills gained during the capstone.

<hr>

# Impact & Future Work
We found that teammate and industry mentor support as critical elements of students’ capstone design experience. Design self-efficacy and preparedness play an important role in controlling for the impact of support on learning. Therefore, capstone instructors should prioritize developing structured ways to facilitate teammate and industry mentor support. 

- Evidence-based best practices should be developed, which enable industry mentors to support students while fulfilling their goals and motivations for participating in capstone programs.
- Capstone instructors should consider developing interventions that help students feel supported by their teammates through alignment in expectations, expertise, and communication.
- Further, instructors and course designers should ensure that students feel technically supported throughout the capstone by having the appropriate educational resources and help.
- Instructors should impart effective collaborative project planning and management strategies so that students can develop a clear understanding of their project in conjunction with their teammates and industry mentors early in the project cycle.
